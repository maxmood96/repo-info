## `golang:tip-20250530-alpine`

```console
$ docker pull golang@sha256:8af5583161247d2c61bf042d98495a764089ab1144f065b2893c791f5033b249
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

### `golang:tip-20250530-alpine` - linux; amd64

```console
$ docker pull golang@sha256:ea02aeafe4c0893f1d8a3aa178bab020375a7f353cc2e2671b87fadf66e54a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130647490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5809d9e75df3473a7d8bb1e6ae957478640ec0d3b2531d29ab6fd010f99dc4dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a42a26d7b563ab316c2246bccf5977bcdbdd6d1fd0e445efb799895e22c0d6`  
		Last Modified: Thu, 05 Jun 2025 20:07:59 GMT  
		Size: 294.9 KB (294913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c772e4d16fa9b2fa9b4ea3dee2c356c3597d08d324bfd3a1c2b9b5a987e5a2`  
		Last Modified: Tue, 03 Jun 2025 13:54:37 GMT  
		Size: 126.6 MB (126555573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71a32facc66dace7de537ca4b4efa8b0a53241cf572343a6f380891e1349eea`  
		Last Modified: Thu, 05 Jun 2025 20:08:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250530-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5daf3eeb5f7d654a65600245c19844cdb4d0414cd6ec2991a166a5296f57503d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 KB (239343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e352f6bc5e3d565600e116a7cd226e3f882b5bddf7b74c949c0d4fdaa817799`

```dockerfile
```

-	Layers:
	-	`sha256:dda8c6e0efe4a184d8f99c4857b52ac747fbbfd7dd465da69dfb75161e7b66a5`  
		Last Modified: Thu, 05 Jun 2025 20:26:53 GMT  
		Size: 214.2 KB (214201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:288b158b10f12290606a2f4c46ce170bbd594635fae5b2d33045d212cf664a82`  
		Last Modified: Thu, 05 Jun 2025 20:26:54 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250530-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:0bc847909a726464a9d6c24ab33c1ce45ebf18f90ba5fb24347a0a273099d39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125532616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893ca1a9f4459b52b2d3b42e98667b49ae179671eca353ca4eb79a0a19e24f02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1a66512d0d840a56a8c3fcd61678c4f71bc9949c18f7ee679feb7494b20e0`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 296.3 KB (296292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c163709194da95c49e3f47c7c0113207e87dd72e97f3fca5d567f2e083b857f`  
		Last Modified: Tue, 03 Jun 2025 19:03:16 GMT  
		Size: 121.7 MB (121735237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429db44520315321ca7d413b62258b2d128bc9e49faf04990e779aa04889efa5`  
		Last Modified: Tue, 03 Jun 2025 14:19:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250530-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0990e57425fb02b67ae48de8f22aa9f84203e9fc7812c7f9cfc7bcaac3330a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f101d16996bd0f9d80c299dd13b443e9e982f73c50966d51ee74dd7d3118e5f2`

```dockerfile
```

-	Layers:
	-	`sha256:a5db14757c528b2a5c3758fb11bb963a7e6509a13c7219019dac678da97fccb2`  
		Last Modified: Thu, 05 Jun 2025 20:26:58 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250530-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:50115cf60d4ed6442816ba8f3f85942d1968c084e9e0c24f593f0da5c2a693af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124921533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942557fd96eb6af669497525c3e56b78dcc31a31fdf30bbe08bc67c7a33911f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6c9cae412d8d42471b3ec2789f87569712940a14bb5b06595436c95f2904f8`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 295.2 KB (295232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaef207e52620490d9796ba5bb1c39803d44a66aaefee2acfd8d44ca0dc7d0b`  
		Last Modified: Tue, 03 Jun 2025 19:04:11 GMT  
		Size: 121.4 MB (121406962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec613ce7f315a5df68cba1e26e1ee2622c01f0c62cb5b56a8f9cba8b316c346`  
		Last Modified: Tue, 03 Jun 2025 13:43:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250530-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:fab3f1bafc7cbc462a518d0dd66fd6bbe043f0ef99b22b63f75dbbd73235ffd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 KB (239463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba26fa2fa0f03c07acb9b70c85fb34abb19422e467d1e8b4f4f8d00352939d5`

```dockerfile
```

-	Layers:
	-	`sha256:4071c7e9281e536187e3bb98f5cbbd1b46adf131407c92233888c51d3c766e83`  
		Last Modified: Tue, 03 Jun 2025 19:04:49 GMT  
		Size: 214.2 KB (214197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ffd0085e1c75d57983c6ea18c9640135ac903b87bcdd14f1183b23e640e0ce2`  
		Last Modified: Tue, 03 Jun 2025 19:04:56 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250530-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:0e34e18173d369e397e04e9e428243bb69493dd683d007c456b3d4a4efb027dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123754702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70aed9fb2c79407fee633629632bdf2de68831ccb5eb7bb2586bdab01188116f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373964117ef6ddcc9d2295f836a878c54d49d139d1981ffedc92cef7282b2a9c`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 297.9 KB (297885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c61459497fa2e2873d988523a87fbbab1017c75b44162e22c190b9fbc0f92`  
		Last Modified: Tue, 03 Jun 2025 13:56:11 GMT  
		Size: 119.3 MB (119320718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8f3e1eba00fa2c20091f1d1b9cfb031804619cc48942646ea7c907d6f2bfda`  
		Last Modified: Tue, 03 Jun 2025 13:56:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250530-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6808f5ef147b6a1ee4d283c1a14c1e39307bb73766f87ee864096fb47e8ddf03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 KB (239559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb801f798f93bf90d0fc8c8f741be324a115d624f5e84df00b3544e50f6df59`

```dockerfile
```

-	Layers:
	-	`sha256:ef9a7499399095a22b0ea07f640bc3fb8e96bfe90622e1484fea59d2fa9917bc`  
		Last Modified: Thu, 05 Jun 2025 20:27:07 GMT  
		Size: 214.3 KB (214257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa578686fa0cd337d5a0c7c8642813e15fe71e9e320f2af3f7e36cd23d1490a`  
		Last Modified: Thu, 05 Jun 2025 20:27:08 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250530-alpine` - linux; 386

```console
$ docker pull golang@sha256:6740be2655d938dd3f1681d3ddff1320296904c8bbf06ceb0c12a9f1ca75322c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128425962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad81dd13b3df518008603aea7d3409071de793ddb50e5b63e22c2a7c7e2c9ea2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a1a137e7f9c0d106f9de3a27f554c48ebb6a3dc5960e98b2e4ce48b5661bce`  
		Last Modified: Thu, 05 Jun 2025 20:04:42 GMT  
		Size: 295.6 KB (295612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59517f64f93ef3235377e65403c21a43aa149e3627f878c0069b20d4472659dd`  
		Last Modified: Tue, 03 Jun 2025 19:06:17 GMT  
		Size: 124.5 MB (124514164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a84bfe49aedf87edccb575dfdb8a9273cc867220f8d76cb4203f5b46da53506`  
		Last Modified: Thu, 05 Jun 2025 20:04:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250530-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:32973a350252fe4b458b004528aa4712130010e452a57d16c00dc8ce2fc59e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 KB (239235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c67d5ab31ccfdd1dfa1361fc7f20b8cb6989f2e012fd31c91c3e651cd2f5aa`

```dockerfile
```

-	Layers:
	-	`sha256:62051a587d562795ccb0bd1e7378f6e2fa8699e1f9835ceacfb84f305199312e`  
		Last Modified: Thu, 05 Jun 2025 20:27:11 GMT  
		Size: 214.1 KB (214136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2605024bf4aa82d71469a3a77845cc96088375abf234c6a69cec023f38fd92`  
		Last Modified: Thu, 05 Jun 2025 20:27:12 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250530-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:d31cf068745e79d2b35473899877ab00f63fd1b6aebd20922107f5aeef6d397d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125476183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864c043e21a06c7b5efbb6c383fa6b555e84105f8aa350282f426dfa498d2c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187c79905be9977c8b81d03082bbff0333d20fe9ac9a7740864c66f7e0e5c7a`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 298.3 KB (298320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00aee01924c56be514b4d5b89dd62e8a80222c3c9c95a0f0907430fb88a09a9`  
		Last Modified: Tue, 03 Jun 2025 19:07:17 GMT  
		Size: 121.4 MB (121447518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe542f65ef7a00f4cb8536f2f71109a616c8c6c6bda53d5333e19c16b76301e0`  
		Last Modified: Tue, 03 Jun 2025 19:07:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250530-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:921d35840092f97c6e3b19c8c95809a42bc8778dd4da65d63b84f86f2bd85666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 KB (237523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196c22e4411075707157fa8c88d2936ffa8bcddd0eb5fb3cbc3bb60d0e57d387`

```dockerfile
```

-	Layers:
	-	`sha256:906e56f62412f6a67307f903b0cb2c7d821b8ca6835a058fd4a33f265f793166`  
		Last Modified: Tue, 03 Jun 2025 19:07:53 GMT  
		Size: 212.3 KB (212324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d61e0921febfa9096af0c6c36031025e7aaa370515e7a8bc8a63d6acd499fb`  
		Last Modified: Tue, 03 Jun 2025 19:07:58 GMT  
		Size: 25.2 KB (25199 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250530-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:59ad92132c5037b56dd973dacbcaa0b1e98f9ce2ca0b9edb15c6ec76319c3185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125517830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f07e10dee472ee05665f1b237db618cb90793effca55a348f43b8ca3ab6f44f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bf8006499bec04d28fe13dec3efd4cf9075748d5dcf5b6dc1415aa6aeb8f0`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 295.4 KB (295390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15922d8e3d7b445acd91995151b18e8d624f8ef4639f5957f7d5815508611e2`  
		Last Modified: Tue, 03 Jun 2025 19:08:17 GMT  
		Size: 121.7 MB (121708471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a0f395128085d92aba6b1a96e1a33696816dd181c998181f5b81c76eba196`  
		Last Modified: Tue, 03 Jun 2025 19:08:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250530-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c700302265169dac5fc4e067119830fb0f950da69927790ec702d9ab1e2384c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 KB (237520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6511b49f72615244aa5ce149da091678ecee6a7eb669abb11d74bcb6383bc93d`

```dockerfile
```

-	Layers:
	-	`sha256:8b24ca7b79b2e8ece80b5c1ec53c95ac613966ff80bd6d3eaff782a1bc48a470`  
		Last Modified: Tue, 03 Jun 2025 19:08:51 GMT  
		Size: 212.3 KB (212320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410b852a5860fdd988d250035ee909292b8da10e26341daae7e3f1530d3c3c78`  
		Last Modified: Tue, 03 Jun 2025 19:08:57 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250530-alpine` - linux; s390x

```console
$ docker pull golang@sha256:85b64f6dcba99936b8f749efacba4864739b5559854741624ff2fbac313d8d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127702391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb180d52f0427400239270b7451b7ffa453cfcf1ba2be2eca8e1c655c8ede28c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02725f6addf0718099c43b5965203aa513fc71aa710978afc18cf384dfb4798`  
		Last Modified: Tue, 03 Jun 2025 13:31:49 GMT  
		Size: 296.2 KB (296215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d9aca011216cb8ec22b40335fd2aee2bbbf158897a84613b9937eba268ae48`  
		Last Modified: Tue, 03 Jun 2025 19:09:17 GMT  
		Size: 123.8 MB (123758489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4bf87afc16eb3453423a148813aee627e935bf7283c419c5060b709f341e75`  
		Last Modified: Tue, 03 Jun 2025 19:09:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250530-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9a698dafe8409896cc1cd1c258ea45397c6d3dd614e9015eeff96a47ee2ae074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 KB (237392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d0528718e7ba7afa258f058f4796e4da3b6a3ac9cb1473beaa2deba51d436d`

```dockerfile
```

-	Layers:
	-	`sha256:7b659eb087577e2c7f6f89e31b2ad56381332ff17130de0ddbb89337fbb2d550`  
		Last Modified: Tue, 03 Jun 2025 19:09:51 GMT  
		Size: 212.2 KB (212250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51457742106826e0340de82e1f00d900637544d4bfad7835ff18f92d96bb570`  
		Last Modified: Tue, 03 Jun 2025 19:09:56 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
