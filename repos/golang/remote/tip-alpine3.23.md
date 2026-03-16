## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:f165abb71494822e4aea07351b3be80a48dd1fb1343e9641edaf18ecbd50c6e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:b80bea9ac54e8ae9de54bb4dd8d9896d0c06eafa489fffff0efa1b0c94d56380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97885123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb6f7dce7c49d6884b556440cea23676a9d39129e0581c99eac75d7544a7cab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Mar 2026 18:04:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:05:45 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:45 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:45 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:05:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:05:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745fabe341fe38d8d9328ec1b4f1b6822c5eda6c035f963b54829ae143c0fbec`  
		Last Modified: Mon, 16 Mar 2026 18:06:01 GMT  
		Size: 296.1 KB (296072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4384ef542a16608e9b825ddf3c86dc09e4324c50fc9718c0261655531fdcaac`  
		Last Modified: Mon, 16 Mar 2026 18:05:32 GMT  
		Size: 93.7 MB (93727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43689c4dbd3be7aaa673816e7cd68a511ac3817adf011cca22445aa40e3b08c5`  
		Last Modified: Mon, 16 Mar 2026 18:06:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:38bcdf89250f8fca8735c9de740d231e0c2e46f4cdf03d713c3ed0e087ee2921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1d9fba312e10d6467c25e7b60067bdd01d59cb6ce3cc1e3b1584d0b69b4e2b`

```dockerfile
```

-	Layers:
	-	`sha256:648df96caf46f45ac44a4c6719a6e717464b61640b799ace52b7cab994662673`  
		Last Modified: Mon, 16 Mar 2026 18:06:01 GMT  
		Size: 195.6 KB (195603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d798cc89ae125289537b61ed6e50828f3ddb118e3de81a7391ab84d5cb47dd`  
		Last Modified: Mon, 16 Mar 2026 18:06:01 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:c70803228249b729c690f0d33f61f9cd11eb8030e28737ae50f31ec7604871fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93991624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bafeb828fdf9a0b230a11557ebdfe9217ed3214b2cc915a1a0ce9a6b3f1898d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 16 Mar 2026 18:04:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:07:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:07:08 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:07:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:07:08 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:07:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:07:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d129efc67f38cce117074a37c6411a57b3eabcda9d11ab3c9fe2f7c6354c2b3d`  
		Last Modified: Mon, 16 Mar 2026 18:07:22 GMT  
		Size: 297.3 KB (297260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c3f6a56e865a19fa0deed8e946128d26d201e7f5b3dbcac6e5be64a7d0b4eb`  
		Last Modified: Mon, 16 Mar 2026 18:07:25 GMT  
		Size: 90.1 MB (90124385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e85fc361b48aaa280b290472c75a394b860fb1a0f243796eea9417d5e64d7ec`  
		Last Modified: Mon, 16 Mar 2026 18:07:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:7ae1974fd38e594af17756f23c4e6a2b1d3b116a355930689f14784e4147f3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aeb12dac4aa27a35f1827d82d9ab3a54549fa859b33eb5322eca95c14d6fe77`

```dockerfile
```

-	Layers:
	-	`sha256:11bd1aaad9af601ebd5e3e4de826e95cada0be7d351346318c151899a1414268`  
		Last Modified: Mon, 16 Mar 2026 18:07:23 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:f0a8575c22498900fc32b183503e083687273233207723d071937d9e22bdcea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93416846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb962d1a5f732b318381f9a11aaff2b8a75685e88fb2f384943ff0db99f93198`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 16 Mar 2026 18:04:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:06:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:51 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:51 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:06:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:06:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ebbc0886e79433f83b4c6ccca9c89bf88fd105a277c4e92e59b0b17383d906`  
		Last Modified: Mon, 16 Mar 2026 18:07:09 GMT  
		Size: 296.2 KB (296196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3549b40c9d6609f7ae376dd04fb2e1ccc5bd7d54b10023e8efe518db570d9`  
		Last Modified: Mon, 16 Mar 2026 18:06:19 GMT  
		Size: 89.8 MB (89838768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075ee6c1fa64e31f3da8c34f3da9ea72187c588286548bfd84e7e1a275aabfcc`  
		Last Modified: Mon, 16 Mar 2026 18:07:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:69f861ec02cc5a212022738493018b7b03178f08d75bba90927a23e37b6d8701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9c1f6fb0a6612d8d491d7b26eeecfe648d1063f799e205da2d6d8c32e6131e`

```dockerfile
```

-	Layers:
	-	`sha256:f76dfbe3670c60259e47d31a2be861fe16fce3bb45f067b66f3286368aa6d552`  
		Last Modified: Mon, 16 Mar 2026 18:07:09 GMT  
		Size: 195.0 KB (194973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894fe6f4c24c8c1c427b49dfc6d1410c81d250303aa1ab41ae53ecf6a60acf0f`  
		Last Modified: Mon, 16 Mar 2026 18:07:09 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f51b02f98fadda417a5a29f5760b9a184fa511d03b4386088f5927c7a5db01e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93409556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b902a51917fe8aabf1bb06b797c9a771a297c6fcf3e56dd093694fa7cd7a2478`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 16 Mar 2026 18:05:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:04:51 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:04:51 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:04:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:04:51 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98da78cdb1ea71ca7399bb91f7799ebfa00b332de69a4ccdd5d206fef8ebb198`  
		Last Modified: Mon, 16 Mar 2026 18:07:25 GMT  
		Size: 298.8 KB (298843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad36eab247615030277063307261e70ef31ab1fb10cb9e2a3d5ec600c3c4c21e`  
		Last Modified: Mon, 16 Mar 2026 18:05:21 GMT  
		Size: 88.9 MB (88913464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f20585a17e606df423056ee1aa888d8a7bad23a72a893335f8123b9a92ac767`  
		Last Modified: Mon, 16 Mar 2026 18:07:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:9ae2decfd9ee110fd9ebc7eab1e77dfb3ba57836a69bffd2ec039d1526b6059d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3b9e73f026c1ff84dd2ac0a70ffabf8101d2a17d64f2d815b5f0dc6f0d6f6e`

```dockerfile
```

-	Layers:
	-	`sha256:567808edf7bd696b5cda5b90c87091125b279fdd13a373a33074e39f0037f8f2`  
		Last Modified: Mon, 16 Mar 2026 18:07:25 GMT  
		Size: 195.0 KB (195009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d7692b689063f1ad437d9c448c7b3197a4ffeeacb87e2a9c9af4873f207d9d`  
		Last Modified: Mon, 16 Mar 2026 18:07:25 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:030eb942a56fe7df1f0b9c8ccb09b9f6bcbde8398780822baaf99fcc85d3bacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95560335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3f361fe6c0389760eaf408eb02db5b9ad4c71b400d21f47df5da432c35c649`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Mon, 16 Mar 2026 18:04:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:06:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:27 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:27 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:06:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:06:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3017f72b2e17d31e9eaad3f8397b354043c13e13ff9cfd8c49a853f768b5fa39`  
		Last Modified: Mon, 16 Mar 2026 18:06:43 GMT  
		Size: 296.7 KB (296670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beadfccec3ab6ced574e10800119a7f79c633318e3fc8b60061f1b218729af5`  
		Last Modified: Mon, 16 Mar 2026 18:05:47 GMT  
		Size: 91.6 MB (91576509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194b2cb25e1644b4172af9589625a9d5fd63ba517f048c424f5c903ff7bdc543`  
		Last Modified: Mon, 16 Mar 2026 18:06:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d7cc2e9d524ec0ae6ec0657539eb8167cfc7a0b7d2b66dc6d74954e6c038930b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a9e1b02b497ae1c8e56e75d35aebc2eac46da4c34412390d95aac60fc91cb2`

```dockerfile
```

-	Layers:
	-	`sha256:4ca055a821c7385daa8d75a5479f714e6155f07d4e7dbfadb298cbf7cbd082bd`  
		Last Modified: Mon, 16 Mar 2026 18:06:43 GMT  
		Size: 195.6 KB (195562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b27e626005810c0cea018d71ed2fe7bb44a6570cf442e83fc37d2fa9510bf55`  
		Last Modified: Mon, 16 Mar 2026 18:06:43 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:6760f70c51d4ec7287df9a565b488606ca15a0b9478e392fac8db588b48d61d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94575032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c97e0434ff4b46eb626427f17e176934e47dfb672fabaa05f8d2d1f43f547f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:42 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:10:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:10:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662a4a3a7cbf153b23a38a961b2078122cec8354bbb9cc27381fb9fd6abd628`  
		Last Modified: Fri, 06 Mar 2026 01:12:55 GMT  
		Size: 299.3 KB (299266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ba3f21f31dd88c9cf395edb0e30aca822e3dcde51bd5a6421a6f428d5671b`  
		Last Modified: Mon, 16 Mar 2026 18:06:39 GMT  
		Size: 90.4 MB (90445965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cb6b859449e976d26673453f2fe53305ab1228fc4e20c2d407f245fadce2ca`  
		Last Modified: Mon, 16 Mar 2026 18:10:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:82ef50a8aa18e20538537fdcb1ae021d5acd309dbfa1f0637060f5f26224c052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da5e0aba9c66661ef16712a981e2bfb25960466972fb07caf8f4c4caa337d8e`

```dockerfile
```

-	Layers:
	-	`sha256:f10ff6b2ee436bcdf4c9be3c39062201fca0cf06ae4a2b009aecec3d8e43c86b`  
		Last Modified: Mon, 16 Mar 2026 18:10:56 GMT  
		Size: 195.0 KB (195002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d059552d5b040a2420ed302c22af25528b16b34cbef1f05e696faf0a60bc6e5`  
		Last Modified: Mon, 16 Mar 2026 18:10:56 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:b7d2f801f5b441cfb42de36a752ab534a77356b2f5b165b64cbd49fa494bbeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94730454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8ac1df05371c6562955e2d5b8fa38efc5f82ae3027d815b576d04b78f5245e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 11 Mar 2026 12:00:31 GMT
ENV GOTOOLCHAIN=local
# Wed, 11 Mar 2026 12:00:31 GMT
ENV GOPATH=/go
# Wed, 11 Mar 2026 12:00:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 12:00:31 GMT
COPY /target/ / # buildkit
# Wed, 11 Mar 2026 12:00:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 11 Mar 2026 12:00:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bc24504758bc2cc1729ec44c511dc8a56283661d267f3db6620c6d9d369bf2`  
		Last Modified: Wed, 11 Mar 2026 12:03:53 GMT  
		Size: 90.8 MB (90848504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb75a4dd4f50a9136ffbfe3c9e506b554bd09e065225613a0da51d4c71700cb`  
		Last Modified: Wed, 11 Mar 2026 12:03:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:5269eea4ef9aef1a8a95a7b40321e4e8df2f2706c301822d4487f210d78f5695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0193feaaac77a81a9ee56866928a52e75dbe35d0825b11e84e0a850c355c4e`

```dockerfile
```

-	Layers:
	-	`sha256:7b6fa7b26fc0ec749dda41937ed8d8dda18e414a90bf22eda19c71026f4a3545`  
		Last Modified: Wed, 11 Mar 2026 12:03:39 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8932970f98c675ffd06205a5450f57c06a01a9854b38fc8db4ad0cd5456ba9f5`  
		Last Modified: Wed, 11 Mar 2026 12:03:39 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:e7855196060d4d431418ac0d5c0824849def972714c4d74d78d7ea48b48c2e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96948027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c776e356500ab4966fe9e4f20c2c7a131c88f83c447593a182318d9af9943dde`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:10:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:06:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:20 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:20 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:06:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:06:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79449d8f37ca627569c53e700d0b5ae9b25ebeef0a08dac074cc719821e22ba7`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 297.2 KB (297183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e78b174fccd5298debc49ecb6092c7b356413921318c225406833e6427b55a`  
		Last Modified: Mon, 16 Mar 2026 18:06:51 GMT  
		Size: 92.9 MB (92925352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004ee7e0e08703b1a9be8bf38c027e997c34a2f3405463a485514dfeb1db9437`  
		Last Modified: Mon, 16 Mar 2026 18:06:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:ffb99dfe9c4422aa328fce5d7e08639053b96e25ab48134a8d736f1008888842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285f2bf1f21e685dbfdca14cdf1aa8af03b7c4b10d2836617c907c963e462a8d`

```dockerfile
```

-	Layers:
	-	`sha256:c1d5b3e16faf0094552e4d1a095d9477450dcb161e01d27c35007249a671c488`  
		Last Modified: Mon, 16 Mar 2026 18:06:47 GMT  
		Size: 195.0 KB (194952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7160a7dbdd464d6e260ff9d41787605e94d7c978c87303c5f16043d9b112bc9`  
		Last Modified: Mon, 16 Mar 2026 18:06:47 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
