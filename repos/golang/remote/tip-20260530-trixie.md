## `golang:tip-20260530-trixie`

```console
$ docker pull golang@sha256:a363e5bfa3c9705f4826648dde494227c8796a871906c4ece4be6c1fc0ee57c5
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260530-trixie` - linux; amd64

```console
$ docker pull golang@sha256:193b99c537bb44ac18cbf14a7e4311280ad7075f1c29020eb395ddef2921eded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.0 MB (346960842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab3d99a27f5eea1bb6aeaecbb4a8ffa50bec537874186d53eeb06bb69fbbc1e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 22:10:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:12:43 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 22:12:43 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 22:12:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:12:43 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 22:12:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 22:12:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb24a28f87f3e2ac6a26b28ed30ce8354599efa1e65614ac8985616751b5dfb3`  
		Last Modified: Tue, 02 Jun 2026 22:13:16 GMT  
		Size: 102.2 MB (102236251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f29da6194068cf9bcb9d5261ce3db2ba9613e69bf068059cae42650df5c10`  
		Last Modified: Tue, 02 Jun 2026 16:41:24 GMT  
		Size: 102.0 MB (102002162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb945a38f716cf57592bf7798346ceaaea08bdcf46e06fe6782946871b17bd37`  
		Last Modified: Tue, 02 Jun 2026 22:13:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1659713d9654f52d0d427191a777814b0511f65393db01a65bad62ce111250f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:580188f27035e45afa4cc12e41f7c5075f95e4ae686ed02a4e574617e5cc49fc`

```dockerfile
```

-	Layers:
	-	`sha256:dc9d77208ff7b7ff640dac8d64a73644c358ca3e8f271b9867b7f213e1c01037`  
		Last Modified: Tue, 02 Jun 2026 22:13:13 GMT  
		Size: 10.8 MB (10785863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c45f79347e23374e83d121c1307fe1efff10b15ce962e530a37a279c918242`  
		Last Modified: Tue, 02 Jun 2026 22:13:12 GMT  
		Size: 29.0 KB (28973 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:d7c63ae1cb5b7323d759c6711ab84a3136d15d5f978fc6ca08c53d8f38fddfab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302713149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a7f088c86890ef21348f71ba213087c5ee17e388cd2bdfdd5b4dc5af6c7b7b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 22:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:12:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 22:12:06 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 22:12:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:12:06 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 22:12:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 22:12:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a203c225dd8522bdd8715f76203677e263257613c0c04e14fd9a434bee887dba`  
		Last Modified: Wed, 20 May 2026 00:04:36 GMT  
		Size: 23.6 MB (23639255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ada0eefe1ba158f90c1cefb9bda61c8de2e55c4f9c92965b87f7151a892d`  
		Last Modified: Wed, 20 May 2026 01:34:53 GMT  
		Size: 62.7 MB (62740413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9a2ade4f36df53a0b903461135c5c2aec1461bfad8e84e4a6ded9b9b4ed6a4`  
		Last Modified: Tue, 02 Jun 2026 22:12:35 GMT  
		Size: 72.9 MB (72876238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c820ebe5b5536b95e87912c5dc1f2663a3e9f184b88c7a174fffa610cef8238c`  
		Last Modified: Tue, 02 Jun 2026 16:42:07 GMT  
		Size: 97.7 MB (97715056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef68dc862c2407aa5d82fa7ac2e9df4ccff70f56bc139d8213917c9ee0f35b54`  
		Last Modified: Tue, 02 Jun 2026 22:12:33 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f3f58852ad606d5e56e9f2ba399350511e86f5d7bb280805458f877fac0fd313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28142c314992e4fcde6f526078147c989b92324a0fd61dbba28e0ff5ba41524f`

```dockerfile
```

-	Layers:
	-	`sha256:73f7b1bc9dc6023d6af4ba1df8c8e4550ecb5752d74b8aceb6d2dda9a4391644`  
		Last Modified: Tue, 02 Jun 2026 22:12:33 GMT  
		Size: 10.6 MB (10581750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a985d18a89fa2571fb4c341c0e0920f937bf0a99756f12853621f836701a0081`  
		Last Modified: Tue, 02 Jun 2026 22:12:33 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:fd59b951bb44a096685525e5e72e9e094cc792916973993e956ac71fe7b3c33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337105842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb00212a2eada9f5412c64b82e8eb4ae45c6bd9a50bea9564cb582fb1b0f517b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 22:10:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:11:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 22:11:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 22:11:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:11:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 22:12:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 22:12:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3777b3b9ab681ee4cbcf7f0da00484eddd87c9feacac47ea60d74c11fb426e1d`  
		Last Modified: Tue, 02 Jun 2026 22:12:28 GMT  
		Size: 98.4 MB (98380427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ffb09d61853e3fb3628a4cb3b2d395b59e27aec015f8f1626a8b2ce9bb2f2`  
		Last Modified: Tue, 02 Jun 2026 16:41:30 GMT  
		Size: 96.4 MB (96434582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836e73be47d27954d3e4fd679b2ff5b0dca370ad70f0ea252cdfbefe0da71756`  
		Last Modified: Tue, 02 Jun 2026 22:12:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:38bc691a7440fada1ca339467c7776ef0de2cf10326bc6417145572ee183a6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088ab413a89db5a42c51b7cf951fd680d26de2ff70f230f9099b89a587c391d6`

```dockerfile
```

-	Layers:
	-	`sha256:e13f01928fdb86ed9cd6b1ba6619180c6ba383df90cd3d49fb94b2b162c1ee18`  
		Last Modified: Tue, 02 Jun 2026 22:12:25 GMT  
		Size: 10.9 MB (10905681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce42734a77475a5fec7a714846991d219cd7394b237ba3b285045a5ae51058f`  
		Last Modified: Tue, 02 Jun 2026 22:12:25 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-trixie` - linux; 386

```console
$ docker pull golang@sha256:cfee2360bd5f161bd8b7505f833434d2311885b0e86b71ab298cb633313171b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347894216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bc9a1c868a5264de1c6743ceacf6908b0f49fe9199943e016edeacb2101c38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 22:10:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 22:13:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 22:13:17 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 22:13:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:13:17 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 22:13:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 22:13:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7297938c03ac6ad4e53525c3e0002337292340d300a5508ffbc391176c4868ac`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 26.8 MB (26795141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6db995dae312f4650e9596da7587e265fd6b48ac92ee4cf787e012233b3a9a`  
		Last Modified: Wed, 20 May 2026 02:45:55 GMT  
		Size: 69.8 MB (69824667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996ce8f2fb9fe9a86a4de3b42adc55918dd6bbd1fc34b499c3bf8b362cc1f89a`  
		Last Modified: Tue, 02 Jun 2026 22:13:49 GMT  
		Size: 100.7 MB (100675167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f630b89f59dc6a4b85d53c6ab2696f0b52ea5d937a0bd9344e6c06fc5883a6`  
		Last Modified: Tue, 02 Jun 2026 16:42:33 GMT  
		Size: 99.8 MB (99769529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b223738ddddd710a35dcc7102f5c45452ccc4b083167a062249c94126aba6`  
		Last Modified: Tue, 02 Jun 2026 22:13:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:3fef62bf025e505b29f1ff6385d2e1c92fc006e3ec8ddd449e3b240974a42d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10786051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b1d641e5ac90a6a7084012d062387375a1aee250ce25b2bf60be49516e6c45`

```dockerfile
```

-	Layers:
	-	`sha256:0efe91bd7c780d1be8d7dcc5dffc40bd945b295998bc7101fd84fc08f2de4793`  
		Last Modified: Tue, 02 Jun 2026 22:13:45 GMT  
		Size: 10.8 MB (10757126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b811e77039d4c9cafbd75c07b8b77213a81777de949e6ed26cc171f94106c28`  
		Last Modified: Tue, 02 Jun 2026 22:13:45 GMT  
		Size: 28.9 KB (28925 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:a023d6f0455cac49ce903a65c87eb212c8d4a8d411a3fee8034a95b42ceaf095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344524649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9865c75a258d6932093d2db5d31fa0c9648b048cf868de73f0383baa22da1815`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 16:42:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:41:50 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:41:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:41:50 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743dcca676e80d0b7074d4f03820f8068053078d4942f2a921fdf172c62897ae`  
		Last Modified: Wed, 20 May 2026 01:14:53 GMT  
		Size: 27.0 MB (27021149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396fcf223bd659e5dda1b961ab403e3df6f9d118708751addc02badc2015799`  
		Last Modified: Wed, 20 May 2026 06:53:00 GMT  
		Size: 73.0 MB (73042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ca70e542a2f090e02cf1f610dbd33362e2bd92c8b359416ee87a47168f5d0b`  
		Last Modified: Tue, 02 Jun 2026 16:43:27 GMT  
		Size: 92.9 MB (92941610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a76d2265265ac98a5752cfbf5ed880207c013050351547f0c225cf8c995ca0`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 98.4 MB (98387092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86a2dc335689548be6519a9c0f348c85e335d8c5acd7538e40702e1a96fe71b`  
		Last Modified: Tue, 02 Jun 2026 16:43:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1ab6d96caa23f66d16052c572ee19db594c300f4809844ebed202a8936bc4562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d8d5f91fe38222eb8afbcb298ab7d8c58ef3600a97201011e40762810413b4`

```dockerfile
```

-	Layers:
	-	`sha256:9d848827aeebcbdaee44b61cef9b735a6b9a5d59ff57bf141641453effe034b4`  
		Last Modified: Tue, 02 Jun 2026 22:14:11 GMT  
		Size: 10.8 MB (10781651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd224c6c31274a0a83d9a5a86b84cef3fcf5c98bed29ec5aecbe9f2fb0d5256`  
		Last Modified: Tue, 02 Jun 2026 22:14:11 GMT  
		Size: 29.0 KB (29021 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:86a71a3ba3e54b89fd2b0a224c98108cd319cd5d26f5f3cbae3ca8e91f3018ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.5 MB (370462879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4c46c1a1e23651a0a25ea2daa0a36020fb7581f46caae4d8d0d7884e0d0bca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 14:01:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 23 May 2026 06:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 24 May 2026 16:39:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 19:36:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 19:36:13 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 19:36:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 19:36:13 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 19:36:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 19:36:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6afb0d9fe2fdfebacf2ccb9782fd129d9e416f637c13f72c2f0427e69c04c88`  
		Last Modified: Tue, 19 May 2026 23:49:54 GMT  
		Size: 47.8 MB (47796268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db76586e2d1a29e7feb120e0fcc7fa49e8df54823efd2e1b4e13ca0fe4ab60d`  
		Last Modified: Thu, 21 May 2026 14:02:51 GMT  
		Size: 25.0 MB (24966381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bfe91065712f707f8614b6bb5478bb453a0332b440e47735c29ab8e1ac33e`  
		Last Modified: Sat, 23 May 2026 06:51:24 GMT  
		Size: 66.7 MB (66673209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398a312ecba685f463e19d1da6c4ef550fa865a7e4e10e59224662d013f3fc84`  
		Last Modified: Sun, 24 May 2026 16:47:40 GMT  
		Size: 131.7 MB (131719359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17ac82c7e9426109984a5c5c0752db17553ade9c9f16d09c7581a1f1ca3da85`  
		Last Modified: Tue, 02 Jun 2026 19:43:27 GMT  
		Size: 99.3 MB (99307504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bc4290640d6c55b3a59a4ff971fd53424d66dd6e2aa9b1ee88d8406f5c4599`  
		Last Modified: Tue, 02 Jun 2026 19:43:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:84968ca4a107dd1085188bf4bcec253056b17915421cb13cf15c2704d4197789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c67ee663b0bdb13a62c47d6998dbf10e3333404a468eddb23af2c4add17b46`

```dockerfile
```

-	Layers:
	-	`sha256:bc4a8164f0f7b3d1ed6be0c0760ba1eea760aabf586bcc790c3fe51689af15cc`  
		Last Modified: Wed, 03 Jun 2026 03:40:15 GMT  
		Size: 10.9 MB (10855484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1176c0ec03ce1dc27963710d558efe1b9b8f69b042dfd5c198b009d42856aa1f`  
		Last Modified: Wed, 03 Jun 2026 03:40:13 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260530-trixie` - linux; s390x

```console
$ docker pull golang@sha256:9d4904cb7d01498720ec51a856703d45135b0a3a6572b2ee47649b0484caf9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321326009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5601be627df4b7cecd1cace96d3b7ae1994b57a9fa9e81562baf7837bec329`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 16:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 16:42:00 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 16:42:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 16:42:00 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 16:42:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 16:42:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a95ac44f164c9c275ab328d3f5219a9cee0e2be081ed2ce1bb7cb8135bd49f`  
		Last Modified: Wed, 20 May 2026 00:19:10 GMT  
		Size: 26.8 MB (26804813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab366c3de62691a29444d50ed3d26e9d7524b8314a9b46521cbec555e978032`  
		Last Modified: Wed, 20 May 2026 02:06:37 GMT  
		Size: 68.6 MB (68638051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd22048fba1465d35621d768bcd327fddf66960714d773f1e88209e32b1e38c`  
		Last Modified: Tue, 02 Jun 2026 16:42:51 GMT  
		Size: 76.0 MB (76049556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca767cc33ca0e2036ed1bd1b9a5ecdd963a3598306969640db0e92025a10887`  
		Last Modified: Tue, 02 Jun 2026 16:42:28 GMT  
		Size: 100.5 MB (100453651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9a8ee68c14b98afb3a8774d01717f9336661c63fb41da7ee6c6eb661b8a1ec`  
		Last Modified: Tue, 02 Jun 2026 16:42:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260530-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4f281e222c4212eadd541b10a2f239bd8a45a16a271d55052581da3d6f6fd9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a61cd0c8bc4937a72e5bba9b492ebf0d04746e9428031226e6266359a63b0f`

```dockerfile
```

-	Layers:
	-	`sha256:ef5b66fbac69020c5449a607f4d2b750244502a2ec750cd4bf3520eb71af07ba`  
		Last Modified: Tue, 02 Jun 2026 22:13:33 GMT  
		Size: 10.6 MB (10597011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27245b1cfad71c8a4ef37b5fe3321c26a57c3b26df2e48f71e329c57c5179f5d`  
		Last Modified: Tue, 02 Jun 2026 22:13:33 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json
