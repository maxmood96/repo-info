## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:8a76ef275fde9c3dcc9e19d81c3a0565e6db822d87384f730a45936c2db2587c
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

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:b335343c80e4035f406b5c45691ebb8f50e66405ebe785cb64ef1d57a5f02fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336074904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c24a6d3caff41c13c6c70ee4d2a17263571c577a7524183e1a9f489d4c9f79`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
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
	-	`sha256:7f830c2a9072c3a137276831472d670a5ffeedfd325c620fa26ca91e51bd76b5`  
		Last Modified: Mon, 24 Mar 2025 21:23:32 GMT  
		Size: 86.0 MB (86000766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59cbe769fc954b1a5756fdf48e31713555a112012d07425d7d4a076ea9376a7`  
		Last Modified: Mon, 24 Mar 2025 21:23:19 GMT  
		Size: 126.0 MB (126022030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6b461259c541b3b9bf9af89564840046f2e3394de2df93ddcb67654d801612`  
		Last Modified: Mon, 24 Mar 2025 21:23:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5c9f7c5975782f56042f04d1b7ff91eb637d7674f55ed62a58feb2dbff39ba09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10291346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0547e88d10a6eb14ff3bff6b76474358bcee8ee11cf737f995a590bdfa54c97e`

```dockerfile
```

-	Layers:
	-	`sha256:63889248f5d90501bb993cef29bdb7b0ff7f88c2d1533febeed960f39845e402`  
		Last Modified: Mon, 24 Mar 2025 21:23:30 GMT  
		Size: 10.3 MB (10264285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c452cc294d4ecc82a68eacebbe50b3e63afb130d947c5d5197c34728b80ebc8f`  
		Last Modified: Mon, 24 Mar 2025 21:23:29 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:15edbb9b44d275186a941514c6cd96c1a42782912c6050ecb65368ec0a28a3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300209178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7397ad7137283a711dc0524c96478267cdbde8d247a4a120e4b235afaec7d302`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
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
	-	`sha256:7353e9c70d02c05f5d0756f45338b0d2910b536c139fce40d68a3d97077441d9`  
		Last Modified: Mon, 24 Mar 2025 21:24:23 GMT  
		Size: 120.9 MB (120945332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c47392e680e6d0ad195f9853c84010f1e34f963f57c53e54b62cfe955ec5ad`  
		Last Modified: Mon, 24 Mar 2025 21:28:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:a7b6d2e3d1837f339d10da83303298047afed460da21e4712ebd4b8aa9eab635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10097794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214c448535a37292639b76c2c19f926986397bd02ed98e0d0bd017ade2b6a121`

```dockerfile
```

-	Layers:
	-	`sha256:2dd143734d3d3c15c1f5917ff5c82db637b6af3a74b6b9a03cf9e79aed924930`  
		Last Modified: Mon, 24 Mar 2025 21:28:33 GMT  
		Size: 10.1 MB (10070625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca72ee01e908cecb7fb7b4955efb014a7006e980acc77e2e98b99f1a750aef38`  
		Last Modified: Mon, 24 Mar 2025 21:28:32 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8f9c7b1145d2d2185646dc4284829c10daaa0d21b2e6b9de9eafc53d4cb57d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322620967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4792c6178ddaeca53e7af60faa8fafeaf6d11d47061ec3ae4be8d291185e7fe6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
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
	-	`sha256:aaa27b15393e951766b04748acddefa2554a614c3407abc8145f05a37f7e1559`  
		Last Modified: Mon, 24 Mar 2025 21:24:41 GMT  
		Size: 118.6 MB (118559237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecac7e530c1ab15762beebf0b780b5d94711cdf701724590c54b964c361fbc23`  
		Last Modified: Mon, 24 Mar 2025 21:27:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7bcc586eeacc574eb6118256efadc5d57f0be19487dd435038ed073fc0b44269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590e13eaaf5f2c243121035b5c45b383a74c9f1ea77ae3e0d9bdc210bcc1174d`

```dockerfile
```

-	Layers:
	-	`sha256:91eda7ba0403d355af2716c1430fc7d714eaa6f60ceb7321fcec148b1c69fa7e`  
		Last Modified: Mon, 24 Mar 2025 21:27:16 GMT  
		Size: 10.3 MB (10265857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebed410201d11219fb31dcc1e6939e81d857efda6960ff8f748a1a236befaf46`  
		Last Modified: Mon, 24 Mar 2025 21:27:15 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:907ecff6e9a00cf56f943d9143fe6ba813aaedfd5323bccb98bf77b21fde0707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338309666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4149e633c40e3c893edeee1cb4bd535a67f704ec59a63c33b599889127fc7048`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 24 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 24 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 24 Mar 2025 05:23:21 GMT
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
	-	`sha256:7284441ee957f002846c215fdd54867de7ada16d071577484673b677c429249b`  
		Last Modified: Mon, 24 Mar 2025 21:24:03 GMT  
		Size: 87.4 MB (87426518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76390dce495fb7dc13ff79afd09a2f809cad266d649bc9c2cf3aae32aea2ff71`  
		Last Modified: Mon, 24 Mar 2025 21:23:39 GMT  
		Size: 124.1 MB (124112320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509de3c06c1996dd34f68e48856aef1d3cd69c6dfe1c46baa0bc5ca9c9c6ae2`  
		Last Modified: Mon, 24 Mar 2025 21:23:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d13985599b2c867eebb4673e68c3d6b3447245f983a5877fc88b2c507520b568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5994644bb46cd115cc9281252c868ebea1ea401eec73fb044813e965eb0fd0b3`

```dockerfile
```

-	Layers:
	-	`sha256:c223cd8d3dcc89c7e83cc1a3ba473c625efc2875114aa303621939209a6b0aee`  
		Last Modified: Mon, 24 Mar 2025 21:23:56 GMT  
		Size: 10.3 MB (10254076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67aabe7313e515f4a05b4de563eaf1134eb5a908a16922fbfe98ece5ac6f6933`  
		Last Modified: Mon, 24 Mar 2025 21:23:55 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
