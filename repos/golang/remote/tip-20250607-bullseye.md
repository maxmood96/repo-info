## `golang:tip-20250607-bullseye`

```console
$ docker pull golang@sha256:1ba8ac1fbe9630a96fecebf09b77cb67bf3032e655dd8461615f083e971db141
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

### `golang:tip-20250607-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:844564cd05ee2bc02c56bb2a98733aa4668d515c4e3d992613c47b7e07622a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293456733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca15017445b4993b2430958ecd7b6f9295cdc58657f597d4857cb885fdc64642`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
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
	-	`sha256:d82486623c2d6d840b4cb7ad98c2b067fa96cbf0d634dbb523cf1346e35e0666`  
		Last Modified: Wed, 11 Jun 2025 05:29:36 GMT  
		Size: 86.0 MB (86021733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc635c4b2a5c576a8a73069e117f29a377ce38e81427c57d725fc1f78f5ae3`  
		Last Modified: Mon, 09 Jun 2025 22:08:44 GMT  
		Size: 83.2 MB (83157558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8d157fb74e46a3e6c616e58816ac5ab7ced61b407196d267923db5d8ed668b`  
		Last Modified: Wed, 11 Jun 2025 02:33:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ac41d27ec833353e9ee6ec3e9b788f104ab38df041b199847cb27ab51cabf2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10509221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06112d2ad5c7b450925d53404aa1c58257f11cffd50db65aa60ccf5e30f8d57e`

```dockerfile
```

-	Layers:
	-	`sha256:dc0ba706dc431af5275f1d2a76cbba7e2de87be05901ebca6bd892cc3708e0e3`  
		Last Modified: Wed, 11 Jun 2025 05:23:30 GMT  
		Size: 10.5 MB (10482164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8137a2ebd45ef262f1c904834f9d9b6d1d702a854aa1cb8c6c474ecc1ded5c`  
		Last Modified: Wed, 11 Jun 2025 05:23:31 GMT  
		Size: 27.1 KB (27057 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:d618d29c498c3911a2083494aa1090c80effbd65d8360aaf6582fd4fc9c30e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259753847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeaf956eb372368a04b5f1e45b45e566438ec82efef123d11d84ebc16adcfbc3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
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
	-	`sha256:cfdbba4495ee849a32b1868921c9f94170c36c552299b715ecef8d63f110b4be`  
		Last Modified: Mon, 09 Jun 2025 22:17:51 GMT  
		Size: 80.3 MB (80255849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75596db36e4e23c35c56c0520cbb297225700e0bf72264140a932cd64b75689a`  
		Last Modified: Thu, 12 Jun 2025 04:18:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:1c70227f40949eabbd6f5b8a7afb7e732ff29bc01cbe91557cd77d7579fb75ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10316330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8707975a2a25ce46ac40444a1de52749f3f7201ceec29953e036ba8f959cdb`

```dockerfile
```

-	Layers:
	-	`sha256:02081a1373a8a3fef48ba5690be5cdfdce4067682a604e46c739927e84d4333d`  
		Last Modified: Thu, 12 Jun 2025 05:23:33 GMT  
		Size: 10.3 MB (10289165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff75ac7792793f849e97ca6f0ed943ad2a7a6b64cac47cba4f68a8f98f783f3`  
		Last Modified: Thu, 12 Jun 2025 05:23:33 GMT  
		Size: 27.2 KB (27165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c7660041d0ec28c6d8b668b625c2bd8ebe84cf08afea1e1c677a95ca13e3d592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283429021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c00060e4ed2ffe96aaf31840e68ddbc771dbdb197b35b7b823381c95d566ff9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
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
	-	`sha256:f9018e4f62f0690ad9682f8c2f1f9edb62acf90f09cff841cc366e0feec33aa3`  
		Last Modified: Mon, 09 Jun 2025 22:08:25 GMT  
		Size: 79.1 MB (79141010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba21242a0ea74c1ea3977ac69fb50e4d7afdd831b11cb5384e1fd3639129fe8`  
		Last Modified: Wed, 11 Jun 2025 23:10:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:b6c5dcc93dbcc412f00e8e3f81d924370305cf5e902aa4729f690c08c3e67b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc9bc054d2de45ee480fccbefa6782aa7fbec2f3550bbfa8020c6cfea11b975`

```dockerfile
```

-	Layers:
	-	`sha256:c623fd6a3c720398c86d2d30ad44ae675563ec1c5ed1c493efce56f7d2cb761e`  
		Last Modified: Thu, 12 Jun 2025 02:23:39 GMT  
		Size: 10.5 MB (10483447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e915b32394c416bb098e8ca6b5672be4bf8a0cb5509aa2769ba47cc7cc7fa5e8`  
		Last Modified: Thu, 12 Jun 2025 02:23:40 GMT  
		Size: 27.2 KB (27193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250607-bullseye` - linux; 386

```console
$ docker pull golang@sha256:4b126417d8baf4a39fa0cf71bc76556bd72320dedfb51ce0f789b1a892c63e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296352515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f4a39027da13758f1d2c5d9ab51407124e656b3dced1c87ebcfa8c14431ea0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Jun 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 09 Jun 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Jun 2025 05:23:21 GMT
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
	-	`sha256:d34f7537f2d9ae29f2ebb3d220b8c8405490be041aa88ba050cece3367509647`  
		Last Modified: Wed, 11 Jun 2025 02:20:53 GMT  
		Size: 87.4 MB (87448062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390b4524b05c1706d1b72e8575c65245c59334a3e5a6eaa54af3aee803a8d9ca`  
		Last Modified: Tue, 10 Jun 2025 00:21:15 GMT  
		Size: 81.9 MB (81895727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569f5bada9beb331334bb795c30e7d6924068f130f75d37bd70866636bf043c0`  
		Last Modified: Wed, 11 Jun 2025 02:20:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250607-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:073dda2a17b6001b09a35bb66e17d0a6018798aa20d4582209f7e5f7837b9aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10498525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5643dd1a0344e958ab2315d268d81ae29f237c4c345aecdd66658328b46836b`

```dockerfile
```

-	Layers:
	-	`sha256:3eee3b0c4e6121d49e8ddcbbae7f01a55cc5a06bfb4f63b26f7d86fea1bca999`  
		Last Modified: Wed, 11 Jun 2025 05:23:49 GMT  
		Size: 10.5 MB (10471501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6037c597926436d3b64d0c1ee10c14043ac09fa231e45cdc500d0a9dd2597c21`  
		Last Modified: Wed, 11 Jun 2025 05:23:50 GMT  
		Size: 27.0 KB (27024 bytes)  
		MIME: application/vnd.in-toto+json
