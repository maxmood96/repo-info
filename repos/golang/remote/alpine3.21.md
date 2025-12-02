## `golang:alpine3.21`

```console
$ docker pull golang@sha256:b4dbd292a0852331c89dfd64e84d16811f3e3aae4c73c13d026c4d200715aff6
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

### `golang:alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:24fbde4c85203ef24be997b1771f3c434c8f9cb744215c0c934cbab9f8e901f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64085167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6b1d6ee108589b06bc8efcb11c95edd57cbfa885ddf864770f17cdf6a7d025`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:47:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:50 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:50 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:50 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948001b8900d5eb1b7409818f83a544642a4754c2efc35044c06f35d970a3d7`  
		Last Modified: Tue, 02 Dec 2025 17:48:19 GMT  
		Size: 291.1 KB (291126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a29c4a2fee2262e0e4d0e719895f0b48f2f1bc35ed1e4f2fc624b73e8e993`  
		Last Modified: Tue, 02 Dec 2025 17:48:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:aa2900df187c530d4022c1f35a3281af48a4868e6eba8835c8c2037a76dbb55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 KB (218372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752c4b3ec3cc521d7b7f62862576536f5371b2fe2e29b807c70316a3b08b305a`

```dockerfile
```

-	Layers:
	-	`sha256:42488f5c910a4de8b341ea4228beac22877f225141744f3da33b6ca34911157e`  
		Last Modified: Tue, 02 Dec 2025 18:09:45 GMT  
		Size: 193.6 KB (193565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e389a5725ff48f1db205104d1b7e4c46ef24396302b915f427a0a09342d10f09`  
		Last Modified: Tue, 02 Dec 2025 18:09:46 GMT  
		Size: 24.8 KB (24807 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:e06d4ae86ca66a7a8367bcd783592e8a54d19c8bb3c24f726a9f4e12bdd7854a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62729836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e8ac7329a69645a47a5ab29fbb4fb8909b6e3282a22a202000ef008f209178`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:46:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:12 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:12 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:47:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:47:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68ad528bd1fbb4fbb988dd18a5582c0082525dc5dc7f9754699a2c7d3cc1eb1`  
		Last Modified: Tue, 02 Dec 2025 17:47:48 GMT  
		Size: 292.3 KB (292255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43dd4211ee5273ca0c5772840c1a03b86bde39c606d1c608d88cc81d6d76501`  
		Last Modified: Tue, 02 Dec 2025 17:47:55 GMT  
		Size: 59.1 MB (59071955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09615bee918a0a1913f982926164fe321067b4ae8a2bd5e632e16e062e052073`  
		Last Modified: Tue, 02 Dec 2025 17:47:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:852318bd98dd4e57617ed41119c65e20d53f53a689e0b3a7a9c81f135e71ebd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339736b8e6f5695a2a45a5bd8ca03a7cf1f868100f426fe227a534440ec5c729`

```dockerfile
```

-	Layers:
	-	`sha256:df10c0ef714c56fe76b93e4d890ec0c69eb8ed47e96f8ee3af6cc4a490be8e3a`  
		Last Modified: Tue, 02 Dec 2025 18:09:49 GMT  
		Size: 24.7 KB (24698 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:d57052049a64d530a34065a29b641c8e83510cfff68d03e01def5ef956ce234d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62461980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb139bc3d588e4ce7905da36b93fdffbdf04d52040d03253f31f08ab62ab9432`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:48:13 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:48:22 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:22 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:22 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5197af787cd4bdb6a73fdb8df08b6d75ed13b22f781b96b9578e273a46c036c`  
		Last Modified: Tue, 02 Dec 2025 17:49:16 GMT  
		Size: 291.1 KB (291149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4946062918dfd3c66a344129edbc562c5cf52fea2ed272d58bac213cc5445869`  
		Last Modified: Tue, 02 Dec 2025 17:48:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:e805d2b4d151077a77c8c98a33a659161c2adc316deb5536aa2b2797ef734da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 KB (218499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc9f313a691186e2c716fc46cfba99d8c8eb5f524b1e0667a770f511e159fb2`

```dockerfile
```

-	Layers:
	-	`sha256:441b0e59f9ae847df7831728de94562f058bab452bae4001e35ba9a9b77afa1f`  
		Last Modified: Tue, 02 Dec 2025 18:09:52 GMT  
		Size: 193.6 KB (193587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0552d4bcb162fe5a2b683ab172668e8025faa244f42b256b84a10b1cde2429bc`  
		Last Modified: Tue, 02 Dec 2025 18:09:53 GMT  
		Size: 24.9 KB (24912 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b7da56a7c021d021bac4c7a69c192d83f1e7a02285a815d2bc863e9234f08fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61937480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67775ef7ec808e6a68952c4ff996af1dfbd0f0025d4318390f8355f761fdeb0a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:48:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:48:22 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:22 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:22 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471b6b8735bccfc6c5e5c5ca758ac7807739cba922e169bb0f03dbc00c5053e5`  
		Last Modified: Tue, 02 Dec 2025 17:48:43 GMT  
		Size: 294.1 KB (294052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4946062918dfd3c66a344129edbc562c5cf52fea2ed272d58bac213cc5445869`  
		Last Modified: Tue, 02 Dec 2025 17:48:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:4102e6e587e22d014e3b4f9a65df25ce74fe25352c709b59e2a173b5dda47a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5b933697ea8cdf651fbe057d6ef24b89c25069bc454eda63f9969e3ea16b0c`

```dockerfile
```

-	Layers:
	-	`sha256:d44ca034ccbc98630f1c0a9b3432ead2515314d5a8899f69a9d0bd1d24de6853`  
		Last Modified: Tue, 02 Dec 2025 18:09:57 GMT  
		Size: 193.6 KB (193621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f45d71d11868d082a809698ed8de08898b61b8fc89cfe859232088fd08ea157`  
		Last Modified: Tue, 02 Dec 2025 18:09:57 GMT  
		Size: 24.9 KB (24941 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:f00c5149c733609017275c653826a4140a0ff5577826e07a8060afb663ac3147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62628403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1890a7cb2b788a5c8e31a58efd4b02afdf1929fa5598acdbe98a87f5e09f641b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 02 Dec 2025 17:48:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:49:56 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:49:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:49:56 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:49:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:49:56 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:49:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:49:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c3e9f87dc113027c5043c28cfec3dc324ab0fc5e213602ecfd7bf9d5cce417`  
		Last Modified: Tue, 02 Dec 2025 17:50:16 GMT  
		Size: 291.6 KB (291602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b0da2f739b41a66eedd8d3b82617bbcf80f4ca5b304911a7a9566314556cdc`  
		Last Modified: Tue, 02 Dec 2025 17:50:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:413d920a4c77068acf739099b69352a504771a648379fcac67ff72be414118ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeadf4167ef176876831b8048d39aecdae142b224f97282d935fe009f1ddcc1`

```dockerfile
```

-	Layers:
	-	`sha256:82cfa13f5cbed0c2313588f8de63343e0d488349f9d674bf91afc25b33fcb512`  
		Last Modified: Tue, 02 Dec 2025 18:10:00 GMT  
		Size: 193.5 KB (193526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448768c2f53caf2ee9a79bff18d6944cc1bd720aac810fa4237a49342644c941`  
		Last Modified: Tue, 02 Dec 2025 18:10:01 GMT  
		Size: 24.8 KB (24771 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:caeb9b9c76b52ba3e34a255131b4ab1286c62a15a644f2b60d04a0f746edf082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62003715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145c7dfb0aa78c0010f1681fbe3c9c17c44edd36ded76e7a07d3d7bc4a03dcf8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:46:09 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:46:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:46:09 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d14bc2600d22e26b66141fbf5771e98d7b9f0ed471d3d19e6d7cdec0462ee2`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.5 KB (294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe3074abc6346584ebb7d175a96261ddfaf687149e8a47e8c83b0d8c9e1691`  
		Last Modified: Tue, 02 Dec 2025 17:49:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:2c793d10c8c36d77d7250674893cfb27964c280051495cbedc40f9dc074bc141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c9a0021428352c8cde1a5afbc17d62232618e34edd348d734b039127923271`

```dockerfile
```

-	Layers:
	-	`sha256:6042b7f1cd11c2bf70a575876b14d0871c7dab166f6680008a8b2ddc2aad2c41`  
		Last Modified: Tue, 02 Dec 2025 18:10:05 GMT  
		Size: 191.7 KB (191662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940bbee643b083fba6f80e88acdfa7d5aeee4dadca67b126d251b34b65bb440f`  
		Last Modified: Tue, 02 Dec 2025 18:10:06 GMT  
		Size: 24.9 KB (24855 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:34ae4408163b33b4d7b04f655578a865238bbf3284400417fe0fb801ba2d86c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62315085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490a0b1414c1e8b2b5e2164bb29b379c2915dbb8d5ecd63521bd70eaf35c0edc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:57:08 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:21 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:58:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:58:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18712178673f08c74f02c4b24f31fd1452a6014b2c1769c0702341368bb31984`  
		Last Modified: Tue, 25 Nov 2025 07:58:45 GMT  
		Size: 291.5 KB (291482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6199a15922cf0533082f2bfb9bf03dc54fb7fdb4f830e8dae324efa57d8b9`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 58.7 MB (58672443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef84fa1ecbae4ef347930cbbdc8e30c8b364ede5e7018ca3ca48a5db8ef33b8`  
		Last Modified: Tue, 02 Dec 2025 17:59:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:6af23fbc8c6a821f2bad8821d82df59aa674f7ecd2d5ecc54d9fe15bab3710eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 KB (216513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efaadd1fab000b9470e9ebf1c9519292131f42011a06e45823bc2ebbb5fb9b`

```dockerfile
```

-	Layers:
	-	`sha256:386a405c5e5be80f6dc60321881a30331ada3afef78d6a336f8d2078c5f7fe75`  
		Last Modified: Tue, 02 Dec 2025 18:10:10 GMT  
		Size: 191.7 KB (191658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd578153dfee3518ae32e6273243ad74d85e1745e5a3178a5ae399960d92a6d`  
		Last Modified: Tue, 02 Dec 2025 18:10:11 GMT  
		Size: 24.9 KB (24855 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:b8d51c7d3eb62070db21fe9c091a950d4daa87ebf7951bd7b21766b8172aea4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63245917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9f8db2f493df9502b6f0ad3ad38e66beaa5fa739200ac5c8844056d6c6b1db`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:37:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:48:11 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:48:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:48:11 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:48:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:48:11 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:48:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:48:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d509e219c5ad3999bec42645217672b0ca85b22769fdf4a1dfd591af7e5d05`  
		Last Modified: Mon, 24 Nov 2025 22:38:18 GMT  
		Size: 292.1 KB (292104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24644c9c8d72b7eeaac69d4fd6498522e17774698cf1d50b5fd84284b60cf43`  
		Last Modified: Tue, 02 Dec 2025 17:49:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8cc7f2f0b062547c6a4b04178aa4ef9672267f26731e57eb400b6a0e12af5043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 KB (216248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c70580bd06dd780bab1d17cf85c6d78d026c3803fc057c2d81c6f187f24afe7`

```dockerfile
```

-	Layers:
	-	`sha256:426b99ee0035c286d707bd88d2d06be80c20a935b3b9ce75df0c7f965b6cbe1f`  
		Last Modified: Tue, 02 Dec 2025 18:10:14 GMT  
		Size: 191.6 KB (191614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14ce386073561b9a04bb40ed5887ea8dd1d82aff29cfbf649a976aa28f806e9`  
		Last Modified: Tue, 02 Dec 2025 18:10:15 GMT  
		Size: 24.6 KB (24634 bytes)  
		MIME: application/vnd.in-toto+json
