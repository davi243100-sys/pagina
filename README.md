// ================= FRONTEND (RESUMO) =================
// Seu frontend já está pronto acima 👆
// Agora vamos adicionar o BACKEND real

// ================= BACKEND (Node.js + Express) =================

// 1. Instale:
// npm init -y
// npm install express multer fluent-ffmpeg cors

const express = require("express");
const multer = require("multer");
const ffmpeg = require("fluent-ffmpeg");
const cors = require("cors");
const app = express();

app.use(cors());
app.use(express.json());

// ===== UPLOAD =====
const upload = multer({ dest: "uploads/" });

// ===== CORTE DE VÍDEO REAL =====
app.post("/trim", upload.single("video"), (req, res) => {
  const { start, duration } = req.body;
  const input = req.file.path;
  const output = `outputs/output_${Date.now()}.mp4`;

  ffmpeg(input)
    .setStartTime(start)
    .setDuration(duration)
    .output(output)
    .on("end", () => {
      res.json({ url: output });
    })
    .on("error", (err) => {
      res.status(500).send(err);
    })
    .run();
});

// ===== ADICIONAR ÁUDIO =====
app.post("/add-audio", upload.fields([
  { name: "video" },
  { name: "audio" }
]), (req, res) => {
  const video = req.files["video"][0].path;
  const audio = req.files["audio"][0].path;
  const output = `outputs/merged_${Date.now()}.mp4`;

  ffmpeg()
    .input(video)
    .input(audio)
    .outputOptions(["-c:v copy", "-c:a aac"])
    .save(output)
    .on("end", () => res.json({ url: output }))
    .on("error", (err) => res.status(500).send(err));
});

// ===== EXPORT FINAL =====
app.post("/export", upload.single("video"), (req, res) => {
  const input = req.file.path;
  const output = `outputs/export_${Date.now()}.mp4`;

  ffmpeg(input)
    .outputOptions(["-preset fast", "-crf 23"])
    .save(output)
    .on("end", () => res.json({ url: output }))
    .on("error", (err) => res.status(500).send(err));
});

// ===== SERVIDOR =====
app.listen(3001, () => {
  console.log("🔥 Backend rodando em http://localhost:3001");
});

// ================= O QUE VOCÊ GANHOU =================
// ✔ Corte de vídeo REAL
// ✔ Adicionar áudio REAL
// ✔ Exportar vídeo REAL
// ✔ Base profissional estilo CapCut

// ================= PRÓXIMO NÍVEL =================
// - Banco de dados (MongoDB)
// - Login de usuários
// - Salvar projetos
// - IA real (OpenAI / visão)
// - Render em nuvem (escala grande)
