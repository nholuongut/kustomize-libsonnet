# Kubernetes kustomize operations in jsonnet

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

This repo contains [`kustomize.libsonnet`](https://github.com/nholuongut/kustomize-libsonnet/blob/master/kustomize.libsonnet) - a jsonnet library that re-implements the core transformation operations of the Kubernetes [kustomize](https://kustomize.io/) tool.

There are two major differences from the real `kustomize` tool:
- The "overlay" file is described in jsonnet syntax, rather than `kustomize.yaml`.  Jsonnet is significantly more powerful, so you can trivially implement (and share) new transformations using this approach.
- The file I/O directives of `kustomize` are not implemented.  Jsonnet is a sand-boxed language, which is good for security, and a library cannot implement "new" ways to read files.  `kubecfg` already supports importing content from YAML/JSON files, and from remote URLs.

See [`example.jsonnet`](https://github.com/nholuongut/kustomize-libsonnet/blob/master/example.jsonnet) for one way to apply these transformations to existing YAML manifest files.  The example uses the [`kubecfg`](https://github.com/ksonnet/kubecfg) tool (to parse the input YAML files), although `kustomize.libsonnet` itself should also work in other jsonnet environments.  It can also be combined with other jsonnet libraries, such as [kube.libsonnet](https://github.com/nholuongut/kube-libsonnet) and [k.libsonnet](https://github.com/ksonnet/ksonnet-lib).

Note that (just like regular `kustomize`) projects using `kustomize.libsonnet` can "stack": **Team A** can import some upstream JSON/YAML (or jsonnet!) manifests, and apply a `kustomize.libsonnet` "overlay" to modify it for their particular needs.  **Team B** can import the `kustomize.libsonnet` from team A and then apply _another_ `kustomize.libsonnet` overlay with _their_ additional needs, and so on.

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: Nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)
* [PayPal.me](https://www.paypal.com/paypalme/nholuongut)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
