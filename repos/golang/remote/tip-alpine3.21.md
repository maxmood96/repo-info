## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:ea097c5cc71e8801b02241e525c8e2c12e18d635754c9d30564729203062a1ad
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:ddae96c07b1d91c6af7be6d17228f243b6d482202b70057e74ed7ed8e0ee4cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95531387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8970667d8741ccd572290b9f26ad7a5b6d35e88414e509c3fc855857511afe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c42a318f34ba9dfa147dc695ffbc6b4e98069ec60af72a85a2820878d0e68c`  
		Last Modified: Mon, 27 Oct 2025 21:09:16 GMT  
		Size: 291.1 KB (291121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed0125ec0f9fecb5ad10be0dd03e9fbc038a3da639715455b9acfe33ee37f3`  
		Last Modified: Mon, 27 Oct 2025 21:07:41 GMT  
		Size: 91.6 MB (91597540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ec022d3280b25593de27a2b2c68564f4266303004c36774348e3325d5a9bd8`  
		Last Modified: Mon, 27 Oct 2025 21:09:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:21b41bd14079055dac525d2a210074e71df712244266762eec849f77d8b10cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2a8d7437c9f2062f9ebb26acfc389e18b11d127a9c8c88c87d1d0d79826c1`

```dockerfile
```

-	Layers:
	-	`sha256:c7888e294c27afeca66d35e9a3bd35d197a751a1f0b8564edc19e8532081853e`  
		Last Modified: Mon, 27 Oct 2025 23:24:14 GMT  
		Size: 194.2 KB (194205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde1050db06f14d01e2f9906ae272ccc1aa89d5f0b4e4bc50912059342f9915f`  
		Last Modified: Mon, 27 Oct 2025 23:24:14 GMT  
		Size: 24.5 KB (24507 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:8e29fceb6d3e480b4e75253a9558866423465224d9d866256acfd6fddc9646ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91829716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209c3e127614a6987095ad5777379797841d598aaf4735d869d5ac43c04e2f1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ce8719ec14ab0c353c5d05b20b3642edb05e96127d3dd21fea53c76f21ea84`  
		Last Modified: Mon, 27 Oct 2025 21:09:29 GMT  
		Size: 292.2 KB (292238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481a45f1b7e81712b6a51b64a28320f5cdc697d0b9d49668a102223a0815a361`  
		Last Modified: Mon, 27 Oct 2025 21:06:57 GMT  
		Size: 88.2 MB (88171853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68fb35008431287b656b630ec31a70b2675ba10332ab8c73f2463a8b4903b5f`  
		Last Modified: Mon, 27 Oct 2025 21:09:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:1674a563d89550171050c137b292b25e53388dbe6daf2d76c8ac185abc8d7cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6eb697326a9629a0f5f13b075777047b3ca2affab787076002332783ad1a61`

```dockerfile
```

-	Layers:
	-	`sha256:8fd11e0380686ac2c7d633b5160b34bcf6e2ad2eb1b228458fb876da7fd4b144`  
		Last Modified: Mon, 27 Oct 2025 23:24:18 GMT  
		Size: 24.4 KB (24404 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:a9028166629c20cbecd5ae112d5945e06a5947677a3e49b6a98f31a22a5d9455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91309230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccada17a0d0518fe346e22b23a789e94dadef6e84c920f21b596473c9e91369d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5234bd264a383cb79b3db7aed4286f08b866c10a46f07279f8c42ff817644ebf`  
		Last Modified: Mon, 27 Oct 2025 21:12:47 GMT  
		Size: 291.1 KB (291144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e78bce73be399b5f32cb65e0bc936590deb899ee136e761115443ad3660df`  
		Last Modified: Mon, 27 Oct 2025 21:11:33 GMT  
		Size: 87.9 MB (87919319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2772a0ccaadf07c79c3c2abbc95a048764e6addcc423b536e628e6aa393502`  
		Last Modified: Mon, 27 Oct 2025 21:12:47 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:49a6e38e423dccf7ea64b41c8a41959697153afe82dbadface1aa770d3e3224b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e4afa54a4e054f0c48a535ab148707ab2866eb613ac7aa0137cc83bb11634b`

```dockerfile
```

-	Layers:
	-	`sha256:ce4be5ecbb93c773b55e13f367f892077ff56721ebd00caaf490b88de00bf578`  
		Last Modified: Mon, 27 Oct 2025 23:24:21 GMT  
		Size: 194.2 KB (194209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73bde7a3de8b1a79e70834422ef78edac299350bab5b657e93b436e227b2ed46`  
		Last Modified: Mon, 27 Oct 2025 23:24:22 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b1f9c004fc618c7dc21c0b6788cb3581154dffa1bedf9699cbbfd7f9702d8d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91142190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c5cd9285b197ef2d0ee804aeda89e6573e025c53234b178aea65c8eb025f09`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f50673edcdbe75a1a89c51ad7d04b751b3e9e29f7a463ca2a65032e148500f2`  
		Last Modified: Mon, 27 Oct 2025 21:09:00 GMT  
		Size: 294.0 KB (294047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75eb2c973c6fbfd8ad3a7e393b43c7170aa83e9a02eff9c12f176ce891587b5`  
		Last Modified: Mon, 27 Oct 2025 21:07:46 GMT  
		Size: 86.9 MB (86855633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e4c0aff515bc60886c6b0b98ef775b7545d5834c0882ae487aa5b1b0d5b87e`  
		Last Modified: Mon, 27 Oct 2025 21:09:00 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a6d0000023bd88edffccd0e0c951b95430e2244f3107e950b4fa11047a396731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2087623e9795e5805521c6d599a7f7da247abc833234f465318f2accd701b829`

```dockerfile
```

-	Layers:
	-	`sha256:d84d6384bb485a92da2fd653036fd4173bd16a398509141630ecc70f7dd0c27d`  
		Last Modified: Mon, 27 Oct 2025 23:24:26 GMT  
		Size: 194.2 KB (194237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0266bc65a16a8f9d9d82e1ec2c7221e7ef82b92f97a20793ee7e057e83cd72`  
		Last Modified: Mon, 27 Oct 2025 23:24:26 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:a997ae9b5c9a00f63b87c92fbd42a60a151c9965898ed43cbbf52024b52b5571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93502362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cf9c6605ba445445aa1ac3f8b7ae475223a3032aed3cf35d53a5f323e49959`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df084e7ddd43f4895ce82177cf6668debfe1f9f04aee06edfb88bf00393ef33`  
		Last Modified: Mon, 27 Oct 2025 21:10:49 GMT  
		Size: 291.6 KB (291579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306627769a351c52d3a3779e00eff7152c4e91ea12a59e21b051f7345636c1ed`  
		Last Modified: Mon, 27 Oct 2025 21:08:46 GMT  
		Size: 89.7 MB (89745922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abf507d8425268bb31c37ea997ae8367bf670ff3b91f2564e31f725b8562741`  
		Last Modified: Mon, 27 Oct 2025 21:10:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:20b2734f76fa4664e9d8b323bc5834a82e7b3ee97998ced27cd045ef010f0edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceef08cd3e5c6706716f651549976b483d624def28e39c0aee5044f595a5f36e`

```dockerfile
```

-	Layers:
	-	`sha256:483bb9804c470075da9e3b5aa3a254ed6ab1fa67c02e2b0fa9f93ae661ebd908`  
		Last Modified: Mon, 27 Oct 2025 23:24:30 GMT  
		Size: 194.2 KB (194174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba5d94a2bdbd50a7905a49f78d51ea9eb17641e9b85184eba6f0b9e2b84379c`  
		Last Modified: Mon, 27 Oct 2025 23:24:30 GMT  
		Size: 24.5 KB (24473 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:1bdb966410b85b191ec270259636a8600538cc7f68cd723f1e136d0fe64fad0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92103016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2149a37bb4becf96464072dad216389b5d81eaf4eab998cef7eaefc8f12ba474`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73de5935c27bbf53bedf5cf444a1a2d137f0c9fa6be0ac31ba3a0af17a0953`  
		Last Modified: Thu, 09 Oct 2025 03:31:32 GMT  
		Size: 294.5 KB (294519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f672a68eba01ff6a61528f0b4d6424e083bf2d654ca12da312b3edc3a8b90`  
		Last Modified: Mon, 27 Oct 2025 21:08:47 GMT  
		Size: 88.2 MB (88234264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef284b21a6447449fbeb8f4b5c662575491fae27be48baead1357e664d15959`  
		Last Modified: Mon, 27 Oct 2025 21:19:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:099c012065840677eb3c1c4eb52d0bcff98ef46739b21e10b48de23d9c6eb0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c13a2695159f26d75fe90d7b8edfff0fabb8a1f88986f300608396e5abb0ef`

```dockerfile
```

-	Layers:
	-	`sha256:1be8befe66fc1f1bff1f25a523f6549292de3c5b3c0cafa946f5ddbdcd28e6c8`  
		Last Modified: Mon, 27 Oct 2025 23:24:34 GMT  
		Size: 192.3 KB (192292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1240bfaf65265c3c46c577e848de9270bd985fc4955be70e7ee4ad9eca05e4`  
		Last Modified: Mon, 27 Oct 2025 23:24:34 GMT  
		Size: 24.6 KB (24554 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:55becfcb0a16074d0fa44e687d90242e46ad3e4fb0c687f8ea2c36046a4a11d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92382003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca15ffb16c929b69d1137dadbcb11dee6dbb245dab166322e8f6f7f7557f8103`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 10 Oct 2025 20:46:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 29 Oct 2025 23:00:38 GMT
ENV GOTOOLCHAIN=local
# Wed, 29 Oct 2025 23:00:38 GMT
ENV GOPATH=/go
# Wed, 29 Oct 2025 23:00:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Oct 2025 23:00:38 GMT
COPY /target/ / # buildkit
# Thu, 30 Oct 2025 00:17:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 30 Oct 2025 00:17:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611661040751365eafd7f1dfe7a29755674f06b893fdaa0640152a38b160d0dc`  
		Last Modified: Fri, 10 Oct 2025 21:10:14 GMT  
		Size: 291.5 KB (291463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873778ff035f412bd2b8c470989bdbe80f9cf50a5717115f02ec5158bcbcac6c`  
		Last Modified: Wed, 29 Oct 2025 23:07:51 GMT  
		Size: 88.7 MB (88739381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04266a950befe805c17e30b1d3e1e05a8f71dd992dd2446effca64ddb84cd9a9`  
		Last Modified: Thu, 30 Oct 2025 00:19:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:1e917de17f612e2cec327334bc4cebf3c48067756166f94b5e92b49cdb178024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d985242208b071a5d1a26f819b2f0fb7696976544c73184f1c661fb0d5a883f9`

```dockerfile
```

-	Layers:
	-	`sha256:778491e773ee037ffceae300b6dc189c0a3394982a70bd95737ca25b31c143b1`  
		Last Modified: Thu, 30 Oct 2025 02:23:39 GMT  
		Size: 192.3 KB (192288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0405d0fdac5e6f8efcc30aab71d9febbb858748865a1d1b34bf02569aa04b8ae`  
		Last Modified: Thu, 30 Oct 2025 02:23:40 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:fc404e87fa47f673e65c4530f61033720506a3cdcd55c62229ea8374c1c86674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93573651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe2782fd07489f1fafb2c9d503d7786b77f145f8b850d473506f12421e0772a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 27 Oct 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc4c05838d57ecfe671b31e7400d015d24d81c7ce717be366103b575ebe388`  
		Last Modified: Thu, 09 Oct 2025 07:53:30 GMT  
		Size: 292.1 KB (292099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a092d1611329304bb10b51ed24c5eb7129e31e22cce2e99b258f719f86a22d0f`  
		Last Modified: Mon, 27 Oct 2025 21:08:13 GMT  
		Size: 89.8 MB (89814961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1516ec5ad35c3232dc3f43d050fe2417b571ebf5f903abd1624a345f05add48`  
		Last Modified: Mon, 27 Oct 2025 21:17:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:09977da4decfe8e5850c23d7bb3a4515ded753ff9d11ef06d533880e6a5ffea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9ab27e17b315944e16c8e38d4a3e680e171b2da4d809687a7b42bc2432574e`

```dockerfile
```

-	Layers:
	-	`sha256:cd67653b99ba3856047c7ff8add40507a18f73141ef2a14dfc98f7aab48084e7`  
		Last Modified: Mon, 27 Oct 2025 23:24:38 GMT  
		Size: 192.3 KB (192254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d59bb00459a62c8d823b918970fa5c3aa0f727e44a9f452a4b8e85fbd69b4b`  
		Last Modified: Mon, 27 Oct 2025 23:24:39 GMT  
		Size: 24.5 KB (24508 bytes)  
		MIME: application/vnd.in-toto+json
