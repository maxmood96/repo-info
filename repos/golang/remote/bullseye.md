## `golang:bullseye`

```console
$ docker pull golang@sha256:d1e5c3fc751d2c55bd3af9450d68c77db1ab562880020021b30ea3a5c40540e7
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

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:07cc333094ece716626cd0667cb7446eb4d5ad693a83e4d0ba37baf97a0299cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (288995139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2017d36000e76b0f16a9c258dd380c54733fc7257ded36ccdfb3678968f834e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322d21cc1b9c3e86a0528fd885e7483a3b2497c1448256bf87a4493be665ab0`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 54.8 MB (54752320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efcab33579810e517a081ea958262d5a66cbe3312c2c54ff2606eda3e2afca0`  
		Last Modified: Tue, 01 Apr 2025 17:07:47 GMT  
		Size: 86.0 MB (86000814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d296901bdc593d88a0813bb00eef0974b68222cba6add046b831c086a1c68c`  
		Last Modified: Tue, 01 Apr 2025 17:07:26 GMT  
		Size: 78.9 MB (78942217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6ecf2bc7f8fe38fc75a76c98728246dc8338083cf49e01972c4a84a0570a9b`  
		Last Modified: Tue, 01 Apr 2025 17:07:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:15a28460de2ed3e032c2dce3574dbc2ace0e43e5f6062cc363ded3ca4a68cefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10289977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38fab8af507c79fbc108d4b614f4c36447d5961f2e2ba5e04d60abf551bb25f`

```dockerfile
```

-	Layers:
	-	`sha256:066220a760b2fdded811c156eba64d0060d9e20429658c735b82ebe7f58baf0b`  
		Last Modified: Tue, 01 Apr 2025 17:07:44 GMT  
		Size: 10.3 MB (10263509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08868fb62391ba89445b8afe679a45ec1e9a44aa5b26b13267f72fcfac820950`  
		Last Modified: Tue, 01 Apr 2025 17:07:44 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:7830b73ba96b5704621ba7998a795cf880bae36b3a46c81006663e5fd05b4c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256365055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740cc8b9b4f9f30b3a6152529df72f1e1011eea63c1ab32a2600b78aaf450fcd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0192ce451b4bc1458959a86a1dd55f46cf5148c4d3e016589a215f847b4e66ae`  
		Last Modified: Tue, 18 Mar 2025 16:49:06 GMT  
		Size: 64.9 MB (64922890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9003e8a4d55742a1a2128c3dabddda68ec2c585f52d2aac5eaee8bd68089640`  
		Last Modified: Tue, 01 Apr 2025 17:07:37 GMT  
		Size: 77.1 MB (77101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a808b38cff5495c1b3614a6c03b2fa95da3624cb272af6ffe48f832fe121793a`  
		Last Modified: Tue, 01 Apr 2025 17:08:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:df4ce0baa46a83aaead67c55cea39b34e8dc511c06eb33de7a376b9c2cc08a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10096439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cf391077d817a5ed580faa5434d944bdef84543b7ecdb82f9c73d20775e310`

```dockerfile
```

-	Layers:
	-	`sha256:dcb4659b39c023c74571decf849e77ca3ef5464fd9f859e0cdbe134d92ff2b25`  
		Last Modified: Tue, 01 Apr 2025 17:08:30 GMT  
		Size: 10.1 MB (10069869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664e1b7dfc65d513f61bc451e7723188b38102ddd4ac0c79fe2a292dec8f7b56`  
		Last Modified: Tue, 01 Apr 2025 17:08:29 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:18a35f11ab71453e8e2678d3403a24ecbf6feb73e3837ddd20108ea92cfe0c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279261938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d8e029eb67b5b7b30c80bfd6ac30fed440898128982b60d8be65036075c4ef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d852072c6d90387d6d845e4f9e792adafa4579fd943cc48eacd0405192508786`  
		Last Modified: Tue, 18 Mar 2025 18:56:37 GMT  
		Size: 81.4 MB (81413745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a002eda2038f0953467f843586445333b2af3e827e57b15849040931f2903fb4`  
		Last Modified: Tue, 01 Apr 2025 17:07:27 GMT  
		Size: 75.2 MB (75200208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb062ac1922a44404f9b81ececec185f36f1ae1d1eefe2d3ebf0316ec609a02`  
		Last Modified: Tue, 01 Apr 2025 17:08:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:197a1244e44b1d8831d399ee1dff9ce731bd4761dd43feb25db607f45276e5f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10291705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca2e15b3ff3c82055ebf8f97806c19023d54524cf4c77baf9ab02b8597a4c14`

```dockerfile
```

-	Layers:
	-	`sha256:bb6b2540eec0ec48829d0fc20f863a20bc38b67c19134eb0da8ed98b75f226e6`  
		Last Modified: Tue, 01 Apr 2025 17:08:18 GMT  
		Size: 10.3 MB (10265105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2c925add9417707aa0ee351f5b520e99e2e4ff9a043ee618fcffcf29283b79`  
		Last Modified: Tue, 01 Apr 2025 17:08:17 GMT  
		Size: 26.6 KB (26600 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:f0435f4b3c14841931520c36f70e447392d2cff20fe5a8d16b7a5aca0acc7773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291070700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7593ebbfef0d4f8bf8fabd787ac8ba981a0a5ac7795484309b3d89c7d140c4c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646cf548789d92bb8cdd143391e700447f1d9fb5df35471386625e2c8831f81d`  
		Last Modified: Tue, 01 Apr 2025 17:07:38 GMT  
		Size: 87.4 MB (87426460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb556227a38cd463b29410ff393a23b771d304e2f2f265b6c233fe487c9ca9ff`  
		Last Modified: Tue, 01 Apr 2025 17:07:28 GMT  
		Size: 76.9 MB (76873414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf209b44236c74d2194d4055b2ee58cf8fc93854e58e956020548d78f17658c`  
		Last Modified: Tue, 01 Apr 2025 17:07:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f5f60ac694135ffa45d14f353ca669597f6f4f94fbb9fff727c70c99f802ed25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882f2dd50f3b3b7220f878d6ffbc8d2db17aaaeed53112a6bb63eb9cbd52e34b`

```dockerfile
```

-	Layers:
	-	`sha256:4a026beb8f4725ea21e11161a873bb57ccfd8eb0e7bcaa312774f07b51a5745d`  
		Last Modified: Tue, 01 Apr 2025 17:07:36 GMT  
		Size: 10.3 MB (10253294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52ff0a4736469e3abeb3a00dfffd94f37f47747ad9865d1123dfda6bfffb685e`  
		Last Modified: Tue, 01 Apr 2025 17:07:35 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json
