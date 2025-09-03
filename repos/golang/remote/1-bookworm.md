## `golang:1-bookworm`

```console
$ docker pull golang@sha256:a0941d4d63a9071a13552c566282749ee7453964d248550fa72ad3e0b0ee4b6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:3ae23f7b7ba16dd26b6ec026166f20cedf431fd1b88edbc8e49379f0207c3b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289339614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c368ca44f5d20c6e755d528b49f0ea8d8ed42884e98326762a8d5dd4c079b34b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e3f33071c55ae5dc9150cb1ebb85939a4206456bbab37d34fd48b6ca0f541b`  
		Last Modified: Wed, 03 Sep 2025 19:04:36 GMT  
		Size: 92.4 MB (92378446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330457f0054be4c07fbaeac90483ac4f534113ccd944fe16beb9e079a3ab3a36`  
		Last Modified: Wed, 03 Sep 2025 18:49:05 GMT  
		Size: 60.0 MB (60045609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0296f41d282175cb9ccb7539566f7129a4a2070899262adb44fa8835993428`  
		Last Modified: Wed, 03 Sep 2025 18:55:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b2fefd7405706352b799984b0065fa6c5e7459901b6046298fd586d60b1f28fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83d658e4d6c58ab5ba492b595bbae5d9391c6901fdc5e5d7470e8889236f5e3`

```dockerfile
```

-	Layers:
	-	`sha256:76cd54e3f7b5b4841d2bc5c868a889d2332c51242012581451dd0fd2e1a662e8`  
		Last Modified: Wed, 03 Sep 2025 19:05:47 GMT  
		Size: 10.5 MB (10488967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4766f1bf8716705a060a43da1db2a463862dd08d5e0303cdc4631bdeadf06c41`  
		Last Modified: Wed, 03 Sep 2025 19:05:48 GMT  
		Size: 27.8 KB (27840 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:f1ee2b5db7516c4abfda731b7ca892e65bcdefe46f51808e50dedee008bd0450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (251017396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8120d2e482ecfacb66c5af0e875d2f5a653067d44c4c9244a12caeb47a1fc8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897d6edccc28c5bb741d67021941e03742df0d455c33993ccd0aa632e1cd6d24`  
		Last Modified: Wed, 13 Aug 2025 06:46:44 GMT  
		Size: 59.7 MB (59656741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646a036d17dea963a87e5b5f829c9131c3947ef44cfc0b2795f389524f661ee`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 66.2 MB (66243912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec999c8e928607a0bc4da54080226a6c247c744815a64f6c10bf38b015958ebf`  
		Last Modified: Wed, 03 Sep 2025 19:08:36 GMT  
		Size: 59.0 MB (58978176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1263033b96d9290f4969661ad0abb50c064aa016a442c57ef7309a1372f7ce`  
		Last Modified: Wed, 03 Sep 2025 18:55:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:b34276ebfc5d7bafbf32d4863e73906e12afd1b9fdd871acbad5ba085b926aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10323623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736f7a111372ad078de6190a3e6107d390ee6e2348e4c3e1a160c1aed107309d`

```dockerfile
```

-	Layers:
	-	`sha256:7f61387daa9d7ff47dc775cf0e7d6fe41ec7c589c1558c4cf7e3a7924f9a1cc1`  
		Last Modified: Wed, 03 Sep 2025 19:05:57 GMT  
		Size: 10.3 MB (10295681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339052bb4f1433e3d657ef5a04324de2864f99ead3b5a18026098e74aa20ed77`  
		Last Modified: Wed, 03 Sep 2025 19:05:58 GMT  
		Size: 27.9 KB (27942 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:87e3db7bb9e15ba05e5773d2f32a81fceb9cc21092e1e458286b4eee18f1b20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280276695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c986ece3a4d89612d8d8143bdaa23a6cfbf8d3adaa1e5829509c862fbfc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022e19889d5b43d1bba827a7f5dfb329b722fbf9878dea6ccf631c82db2efc8a`  
		Last Modified: Tue, 02 Sep 2025 21:42:11 GMT  
		Size: 86.4 MB (86441757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4681030a890db37290ab2fddf45adb75dbd1fbf983ba1b16efefb7221b97b1ec`  
		Last Modified: Wed, 03 Sep 2025 18:48:35 GMT  
		Size: 57.6 MB (57555480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be872b02523740b6ca8c29fb21df5179a7b4e6996d9bbece08fa4e8d7242fd2`  
		Last Modified: Wed, 03 Sep 2025 19:08:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6cd6c97e7b61b4dfe4e0829abae41fec72284d22db4b5b2d95c48f7b31eba8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10544789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8df7ead0eb8cec58ac31f332bc754cc80cf0e34ab4be5db845f55b05f5c22b`

```dockerfile
```

-	Layers:
	-	`sha256:0e09996da646a35094dfe0ed4235d5a5f6ae2c4672f051462e93de69e8a6ede1`  
		Last Modified: Wed, 03 Sep 2025 19:06:06 GMT  
		Size: 10.5 MB (10516815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d73c4c57e5287a71ce0361743d1ddcf5008c435521e2983818b5d7e0979e4a`  
		Last Modified: Wed, 03 Sep 2025 19:06:08 GMT  
		Size: 28.0 KB (27974 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:a690112a6c6e46f3116dfe106eca0532145bc6b968a1e5a488837f99343e64af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289137854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7c9432c1df085a1a257c300505cf55e16bf8f0442fe08d91b5c05665b81ecf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874646e2459984b117c58d731a64ebcb9d23f76cf755c68e1ddb30317e57abc0`  
		Last Modified: Tue, 12 Aug 2025 22:13:36 GMT  
		Size: 24.9 MB (24861125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c25d261fc893dbf63d447e191cad0237f37f95f01960ee9b9026b75ab3a74`  
		Last Modified: Tue, 12 Aug 2025 22:14:47 GMT  
		Size: 66.2 MB (66226107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e2a046d268ce1c665646a202741ec2c76a2d57902bc1ad12bee7726938e325`  
		Last Modified: Wed, 03 Sep 2025 18:50:58 GMT  
		Size: 89.8 MB (89808300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8134730600d4cfc74c5293aacb74478de1de4810632b08ac46dafe23f69bbce`  
		Last Modified: Wed, 03 Sep 2025 19:04:05 GMT  
		Size: 58.8 MB (58764049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9636c9117f6ae65bbff5bfa4c302ad3422bb685853e8a11a97dd53beb5cbd8f`  
		Last Modified: Wed, 03 Sep 2025 18:50:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5f12a16f364daf99a66a5b881e69311fc68c9f1080bce8f57961ffb7ff2a39eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5efb36bd5c7b943b0da7cc8e0a9b1b6c9c9daf3378d91d75e7522f4b1b6850`

```dockerfile
```

-	Layers:
	-	`sha256:c5ad80eded30c93e31661d27d01267ebc280a03160896c47c696b52ccad6b8dc`  
		Last Modified: Wed, 03 Sep 2025 19:06:16 GMT  
		Size: 10.5 MB (10468545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964947394a6f825e5dd1b9008e3e7614aa26a597da0f52cdcef60c2f5681fbb4`  
		Last Modified: Wed, 03 Sep 2025 19:06:17 GMT  
		Size: 27.8 KB (27804 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:bfa58fcb58d22c0c2d3db1826df7a6fdef48757058a76cb2c8190224c964c691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262151285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dfb9f877708e3d8783448a167097ea50a228b3ceadb44e9d7b9be05b611cfb6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bf976bc5466a2e4cdc6d87c28337bf663ea094da7d169694d61961d11248d`  
		Last Modified: Wed, 13 Aug 2025 06:38:46 GMT  
		Size: 23.6 MB (23603659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e53fb77ec58b351a832fef6343e52e81f478bfac5e6664210978fbb38a2cddf`  
		Last Modified: Wed, 13 Aug 2025 19:21:03 GMT  
		Size: 63.3 MB (63308715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b41136c2f291bd13099a18611b2b7518da292943df8ae3469285b2a82ab662d`  
		Last Modified: Fri, 22 Aug 2025 17:35:21 GMT  
		Size: 70.0 MB (69983468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d29a42ef2530f05f5cf537801a54b97139f5ccd83724c719331ac0f6142402`  
		Last Modified: Wed, 03 Sep 2025 18:52:00 GMT  
		Size: 56.5 MB (56478629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d6671137dcd9ea2c5cb0c5c6dd0ad00ee52ecea8602136342a6ff407685bd2`  
		Last Modified: Wed, 03 Sep 2025 18:51:46 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:61c960503c292ec4399332fc3e74e2e97f67de4b75a6b9b82a9837df6cf21762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a0149f3064a97b8a6598129117113b92693b608306505a061cdba9c123dba7`

```dockerfile
```

-	Layers:
	-	`sha256:5079004893f529aa48537508d2c6dd95d312dd6fd480100c7f9b5666192e5ab1`  
		Last Modified: Wed, 03 Sep 2025 19:06:25 GMT  
		Size: 27.7 KB (27697 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:b1d168d8f30431fe42bb75af76edd6ed45fc09631c875cc016cc89f9b31ffad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296266288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5153a60d1f7c8b3d689ecc073ff3c72053f8544b7b62b27fffdd38c07f1d662`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f87ea767eb09118b3668a0dc44ddf5bf258db4f1bebc7989803cb1b75a66c9`  
		Last Modified: Wed, 13 Aug 2025 14:33:16 GMT  
		Size: 25.7 MB (25666039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb09aa58684adf8f458ec24cfe46bcd658b8344a3c5c5ec70c88bbe9010b255`  
		Last Modified: Wed, 13 Aug 2025 22:43:40 GMT  
		Size: 69.8 MB (69839966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a90f33dee95b0cc1cac58b7d8f984ddb9d36a6f3d6f293da1b4570532671ca`  
		Last Modified: Tue, 02 Sep 2025 17:33:11 GMT  
		Size: 90.4 MB (90385885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9295eaa21ceb778d7859c40f41ccdf7cdeffaaa99a56ac388f747e3eb72308f3`  
		Last Modified: Wed, 03 Sep 2025 18:50:02 GMT  
		Size: 58.0 MB (58036165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a247d95614a77ed131b9a6c6be10bd6835cc246094af34c3c334ba4365f3356d`  
		Last Modified: Wed, 03 Sep 2025 18:51:11 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8aad72f67e920bc237cfe07fdd3cefebbbd893e9552330f8331739ccfc74ba6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10489338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4183e18c170fc60cfc708b072078f7dcaa14694914e2e7d07b620bdcab2d1a51`

```dockerfile
```

-	Layers:
	-	`sha256:bbb5f22964c34e04c50cae481b9375188732fe12da92757d461beca3f434a3c0`  
		Last Modified: Wed, 03 Sep 2025 19:06:31 GMT  
		Size: 10.5 MB (10461450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac76e92b27ea3bb2e1d15d977316c6c74709eb7560338d1011e0a0f991b27a3e`  
		Last Modified: Wed, 03 Sep 2025 19:06:32 GMT  
		Size: 27.9 KB (27888 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:adad65a54f6f978b629f22292897e9db462175e9ddfe2fcc90b3dee1fdabd53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263018809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637ea9183ece7cc5c5c9991f872cea45d443b67df7c0fecf4ff082966f660c5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOLANG_VERSION=1.25.0
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75c300f83884b3a2b4352096299334113ee00d6718ab116cdad0fd28ea4064`  
		Last Modified: Wed, 13 Aug 2025 03:14:49 GMT  
		Size: 24.0 MB (24020172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afd6f1f2a58fa1289478b7c4157102354638b354f847958c5d7c5b4449c508e`  
		Last Modified: Wed, 13 Aug 2025 08:03:43 GMT  
		Size: 63.5 MB (63497769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46ddef82679eb8cfd4c812771b109c61028186c876518a5ed5996cecaff887f`  
		Last Modified: Fri, 22 Aug 2025 17:37:49 GMT  
		Size: 69.0 MB (68975042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a816d9df67a6c8d2ec0bec0727b10be162fd4c8589e6c1ca985eaeac4418533`  
		Last Modified: Fri, 22 Aug 2025 17:37:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:00028900c48eda7419612022e2202e97decfd79f2cadb671699ea17ba97aaa7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d4fc8095e8b801c51edd6d011642a2fe9b3484609070f20668390f0a2d2eca`

```dockerfile
```

-	Layers:
	-	`sha256:9ab53845e7119f9865c1b7afe75f129dea0c6e393f876ef7f71adad1da0ad537`  
		Last Modified: Fri, 22 Aug 2025 20:23:49 GMT  
		Size: 10.3 MB (10320725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80444b23f0e76d8f7ffe9c4e939d1f2b2b5da3f174d75ef7d14c5998ebc0d910`  
		Last Modified: Fri, 22 Aug 2025 20:23:50 GMT  
		Size: 27.8 KB (27840 bytes)  
		MIME: application/vnd.in-toto+json
