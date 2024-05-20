# flux2-whisper-services

export GITHUB_TOKEN=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

flux bootstrap github \
  --token-auth \
  --owner=yingeli \
  --repository=flux2-whisper-services \
  --branch=main \
  --path=clusters/test \
  --personal

  az aks get-credentials --name aks-test-sea --resource-group aks-test-sea

  curl -X POST -H "content-type: multipart/form-data" -F "audio_file=@./audio/issue3/0_5f9df078-2617-4fbe-a01a-5c2e0a7f5d73.wav" https://whisper.yglabs.eu.org/detect-language?output=json
