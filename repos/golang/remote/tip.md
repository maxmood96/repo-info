## `golang:tip`

```console
$ docker pull golang@sha256:d197f728974a70e67fd633a1f035ee634e64f546fa0c0ac533b77922c3a4d35d
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:b26070188345f40b172eb3a577fe6db8d112fecdaed6864975a493ffb09ad5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355265788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19072a106bfa092ef8dae6cbfdfb973b095a1ef577d44bf9710d0ff75564c7d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255774e0027b72d2327719e78dbad5ad8c9cf446d055e45be7fc149418470bae`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 64.4 MB (64396484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cc2f07f2614dfb7d2502118880e24f6a5e27de8174d0f74280003ab6dc6849`  
		Last Modified: Tue, 01 Apr 2025 17:13:49 GMT  
		Size: 92.3 MB (92333163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdcf0ac50c31370559153f24cee269e765f93f7d9caa55e2923550ee66d79`  
		Last Modified: Mon, 31 Mar 2025 17:35:08 GMT  
		Size: 126.1 MB (126057009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85e364b62035165b6256d5599510e0b753513d567de74e7caa6ca4128867460`  
		Last Modified: Tue, 01 Apr 2025 17:13:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:808ad83bb3f411d1b5e089f21a15a6031c3d094e75610a36748cddd7f3bfa59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aea24eaecd2d5e94da5c4d70b765f530c77da26f08bf4ac8302ebc9265b145`

```dockerfile
```

-	Layers:
	-	`sha256:e74caf28442f8b63f766432e21b34e983acb1fa1fe06529f068656bca9432e4f`  
		Last Modified: Tue, 01 Apr 2025 17:13:47 GMT  
		Size: 10.3 MB (10270530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe10c4152d1467a37fe7cbce32ed269d2cc5cff77501b551791beca3968ea16`  
		Last Modified: Tue, 01 Apr 2025 17:13:47 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:fb37ae035e34febc964532904600a378a84fa2ad93fd06aca3df21f10e385ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312923690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4251111467eb132f1b49c0bc242114bd8ff9aac72979bcf08079595fc63648`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e54aae01c229d841c2a283cd0dc10f5715734525136c6155468d1b2a9ab68292`  
		Last Modified: Mon, 17 Mar 2025 22:57:31 GMT  
		Size: 44.2 MB (44178003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a319072ea86a8c9aa06075cbf6677da28654a48a38fc6adb52aa04f271ddd06`  
		Last Modified: Tue, 18 Mar 2025 07:30:13 GMT  
		Size: 21.9 MB (21918018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f325c93a6cb0439e3bf485f3a1ca5c31cca2f6b205d5c37e15890e18b5fe0`  
		Last Modified: Tue, 18 Mar 2025 15:26:53 GMT  
		Size: 59.6 MB (59639263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00519b34344176105ca045ed023ebae6a0a5c6298dc42892bd398946022f439c`  
		Last Modified: Tue, 18 Mar 2025 16:42:48 GMT  
		Size: 66.2 MB (66197750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df465922d4d37689f205f8db79322885e1b2a4fcb76bc9411e873e87dc4d228`  
		Last Modified: Mon, 31 Mar 2025 19:49:55 GMT  
		Size: 121.0 MB (120990498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b9c31300a004f894ef6f65f7ae7ee8fdd48b4144de201e4a1557beb86bbbf0`  
		Last Modified: Mon, 31 Mar 2025 19:49:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:470744ee173e705deedf7c52ff394704598f38926a8f98d5809d41d689427943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10106639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9db540cd740e0e93c06800ff6d20ac7ae20b0704d5aaca74c55ceaf7b29f0e`

```dockerfile
```

-	Layers:
	-	`sha256:04bba9ddcb247aaa531b90175645c865dc2cb1570f3fb5d5be5be8dac7c13bd1`  
		Last Modified: Tue, 01 Apr 2025 17:17:23 GMT  
		Size: 10.1 MB (10078852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb974e6f4d94352df510d4537c32f89ffe71a8e457dbd2ea278bd203367f50af`  
		Last Modified: Tue, 01 Apr 2025 17:17:23 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8284c832db68f5bbac3ddd5af388d14f97cb8605d00d09683d8e9afd0d7252eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341206916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3bf9a18382808e331fedc35fd3c2a8f9a41ea2788bf2c2351ca70630008026`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378a6c11dea5043896b9425853a850807e5845b0018fe01ddee56c16245fc3c`  
		Last Modified: Tue, 18 Mar 2025 05:00:37 GMT  
		Size: 23.5 MB (23544349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140d15be2fea6dcd21c20cadae2601a118c08a938168718b2612ad6aca91f74a`  
		Last Modified: Tue, 18 Mar 2025 13:13:07 GMT  
		Size: 64.4 MB (64355791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c7d0b299d26ce0f065a1fac5d6ad12aaa605ef18f04114a5b9e048f7d59782`  
		Last Modified: Tue, 18 Mar 2025 14:43:52 GMT  
		Size: 86.4 MB (86397409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15331666df650886c34693df6448a24027e3a0aedd81057f599d0c56087566f5`  
		Last Modified: Mon, 31 Mar 2025 17:54:53 GMT  
		Size: 118.6 MB (118604354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38ba234a6e4f7332e1fb15695015092c7d832f366757796e91bb09542dd5ff9`  
		Last Modified: Mon, 31 Mar 2025 17:54:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:2c6ea3d4da2a6823e664f73d461caa31b777fd787aaa3daf605569f79ca3ec2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bbad9314ac2bb762ac847a1c63bb5898918174285bb10139aa34c19a10ce5b`

```dockerfile
```

-	Layers:
	-	`sha256:c2ce0e9b37b0627e19fd190f4df5f00f74503bd65214e026346ec4990911b28a`  
		Last Modified: Tue, 01 Apr 2025 17:13:56 GMT  
		Size: 10.3 MB (10298377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e7f2f1d38131072aa84afd015cad7d79cd824631a40f172106f75c916509c36`  
		Last Modified: Tue, 01 Apr 2025 17:13:55 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:14fe380ba538bc2d85a7c952806f8a137f9cbbd487871fb4d01af76c981c34eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.4 MB (354438677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d4ec8cda5866138ff4e33b299307fb208fd6d827cfa0d4a379e58c4a81e67f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f093c698fbf9398dcc78e7920fa6ac4ed36d36e94641983077879670b120bc41`  
		Last Modified: Tue, 01 Apr 2025 17:14:28 GMT  
		Size: 89.8 MB (89753162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20357d85d18b3e3e63dc269591697947f7bf020ba7021f1f8a7b1b769a804fe`  
		Last Modified: Mon, 31 Mar 2025 17:36:49 GMT  
		Size: 124.1 MB (124146637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5208d847834a5fca3a1d5b045d4dbe3af8f9a0ee1ed5913f5a39b70c237484da`  
		Last Modified: Tue, 01 Apr 2025 17:14:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:e81049cf38b8db2e65a532b49c6a22fc8a11d060c23ffc0928b023abea7f8ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10278224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18016c4c853c3657da5680d0406204251853e0ccbc8d407ef745eeba52b6512`

```dockerfile
```

-	Layers:
	-	`sha256:2c3e1c72b6372321326cdaa4266eeb2c69f12718f93ee5d9fcae6ab44b10bfb4`  
		Last Modified: Tue, 01 Apr 2025 17:14:26 GMT  
		Size: 10.3 MB (10250604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:589b19941d82c72ac95923c84cb981bca013d44bef055305caa89d6c56beb3ba`  
		Last Modified: Tue, 01 Apr 2025 17:14:25 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:ccc933174cdda314a79f8e6242fb059e6d52ba43c0202fe5c101c0e37f75be42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321970196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e65c4d8e5be13eee5f4126a01874b026a6543534a26bde069fd3a2dc68da6d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:579ff6a9178b7f862c70c40b253d6f0090e7792eed3ce083de0732adfc5f4826`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 48.8 MB (48756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19bfe112f8e8e887df88219c2ac69098bcc8afda18a25b53168674379a8365`  
		Last Modified: Tue, 18 Mar 2025 16:33:21 GMT  
		Size: 23.6 MB (23595590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0a4688093ff24a7c0a47c52d04ce08c1411187824a95dc1fb509b4ab01c8c4`  
		Last Modified: Wed, 19 Mar 2025 05:02:22 GMT  
		Size: 63.3 MB (63308534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2231f6ba5c37aa271ccac7a0771657978751e91d524c076449ab434853b6fbd6`  
		Last Modified: Wed, 19 Mar 2025 09:15:32 GMT  
		Size: 69.9 MB (69916047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eca2bf1f658783f3e1ed954d751625ce22ae1e523192bdf96be61cf245ae0c`  
		Last Modified: Mon, 31 Mar 2025 17:53:42 GMT  
		Size: 116.4 MB (116393696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299bb7cbf8c87bff21ddcca1841b54af927b648a424788cdc99633ed260063d2`  
		Last Modified: Mon, 31 Mar 2025 17:53:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f6806190e92dc6b8cdeb66a485554877ccbb293bc8da3f1f5ed3e43a6adc6799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b427931baada9bc5a00239f727f4bef0643361efd8898b40a1e77136eac281`

```dockerfile
```

-	Layers:
	-	`sha256:133b775254962fb9e91746eada73b12f9249f380e18ab6f4b540cbc5aecdedc5`  
		Last Modified: Tue, 01 Apr 2025 17:34:53 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:f86f6315c26a1e9548b780b2473c608784ce6abf27f1655b0d8504770553fc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359040319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1cf6521c43c621653da8009f1b951b7e7fae013dfc254656faad3ec0b6c316`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c3d0039c25f88e5b7c3da861e5a41bc617f045eff9521b410ceced36c47c971`  
		Last Modified: Mon, 17 Mar 2025 22:17:38 GMT  
		Size: 52.3 MB (52306033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b570e1ccee8c153bcd6622cbc7c9c8f1150932eca72b58d0e1d93a81c2d4b`  
		Last Modified: Tue, 18 Mar 2025 00:06:46 GMT  
		Size: 25.7 MB (25650089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3219f8cada3f1c641a91887b1112d0699cc708ea02d9c8f85a77e08659008bf`  
		Last Modified: Tue, 18 Mar 2025 07:04:49 GMT  
		Size: 69.8 MB (69844086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d300aacbc73f5f66a38fd8a02deb1a013bd64c099f17f3efe76c226cb8443355`  
		Last Modified: Mon, 24 Mar 2025 21:44:57 GMT  
		Size: 90.3 MB (90334664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22730901dc3a920565010f112cf1fbaf34e7ad303fd15179e51589258f9c3f8c`  
		Last Modified: Mon, 31 Mar 2025 19:23:49 GMT  
		Size: 120.9 MB (120905289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b68515d7dd683b949386ef35ccb6fe2ea81c69a3b5b146ea95a09da0f2c139e`  
		Last Modified: Mon, 31 Mar 2025 19:23:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:c76e046b9237b721d228d4e332f2d4a1a5389703ca737110fa995d7b8eb01cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10270944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26d946f606607b755710b1aa9834ab3462293583c1a06ad36d1e1f57544f85c`

```dockerfile
```

-	Layers:
	-	`sha256:3fc370309afbd222f462609328f0b559db13c97067a732ffc8efa252483c28d4`  
		Last Modified: Tue, 01 Apr 2025 17:17:20 GMT  
		Size: 10.2 MB (10243223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e84d013ba6bc3b2322ae5d8e95bdd3a5ded41fea1bc7b1a41db19dea6784972`  
		Last Modified: Tue, 01 Apr 2025 17:17:19 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:c6c32951475b4fe9c3252d51f4dc0aee0c875c4b66d0281aefd7ee70db7e88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326893992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a896098f45d9b088dacca7efe9956d8bc86809c9433b01dc47f90e8a48a20af6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 31 Mar 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 31 Mar 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 31 Mar 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 31 Mar 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ea48981a9fc9115877d4666b28ace59b31b650cc30850dc9dbcd586ba0a496cb`  
		Last Modified: Mon, 17 Mar 2025 22:26:07 GMT  
		Size: 47.1 MB (47127836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d2fcabaa2191a259a1c138c1eae49463f7916a91e0b0f61fdbaa5dba7f4e2`  
		Last Modified: Tue, 18 Mar 2025 02:53:59 GMT  
		Size: 24.0 MB (24007981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4163fc9bb4b1cfe20bf3ee0f067c3cb219407f1ed0b91eb04a5759f702712`  
		Last Modified: Tue, 18 Mar 2025 05:55:51 GMT  
		Size: 63.5 MB (63498480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319b90f4963e2742395335d2bc5e908f7c9081649b808703a7348aa8213d7b75`  
		Last Modified: Mon, 24 Mar 2025 21:23:36 GMT  
		Size: 68.9 MB (68922898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9fd359663b603237a3ae91c837b8d5c159e2e6258d720d7dd1b12433408ceb`  
		Last Modified: Mon, 31 Mar 2025 19:12:01 GMT  
		Size: 123.3 MB (123336639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375ffbe653368b3e76d8132b9c778bc64924dc2f7a3b2c1a77675c17382b8856`  
		Last Modified: Mon, 31 Mar 2025 19:11:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:d74d81362137bedbbc46a80d2a6e671494ce1ba5d4294716b3431315f1f80655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10134173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70df1d0bf91e320cea413f932cdd060c4bf4abbe6671f0c705bb022665dc7c3f`

```dockerfile
```

-	Layers:
	-	`sha256:a561faa932ea34f4c29566f4aea715d513001f5fff07fed08422c57b0f760b4d`  
		Last Modified: Tue, 01 Apr 2025 17:15:54 GMT  
		Size: 10.1 MB (10106510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d79c1961201541df7f5f1931e3bc23240b583a7a45ea1995a2b9cf8d90bbc7`  
		Last Modified: Tue, 01 Apr 2025 17:15:54 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
