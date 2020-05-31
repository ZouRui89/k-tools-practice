# lesson 1 - cannot change resource name in patch yaml
```ssh
$ kustomize build $pwd
Error: no matches for OriginalId apps_v1_Deployment|~X|april; no matches for CurrentId apps_v1_Deployment|~X|april; failed to find unique target for patch apps_v1_Deployment|april
```
# lesson 2 - cannot leave resource name blank in patch yaml  
```ssh
$ kustomize build $pwd
Error: trouble configuring builtin PatchStrategicMergeTransformer with config: `
paths:
- restartStrategy.yaml
`: missing metadata.name in object {map[apiVersion:apps/v1 kind:Deployment spec:map[strategy:map[type:rolling-update]]]}
```
