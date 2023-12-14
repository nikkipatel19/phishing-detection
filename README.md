phishing-website-detection
Follow below steps to setup phishing detector

Clone repo

git clone https://github.com/rubaramanan/phishing-website-detection.git
cd phishing-website-detection
mkdir -p models/sota
mkdir -p models/ensemble
mkdir -p models/traditional_ml
build docker image

docker build . -t phish_detector:1.0
Run the training model

docker-compose up train_model
Run the testing UI

docker-compose up -d streamlit
Open the ui using the link: http://localhost:8501
