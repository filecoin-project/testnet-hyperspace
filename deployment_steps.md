# Deployment steps:

1. Confirm that all the work in the built-in actors `integration/builtin-api` branch is also in the `next` branch before we cut the actors release bundle for the deployment. (ask @aayush to check)
2. Use a branch @jennijuju will prepare based on M2 branch at https://github.com/filecoin-project/lotus/tree/experimental/fvm-m2
3. Add `build/params_hyperspace.go`
4. Create PR to Lotus
5. Wait 24 hours for any community requests for changes
6. Deploy the testnet
7. Ask the Lotus team to create a tag
8. Update this `filecoin-project/testnet-hyperspace` repo's [README](README.md) with exact commit/tag used
9. Notify testnet RPC endpoint providers and block explorers
10. Update Filecoin developers in Slack
