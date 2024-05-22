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

az aks nodepool add \
    --resource-group aks-test-sea \
    --cluster-name aks-test-sea \
    --name a100pool \
    --priority Spot \
    --eviction-policy Delete \
    --spot-max-price -1 \
    --node-count 1 \
    --node-vm-size standard_nc24ads_a100_v4 \
    --node-taints sku=gpu:NoSchedule \
    --aks-custom-headers UseGPUDedicatedVHD=true \
    --gpu-instance-profile MIG1g