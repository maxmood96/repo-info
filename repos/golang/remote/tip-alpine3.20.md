## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:9e03102f5ce4d71aa0a4f3cf2cd434d4fd45972ffac51a6eb6543f79092d44dc
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

### `golang:tip-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:7fad61d8f3a520823a7ca9c068de2b306051f477c7d502193522a8e0ac8a111e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130577793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de607f01e680860e9125927e12535bd59b7c73845588b84d6ac7cb1bf9bc25a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Apr 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2187bbd37c5f966706818ac1e054e1e67f25477db5e5b40bac592c3ca52acd`  
		Last Modified: Mon, 28 Apr 2025 18:22:57 GMT  
		Size: 294.4 KB (294392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65846c33088373b4d6ff39b83056f623dac3e1cb831137df32e4e70bf9d848be`  
		Last Modified: Mon, 28 Apr 2025 18:22:59 GMT  
		Size: 126.7 MB (126656346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8706dc33c20d96b926af6ae104b061ec93372d55d2860518181c8ef1c3e2409`  
		Last Modified: Mon, 28 Apr 2025 18:22:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:d59fef97e2e7a2dbe76b63f269475482942d5471521989abf09ce87836237a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8612f508547855a8c6760fb81a92587c8b74c7312711ba3ec0b81452ac78845`

```dockerfile
```

-	Layers:
	-	`sha256:447a72bed71f1611d026f5d31ad96b510502a5b7d812e6d44c082845370fc1d3`  
		Last Modified: Mon, 28 Apr 2025 18:22:57 GMT  
		Size: 205.4 KB (205443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cdfb580f32910cb73ba29b1c3c22b1ca14c17d78f4130764b7ab9d609c7785e`  
		Last Modified: Mon, 28 Apr 2025 18:22:57 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:e81a9990d49d4fb43f419ba6bf6aa478cbd9a229c4de830d35039323b4ec023e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125666007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72236294477a8e7d28cf92cecda749d101fd96d8635d41016ee4de672bfd4bff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Apr 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97851062255dcc908b267be280f34f34aa5fae0f9d43c72504ba8ac52739c9`  
		Last Modified: Mon, 28 Apr 2025 18:32:38 GMT  
		Size: 122.0 MB (121997485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d129235a8278218f5de7b65cb4edd4c0874aa1dccada614c0eabf053d52267f`  
		Last Modified: Mon, 28 Apr 2025 18:35:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:64a38b68389a53914211e8bbf7290ddaddc63da30846ab4e6cc772c855a94b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47e811965c381ad358528959cdc1b2dd2574514ba8cf9079c954851dfd8e993`

```dockerfile
```

-	Layers:
	-	`sha256:dee08ae04280a298050fb22494682ef03190a99fbe8e87383d76b656a0f81ea6`  
		Last Modified: Mon, 28 Apr 2025 18:35:36 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:2acd71c1785eb1b5e0e9fe8b0c3189a8009be29e741d6f951c274d575a8daf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125065610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279b5732900f8385c8431a68675970c2c6a69e9993199cee27fb8e6581bd4890`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Apr 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33618dace1ba528dcd7b40e80a4e895530a8d058bda71f5a87abf8312ed70c2`  
		Last Modified: Mon, 28 Apr 2025 18:46:15 GMT  
		Size: 121.7 MB (121674729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0d279648713dadfb6f6566883dacb6d3f25b822a3f2be7870d00f8ecbc5e4e`  
		Last Modified: Mon, 28 Apr 2025 18:56:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:8d23e37e83731da25ac991964dcb9794fedcff34be5eab59bf314d0979f2223a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70cfbbc01e608580ff938b842a110fcfcabaa6173b58150c2a19b2f3f0d7293`

```dockerfile
```

-	Layers:
	-	`sha256:c7fcdf5d51b39dd95507271c530a2275de2386503d2fe626d05e8173d150bc91`  
		Last Modified: Mon, 28 Apr 2025 18:56:12 GMT  
		Size: 205.4 KB (205423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca539374a3d9a9b55aa0036f805ec69ecf4d888b778e40a291b18bcc9deac77`  
		Last Modified: Mon, 28 Apr 2025 18:56:12 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7ef90986aa6512d74b4151581f86ef005a51e28a5ca47b9e946d4cc71f2f68ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123789189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614cd08b9729414621e5ddc3f5274dcb71b417c3fcd9da297390dc6b53d33c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Apr 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d91181a4474d3822cc4cabd1e8df2eed7942133a31b6fe7528c1a3639a00d`  
		Last Modified: Mon, 14 Apr 2025 21:56:34 GMT  
		Size: 297.5 KB (297478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280b2cbe9b185a145cd427125ccd35e0250a80679d21036014ab14fdf1e6e707`  
		Last Modified: Mon, 28 Apr 2025 18:48:43 GMT  
		Size: 119.4 MB (119400389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc807d92433ee678a0a3658960e37b015b5fb2dd88baa644a5e2abc169e7036`  
		Last Modified: Mon, 28 Apr 2025 18:55:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a51ae182b06d48a09c5afe6faa49ce935973d75ed26a75bae46369165eacf8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 KB (230123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915b9d5e16796e5b472535e78f6c902270330bafcab9a674ec5bc25802d595a`

```dockerfile
```

-	Layers:
	-	`sha256:3096d7805b17f9fd2fb81729e435ca244f5284c0be98810abcf257e6f7f4a766`  
		Last Modified: Mon, 28 Apr 2025 18:55:01 GMT  
		Size: 205.5 KB (205475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d965642f5f5c8b53c654f3427d913d2a414dce211e4e5e718a6bec932b7a36c6`  
		Last Modified: Mon, 28 Apr 2025 18:55:00 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:ba4449677bffc85884134e155016fdf8ad1cde7d3d932c47a279f7792a9c9728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128809664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd67c8e48ae98386094f5987c9e1b19efe775741d08b9ecea9f73dbf41425b36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Apr 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f796f621f7690e2bf4044fe8dfd31f16f7771531836181d7f81b59d7d00f794c`  
		Last Modified: Mon, 28 Apr 2025 18:23:33 GMT  
		Size: 295.2 KB (295153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42eb229ffaec8bb2d4ae5f6af15344b1b77eb404d2dcc67eaa5dd80ff2f2957`  
		Last Modified: Mon, 28 Apr 2025 18:23:36 GMT  
		Size: 125.0 MB (125042685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe8266eb7a2c09e00b6f8a773db31f894ed42184d65bc16c81a58ad4e260901`  
		Last Modified: Mon, 28 Apr 2025 18:23:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ac21daf7cf7206d83d98fae6ddde0e678802f6da45f6026281ac6490156390a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284e74c9bb0ce709a270193afe972cea3ffe8dd0b70f027c06b4c00fafa6b1e1`

```dockerfile
```

-	Layers:
	-	`sha256:d25771377f9aa71d41f23b45c7bec9bc2730ebcc3730a0ea795611e1632f5d0d`  
		Last Modified: Mon, 28 Apr 2025 18:23:33 GMT  
		Size: 205.4 KB (205388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3975ef61be34289f7995c15fc101ec7cd11f10c5aa66eed4cfd90b98042a11`  
		Last Modified: Mon, 28 Apr 2025 18:23:33 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:f63b7e71b79cba18c1c0c004b6231fc78dd62219468b5659e33f5c69419a641f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125433175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bf0d7edd68f5f42464cd55885ac136eba8aa94596bf80eef25524a9df629d5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Apr 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5950c2617b2e37b28d36382b32bdc610566f7587eaecf172653230b9278424e`  
		Last Modified: Mon, 14 Apr 2025 21:58:56 GMT  
		Size: 297.9 KB (297899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e2c76c2b3dfa96df067175069013952b6bbd2cd22cc810dd73e4d9fc005619`  
		Last Modified: Mon, 28 Apr 2025 19:13:46 GMT  
		Size: 121.6 MB (121559438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e307666cbf98dc284ce60254bcf3c5efc32ee7e501a5d951c6ea9b86fa206c`  
		Last Modified: Mon, 28 Apr 2025 19:20:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:3f04c468ab21c6827c5f2fc026dc69a78b195abebc2d65eef322c1cc718a002f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 KB (228112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589c76a24adc5e6d10679dbe0923b0647bf9697068dd77f7dc7f6654549d61fe`

```dockerfile
```

-	Layers:
	-	`sha256:24096b6f12c58c77b8726fc11d5a551a0814dc933e750fbf37d0a42cbc90359d`  
		Last Modified: Mon, 28 Apr 2025 19:20:32 GMT  
		Size: 203.6 KB (203554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc169ca73d2be6b65f4b21e9918347d953475131622f1c49393ea1aad2bee2e`  
		Last Modified: Mon, 28 Apr 2025 19:20:32 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:db07878f4da6209130b3f4e87f0d321f44433af738534e0cd484ebf8a05913b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125707381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb5576084690850b0e23172bb3e7a6f3c5d39f38bb3994c583969b010a8f9c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 21 Apr 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb12bf697d577c42f53f652ba0fb4c4093c94ce6986095953e539f07ea9b28f`  
		Last Modified: Tue, 22 Apr 2025 00:14:55 GMT  
		Size: 122.0 MB (122038546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4e481f4d39b148cbfee82157b624667c704179fc22ee5d81ffab8d666be2d9`  
		Last Modified: Tue, 22 Apr 2025 00:52:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:fa579489812307ca0ddf69976299c3589f0e5a50e03abe628bc1f921ffd955b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 KB (228108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b9316e257af9230b0b6604d71c5828dbbaf1909913b801deb18e0f3b36aff2`

```dockerfile
```

-	Layers:
	-	`sha256:e30e50012223f2363d51f28474054af21031a5f47031a9657547b42d78f4e74b`  
		Last Modified: Tue, 22 Apr 2025 00:52:45 GMT  
		Size: 203.6 KB (203550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81483f02d569793e591c6c1a22ccfad8da418c3d5e7c1039b2aa5f0eb31ac972`  
		Last Modified: Tue, 22 Apr 2025 00:52:45 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:eb54d508a6bc1ff8a2f601d425048563411914b10c62547b8bc869d190441fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127830237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9300835b87b751dc7351115246ccbc3e4ee4b03bef17623526247cffa6cb7fec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Apr 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 28 Apr 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 28 Apr 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 28 Apr 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e7fca1d9a730d1f433c30e90db2ee0f57358064bb42fafd714109fc27562`  
		Last Modified: Mon, 14 Apr 2025 21:59:00 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2d83862091acf5554bf81b44e1663cf8d039b94a8cf88149d288c587c3ad0`  
		Last Modified: Mon, 28 Apr 2025 18:30:52 GMT  
		Size: 124.1 MB (124070245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624e23990f98662982652b76ee74a65ea8f20ea0a69e891addbb7d1a42e439e9`  
		Last Modified: Mon, 28 Apr 2025 18:36:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:86cf3c814d7625ac2ada0f5f44cb00121b6a2d7419229db43550331924058cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513a959376b59365430edd5063bfb8084900746944421cf9234a3855b57ccaa9`

```dockerfile
```

-	Layers:
	-	`sha256:ac8714baa21716430700378d7fb972de83e810aa19b9e5ff3c8aa1517691b8b1`  
		Last Modified: Mon, 28 Apr 2025 18:36:45 GMT  
		Size: 203.5 KB (203492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1424175f2a98a1449fece651f048f842461e67cc8106aa931e8a1929fdfe17ad`  
		Last Modified: Mon, 28 Apr 2025 18:36:44 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json
