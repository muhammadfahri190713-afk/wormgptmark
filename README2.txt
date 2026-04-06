# Update & install Node.js
pkg update && pkg upgrade
pkg install nodejs git

# Buat folder
mkdir wormgpt && cd wormgpt

# Buat file package.json (copy dari atas)
cat > package.json << 'EOF'
{
  "name": "wormgpt",
  "version": "2.1.0",
  "description": "WormGPT - Unfiltered AI Assistant",
  "main": "wormgpt.js",
  "scripts": {
    "start": "node wormgpt.js"
  },
  "dependencies": {
    "@google/generative-ai": "^0.21.0",
    "chalk": "^4.1.2"
  }
}
EOF

# Buat file wormgpt.js (copy dari atas)
nano wormgpt.js  # paste seluruh script

# Install dependencies
npm install

# Jalankan WormGPT
npm start
