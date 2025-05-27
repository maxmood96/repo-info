## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:711548e6463d75c92dededcf4ed02f3cda459c8fa574c893e88fff6867bb93f3
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

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:d300845f8af1612bf73cc65be7d50ee1b34a198fde24158ce9ad6e37ded0e0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.5 MB (355499811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bee35a9106dced5cc59a237c2a37d2070e1d0b3be7eab84f8e95230f513e5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Wed, 21 May 2025 23:20:21 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Wed, 21 May 2025 23:37:25 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7a1c3042302c77450d34f145eae06f14da15d5a8036c0d3227545a19bf8ebd`  
		Last Modified: Tue, 27 May 2025 19:04:55 GMT  
		Size: 92.4 MB (92354997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37739a11166de3eef493c06e2f945d1e527fcbc7b45049a9bf54b5049c44176`  
		Last Modified: Tue, 27 May 2025 19:04:56 GMT  
		Size: 126.2 MB (126240918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ff815c2fbf6cee756517c29552552a37c00f311edcddd8f2460a3a5d6b6ab6`  
		Last Modified: Tue, 27 May 2025 19:04:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c90979b1afe638292a347bb1edda8058f85f83d40fa6c8bee0706b55ff70de2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10340783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecad25a115009006a5a3e73dc9932500d2c4a87867eff43772473dfd03685c5b`

```dockerfile
```

-	Layers:
	-	`sha256:34d73f848fd62303f1e70af178f1fbb381cf6cca3380810764cb15eac1485656`  
		Last Modified: Tue, 27 May 2025 19:04:54 GMT  
		Size: 10.3 MB (10313121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a1a81e6fba132a15d8c3937815de45f4a1348bb239c667160da0fd7fdb8772`  
		Last Modified: Tue, 27 May 2025 19:04:54 GMT  
		Size: 27.7 KB (27662 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:2f9dc801ea8555e44b8543e6e8db9152ebe5e7accea5920b2c14a9324a45b6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313103271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff391acce732f5758f073d406f14d3a34e99f89d95b1f46ed9629eab793d4b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Wed, 21 May 2025 22:27:37 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Thu, 22 May 2025 02:28:04 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Thu, 22 May 2025 12:11:29 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6769ccbcbb302e58183ef7d1b1458e5ec9e4e0e712cf266d56ddefb34341bfd`  
		Last Modified: Thu, 22 May 2025 15:40:09 GMT  
		Size: 66.2 MB (66210504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d0fe5e7d3d09e12944b416a2054aa6712ade9bdcb8b3878cad2dddeefd549a`  
		Last Modified: Tue, 27 May 2025 19:07:16 GMT  
		Size: 121.1 MB (121108917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772f59ed354862d2360a07591ce55b9cb4f75f6fef9bc9aaee169f0b43539bc9`  
		Last Modified: Tue, 27 May 2025 19:07:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1e6841a057a49173a6e3c46de0cf0e3b689af018224230cc65a2c936cef119c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10147593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88164cfbb0df2b41db7280957ff2484a4fa85bc410742c237d4d9cfb9c1e540c`

```dockerfile
```

-	Layers:
	-	`sha256:ae3f92edd4d1296e8ff05c7466e5ade35ab70e6b17466137f6253674e3b13bc4`  
		Last Modified: Tue, 27 May 2025 19:07:13 GMT  
		Size: 10.1 MB (10119806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef0f6bc88ed455755f377bac045c0bb9bdf4f99004cfb4bed3e30713b2b2f38`  
		Last Modified: Tue, 27 May 2025 19:07:13 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:132248814fecc8ae4eebb1cd79e94d2504d77b6b58c50fdeee57b0fc67fbf866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341704121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cabdcc853fbf80ec8ef97da8b5e7689a22bc4c5d4df90884ebdf90c85415d17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Thu, 22 May 2025 02:47:26 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Thu, 22 May 2025 09:17:58 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e45158653cee17fd0433bb95f654076603c1dace770784457d1f08ffc1f1bd`  
		Last Modified: Thu, 22 May 2025 12:32:49 GMT  
		Size: 86.4 MB (86409121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea33ecb4b895f73f5e4d5736d5a0a4109e5ac27823a9c5ca57f0642e5a3d9a8b`  
		Last Modified: Tue, 27 May 2025 19:23:28 GMT  
		Size: 119.1 MB (119054274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7895b6f91029ed8638c2fc7d6e593355cd05e215e03f13cee6042817879a666e`  
		Last Modified: Tue, 27 May 2025 19:23:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a5a1e4be6b7b88a6666aefb75205f2e7b4468ba10f308414c025f68899801095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10368791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2558fcb29759fd4fedeba83be19c138686b96f43a68c8d07b22c9c34350a9c61`

```dockerfile
```

-	Layers:
	-	`sha256:00543fefd9ca5067bbe80016c8f07d5535a1b44d3d3e479a3c329fd44ac84091`  
		Last Modified: Tue, 27 May 2025 19:23:25 GMT  
		Size: 10.3 MB (10340968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe5545eacb7a4cf012e33c81f635ea848709fdbbbd360142bbb357c94e88f39`  
		Last Modified: Tue, 27 May 2025 19:23:24 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:64dc76b692deb0e09f0778b75c19e78da39e900ebca3dbba63b8e5f7978a0517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.5 MB (354532931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbb173eb14d3c91f51317326717251d758c543e611b306f28ee1332a152b3eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Wed, 21 May 2025 23:20:06 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Wed, 21 May 2025 23:37:30 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead1d26d6dc62e8204156afac23052644c38e3fa8d22ad82ac6449e72810d4d9`  
		Last Modified: Tue, 27 May 2025 19:05:47 GMT  
		Size: 89.8 MB (89774250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb63d3af1099d61647a313155e9eaa0aeecda078cbf5fcab7fb7996b234e196d`  
		Last Modified: Tue, 27 May 2025 19:05:30 GMT  
		Size: 124.2 MB (124207178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e221cf0102d64e9cc6146f2df0ca7beba7c73744032c51f113edb86aa5f06127`  
		Last Modified: Tue, 27 May 2025 19:05:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e9ec4961f4c518d7b4ff5ab99bd477ba2c4fd4d5412a40970775b05d6a9d5ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10320295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfb702ee71e95430b86455ca0c8abd7f4ca187a3194ee9cfe3cbbd939689343`

```dockerfile
```

-	Layers:
	-	`sha256:8d668acaa12093ae62e64d046ec8ad1d60b5c018dfe3462bb910322652dc01ac`  
		Last Modified: Tue, 27 May 2025 19:05:45 GMT  
		Size: 10.3 MB (10292675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a92d324a60fb518049c6c03e1ff36978ef12e9b43aed1623b3213017cc148f04`  
		Last Modified: Tue, 27 May 2025 19:05:45 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:0d5036865752ab5c94e1ad7dfeffc6ec5ca846291e2b78d43015823a08710d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322248152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eac1f00640ccf6e21e88e21fe5e733e06865949c0f3e92c6b87b07f9922a4e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc05e2d1c7537a7663041b66446ee4a24f98e673290839931cdaf3c0b93f56`  
		Last Modified: Thu, 22 May 2025 06:16:24 GMT  
		Size: 23.6 MB (23598613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fef5bce771d4c7090ec3bddacaa83a3ac07da89649b62764c8f0bb14e3e0ed`  
		Last Modified: Thu, 22 May 2025 14:29:03 GMT  
		Size: 63.3 MB (63308472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4ece845a4d4a4ec28b24cc19384f49afd8d3bee80380c09f3a36d476d34fc`  
		Last Modified: Fri, 23 May 2025 05:00:06 GMT  
		Size: 70.0 MB (69950183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c730bd20531d61e28921f7ed43a499a973c3ae313ad77cc27080f714a04e49a`  
		Last Modified: Tue, 27 May 2025 19:27:52 GMT  
		Size: 116.6 MB (116620973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb895bb8376d4de5bf2f131692a54d9c76a07775f85f1a5264ba55a340f7f30`  
		Last Modified: Tue, 27 May 2025 19:27:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:11a022ac518274e6a2ae92bfcec89984dfe130018f54483b39253c92749371c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a314e285e664f618ecac1c9771c86c7b7654f2d381fc1e273678012dfa05105`

```dockerfile
```

-	Layers:
	-	`sha256:6b215f3e4f93e22d7be771c680de216e6029e41d9898bf24262c90418871b764`  
		Last Modified: Tue, 27 May 2025 19:27:41 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:3cce11a4dc7d74f71a9013f630a3d94fbe9bbde046b8e39bf667a37688fcf960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.3 MB (359348891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bd209ff32a4309f680e3c5a6a5100a8592183f8848868799a2c2b5ddff0c4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Thu, 22 May 2025 11:54:40 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Thu, 22 May 2025 16:52:03 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3651009f91cf27e970ae7dc7349e20fba94b97f4d2143617e748afd3d930d`  
		Last Modified: Thu, 22 May 2025 17:40:50 GMT  
		Size: 90.4 MB (90354720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4275b8143ff44473029dc987922dbd1dd91e814dab86dd3c175ed73d2ef81d1c`  
		Last Modified: Tue, 27 May 2025 19:06:55 GMT  
		Size: 121.2 MB (121165419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cac817c0f48d3e86d523713a421318550ee262578232a0e71155f343b44f074`  
		Last Modified: Tue, 27 May 2025 19:06:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f73cdc9392ff07ecb1e9d17dc2fbb6f9a7a758c9be56f4130008fb9fa1274f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10313346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e320b55db84c0da619e49514914b8845cda0826de75a573e41f3c38df3ceebaf`

```dockerfile
```

-	Layers:
	-	`sha256:6de4eb403ca2ff3c773f61f21a0768290de059f29ce501d9fade8d6d598368a1`  
		Last Modified: Tue, 27 May 2025 19:06:51 GMT  
		Size: 10.3 MB (10285625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0dc109e9dd08d71e2385c7d85029bda3d5fcd98f99b8aaa033c4266088c7ed`  
		Last Modified: Tue, 27 May 2025 19:06:50 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:6616c8094c2bbac45cd8fcc0b06ac919c43b719885c70a9fff8ec23b2df95252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327063617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0baa3578d10239dcab4591b98c569435802fc82f2fadf0e9edf61cc0dc6e74a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 05:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 May 2025 05:23:21 GMT
ENV GOPATH=/go
# Mon, 26 May 2025 05:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 05:23:21 GMT
COPY /target/ / # buildkit
# Mon, 26 May 2025 05:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 May 2025 05:23:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Thu, 22 May 2025 01:01:58 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Thu, 22 May 2025 04:37:16 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd113c317127acbfc86d7af2a1be3cb7e330fa8c58847cef98b51c46d4e19c94`  
		Last Modified: Thu, 22 May 2025 06:45:25 GMT  
		Size: 68.9 MB (68943692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a53d6c9d36291056f30ae15703f561e0a8333bad5f15ea579763f74d2b6616b`  
		Last Modified: Tue, 27 May 2025 19:05:45 GMT  
		Size: 123.5 MB (123462542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e112008f68effc6f567e48d21b95a10ba5c6229b9e1e746398deb00915a8db`  
		Last Modified: Tue, 27 May 2025 19:05:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:808d12c7c9a65b7c279de44d185b22b42c09e1e5a52b2879fd997c34285812fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10175433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f55439a599f6dc7e5328a0deb0f7004697d6f48d30fca3d45237514e7686e8`

```dockerfile
```

-	Layers:
	-	`sha256:06bec8d68f70425dbc1edc30903d85396b666e46db0d7ad6300a02026488e957`  
		Last Modified: Tue, 27 May 2025 19:05:39 GMT  
		Size: 10.1 MB (10147772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08dd31dcc11b2639d8daf099a1d9159318805da4a66b9516c43b2dc98549fae8`  
		Last Modified: Tue, 27 May 2025 19:05:39 GMT  
		Size: 27.7 KB (27661 bytes)  
		MIME: application/vnd.in-toto+json
