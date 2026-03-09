const express = require('express');
const HaxballJS = require('haxball.js');
const app = express();

app.get('/', (req, res) => {
  res.send('✅ Servidor Nobre Haxball Ativo!');
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => console.log(`🚀 Servidor rodando na porta ${PORT}`));

// Iniciar Haxball
HaxballJS.then(HBInit => {
  const room = HBInit({
    roomName: "NOBRE HAXBALL",
    maxPlayers: 20,
    public: true,
    geo: { code: "BR" }
  });
  
  room.onRoomLink = link => console.log('✅ Sala criada:', link);
  console.log('🎮 Sala Haxball iniciada!');
}).catch(err => console.error('❌ Erro:', err));
