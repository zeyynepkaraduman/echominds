🧠 EchoMinds
Türkçe Akıllı Sesli Asistan — ElevenLabs + XTTS Entegrasyonlu

EchoMinds, Flutter kullanılarak geliştirilen bir sesli asistan uygulamasıdır.
Kullanıcılar hem metni sese (Text-to-Speech, TTS) dönüştürebilir hem de sesi metne (Speech-to-Text, STT) çevirebilir.
Ayrıca ElevenLabs API’si veya yerel XTTS v2 (Coqui.ai) sunucusu sayesinde, Türkçe konuşan klonlanmış bir ses oluşturabilir.

🚀 Özellikler

🎨 Modern, sade ve kullanıcı dostu Flutter arayüzü

🗣️ Türkçe metinden doğal ses üretimi (TTS)

🎧 Otomatik ses tanıma ve metne dönüştürme (STT)

🧠 ElevenLabs veya yerel XTTS ses desteği

💻 Android, iOS, Web ve masaüstü desteği

🔒 API anahtarlarını .env dosyasıyla güvenle yönetme

⚡ Kolay kurulum, açık kaynak ve geliştirici dostu yapı

⚙️ Kurulum
1️⃣ Flutter Ortamını Kur

Önce Flutter’ı sistemine kur:
👉 Flutter Kurulum Rehberi

2️⃣ Depoyu Klonla
git clone https://github.com/zeyynepkaraduman/echominds.git
cd echominds

3️⃣ Ortam Değişkenlerini Ayarla

Projedeki .env.example dosyasını kopyalayıp .env olarak yeniden adlandır:

cp .env.example .env


Daha sonra ElevenLabs hesabından API key al → ElevenLabs

ve şu şekilde ekle 👇

ELEVENLABS_API_KEY=your_api_key_here
ELEVENLABS_VOICE_ID=your_voice_id
ELEVENLABS_STT_MODEL=scribe_v1
# Yerel ses sunucusu kullanmak istersen:
LOCAL_TTS_URL=http://localhost:8000/tts


⚠️ Uyarı: Bu dosya .gitignore içinde gizlidir — asla GitHub’a yüklenmez!

4️⃣ Bağımlılıkları Yükle ve Çalıştır
flutter pub get
flutter run           # Mobil veya masaüstü için
# veya web için:
flutter run -d chrome

🔊 Yerel XTTS v2 Sunucusu Kurulumu (Opsiyonel)

Kendi ses tonunu kullanmak istiyorsan, yerel XTTS sunucusunu çalıştırabilirsin:

Gereksinimler:

Python 3.10+

ffmpeg

pip

pip install TTS fastapi uvicorn pydub numpy


Proje dizinine server.py dosyasını ekle (örnek yapı Issues kısmında mevcut).
Sonra sunucuyu başlat:

uvicorn server:app --host 0.0.0.0 --port 8000


.env içine ekle:

LOCAL_TTS_URL=http://localhost:8000/tts

🧩 Güvenlik

.env dosyası .gitignore içinde saklanır

Anahtarlar dotenv paketiyle güvenli şekilde okunur

Örnek .env.example dosyası geliştiricilere rehberlik eder

💬 Katkıda Bulun

EchoMinds açık kaynaklı bir projedir.
Yeni özellik önerileri, hata raporları veya pull request’ler her zaman açıktır. 💡

📬 İletişim: @zeyynepkaraduman

🌟 Destek Ol

Projeyi faydalı bulduysan lütfen bir ⭐ bırak!
EchoMinds, Türkçe ses teknolojilerini geliştirmek için topluluk desteğine açık. 💖
