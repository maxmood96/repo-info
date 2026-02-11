## `golang:tip-20260207-bookworm`

```console
$ docker pull golang@sha256:b2c239c86b0d5f7e317242a0973fa75e4a712242ee859ee1dae09278653f4d9c
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

### `golang:tip-20260207-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:09432072e230fd87d9cb294f3187d1833594644827831d3ab0f9fff13f0783d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322822947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bbe126e526073759a03df14e48bf1d6204470637203d0f3faf14375572d7f57`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:48:44 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:48:44 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:48:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:48:44 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:48:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:48:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4864e6b451b67f6fa795c73d5037482a24c551508239982daabf256a0ecae37`  
		Last Modified: Tue, 10 Feb 2026 21:49:13 GMT  
		Size: 92.4 MB (92444872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac0d50002cbee1e950896b157d609a44688d9a2715460c4e3c92d9a126868`  
		Last Modified: Mon, 09 Feb 2026 20:03:44 GMT  
		Size: 93.5 MB (93462017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3589c27dc9352ab6cc9138c27d608221906c5e7252a5d3dc17f5ef802bed4d59`  
		Last Modified: Tue, 10 Feb 2026 21:49:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:dab97815bbbc1fb8fd103a43df5610aee756fce18ea35f07913007a7f5694dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd1a8d276e8ba67748e730416ef2440f53e5d353302a228b81e162fc4f190ec`

```dockerfile
```

-	Layers:
	-	`sha256:153aaf8801f36c8b1bc6f82c9b5b6fd9699716a26d2920626642a16edce6ac11`  
		Last Modified: Tue, 10 Feb 2026 21:49:10 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d0d5d0853cb31e7892945a560f9f04d1036ddc112dfa7aef11b4e5dcc9ce9f`  
		Last Modified: Tue, 10 Feb 2026 21:49:10 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:3a14250a5bbfe24faf256088bd7984c82e6fe317b52b3c03c6bee06be0ce1298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.7 MB (281686947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a64a68fff24e06261a676b76c120b2f91f22d12d2f994bc370266f78322eed6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:46:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:49:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:49:26 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:49:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:49:26 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:49:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:49:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb0551578bad740c3a20b6a29166ce3ad8980e037c23d30c90a060f62da5338`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 59.7 MB (59651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485addc00e31bacfa8199091d72d75595e52701dab642db2f0959b6c83db9473`  
		Last Modified: Tue, 10 Feb 2026 21:49:53 GMT  
		Size: 66.3 MB (66310378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60c394ecd04fc3ba572f8a2c09a22e7e8c913f51a7766b230d8afa0ed0ae01`  
		Last Modified: Mon, 09 Feb 2026 19:59:07 GMT  
		Size: 89.6 MB (89583671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2bb58aaea47819d8c5c646037a1b5a7d7c239e1a9705c89b97d5cff023586`  
		Last Modified: Tue, 10 Feb 2026 21:49:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:58e527acf62f32d4156eeeac428c828aa157f0793377852fcc8ab9ef7b662ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0ef266a2587f93c2ac6ebddd3d89f2898df139de2d2d1944b89f03b490ea31`

```dockerfile
```

-	Layers:
	-	`sha256:9f8a2ca0d73a79be56c0a422b8b70a36857004742ccdcbc8ef5a61864997c1f4`  
		Last Modified: Tue, 10 Feb 2026 21:49:52 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d7dca84d707c7eec39b45ec1afa878e4d1feef31f72728eeef7642928c9ccd7`  
		Last Modified: Tue, 10 Feb 2026 21:49:51 GMT  
		Size: 28.5 KB (28497 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:34e9df344da599b0c0640f514b970e91494bbbb9a1c03b3c01daaa55efcc19b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311450032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b197a86b1252fc47f9c70b24cb9bcd39a99e33b6cf5fc8ec423429e6a61511cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:46:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:48:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:48:28 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:48:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:48:28 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:48:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:48:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a479e2861e732cd21c824eb5bb72684043f4b153e8e017c88b82ba6c51682a`  
		Last Modified: Tue, 10 Feb 2026 21:48:56 GMT  
		Size: 86.5 MB (86525269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700ae6b9569c22fdb680312e3253454dffff750989d3faaa4cebeb6c55de9593`  
		Last Modified: Mon, 09 Feb 2026 20:03:10 GMT  
		Size: 88.5 MB (88474120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc5a15d5fa68eca1d09fb14d75e0d320418c5f3c3c6ebed10865db369f67f72`  
		Last Modified: Tue, 10 Feb 2026 21:48:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f05fe6a896433ebfeab2af73b2179ca8d707d0e334815908a2f40e868bc9d94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e82fc718bbde968229edb95bc7eb94a5c69694ead5e8582673af8f8eb4b9f35`

```dockerfile
```

-	Layers:
	-	`sha256:3bb0e798a9c7afbf74921714f5cec8aa4abc3179849d6e65a542fc2625270ac2`  
		Last Modified: Tue, 10 Feb 2026 21:48:54 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362eb75e9156e290a8198dca485e15f53addf238597c87d46e9d21831b20a843`  
		Last Modified: Tue, 10 Feb 2026 21:48:54 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; 386

```console
$ docker pull golang@sha256:fd3f2b50083552ec1d0b63551ca05fe6c4f818f719ac1f9beb7e437c33f43171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321966069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899aefaae94bff04b470c8cbe83f1ce512dce89c96a0bdaa4fca86452a0298c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:47:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Feb 2026 21:49:36 GMT
ENV GOTOOLCHAIN=local
# Tue, 10 Feb 2026 21:49:36 GMT
ENV GOPATH=/go
# Tue, 10 Feb 2026 21:49:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 21:49:36 GMT
COPY /target/ / # buildkit
# Tue, 10 Feb 2026 21:49:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 10 Feb 2026 21:49:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50ea552b26a58c13b4166d933269500891fb4897db09bc72d932372276b158f`  
		Last Modified: Tue, 03 Feb 2026 02:49:31 GMT  
		Size: 24.9 MB (24872100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc15e0cd687cd62190081200fbe30ab5102ae840cc68b0386259c387aef2b9a`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 66.2 MB (66234564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc790d317ce4176762a97b42535aaef4714d1a127542e417f587f1288392454`  
		Last Modified: Tue, 10 Feb 2026 21:50:03 GMT  
		Size: 89.9 MB (89871544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9eeab623b500684be7941586d4f5950cd5be2f0139f940b2104a8b3b5d40cc`  
		Last Modified: Mon, 09 Feb 2026 19:58:40 GMT  
		Size: 91.5 MB (91519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642c1ba5629fceac128fef544ef143d88cf7cb68b612368ce0ec29d83452e7f6`  
		Last Modified: Tue, 10 Feb 2026 21:50:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:32b4f554c6333f8c38687d7b8fe19f409555137a132fbca4e4475cf04610bc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08a12cd503df0b1f1cb71979468db3e9a0618b5bec9c63fd4ff7647e2a8f4c0`

```dockerfile
```

-	Layers:
	-	`sha256:4debaaa654115aa38f492e8f6e5825e74e74fbd825e2d4f25d34a4d0c32217d1`  
		Last Modified: Tue, 10 Feb 2026 21:50:01 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deab71d1f54ebb09094ae8b140ce38c0e38ba7755c451f7f39c10212e496cd6a`  
		Last Modified: Tue, 10 Feb 2026 21:50:01 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:1044fd9ed6eab5dd507580c170988dd1f4ab9280374e8dc15b9b673e63141764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (292984683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9070f918e317c6ab1b0db26dbdd191dfff28c5602f59dbe369a52ef45460cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 21:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 22:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:20:30 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:20:30 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:20:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:20:30 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:20:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:20:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0ad746711a3754afd4dc1df1be9308a858da3b48f46cc1d318cd1dbf2cb47`  
		Last Modified: Tue, 03 Feb 2026 21:29:58 GMT  
		Size: 63.3 MB (63310108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164c80380b0dcd60ea92fbd5645d9478bdfb6a0b5dfaabf0daa2a974ecfb949`  
		Last Modified: Tue, 03 Feb 2026 22:20:18 GMT  
		Size: 70.0 MB (70021714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2941bc26ecd1a5504138788ecec8521b1cfe7a3f3f863ffffca2809c5df941`  
		Last Modified: Mon, 09 Feb 2026 20:22:42 GMT  
		Size: 87.3 MB (87274048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d861435e1d0a2c911db9037d5c879172be967a1e656857f44071e410e4e4690f`  
		Last Modified: Mon, 09 Feb 2026 20:22:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2612fcd483864f80b29091fb985e4f612191f9c30ec5b33cae446513ca7af589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c363aed16c2d9b8985bc9868c2a8de1aa4cb2610a78e7f4ab3658f3efa72909c`

```dockerfile
```

-	Layers:
	-	`sha256:89440ebce8afd64c886a7d1c098663f60b686ec07d7799b32d89f1ec0ea01f0f`  
		Last Modified: Tue, 10 Feb 2026 22:08:17 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:2a6ea5d3a9d978fd327535f5ae12a703fa2f6a3b59e3157b62e4f23d90dc3c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328402975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b9eb44869e3f3f7f9e2704caa11204a2dc3c37302f8984c1b041ee4bfb2cc1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 10:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:26:29 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:26:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:26:29 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:27:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:27:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1311f6670d65067c1adb8d518ab8836a9d3d42058afdd776824845f91935c9`  
		Last Modified: Tue, 03 Feb 2026 05:22:25 GMT  
		Size: 25.7 MB (25671343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c21a9818f8ca2f73ccd29b595b5a2bc7818b3057c3895ec555bee901eb365`  
		Last Modified: Tue, 03 Feb 2026 10:36:21 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bf9d9076f39b8e2c0aced7f1f28dac543d58a8aafe215df11bf80a17810efe`  
		Last Modified: Mon, 09 Feb 2026 20:28:08 GMT  
		Size: 90.5 MB (90451427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f34b281626db46d13e5a751b54221f74b1d0be2bfad3701f6dc696782f8809`  
		Last Modified: Mon, 09 Feb 2026 20:28:07 GMT  
		Size: 90.1 MB (90106742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cfadcf20d903a47d690dfd9f21897f8f86a35c7a28fbf8fd9c48103eaf27c`  
		Last Modified: Mon, 09 Feb 2026 20:28:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:fe0ed98f0e5e71e979e44fb383f5fb651eafdc786ad38840869f60693e868636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236e4f0232f4ed0b039100a60bd3e185614e3b41d96c31cc13e1a902ea777752`

```dockerfile
```

-	Layers:
	-	`sha256:88f5516b26b8b9b3e75632b6e82ee7bb74f3e49036d8ce308a8390c6bd806f9c`  
		Last Modified: Tue, 10 Feb 2026 21:49:34 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7f4ef8cc6af9b89e997025533a22ac4a7175c21b31365338416a7b8d7bf472`  
		Last Modified: Tue, 10 Feb 2026 21:49:34 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260207-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:595944b2fd926ef8980856b6c7b76617bb1c26aa003a732bc2d85a5cb866da3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296367507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f75bdb0d6fe63fc542f56ec353f8b7c7f719a8ae42cefba819b7ed766e859e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:00:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:00:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Feb 2026 20:00:01 GMT
ENV GOPATH=/go
# Mon, 09 Feb 2026 20:00:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 20:00:01 GMT
COPY /target/ / # buildkit
# Mon, 09 Feb 2026 20:00:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Feb 2026 20:00:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be60f9687e53e1d931599c2c97d67403bb6a6a87fba5a8672d8f14c72b51e5e`  
		Last Modified: Mon, 09 Feb 2026 20:00:52 GMT  
		Size: 69.0 MB (69045163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9ec9ce8a3837e5750bcd10b11df694113758518fac79cbd3aa70f831f2db7`  
		Last Modified: Mon, 09 Feb 2026 20:00:45 GMT  
		Size: 92.6 MB (92648889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79fc8e988c972d4fb98e4774410a8e4d457ae2f49d884af58cf3ec6766758c5`  
		Last Modified: Mon, 09 Feb 2026 20:00:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260207-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e03412f165e5d8c17190e80b76095fd4553d2ae0b87f6c285a86bb2a8bf7755f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db158bffbe1f2d589dc559ee114f44ba1bd188865891288a7042ff2b942e8a7a`

```dockerfile
```

-	Layers:
	-	`sha256:80534d21f2eebc3b665d9462278b2e7f7e97a86efaef021d55105b3f9d817e7b`  
		Last Modified: Tue, 10 Feb 2026 21:50:18 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9056ac21585ff1196d9445dc1e631fcbf0aeda1d191b27cc7bfd044bb8c3db`  
		Last Modified: Tue, 10 Feb 2026 21:50:18 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
