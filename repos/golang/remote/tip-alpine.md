## `golang:tip-alpine`

```console
$ docker pull golang@sha256:191a74b78dc8e273b7fdeed1893b3384c58b79e550d688bfff50517420c8dd68
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

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:ed242aa1a3d04aa60fb11f2bee117eb38e6951b041d61843083ed3c851210488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98542544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e70e460e12ad66b05ed751adfd88fb21458a2c85e585d37245b6a090734dbee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:05:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Dec 2025 20:07:36 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:07:36 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:07:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:07:36 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:07:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:07:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43c85ef0264475e5a3c9a48ac00267ad031164f5d0201db53229f644006e9f`  
		Last Modified: Mon, 08 Dec 2025 20:08:00 GMT  
		Size: 296.1 KB (296082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949364a36b81a9ad117004649aaa40ca173e0cb5059f62e3ed14f9d09d82b4b7`  
		Last Modified: Mon, 08 Dec 2025 20:07:50 GMT  
		Size: 94.4 MB (94386989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb5e72e026cf3f89dcefee0a5e730b261fe7ebfc812c024b3a8ac50817fc77f`  
		Last Modified: Mon, 08 Dec 2025 20:08:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:17bb2d342fbefd504cc44844b93d5b5dc6ee64a8e08e6d61a38a8e69e63f3e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3762a72f2fb14932f066df92a9cda11b30ccdeb5793febaa9d79ea24fb9f9fd`

```dockerfile
```

-	Layers:
	-	`sha256:9881bebe2da4ad183d46aeb9792c529723e5fe14ddec53d744f8b98d6faac811`  
		Last Modified: Mon, 08 Dec 2025 21:23:53 GMT  
		Size: 195.6 KB (195601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1765a489a87391c705b687897375ec1540ccf638ae0ca98b8dab6f143a275c0`  
		Last Modified: Mon, 08 Dec 2025 21:23:54 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:f2bde3d8d6a59e0130391732d7fd2467bd7c7249902125cb853f52b804259867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94594342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5588d2450a2d65f831b0c838727dd06f96e260c517907e38b467be37b8ec7a93`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:04:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Dec 2025 20:06:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:06:57 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:06:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:06:57 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:07:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:07:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eb1409f8473744659983d93546a14f1278b4da264c2c73c158ad7eaa45b454`  
		Last Modified: Mon, 08 Dec 2025 21:07:36 GMT  
		Size: 297.3 KB (297278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e363a58cbabcd22bad4e477b10881416848bcee00f0f66c9e62404bf1ff3d435`  
		Last Modified: Mon, 08 Dec 2025 21:09:42 GMT  
		Size: 90.7 MB (90729013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08a88029f982d7e517295181ffe2b9477cfaaddd69600023f48965969614727`  
		Last Modified: Mon, 08 Dec 2025 21:07:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3b071a5e78bd935329160a45a9453e6a77cfe0084f8c3eb3d6f7174f743ec33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d74c9b0a45595e02970a0addf8d200cf58aea0e3af15a3d928e65e2d7dc858d`

```dockerfile
```

-	Layers:
	-	`sha256:b82045d6a1115930ce64e9be1b74743defd90006d2393ad825bbcdb9020e3b9e`  
		Last Modified: Mon, 08 Dec 2025 21:23:58 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:0cc20b5a122774f79b1321e2b591a2e2d4ca210dbdf89bcc762cfd35a97b8964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94026081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f383eb1f52bc0e02ef7f41650864970fe4f2d2a0d85c4050d124381a5e12359`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:20:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Dec 2025 20:19:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:19:49 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:19:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:19:49 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:23:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:23:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd00960058b59295a452d399130ddeaa5610600f62c7edf975378dd79aa5ac0`  
		Last Modified: Mon, 08 Dec 2025 20:23:17 GMT  
		Size: 296.2 KB (296183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fa0b6c68e96e333f64da015866d36d22ecf4302421d4e561b2c28faa5b8bbd`  
		Last Modified: Mon, 08 Dec 2025 20:20:43 GMT  
		Size: 90.5 MB (90451274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa3bb5bccea0c3adb2bc5bab303166dd6910a67b81208a50fedd64c353c6140`  
		Last Modified: Mon, 08 Dec 2025 20:23:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:db1676e5e6ae57dddb5421735009da8f390a1681cf9d632ec69c31eb4a5044b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcaf222e7ee1f18d9d768722da44d401d7d827379916331c6273ee694914d34`

```dockerfile
```

-	Layers:
	-	`sha256:23f4242580a37c3035d1321f2d3b7cf44e432ee670aa7475bb4511b8e55f1947`  
		Last Modified: Mon, 08 Dec 2025 21:24:02 GMT  
		Size: 195.0 KB (194971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5617262fa4f02ef36f173448512f3ac74b0510c70754640f0be8b3b9e6854d88`  
		Last Modified: Mon, 08 Dec 2025 21:24:12 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b19d4e145b754a0095bee7b7b4cad2339e984bd5a09f20526a7f9188457fd2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93949180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c7045af5676276772f4c0ea23bf69b24a82991287ec147eec169da6588b0c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:07:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Dec 2025 20:09:03 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:09:03 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:09:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:09:03 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:09:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:09:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf77ad39f96c92bcae58e74f4c8cd80245d00b204f231171475f41c7e4c65d97`  
		Last Modified: Mon, 08 Dec 2025 20:09:30 GMT  
		Size: 298.8 KB (298817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2568df0f74d7435ccc404d81d30d0f293c9c2980ac0f029d1100be5d1622d029`  
		Last Modified: Mon, 08 Dec 2025 20:09:47 GMT  
		Size: 89.5 MB (89455005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2966ed629eaa674c870d25ab7da9235fa16b26c178e202e4182d033f14c6e4a3`  
		Last Modified: Mon, 08 Dec 2025 20:09:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:22baff4a036c1a21e6b7ca18317ef27d99056b5b0caba11e5206f8daaada0f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e10c44705a7cee1353d74bbba77c467f0c27849bf04c3ad59d1759a000add2f`

```dockerfile
```

-	Layers:
	-	`sha256:41ed72ef978676858533bb76d260c39b841085161e8fb477feea5286ce9ab6e8`  
		Last Modified: Mon, 08 Dec 2025 21:24:15 GMT  
		Size: 195.0 KB (195007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:533ade1c1ae39cd961012378161d6b215c7891b384d5964243c283fc92898930`  
		Last Modified: Mon, 08 Dec 2025 21:24:16 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:1115743f362eeb8e6eb584b35eb685cd7d2a92f63717f764d78b3440becdb436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96260210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347a3fb055f4844fbec081f7e1604ccfac127fb2c1fccc786aaadc6ce99fc613`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:06:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Dec 2025 20:08:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:08:09 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:08:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:08:09 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:08:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:08:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d4c65b006387adf24f8ee4d2ca1dcf1ffdd49a69c6b557f63a0e0466a2f04c`  
		Last Modified: Mon, 08 Dec 2025 20:08:39 GMT  
		Size: 296.7 KB (296677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714e644cc32cbf0646554d2bf879368eb0872b6982a8a69088b6c556adfd2f1`  
		Last Modified: Mon, 08 Dec 2025 20:08:50 GMT  
		Size: 92.3 MB (92277519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95a49142149ef77dd7da88a9eb27dcb4f6045e8dbb23efe2e8db5e216db7d7f`  
		Last Modified: Mon, 08 Dec 2025 20:08:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:72002b5e7bbf60b0bdc8f9fcebe5ee2b6234b3f6b0eb5aa29c053f89982a80d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71819b823fe86aaf995674b3c57ab142d05c93bef00d43bd48ad69c9451402fd`

```dockerfile
```

-	Layers:
	-	`sha256:fd21ec561eab005fe8899a638d60251ba989eff8723487249eeea51010e630d2`  
		Last Modified: Mon, 08 Dec 2025 21:24:19 GMT  
		Size: 195.6 KB (195560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62b19b5c981cd1afc548d7a3ace7d65195cc1a439bbe2d9fec0c23a923306c9b`  
		Last Modified: Mon, 08 Dec 2025 21:24:20 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:f2977deabf30b5768d9f94b468f96d186ba8de7acf5fa72be4b11109ebee73c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95122752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f970ff82217ea4761a1dd0aa589cb81489910fca20f318eee4cedc6daae80d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:29:04 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Dec 2025 20:23:03 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:23:03 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:23:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:23:03 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:29:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:29:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d26687d4427959db5b2394319b9ac21d2338eaf775321e4a8f305c1ad04364`  
		Last Modified: Mon, 08 Dec 2025 20:29:33 GMT  
		Size: 299.2 KB (299248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7f78d7b3fff51dbf03b6fcb119f6f6c12d036239dbfd1e84cb159ba6461fe1`  
		Last Modified: Mon, 08 Dec 2025 20:25:32 GMT  
		Size: 91.0 MB (90996328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c3f3d7e134e216cb057c621f489660801b5a13fb517f0c75dc9383b8b51738`  
		Last Modified: Mon, 08 Dec 2025 20:29:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0431570d1c05c144166ae7ffac63d64fd2b85d28b287dbaf99aafa3573cb4c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19e334f6fcfc24e97bf2e028ca8670938052e9f3f0dcbbb769a34b27bfc89e6`

```dockerfile
```

-	Layers:
	-	`sha256:af5854bfd16d4a77c6e40cfe2b35b8cb588c06631493579987c199e187897732`  
		Last Modified: Mon, 08 Dec 2025 21:24:24 GMT  
		Size: 195.0 KB (195000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:121eab8260735bb8d837c9255e93a452a90750697a19c722332d518a9663e48a`  
		Last Modified: Mon, 08 Dec 2025 21:24:25 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:729556eae82f614596903153d105b155881a997590ba6b5e07131e1bbf36f89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95522298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2af0f9d8bd6663c8d765e09b09bc41241e10f864d58a994b5b7d0b39e5ac7e9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:32:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Dec 2025 21:37:12 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 21:37:12 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 21:37:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 21:37:12 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 22:22:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 22:22:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee2260aaa09ba7162340fe5926c0fe305f447e406ba4020d7a84ed8048186cd`  
		Last Modified: Thu, 04 Dec 2025 00:35:11 GMT  
		Size: 296.5 KB (296503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305a0d5488487114fae9eff5e7d2b05535888e36450abce33d63c253df6ef6b0`  
		Last Modified: Mon, 08 Dec 2025 21:44:31 GMT  
		Size: 91.6 MB (91642118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a2d737f0eec4f0b11047f67ebe538cca31121f5b8e903adcc5361c47940565`  
		Last Modified: Mon, 08 Dec 2025 22:23:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c09ed0e315d39534e22de4d93b0b7a2fd787a11e766ea660b5a72c215c7bd07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c090d252f82d833e0b34c1b7b718e42fe0a324bd93af3b61d5a1d6f631d8f3a4`

```dockerfile
```

-	Layers:
	-	`sha256:5f97587d5a3b715579102ef8b8962f15f1bf28b78bd1de56b23eb65eadf7a769`  
		Last Modified: Tue, 09 Dec 2025 00:24:13 GMT  
		Size: 195.0 KB (194996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3044c5dfedeeed1bfea94cf5fb4955a1db0fffd0efe85ebebe492c5d63582f0c`  
		Last Modified: Tue, 09 Dec 2025 00:24:14 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:b5716bced182fbf9d074964d9307fbc829fb74b77439341ba5582e2318a24558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97574272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f3d1d9d87d68d183fe61ecbe4bb051220f1233768073c1c485390ec23152be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:10:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Dec 2025 20:10:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Dec 2025 20:10:20 GMT
ENV GOPATH=/go
# Mon, 08 Dec 2025 20:10:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Dec 2025 20:10:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Dec 2025 20:10:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb0495a965cff38fffc5035354b088c3d76314e583d7e3003bd53417892d478`  
		Last Modified: Mon, 08 Dec 2025 20:10:51 GMT  
		Size: 297.2 KB (297177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d45aee96e59637b1f14b3eb6f81f4f4c64edb3653263ca9a0c489bd88115cb`  
		Last Modified: Mon, 08 Dec 2025 20:11:07 GMT  
		Size: 93.6 MB (93553127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe2a166417274337b9b9846860b357cd5544482d0e8d938371c9f8dca7277b4`  
		Last Modified: Mon, 08 Dec 2025 20:10:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4e18ec029904541981db018090c3ed70151c7e8ae49085ab2e17dd7860a8e413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 KB (220045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de873233d522853f871fff67bb74851690dc8d83d59914689c09e7c1d807a7c`

```dockerfile
```

-	Layers:
	-	`sha256:823fd3ee18ccecd6fd46e4154368fd4a0d0bd63c0aedcc4765e2e9630f59bd32`  
		Last Modified: Mon, 08 Dec 2025 21:25:13 GMT  
		Size: 194.9 KB (194950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:915e43ec992a78739b26b9c25ab4d9f9d6ea20dd8753d8594abe10a84c140314`  
		Last Modified: Mon, 08 Dec 2025 21:25:14 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
