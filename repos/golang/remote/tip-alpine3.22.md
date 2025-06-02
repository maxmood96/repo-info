## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:77ebdc08d0c54ff7be7ca7dfb89d8e531c21e7b2195278d953ccc5b0dafe361d
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:8ec80f760f58121c4748997ba581144cbba42a08301a2e23f4a9ebb9e2411e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130647493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7950e8c8498e72f7575737de0a89e1b090aa0c3651ccef8b27ea63e2953886`
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
		Last Modified: Fri, 30 May 2025 18:04:24 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4334eb50b5c8ee48b792510eab33bdbeb92fe0003f31919c4d7e112bc9e4022`  
		Last Modified: Mon, 02 Jun 2025 18:23:39 GMT  
		Size: 294.9 KB (294916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c772e4d16fa9b2fa9b4ea3dee2c356c3597d08d324bfd3a1c2b9b5a987e5a2`  
		Last Modified: Mon, 02 Jun 2025 18:23:36 GMT  
		Size: 126.6 MB (126555573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e63c7832afb56ddcfafe45bf2e014851cb382b193590593503ec0d7eed3ca31`  
		Last Modified: Mon, 02 Jun 2025 18:23:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:13c46aa61f8ff8b8a65b50935f3d4f6acb5d910ce427b6208fe318581d31aa27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 KB (239342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776f9fb55f272b87b1b2681d6d872fb5036ad19fcb0ccac1511d7ab3281eee96`

```dockerfile
```

-	Layers:
	-	`sha256:5fd0893e3dcc7813e911836da1384efcec262107850a50a6136086a6b5c0bbbf`  
		Last Modified: Mon, 02 Jun 2025 18:23:39 GMT  
		Size: 214.2 KB (214201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f546aa03629ea469b3a6152b24ca02ac0e148f1cdb8c42c3644c4ed2a50ef6e2`  
		Last Modified: Mon, 02 Jun 2025 18:23:39 GMT  
		Size: 25.1 KB (25141 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

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
		Last Modified: Fri, 30 May 2025 18:04:31 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1a66512d0d840a56a8c3fcd61678c4f71bc9949c18f7ee679feb7494b20e0`  
		Last Modified: Sat, 31 May 2025 00:11:16 GMT  
		Size: 296.3 KB (296292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c163709194da95c49e3f47c7c0113207e87dd72e97f3fca5d567f2e083b857f`  
		Last Modified: Mon, 02 Jun 2025 18:24:06 GMT  
		Size: 121.7 MB (121735237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429db44520315321ca7d413b62258b2d128bc9e49faf04990e779aa04889efa5`  
		Last Modified: Mon, 02 Jun 2025 18:24:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6d61a1c8c535a7bd31dd8e20efe2d609da07086626d0b16f02102650b70b04a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380de617bb6009711514e2fba7134c0a4905365dca584d03e15226a87b78368d`

```dockerfile
```

-	Layers:
	-	`sha256:16490dd9d951cffd805306964255c7ae37219f802b95d39e9aea7335d8a03afa`  
		Last Modified: Mon, 02 Jun 2025 18:24:02 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

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
		Last Modified: Fri, 30 May 2025 18:14:23 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6c9cae412d8d42471b3ec2789f87569712940a14bb5b06595436c95f2904f8`  
		Last Modified: Sat, 31 May 2025 04:58:03 GMT  
		Size: 295.2 KB (295232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaef207e52620490d9796ba5bb1c39803d44a66aaefee2acfd8d44ca0dc7d0b`  
		Last Modified: Mon, 02 Jun 2025 18:24:58 GMT  
		Size: 121.4 MB (121406962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec613ce7f315a5df68cba1e26e1ee2622c01f0c62cb5b56a8f9cba8b316c346`  
		Last Modified: Mon, 02 Jun 2025 18:31:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

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
		Last Modified: Mon, 02 Jun 2025 18:31:37 GMT  
		Size: 214.2 KB (214197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ffd0085e1c75d57983c6ea18c9640135ac903b87bcdd14f1183b23e640e0ce2`  
		Last Modified: Mon, 02 Jun 2025 18:31:36 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

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
		Last Modified: Fri, 30 May 2025 18:15:21 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373964117ef6ddcc9d2295f836a878c54d49d139d1981ffedc92cef7282b2a9c`  
		Last Modified: Sat, 31 May 2025 03:56:24 GMT  
		Size: 297.9 KB (297885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c61459497fa2e2873d988523a87fbbab1017c75b44162e22c190b9fbc0f92`  
		Last Modified: Mon, 02 Jun 2025 19:41:52 GMT  
		Size: 119.3 MB (119320718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8f3e1eba00fa2c20091f1d1b9cfb031804619cc48942646ea7c907d6f2bfda`  
		Last Modified: Mon, 02 Jun 2025 19:46:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ceef0f6beac5ecfcf7bdc161a6abdfd8f22ae63374ed2c0fa780c50c5d851f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 KB (239559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eb2db79d67975fb9bdd32f242bd55884fde40d21fe00e0faa2559c9f153f15`

```dockerfile
```

-	Layers:
	-	`sha256:b74d188adf5da8f14e18e6f508e48be58f3dadaf6ccd558ba3bee7da64a9c66e`  
		Last Modified: Mon, 02 Jun 2025 19:46:26 GMT  
		Size: 214.3 KB (214257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da213e1175120dc12dfc5c1988433065294375d6afc86ee265fffdf89621ff6e`  
		Last Modified: Mon, 02 Jun 2025 19:46:26 GMT  
		Size: 25.3 KB (25302 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:00e1a5360fbfa9e0a70323d2a50e87f8ff1412973ed07b8941186dd32b0806ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128425961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0152904f0e9f4a7c88691c2c7ba53b65b4f8fff49fc542f35981a75b32d3317`
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
		Last Modified: Fri, 30 May 2025 18:04:26 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377403ecd55e7141da54f633574702068993c94d5f15cb93b5176eb5c0dde5b`  
		Last Modified: Mon, 02 Jun 2025 18:24:12 GMT  
		Size: 295.6 KB (295610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59517f64f93ef3235377e65403c21a43aa149e3627f878c0069b20d4472659dd`  
		Last Modified: Mon, 02 Jun 2025 18:24:11 GMT  
		Size: 124.5 MB (124514164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3aaf0df08fd5c4a2b8a0a03f64c2a965d4f4de3c0fbc735e6bab4b40629d26`  
		Last Modified: Mon, 02 Jun 2025 18:24:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9ee96acd3f93e0358fc1ca13d38c79d4615d003ec487ca8af9ce4d190ea406a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 KB (239235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14043fa1232d7093484d35f978ce1b60192afdfdb513719e6a085409f85c014`

```dockerfile
```

-	Layers:
	-	`sha256:5639e8e5767b48b69b80b0386d7deb8a793d0221f9bba3ba2f9946daeb6213b6`  
		Last Modified: Mon, 02 Jun 2025 18:24:12 GMT  
		Size: 214.1 KB (214136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a0a59d078f43163f7505c868f38fe2e37b25ccbd27a10669a000579b870fc7`  
		Last Modified: Mon, 02 Jun 2025 18:24:11 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

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
		Last Modified: Fri, 30 May 2025 18:14:22 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187c79905be9977c8b81d03082bbff0333d20fe9ac9a7740864c66f7e0e5c7a`  
		Last Modified: Sat, 31 May 2025 00:09:46 GMT  
		Size: 298.3 KB (298320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00aee01924c56be514b4d5b89dd62e8a80222c3c9c95a0f0907430fb88a09a9`  
		Last Modified: Mon, 02 Jun 2025 19:30:35 GMT  
		Size: 121.4 MB (121447518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe542f65ef7a00f4cb8536f2f71109a616c8c6c6bda53d5333e19c16b76301e0`  
		Last Modified: Mon, 02 Jun 2025 19:33:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

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
		Last Modified: Mon, 02 Jun 2025 19:33:52 GMT  
		Size: 212.3 KB (212324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d61e0921febfa9096af0c6c36031025e7aaa370515e7a8bc8a63d6acd499fb`  
		Last Modified: Mon, 02 Jun 2025 19:33:51 GMT  
		Size: 25.2 KB (25199 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:5b3e702fa335d596ea045f6e6c6fd780e04f9bd896a26bfe604ca6790325537a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125203140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9324e0f6c1fd87c2129a249e5eb4788853dac4b087a02d87e52efef0555c0178`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Fri, 30 May 2025 18:54:40 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bf8006499bec04d28fe13dec3efd4cf9075748d5dcf5b6dc1415aa6aeb8f0`  
		Last Modified: Sat, 31 May 2025 03:27:47 GMT  
		Size: 295.4 KB (295390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf501e8ac8e034ccf3f3064d2d56237fc55dc6b377839b153c3f162a1fadf302`  
		Last Modified: Tue, 27 May 2025 20:07:53 GMT  
		Size: 121.4 MB (121393782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4ffe88e75a9bf6641394bd699c19a6852fd1260e8246048f9113a3f35391f2`  
		Last Modified: Sat, 31 May 2025 14:14:49 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:686ae9250b048277587c2ebd065aead2079e223dfb099877540bdb01d8bc13e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 KB (237520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4cee7c445a06f336c54f65de2c349d0826c30b18f9be4f5773c72b7879d334`

```dockerfile
```

-	Layers:
	-	`sha256:7cf3dd315217b44ff5a43d4196898495b675c7555d7e89920a8568379d312e52`  
		Last Modified: Sat, 31 May 2025 14:14:49 GMT  
		Size: 212.3 KB (212320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f482b53928edfe53dbd61faf4af28a1e91caa36635ab8e03f8e35469e0e03c1c`  
		Last Modified: Sat, 31 May 2025 14:14:49 GMT  
		Size: 25.2 KB (25200 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

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
		Last Modified: Fri, 30 May 2025 18:13:14 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02725f6addf0718099c43b5965203aa513fc71aa710978afc18cf384dfb4798`  
		Last Modified: Sat, 31 May 2025 00:11:27 GMT  
		Size: 296.2 KB (296215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d9aca011216cb8ec22b40335fd2aee2bbbf158897a84613b9937eba268ae48`  
		Last Modified: Mon, 02 Jun 2025 19:06:01 GMT  
		Size: 123.8 MB (123758489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4bf87afc16eb3453423a148813aee627e935bf7283c419c5060b709f341e75`  
		Last Modified: Mon, 02 Jun 2025 19:09:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

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
		Last Modified: Mon, 02 Jun 2025 19:09:04 GMT  
		Size: 212.2 KB (212250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51457742106826e0340de82e1f00d900637544d4bfad7835ff18f92d96bb570`  
		Last Modified: Mon, 02 Jun 2025 19:09:04 GMT  
		Size: 25.1 KB (25142 bytes)  
		MIME: application/vnd.in-toto+json
