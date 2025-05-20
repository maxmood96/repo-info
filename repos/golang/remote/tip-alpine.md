## `golang:tip-alpine`

```console
$ docker pull golang@sha256:ed9097a3dab5536d26c469dbed2e74d1d6cf6e1f811837a1b368788b44ff1752
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
$ docker pull golang@sha256:743bad64bebb22fdd1c22ae57a9e43098906fccb329481d95880b64d4d8adb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131551443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa03de11d21efbe4b1368223830610c4b5a6394e746c0bd72e5514f6889ff041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806dcc2ae8e7d849ee2d6c3de356c504776a0fa097faafe37ab9d783a40b88ef`  
		Last Modified: Mon, 19 May 2025 23:28:48 GMT  
		Size: 294.9 KB (294908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152514912bccc29796b149fde0366f2c5aabf882d40321f8719bdbe9b9c2cb5`  
		Last Modified: Mon, 19 May 2025 23:28:50 GMT  
		Size: 127.6 MB (127614129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf000a14f9a16ad9e1982a0d036acf30659c9375536f9268865334339f12c1e`  
		Last Modified: Mon, 19 May 2025 23:28:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:905161d29f925088be00a36738cce357d8efb86c6d4d76851dd66822238be956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 KB (238566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d396662111bf877f3c5965f31aa94ebada1521c07b27e7df6a1c171fc1113b`

```dockerfile
```

-	Layers:
	-	`sha256:c10e4352f90e37b29e2f2d228fe534c08ca14dfc035658d8df0e60f44db15b38`  
		Last Modified: Mon, 19 May 2025 23:28:48 GMT  
		Size: 213.4 KB (213424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:467fcfe4034f12a4cc9d1b3e124bfb4cba9f3559c79f111726e513eac43797c2`  
		Last Modified: Mon, 19 May 2025 23:28:48 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:ab219528ada4e84f7417225d3e8655cddc39f352db62bfbc49f9cd4957dab7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126502220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be24ed52a60340f533fc2efcee3721e96c0928a0c7c8f5577bfde18998ee7c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e200e7ad5e2f13ee1ee5c295f12b94fa96417ce036e2a8026a7db4231fdba9a2`  
		Last Modified: Fri, 14 Feb 2025 22:09:20 GMT  
		Size: 296.3 KB (296252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efb37cebd99fd0b517d6fd00b2198946bb12bfe30a359db4a10da3327389c53`  
		Last Modified: Mon, 19 May 2025 23:38:57 GMT  
		Size: 122.8 MB (122841079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe32d63f469053b2cb606ac1466173251db5d3c1368c05f74aee5bbf538a334`  
		Last Modified: Mon, 19 May 2025 23:38:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cc97458e00cd37ff840da3737a67fcc3c88be4f6c2203dbc5be8840835cb8841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb19d521ff20008c9665c211f481263236cde60018611c4f11f20b7627f66364`

```dockerfile
```

-	Layers:
	-	`sha256:16ffe6e459c9bbb942043a77f51ec32b2f55638ec95a13ece73ed2a67d6fb36d`  
		Last Modified: Mon, 19 May 2025 23:38:53 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:3e7dc45e525ed88eb6ffb001ecfe2a73cba33591b611d590281dbf390eebf2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125901429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1743225a5f9fe75649474b644df862925db830de65c7b586d99508132c68c636`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57e96661f23b74a5007ca5b539e5d28d960192676ad8b6b38063081e7fce05`  
		Last Modified: Mon, 19 May 2025 23:31:19 GMT  
		Size: 122.5 MB (122507949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc920afaee8f5d947418044321c6a1860a3e078bf41bbfc2896e5d917168895`  
		Last Modified: Mon, 19 May 2025 23:38:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:11e6140d74f64e401d33ab6fb255b7ae42f98e75bbbccde262f5b5694583d156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 KB (238686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a69345ebac9e53a41a6454676084369ba2b3b35651aecc8339cd0a3db9d5414`

```dockerfile
```

-	Layers:
	-	`sha256:ab6b35ee89ed1443be40970391f5c382ea848769ee56d23bd499770b15e1ad44`  
		Last Modified: Mon, 19 May 2025 23:38:33 GMT  
		Size: 213.4 KB (213420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f73ae91fc584fcce91f016abfa626ca47730d7f3a9caf63a6ff56c22a0d82ef`  
		Last Modified: Mon, 19 May 2025 23:38:33 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b197f0e9bc35b0bf06b100b2c67f1180bff651b9cd2b16b20a748057e2c8b962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124557212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afd528789b970e12b301079b75faa9114436b4b45fd9703a56409d16451aa9f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2f34450ab6893f9de21e818c13da20ab31676614598eac0352797a074049df`  
		Last Modified: Mon, 05 May 2025 21:13:39 GMT  
		Size: 297.9 KB (297874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583af8027226f07cd540ce15387789410501e4b5b5d00ffa1a05fcb1dc81e7e9`  
		Last Modified: Mon, 19 May 2025 23:28:57 GMT  
		Size: 120.3 MB (120266151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2b7bc65df7fecb9cc23bb0082bd5a4bdac4f801189ed957cec634fc581effc`  
		Last Modified: Mon, 19 May 2025 23:33:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5d0bcfe10657fb6bf6fc29955e435eee8c5753cc1da786d464b540a3a35780a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 KB (238782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc4d47e0e32ecac0652d504bb8978d0870473dfa9ffbb6910b748f065991f6`

```dockerfile
```

-	Layers:
	-	`sha256:a2808ab7f5b5f18489279e0d26e57b5c3a7af739f5ec67e51a8fc77924d2619b`  
		Last Modified: Mon, 19 May 2025 23:33:08 GMT  
		Size: 213.5 KB (213480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1255ca7c969f53ed765b3c96fcd6de297a86b80517ce269dc9852e55edc0c14a`  
		Last Modified: Mon, 19 May 2025 23:33:08 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:e1c2911d204f6e5962bf897d48ee10e42e2aae98102efeab8352554ac773d92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129456820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398f8f23780a0b3d6af7f66c8acb2b11e065f7b2036472e808573705d94bbd71`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6cf960dfddef61466e8eb49ae0231cf6afb9801dfe79a4c5ad5e6d7486761d`  
		Last Modified: Mon, 19 May 2025 23:29:27 GMT  
		Size: 295.6 KB (295599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24d8be6f5d36fbc3aec81708ca11efa4fc67dbd10e5ba59a5e7c3fa29e59478`  
		Last Modified: Mon, 19 May 2025 23:29:26 GMT  
		Size: 125.7 MB (125697440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab358fc18ace783ba048e3af14079e7f6c8d2ba3ee2a336bee608fbea33286e5`  
		Last Modified: Mon, 19 May 2025 23:29:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dc869cef5baef559f5234df2555e3d4ec4414c487dbf0c0729c6d1a8bf4c54f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 KB (238458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f277f8245c328668b539adb2642d2b185e0959f2a21ea510c2b0521b806f43`

```dockerfile
```

-	Layers:
	-	`sha256:6dfd13df85d33464cff66b2fc8acd9e3ab3d29e191030d774d564492246afee0`  
		Last Modified: Mon, 19 May 2025 23:29:27 GMT  
		Size: 213.4 KB (213359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94bcd80b16446cd155103fa80083d113e09ab201a0e05121b7e3b66d29135525`  
		Last Modified: Mon, 19 May 2025 23:29:27 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:2d769c158bce822bd4c267426a878d66f681372671e7d31f0a1c83908a52da73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126258019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237558e2e8bef9dea8260316e08d97c6506ec7232f153f3bccbd7f3cdcafa4bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07c13e49694099e3952065321ca0fc45938d3a118b16ce109a83e147045f6`  
		Last Modified: Mon, 05 May 2025 19:01:05 GMT  
		Size: 298.3 KB (298290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625dd3861bcafa29471847412cc81631c8096f3d258fbc027fee8d5eaf7e70a`  
		Last Modified: Mon, 19 May 2025 23:29:10 GMT  
		Size: 122.4 MB (122385228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ae4f3096f5fdfbe449072744d1c631bbe9f5e3ab7b03be32753797d2faaefc`  
		Last Modified: Mon, 19 May 2025 23:32:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3f57d5a493ee482a76ab6a6c63b3b6f82f77b3da1b0eff4a17605bd2bb6db1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 KB (236747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3eb1dea987ae9d79cc85fc2371b20d0f9b866d4e15510245661957a556b9d7c`

```dockerfile
```

-	Layers:
	-	`sha256:f8bcce364facee0e7497a8c3429affb76d9f9a0b0c9f0f8836992057af157478`  
		Last Modified: Mon, 19 May 2025 23:32:11 GMT  
		Size: 211.5 KB (211547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:908599878d6e158f3b7edc4efaf4ee769ac9e0a32008147a481bb42cc28e5341`  
		Last Modified: Mon, 19 May 2025 23:32:11 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:a3f45263f7bebb7998ea4086178fb6f769c6e79b2bdbb3978d0ab2425295b1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126338501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8e939f69e244a40c46ce7aa7707e7ec37d82f73030ca535fb0b0238191eef3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36025d1768b2a36a3b5fc0f9fc7b0696ad8813db3b61b45c20397b47e01e2998`  
		Last Modified: Tue, 20 May 2025 00:05:58 GMT  
		Size: 122.7 MB (122691557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34599b4315ffced5d1796d2d8df7fcad78cfb62b1f76f42f584803c579f22cf5`  
		Last Modified: Tue, 20 May 2025 00:05:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:172ac1ea67b9e83e98392c2a60861b1ddea50db210da0e1bef0b5456c7be54c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 KB (236743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc51f7c423f2817ce275aafb9067d2ba6571ce838bf8f6485abf8d3c4517899a`

```dockerfile
```

-	Layers:
	-	`sha256:9a02bac615f133ee4075863f1c0e8bbc680979eb6e12705a9992a4a59afb80eb`  
		Last Modified: Tue, 20 May 2025 00:05:41 GMT  
		Size: 211.5 KB (211543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0052c043e8f25090d886ff92e42dbec51da52035425cc6f919328e8659592a2`  
		Last Modified: Tue, 20 May 2025 00:05:40 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:6ef89ad32475b8bb809d80aac145a0924ddee74f852166f71655be7c519f5aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128556430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c095259a67de7f64ddc3df6a2e0a438478aa1614b0d79b438d75d6e6b230ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 19 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 19 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 19 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 19 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 19 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd99af01c56b56dd8b4b638222a30d969ae806a266626016d5a030517f57428`  
		Last Modified: Mon, 05 May 2025 17:56:04 GMT  
		Size: 296.2 KB (296192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd075cef311d6599616d573e5ef671ecd5f92da8e8f3aacdc51de2708883d635`  
		Last Modified: Mon, 19 May 2025 23:29:02 GMT  
		Size: 124.8 MB (124792513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f63c44d2a26cfcf38c9d3bc4772a235563fe75e3fc24b3b790a09b5a87a2e5`  
		Last Modified: Mon, 19 May 2025 23:32:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:3d73e14de52be5eb6fc13a0b91f27f3da4cd608b9231c670aadfc4b320e010c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 KB (236615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261725b7a4515ad35e30fd2d0d9430081246141b3e7611581b1e18d67b3ebcfe`

```dockerfile
```

-	Layers:
	-	`sha256:d2d4a0d83f111b018df66c9685565cef2df36de66e272f525accbbfb4f6619b6`  
		Last Modified: Mon, 19 May 2025 23:32:05 GMT  
		Size: 211.5 KB (211473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4198bb75e95728cdc955fc7b914cc8fca9ccb52276f6a7f899f7bb8a17edb86a`  
		Last Modified: Mon, 19 May 2025 23:32:05 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
