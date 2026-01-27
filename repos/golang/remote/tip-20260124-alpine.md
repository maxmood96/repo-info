## `golang:tip-20260124-alpine`

```console
$ docker pull golang@sha256:51aeffaec42fc29edbd17833ec89ef8ee4b9fb9d3b9ef90e9e9f299eb79b6124
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

### `golang:tip-20260124-alpine` - linux; amd64

```console
$ docker pull golang@sha256:e18f0d3cb94e515d2a4f8a6af5c1b00870fa6b37dfa342fb3dda3e54605f9d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97510887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67d74f4f39c0b1f3c125db6cb16f6c78814d7415abe5938433a6f077086315d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:05:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:07:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:07:34 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:07:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:34 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:07:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:07:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01f14f5edd0bcdce4ac8d3352fbdffd8f30755eed4c2032d46005c172f93c31`  
		Last Modified: Mon, 26 Jan 2026 22:07:51 GMT  
		Size: 296.1 KB (296088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606b852e3c333533b6267cbada59c6fbc954cef2b3af5c4c84f2f9bd6ca56999`  
		Last Modified: Mon, 26 Jan 2026 22:07:54 GMT  
		Size: 93.4 MB (93354538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5624779d17366e11b973c7f9bf647fc2bf5c3d213741a22f594c4e70516a2648`  
		Last Modified: Mon, 26 Jan 2026 22:07:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260124-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7427f16596a22251095a2b68b0ba2712646de5ae5222b268b9d9845dfecf332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7825bcc6850a4b128ed77e105e43088c2988d3f7ba8685a4eab9fe7beeecf9f`

```dockerfile
```

-	Layers:
	-	`sha256:249285b733f89aea626188b584072e3c97395cb6d8d4cb4aa0405c1ff8773244`  
		Last Modified: Mon, 26 Jan 2026 22:07:51 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a446976e6e2ae893e2ed2fc8b32bbdbbf9f8e3d5d5c9e20a1f87ba76056236a7`  
		Last Modified: Mon, 26 Jan 2026 22:07:51 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260124-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:c673851597d93bc050b9f2ae8275f54a04595c52b950096d7a0e4a977d16c08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93664912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694e8c69fa763ff7e123933c0ac53093bc7998fee3cde10e9d45fd0299059ae4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 21:53:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 21:56:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 21:56:07 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 21:56:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 21:56:07 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 21:56:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 21:56:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b358ac4054c4f7234a74159ad5dbc556119bd0c7c65f41467bcc7a3856db2b`  
		Last Modified: Mon, 26 Jan 2026 21:56:21 GMT  
		Size: 297.3 KB (297279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4ad1d715926b64a8f9ca2f7e3d6d0a5b04fcb12082a02013bdd6dc9c89d61c`  
		Last Modified: Mon, 26 Jan 2026 21:56:24 GMT  
		Size: 89.8 MB (89799045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc4f11ecda0ce429eb698ddd5e1a2e528892ab62ddd7bb37ff47ac8eb161458`  
		Last Modified: Mon, 26 Jan 2026 21:56:21 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260124-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8843b39ae14109931553c7665cefd3085e94f1f8e561659ded9226a43f3566ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005d0699b673b33a29e6930edb225059cae28a8a77493d362b85aa213d9f25de`

```dockerfile
```

-	Layers:
	-	`sha256:e38427b8d6a2ed2d1478fb4d1ef4b47bd5309aca4b5ebd46470e0e1552f9647f`  
		Last Modified: Mon, 26 Jan 2026 21:56:21 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260124-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:a2b61d0d743747fef29a5101755dd47eb1fe1a2e858847999ebc5d5e04fc7259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93102514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b04e0c1ea304efd4119d43361b03dde94951eeb5a701e2c8d462bb22a4681b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:11:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:14:06 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:14:06 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:14:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:14:06 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:14:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:14:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29e02e36b1ed0d47a90e21b8d3dc3d6c538c16479f51446fcc20b1176ac5a39`  
		Last Modified: Mon, 26 Jan 2026 22:14:23 GMT  
		Size: 296.2 KB (296208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205fc7a73de56b4f5ea25cad036ec0f33fb7b33229a77437a24f71a2e0db125`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 89.5 MB (89526761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216254c0a1b7b945aa04d6fd06d86e2be8a3194a6c898bb93c413727a65d0535`  
		Last Modified: Mon, 26 Jan 2026 22:14:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260124-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ee10b8e24711a723c5cd437bb3b6f95128cdf3428d2fefea3db04441e0a87fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96cda10317fb70937f6c7e5f9c0a2b3bc3c012dca58d45f99e9ffe073b1a540`

```dockerfile
```

-	Layers:
	-	`sha256:94060ad10d2569943946bab1dce3b9e12e0b5d78d3917dced2a02bb02aaca89b`  
		Last Modified: Mon, 26 Jan 2026 22:14:23 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4bfe34228a88fd08e3b65ea3930b146ae1e2dfef473a2d0e79880cd8934b7ea`  
		Last Modified: Mon, 26 Jan 2026 22:14:23 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260124-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5eccd337b4ce7712ae4d5c26ea542cbbe72ddcd9a57e35c65b76b145a7abd65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92912007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f25d03713dd2c4e3ffc166948e36b69e31c47e7a0d8d3acea44b955b7c4c10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:05:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:07:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:07:25 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:07:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:25 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:07:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:07:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c016c4d11a63bb104c6a19b8ed690fc2594eedfc1a59e1ddfa3b0cdd26ef6f4c`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 298.9 KB (298852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3fde52f4a9ce3ba79f004ba1b1e261e66970dc6baaa4a0f9b9bee7c6d5ab5`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 88.4 MB (88417257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bccd6c4411e5c3741585b7806f720d84152a1f7aa885c6754748a64c934c89b`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260124-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:51189ba56ca40ede75efc0a2a6007f6f0d4076d20e8e3cbf35eacf70a161a020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2f7c32e80796a458c7e1b8f7bb7c5896ac3c1007564e2d93549865132b9241`

```dockerfile
```

-	Layers:
	-	`sha256:1240a724f06894f36d3fbfa3f40cd6768d187b1905b6fab3ce010165f97f71d5`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ea427894d0ef861009a9df333d9d2373446a904227db096976cbff2a5b6b01`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260124-alpine` - linux; 386

```console
$ docker pull golang@sha256:731717a06007e10ddb9f8c1780c87d2776c384075c5366e1e55ab7d1fb3e8a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95420661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0840a62914aef24ea9ae49e9fd6faddace8dfc9b1f6b21dc8fc35d8af293c1dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:02:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:04:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:04:41 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:04:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:04:41 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:04:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:04:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07d32031ed1ee254ee6d9d892aa5e9bafa478b8fceba3ac81ab84a909c05d2`  
		Last Modified: Mon, 26 Jan 2026 22:04:57 GMT  
		Size: 296.7 KB (296677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb24967b184a59692854afa79a294d0d5b0fa84b707a952b78449312c20956e`  
		Last Modified: Mon, 26 Jan 2026 22:04:59 GMT  
		Size: 91.4 MB (91437726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827bcd72b9c8a6d0af6dbd4394f6019b1340ff72fb9967ee866d11b94208a113`  
		Last Modified: Mon, 26 Jan 2026 22:04:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260124-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:122c6f90aa5420dbd953c42ba595c7798b16eba4d89b31bb4afd8f7d5e955c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29896aa84689e40b96bb755d27217f983d71a097d6c9f0cbed05f0359575835a`

```dockerfile
```

-	Layers:
	-	`sha256:0f7f5d8ab801e175fa9e37bebd6fcd57aec4e102a8b7f98b066c779ff6ca4281`  
		Last Modified: Mon, 26 Jan 2026 22:04:56 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa6e73bd9583b647bf3a3a934f23f068a2240730e22a9cf017dcf3f6573ea243`  
		Last Modified: Mon, 26 Jan 2026 22:04:56 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260124-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:11f9749d7b79ee6e0c200715a4db8a06ae3c50b2e3cff01eebbd38e27b992ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94178107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f3a69384b8d5c4e5522ff3b70577be0b5055724830f9724d617f6bb90bf29f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Mon, 26 Jan 2026 22:40:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:34:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:34:17 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:40:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:40:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72241574afa4c8148f9cf751319064098bfa6cc4347681527b94330594ac0568`  
		Last Modified: Mon, 26 Jan 2026 22:41:10 GMT  
		Size: 299.3 KB (299269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db3fbdd047cc229947289d64050103b3f46ea0891f972e8e261f84917802eea`  
		Last Modified: Mon, 26 Jan 2026 22:36:06 GMT  
		Size: 90.1 MB (90050925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cef0912efe3bc1af02a9d4523c3221a028b0de62a7bf524763cbe4a0688ab5`  
		Last Modified: Mon, 26 Jan 2026 22:41:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260124-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e4460cc69d4ea602619fc29dffd02a086477e0e3b10c3396c7fe84f85f346b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (219979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c83bc51622fe3f3dc173637e69188eaaa0a735ac4903d3706f6f16a3244b60`

```dockerfile
```

-	Layers:
	-	`sha256:ea823d4baa1660bc757f0d64c47c2b494963c47038a41b8a9cc4688f9799fbd8`  
		Last Modified: Mon, 26 Jan 2026 22:41:10 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c34c3d6c06a1f3bf0c63c5e1df8ba2ef08f57f649c74a4d4a33a4cb70645bb51`  
		Last Modified: Mon, 26 Jan 2026 22:41:10 GMT  
		Size: 25.0 KB (24979 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260124-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:e68648fac0d55ffb6b05634129822c46efe82034359cc0937c17970f3fd21707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94465415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba08815c2511f3674581c7de3d23ada67e038a3f6fbdcaf2648b3f4c1e1dbcd2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:47:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 27 Jan 2026 04:27:07 GMT
ENV GOTOOLCHAIN=local
# Tue, 27 Jan 2026 04:27:07 GMT
ENV GOPATH=/go
# Tue, 27 Jan 2026 04:27:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 04:27:07 GMT
COPY /target/ / # buildkit
# Tue, 27 Jan 2026 05:14:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 27 Jan 2026 05:14:06 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c358a50d2f39217ca62c3bf8831f5ece762bf2d424204f727fa6a6f9f5124f1`  
		Last Modified: Fri, 19 Dec 2025 05:50:16 GMT  
		Size: 296.5 KB (296519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336390632e3dab506cd0230c48180b8fdc0e8dcf2f397506712faf9caae798e8`  
		Last Modified: Tue, 27 Jan 2026 04:34:16 GMT  
		Size: 90.6 MB (90584800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a694671488bf2e9877e89d5b9da398a6699e157dda62cb71fe91c2720c5a5f39`  
		Last Modified: Tue, 27 Jan 2026 05:15:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260124-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a1fd609a9d8895cf5a8ce1528630bbf716e7340aa926163ca8db79ca44ac27d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e196b23dd0b32362bdd63901c3ec3216165463dc9336f3db632ad1b6a98c1b11`

```dockerfile
```

-	Layers:
	-	`sha256:1298ca67bca9f04eabd6e371058bc60510f0a30fbd130a6e3d895b21f5b086e9`  
		Last Modified: Tue, 27 Jan 2026 05:15:31 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67cec1b779f8d2c605b6e4e2cdd20acf2987a46e3c20da6dc0e9d87efa985ed2`  
		Last Modified: Tue, 27 Jan 2026 05:15:31 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260124-alpine` - linux; s390x

```console
$ docker pull golang@sha256:f8cce7eb5294683ac7341383f63caaafd44d1a814de1b63fd36437555b3e645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96629684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d950a481a4c7728cd15b8966502ccd94cddd1b10cad71fee1d5b5d36b936aed2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:30:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 26 Jan 2026 22:12:17 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:12:17 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:12:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:12:17 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:13:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:13:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c3921107d409df0e99b4231287ce5a7267626ae3ee2e9fb513d5bf7afeeca1`  
		Last Modified: Thu, 15 Jan 2026 19:31:34 GMT  
		Size: 297.2 KB (297197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d1ebc1a42fde765fe01b70de439084ec52a344bfa25acb00b6d281dc10102e`  
		Last Modified: Mon, 26 Jan 2026 22:12:55 GMT  
		Size: 92.6 MB (92608018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def9b8da8e18ff45d9a4c0223cf1773412a1e38596a5df6dc6319a4ef542536d`  
		Last Modified: Mon, 26 Jan 2026 22:13:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260124-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7dab12c5217f2d4497c705425511d34c26a60a3ddc86eb29120d25eeac9740b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6c46dadf0f9a9275c9c9699146e30825c463d53492a60f9c07113b01b50393`

```dockerfile
```

-	Layers:
	-	`sha256:dc88c5d3d7ce8e775dd55017478a55cc6f1821527c6af49470c0fdcc8f3ebe10`  
		Last Modified: Mon, 26 Jan 2026 22:13:26 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952d8a9a31e8347fc099ab267c7e7ef10abcfed0b05f85cd52a34c0e32f08753`  
		Last Modified: Mon, 26 Jan 2026 22:13:25 GMT  
		Size: 25.1 KB (25094 bytes)  
		MIME: application/vnd.in-toto+json
