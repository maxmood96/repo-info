## `golang:tip-20250629-bullseye`

```console
$ docker pull golang@sha256:9f8b88ae5da60d136f8fb36f37d62ce76385ceb73875c09c39d557abf02b77d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20250629-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:984ce9415864ab8cc6590728aed8e2275b9387e845ce8abc631724905565bfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293384507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ff61e30add2ef8a9e4ba2673ad72f294199526dde756b4993a64516cc27c2a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2678613884c2f141cc551880b1a1587f0c890606a900bbac5a1ace2645be657`  
		Last Modified: Wed, 11 Jun 2025 00:02:35 GMT  
		Size: 54.8 MB (54757363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9bb11977be2e78535a73321366655a97837e7b979c9ffae604e535e7c9755a`  
		Last Modified: Mon, 30 Jun 2025 17:31:05 GMT  
		Size: 86.0 MB (86022010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d8f8c49f445d30fa7cd4c028a18d5365e5bdfe97436ef61eb7709425c99cad`  
		Last Modified: Mon, 30 Jun 2025 17:30:36 GMT  
		Size: 83.1 MB (83085055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041ea05f74855e8f89ee216a95891243a495147acc16852796996e2961aa7c4e`  
		Last Modified: Mon, 30 Jun 2025 17:30:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250629-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d619c6253866dc7a7bf7d7ef217549c01021ea4bc50239fa75fdab15853220a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10509220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aceff7c579553e4083cdf203efae617ff2cef9284834abdb797e5b620605dbee`

```dockerfile
```

-	Layers:
	-	`sha256:42cb18a39dce921aaa6d7ffe61a1b57dbac61c8f758752717a6523dee7a6ef25`  
		Last Modified: Mon, 30 Jun 2025 20:25:08 GMT  
		Size: 10.5 MB (10482164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32c8ec00b9ac1089ab6dd2d489d6e55062aaf804682ed9f41ed2e70cf403e693`  
		Last Modified: Mon, 30 Jun 2025 20:25:09 GMT  
		Size: 27.1 KB (27056 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250629-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:3886292f77800645d840009c376da1ae48b08ed8d9b01cb4ba3c73522fea9fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259661368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0a966b5d92dfbd678a81e68e70d0197ab920ffa9f80cc479b971c636d550fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f7feeb0b6a1c7b2f8058fc4bcf8523950540bd39c01231df0b01c7791add68`  
		Last Modified: Wed, 11 Jun 2025 18:28:34 GMT  
		Size: 64.9 MB (64942390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6586f6a3b72edca5355ba2231baded357cf799f55b8944edc8ae75b0c7b67acf`  
		Last Modified: Mon, 30 Jun 2025 17:31:46 GMT  
		Size: 80.2 MB (80163369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be63f93a75831bb3cbe2364b60cedca7d06c643c073ecaf72e637e23a317eec9`  
		Last Modified: Mon, 30 Jun 2025 17:35:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250629-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f58ccc8703c8ae6e5e95c2999e95c73493210ff37d19c59ce9e6fe27f06f6f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10316329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef442bdbfd4bdb2cc383499fa57e9863bffdfd80c19514a2dbc21f6e1645c6a`

```dockerfile
```

-	Layers:
	-	`sha256:e297eccf639db4cfe39e2f3ebbb2c9d4f81ef0e000327d514a087fbeb190a3db`  
		Last Modified: Mon, 30 Jun 2025 20:25:17 GMT  
		Size: 10.3 MB (10289165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0c8a5c321facf3ffff7ccd044500c0bf3ace88d0fba226c69340ddde4c7e554`  
		Last Modified: Mon, 30 Jun 2025 20:25:18 GMT  
		Size: 27.2 KB (27164 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250629-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:92598b39367549813637f4b3344f102883bcca8684962e912b205f32d44ea0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283345781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a3ac2f410d9dcd124a32d51993fdea78de9ac89bb5bff1dc71e2077f4c3e44`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44d5956aed85d3d6d2c696b8489053af4a6a4d168314e425819189773cd2fb`  
		Last Modified: Wed, 11 Jun 2025 23:10:33 GMT  
		Size: 81.4 MB (81431904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f0e5c856fb20135c901f955406b40129ab946b3615cd5e0d5839e969930423`  
		Last Modified: Mon, 30 Jun 2025 17:34:31 GMT  
		Size: 79.1 MB (79057770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dc9b5a9728d8f4ad9b9d089d8c95beb611c03e6c20459aa655d686913b3f2f`  
		Last Modified: Mon, 30 Jun 2025 17:36:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250629-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5115d479328cbcbc5c38c36121898b50dab295f2b973110b01ea7fa12effa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42f92d0daaf72475c8f678cb124f438ef4eca00dd72f4251a9194cc9df87db`

```dockerfile
```

-	Layers:
	-	`sha256:087e937579aa430df1087aaa5834342106cbeb729855ff4f0bdab50ff5a338c6`  
		Last Modified: Mon, 30 Jun 2025 20:25:26 GMT  
		Size: 10.5 MB (10483447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50da57d1ec156dfaa94169446f0015045869cfeb18919ceae9ab2d0b2c7e9ed6`  
		Last Modified: Mon, 30 Jun 2025 20:25:26 GMT  
		Size: 27.2 KB (27193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250629-bullseye` - linux; 386

```console
$ docker pull golang@sha256:fdd837704f96f184a6b942dea4b3e9220adcafc9b39a0b0d210a9a70646141ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296266956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305282b59297ae3afea934ee0536e6f2ff2049f834fd5ad5574b0f007f506c93`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a34392e433938214bbf2cba34365a474d819c470686803059c6d8390cf680`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 56.0 MB (56049939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5b7f11214e346d22e2a3214f7021eb6f025312183ad17384b846072e3e5cb2`  
		Last Modified: Mon, 30 Jun 2025 17:31:44 GMT  
		Size: 87.4 MB (87448088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2781a7c01ceed520d1e8478386c7e0683cbeab9ca6a32207c24229a367897`  
		Last Modified: Mon, 30 Jun 2025 17:31:11 GMT  
		Size: 81.8 MB (81810142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a1d8b4d6839d19edddeb2811661dbf4460cd7eb3688e3938f447992968c2f4`  
		Last Modified: Mon, 30 Jun 2025 17:31:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250629-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5f8e587d9614ae88517d8192412eb2bb533f293e90aa323162999496d3f2a851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84402436fcda9204365649cc14c1f26054d8a781c67e8d22f9d8fc25ef4ee903`

```dockerfile
```

-	Layers:
	-	`sha256:0a6566c8fe83da949cc192d0a0a3759c242b8db5164784ac9307db5dd825afc5`  
		Last Modified: Mon, 30 Jun 2025 20:25:34 GMT  
		Size: 10.5 MB (10471501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5530ce44b87526ee011528b8bb5645eb8cb11d410cc04a6d4d9defaf4bbad3d1`  
		Last Modified: Mon, 30 Jun 2025 20:25:35 GMT  
		Size: 27.0 KB (27021 bytes)  
		MIME: application/vnd.in-toto+json
