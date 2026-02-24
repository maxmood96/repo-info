## `golang:tip-20260221-alpine`

```console
$ docker pull golang@sha256:4549c4199a59b02f62df99d3b051f10fd7d767d5aaece262055ffc992e2392dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `golang:tip-20260221-alpine` - linux; amd64

```console
$ docker pull golang@sha256:80c98b2f591b559298fbf6e35c0b126e8d3e45a6230609a1fadc11eba3574617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97722014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36799d2a361a92df0a95e35ba9c5531a28de0cc77872af928885143462a612a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 18:59:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 19:00:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 19:00:52 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 19:00:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:00:52 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 19:00:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 19:00:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aab7fd08c93b92d1bf4ffa9c91cd9f96730a2d31b8beae96be708709fa9bcc`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 296.1 KB (296077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d495feeee1b60c984a8277e0860f99ef7f9650e71ef87f6e01f020f04c712c1e`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 93.6 MB (93563958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a3c7431ca94d41cd1559e8378df7ee46baa6b3b5de81a74f0362c0cf39cc77`  
		Last Modified: Tue, 24 Feb 2026 19:01:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:254e606ae22cb7a9cb801655942a8ccd20307e33f23df6de7a829aee93ee871b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daf1c571cb949f786b59c60a1e34bce2b7d400293751d40531d3a7111e22377`

```dockerfile
```

-	Layers:
	-	`sha256:01ebe897a0e718a655d77a11ed736d55987c8f9c4151f2860f09c9326d6dbd6e`  
		Last Modified: Tue, 24 Feb 2026 19:01:09 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:337b6d89b9463532274627c9757a6f6f3c4d4be499e5763db149ca84abc242aa`  
		Last Modified: Tue, 24 Feb 2026 19:01:11 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260221-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:d1ca2f7adbb55d768d8b743c51cefaaf515ea254e9aeb01dde05ad0c0b76edf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93791665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755ac43348efb03416cfb8e6d1091d9f268077e66b1a43635a12325b5e27a798`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 18:52:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 24 Feb 2026 18:55:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 24 Feb 2026 18:55:11 GMT
ENV GOPATH=/go
# Tue, 24 Feb 2026 18:55:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 18:55:11 GMT
COPY /target/ / # buildkit
# Tue, 24 Feb 2026 18:55:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 24 Feb 2026 18:55:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65468684cd5cedb57d9b6d7eb6dfce87d67815259cfcc4e47e7b1bd90acc3528`  
		Last Modified: Tue, 24 Feb 2026 18:55:25 GMT  
		Size: 297.3 KB (297253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2e155fb43fa9561b40b4cc63456cea59d7ad2c026c1d617fd7ee8b216af790`  
		Last Modified: Tue, 24 Feb 2026 18:55:27 GMT  
		Size: 89.9 MB (89924433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0884bd8cc8cab88ed070b29fe82c67cf5aaa677c8e657cd9f11bf501b199573`  
		Last Modified: Tue, 24 Feb 2026 18:55:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260221-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cbf652461dd3fafb791ccbc07b19654d4d4086eccf33eba458c8e858e2e61ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854e66f0937d0b504f278ebd13820b815ad895f1aa47f23584ea3171782ef5a0`

```dockerfile
```

-	Layers:
	-	`sha256:2a0f33b3a7e3838197fe7b47c2b4e37a15941c1558a1ed8f2d00d7ee1459ec94`  
		Last Modified: Tue, 24 Feb 2026 18:55:25 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json
