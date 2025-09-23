## `golang:tip-alpine`

```console
$ docker pull golang@sha256:62aed27922f188456a677ce5bb1de0e7c91584f5c8a5c068680765f900008c4d
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
$ docker pull golang@sha256:94f6cac365498736e4785285b4f2ee84f9d82033dbeec9bb879fdb81a595e9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87767466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22e8cfcb7461af856402a26925cad0ca1af817f1f88858ec8c2d412cc88b598`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29199d42b6c7b094e9f97f689c9fc75c18abe6a015ab431641b0c450cb5f5e3`  
		Last Modified: Mon, 15 Sep 2025 21:12:36 GMT  
		Size: 282.4 KB (282449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8084ae79718311fedfafbc5a50335db8ff6184359260f7408a58117f5eecec`  
		Last Modified: Mon, 15 Sep 2025 21:12:40 GMT  
		Size: 83.7 MB (83685170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a9a06c34b13d4a0aef368aed5f69b10bc4b01e7b4d2124aab1e598b4f861d`  
		Last Modified: Mon, 15 Sep 2025 21:12:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cccae355c51d0b51859e49232be0394f93abdf007223727fb9ad0889b5455408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a0c02f36eb68359d6a1205b4eb889659f0957331f01507ca6453699cd51e09`

```dockerfile
```

-	Layers:
	-	`sha256:6d1d861403ab20c62d51b487f158f1d70204d3dd77b111e2eceebbd0bf9cccb9`  
		Last Modified: Mon, 15 Sep 2025 23:23:58 GMT  
		Size: 191.5 KB (191527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15d5701d13195e8115989a97b3ee542c8fa349c3661b27bda3eb84b05ff5354`  
		Last Modified: Mon, 15 Sep 2025 23:23:58 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:c732a0f83ee71fb1614899bd49cd356e4c1a6071ea687a7a3dc2a7db449a14a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84860030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720e60caa3dc08abcb540c159489638739585dde4a90a264af3628b557f99032`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4506233d24d29aff445ca61a62e0b4697cba3d4eaec4c145225ec36461ed6cb`  
		Last Modified: Mon, 22 Sep 2025 22:15:54 GMT  
		Size: 283.3 KB (283326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667cfeddc27e53555bca4026de0a43b07fc7f2fea60a4d56cdbfb0279068e3f4`  
		Last Modified: Mon, 22 Sep 2025 22:16:12 GMT  
		Size: 81.1 MB (81075635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68115829e4fd9c2e8c9d8ddec718af9d997730ac79edbec2b126c4844c39c3`  
		Last Modified: Mon, 22 Sep 2025 22:15:54 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1c53dc70444c2cd62b75d90bf8678e8533d2aea62ea8a08d02ff7366d7e0d63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f31db323d59a0163556345e5389ff5ac78d621db72a3ef70c1b2f494654b2b8`

```dockerfile
```

-	Layers:
	-	`sha256:30a0b679badce0920cfb4957775ad4cd9489aaeeaecbff3a9873081245c70324`  
		Last Modified: Mon, 22 Sep 2025 23:23:52 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:733387ece66f2045eea8f27dc4c0c3835f2d9b9e395c07e00b0e24527e6ed3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84356508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abbac57d4125c23469cd44dd927968a9dd0cbdd0a6d5b31c124a08acc6a346c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2d8db900f3b23956c617ec6891b120e7a87558c4259d66026a65058b063a81`  
		Last Modified: Mon, 22 Sep 2025 22:17:58 GMT  
		Size: 282.5 KB (282499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b53903587a634418235ca9a2a24afbf265d09dc392f55b668e6b9d3c5f19d2`  
		Last Modified: Mon, 22 Sep 2025 22:17:28 GMT  
		Size: 80.9 MB (80854813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5e1c1304f722e1d0bfbdaf71388e04df84c739d7c2a3bcba38c08941e83d94`  
		Last Modified: Mon, 22 Sep 2025 22:17:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:5299a8618a12105bbc39d4e654fce18e42c4adc8172577052481e88245db268e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3aa37f27f2f72ac9fe557e7dab93c1fa923fc83925681b6e4ef8c5fb971159b`

```dockerfile
```

-	Layers:
	-	`sha256:dff3ef0362a2afcf36022cf86eb83b3a83086185afde68ced4ad8752e1b1ee57`  
		Last Modified: Mon, 22 Sep 2025 23:23:55 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667fd0f473d32f938e29e57403c0637dba822c4d772b2af605e8bc4a68a9357d`  
		Last Modified: Mon, 22 Sep 2025 23:23:56 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:78f021e6c5f3ac80b02c41d9f34573d11568d364ba9ff2eafacfe4668a644dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84182896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401249d4570c5bd7ce0b56215e996abed1ec3976483a117c3406bf7643393bdb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28578f59ec293a501333f3330dabed06dc2208ac7681aa9ac2f2b1dd7c0b11cd`  
		Last Modified: Mon, 22 Sep 2025 22:15:52 GMT  
		Size: 284.7 KB (284713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3b299721a40c4d6ce1f1cb5eea411e8ebfdde21f8badd13b95f602420e920d`  
		Last Modified: Mon, 22 Sep 2025 22:16:02 GMT  
		Size: 79.8 MB (79767276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a86606dcd015c349626df097d9c428dd156580d86f6ff08ab804ce5f60939c3`  
		Last Modified: Mon, 22 Sep 2025 22:15:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:583e459a372704069b06d229f078dd79a11d325e71eea74887daf815af95f75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08562fc92c39f2cdb93f9389ef012e9b3a80886fe2a5f4680f709875b1f0da0a`

```dockerfile
```

-	Layers:
	-	`sha256:4be8932f6b5abefb9b3a592f4801423352e0833531029a50a8b4721b342e8675`  
		Last Modified: Mon, 22 Sep 2025 23:23:59 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7368ead943868f84c4bdef586b51941f3c6950044ca5a16b02fa75a19ff8b88f`  
		Last Modified: Mon, 22 Sep 2025 23:24:00 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:f76808dddaee6e768a374b9994995492976313942f8159f4ffe9cbdd5d1081b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86371535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaecd92f16b768f5dc911a2e496a4e1ff940a5ef46266d0118c11c86da6444c2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf50ea3d9d2d9f5841fd142b44a799b3e4dc653d6c51ee87520e664037dfaf`  
		Last Modified: Mon, 22 Sep 2025 22:14:22 GMT  
		Size: 282.9 KB (282920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3896767490999bcc9dd9f56984e3a495c1802d5f9283b126ed682e5e7c6e34ea`  
		Last Modified: Mon, 22 Sep 2025 22:14:34 GMT  
		Size: 82.5 MB (82473451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a31bff739631f510180f7498e46c6eff572f2aeb84131f3437026f009deba4`  
		Last Modified: Mon, 22 Sep 2025 22:14:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a656c229e93eb7eb915940e77ecea8cdb5315f1e0eb1c88bda4248926a159533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01af9c8d806bb263fba5d17e240b06e7eeb452ade26e32f1c6709da84a31a875`

```dockerfile
```

-	Layers:
	-	`sha256:1e7bd746ed8b4197029111419f8aba0ead4c5b1dc6078a154d6a071b8503fe5a`  
		Last Modified: Mon, 22 Sep 2025 23:24:04 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6cb92c84c6a080420db2335d3d1003d844e246dadb1ff0df27665de4535164`  
		Last Modified: Mon, 22 Sep 2025 23:24:05 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:7a7c11c123e1575063d8a5f87aa6c85a2fb7bc0807667004f9d7200883e9b685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85168256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9647f03e57cb61f18583ce452c4d3592d072faf3757182cffbb7d113f49971c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093a8784e85737b54c7bd288e58eb1c4d919cf932185be9835fe0acd194ad05`  
		Last Modified: Tue, 02 Sep 2025 17:37:11 GMT  
		Size: 285.1 KB (285121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cde134c38211f8221348f6d1f1e1ad94732dd62caecb5c0a2623dc2674afdd`  
		Last Modified: Mon, 22 Sep 2025 22:19:09 GMT  
		Size: 81.2 MB (81155866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdfea48646ef474293f5cbeea6212ab819c6bea2c8f912205e8c7fdab610087`  
		Last Modified: Mon, 22 Sep 2025 22:27:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:23b638756751412daf0d04c6e3c26c3ebd995e9652a391bafdda2b42bad8157b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd77fefc156003cc129021ebee3f4aac7bae3dae47ce83d8d84b06afb57c26db`

```dockerfile
```

-	Layers:
	-	`sha256:b2e842902a79043dbdfc255420e34697b08a070688347c6b7aaf7eb589e90739`  
		Last Modified: Mon, 22 Sep 2025 23:24:08 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c9ab5cbecc34c0374ad00e28e92b663417ff6c72f479874ecdfab3597eda57`  
		Last Modified: Mon, 22 Sep 2025 23:24:09 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:acf866d986184949486851aeaa0e9cc8bac4af08e6b17b5b9e3675107c6a82a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85140944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9e704954208944a2aeea2efacc13ad7a276fabfbd565c0cb9fc4a932ff2e14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 15 Sep 2025 05:23:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 15 Sep 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 15 Sep 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Sep 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 15 Sep 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8d07cad9e20eb82eca55470c44bb00c784ba041cde1a36f0b2f92a234216b9`  
		Last Modified: Tue, 16 Sep 2025 20:34:48 GMT  
		Size: 81.3 MB (81345205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8db732bad719e724f4be69b960e2361e3a49f9682d1fe1e258efd411f6f899`  
		Last Modified: Tue, 16 Sep 2025 21:08:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:aae74877eba214ed72c6835c803fc0c972a5d9f5e2db1cc24eb900d852670086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af335b9fa31143241126d6ee50672fe83e85b9ad76b1c4a1771344326ec27275`

```dockerfile
```

-	Layers:
	-	`sha256:e1c6b5acb18780d8779ada0cf1e17fcc786cc2739be3afb1bcbf5145f24d130d`  
		Last Modified: Tue, 16 Sep 2025 23:23:42 GMT  
		Size: 189.6 KB (189620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cb2719688b471ddca1d6107fcec73443929f8258d235c43307f448a0371aead`  
		Last Modified: Tue, 16 Sep 2025 23:23:43 GMT  
		Size: 25.2 KB (25195 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:b37c6d6141fac267f476698ee0ec4c6fee1707201ba0d6e687dd3dfcde242276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86306810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd1e44c2d9b5ee1305aafae6853e80a2a97c03f08bea96407b2c66e90624e7e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 05:23:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Sep 2025 05:23:31 GMT
ENV GOPATH=/go
# Mon, 22 Sep 2025 05:23:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 05:23:31 GMT
COPY /target/ / # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Sep 2025 05:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82129bb6bf719d3efe5e37bbda9c61ccb03eefc8feac9fceac09035731c0c7d`  
		Last Modified: Wed, 03 Sep 2025 20:46:26 GMT  
		Size: 283.5 KB (283475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378803bc6cc1e0c01f411ee825bdc456b59e4a7d5184c546614a84a4ce15dd67`  
		Last Modified: Mon, 22 Sep 2025 22:15:10 GMT  
		Size: 82.4 MB (82378206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca750661e5cbaaa75f119177ac0249203aa098e104063e85f7520b58fd5c646`  
		Last Modified: Mon, 22 Sep 2025 22:22:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:25ad95b6c1fe98ad7af78175f51a123683ee0a6260914550937129a7bc52ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9dadd7c87ece82985d4313218184c1786ff0f729f97c6d47c9283142e5d0a9`

```dockerfile
```

-	Layers:
	-	`sha256:2c95920d07464fc50916ffb5f9f1db9093c3a9ede602eb88a94f4edc0aa2f17e`  
		Last Modified: Mon, 22 Sep 2025 23:24:12 GMT  
		Size: 189.6 KB (189576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:476a869cde6cc5bb6bd7b001cc58c0c86eddb015c19e445d6178bb7a59606ad8`  
		Last Modified: Mon, 22 Sep 2025 23:24:13 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
