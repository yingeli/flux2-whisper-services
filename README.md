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