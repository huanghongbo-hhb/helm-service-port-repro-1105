# Helm Service same-port protocol reproduction

The `chart/templates/service.yaml` initially defines TCP/5060 only.
The next commit adds UDP/5060 directly to the template.
`chart/values.yaml` stays `{}` in both versions.

A zero-replica Deployment allows Zadig runtime inspection without running Pods.
Deploy this Chart only in an isolated test namespace.
