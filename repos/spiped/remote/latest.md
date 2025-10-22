## `spiped:latest`

```console
$ docker pull spiped@sha256:d94f4cbd7a78813cdc3333e090ea46446321494c5230dacb327e1842c15448da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:6f0a728f4d254706eee699322a9e2ed5c8893313d3ca13d424733be76eb2a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f93e597f7224b9a49d8bb5454cc135acb74a23884a3159e6a4820bed12bcf38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7368ddec81d901cdec9b466bd91ad6b199e14e8e78137767a02f2fcd4f145faa`  
		Last Modified: Tue, 21 Oct 2025 01:41:17 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d776fa84caee71716a6e6c781b5bb52a8871fd5b874c0a3e89e5f00670aae9`  
		Last Modified: Tue, 21 Oct 2025 01:41:17 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81159f1417a08ba990dd015fb6c0c247c4acc0c26f0d950cb2b3c144b40c36c4`  
		Last Modified: Tue, 21 Oct 2025 01:41:19 GMT  
		Size: 7.0 MB (7048330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b02607dd6fcd762f5ef1300b14146d6615749aac9578f7aee242e074e120b15`  
		Last Modified: Tue, 21 Oct 2025 01:41:18 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e4278b7bad0ea830fe7d7aa78b234c6bc9a110c7b5d77fab4efb8ad57a81dd`  
		Last Modified: Tue, 21 Oct 2025 01:41:18 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:631579407c1a03546c504c76883484169da75fcad73063a37482ec4ef17a7978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863aae559efb9d9deea4e9bc5215560a2f74bbdb9197546d7e276d4810b485f3`

```dockerfile
```

-	Layers:
	-	`sha256:95248887450f95aaeeb77a13628db8eacabad2de38e401457dc60ce116e377f4`  
		Last Modified: Tue, 21 Oct 2025 10:04:28 GMT  
		Size: 3.6 MB (3626132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8fbe7d53b7992a05f11b630c77a28df904fe106a9a45e5ca4321446072b2c08`  
		Last Modified: Tue, 21 Oct 2025 10:04:29 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:41a66bce033c58da83851f16f0bf1fa0747a2b77cd668c59edb085e3c0abb111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33737943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d155bdfe02f9e97c2f563e4a2d54f035b18d5aad6caa38ebaa7ff394137609cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb1ec6461420e1c390afe2aed634a24a7f4b1344e5f9f40f16a210319d7b4ad`  
		Last Modified: Tue, 21 Oct 2025 02:31:25 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b41304abfa70b74311ff2f4ba2b5e0e9e6ec6ddf8f58a7b5d10f2a1663d2c`  
		Last Modified: Tue, 21 Oct 2025 02:31:25 GMT  
		Size: 833.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fee20e75d820449acdca278129b53ff4318ab729c53d2fe1888b4ee3292df91`  
		Last Modified: Tue, 21 Oct 2025 02:31:27 GMT  
		Size: 5.8 MB (5789291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd8ce85e02d9b26f353b6ed6d5006efb1baf80c31f72a4489873d40be3211a1`  
		Last Modified: Tue, 21 Oct 2025 02:31:26 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da13ca052164b735b7b5a3cbffef97f52cf2594d5c2238b702577c1a3523e68c`  
		Last Modified: Tue, 21 Oct 2025 02:31:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9199dcbfdaa4899d9d5fe637f3e31a78b34acf54a65251ff42d9ed98d866a58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3634257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ebbcd06d7a1cf5e302e26da8f9bec64c0d0198edd106cc4033db4061535e01`

```dockerfile
```

-	Layers:
	-	`sha256:0b8db29092b2c301a0e86df999bdded6f64c4ed820d38708bfea172d4b1f41b9`  
		Last Modified: Tue, 21 Oct 2025 07:04:27 GMT  
		Size: 3.6 MB (3619126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44cb655d23a794d0dacc87795704c80efc4fdc474b6b1fc56cd5235d9b47fd6`  
		Last Modified: Tue, 21 Oct 2025 07:04:27 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:3939da03ec163fd531d639a2ae776ec67eecf89e3248fc1155f4cfdb58cee957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31799924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2cbd00886514998325fb65fcea2147ab0d99f50fc64c48d215ea538b9f6266`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aada44c12527f41ef724e46766ab4c9eee3bdde03409c8723be4e92510b891`  
		Last Modified: Tue, 21 Oct 2025 02:35:58 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2500836ad56b559eeb49b7013cc80ebf98a1d06b081333e205a7a12ff396ef`  
		Last Modified: Tue, 21 Oct 2025 02:35:58 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fe5dffe3276bd869c48d2fec6ff8f066295d9942d194634fccd6748c5b45de`  
		Last Modified: Tue, 21 Oct 2025 02:35:59 GMT  
		Size: 5.6 MB (5584664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f83bc6307c5771e50c88ff0bb4f92094261df47b438a0449b1c47d9031971c2`  
		Last Modified: Tue, 21 Oct 2025 02:35:58 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a5bddaeb16f7a4dbdded60dd41f18789162c6b6a4c1b1760df97e45d590e5d`  
		Last Modified: Tue, 21 Oct 2025 02:35:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:8788163bfbb05edb8e7acb335187c54e0bead6b142b3d4c1a5cf8090bf591c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a6418658eae29a8615cba2eab78175c279349220e16886f1cbf1396a06be54`

```dockerfile
```

-	Layers:
	-	`sha256:edd8f4cb77eb41b2858789f4c399c6dd2bc91f8530bbd7a90e2f1961cf19998d`  
		Last Modified: Tue, 21 Oct 2025 07:04:31 GMT  
		Size: 3.6 MB (3618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66c41ab0c79b2d9914aa3a3db22a83d7162fb48bd12df023fa2c39e380ca1f5`  
		Last Modified: Tue, 21 Oct 2025 07:04:31 GMT  
		Size: 15.1 KB (15131 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3c15e3759c43edd67184d1911bc75398abd393ccb2c720e2ade757239f881ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36376189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99283062f1a1ae6c6f210a5607f047cc899b66315197b1977ba3cb23c1001037`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec76278d7a26f099a61d514820b2d60f27d9b3e49aeb26df47fa2e94689d6c6`  
		Last Modified: Tue, 21 Oct 2025 01:45:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c735f7d994c915dd9d00d77ee51eded03f9790aa26a575f60b057b6651ca48`  
		Last Modified: Tue, 21 Oct 2025 01:45:33 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54b5bbb375433715edabee195528c8f5ae8a308885b051a148b75ba81959fbd`  
		Last Modified: Tue, 21 Oct 2025 01:45:34 GMT  
		Size: 6.2 MB (6231698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ab015d7b18f94a0fd52a31022f5447fe59057f2351e980e1975ff2e76e6c0d`  
		Last Modified: Tue, 21 Oct 2025 01:45:33 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdadfdaa66d11695433b0d3c72ae6670d36c48797ce69ceb4be9f63a5bbe6f8`  
		Last Modified: Tue, 21 Oct 2025 01:45:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d6fe20552845e15ab0d467813ba93b179c8e496a90712fb89ed0fa92c208d9c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eda9e9aae57486b9424d02603fa26ebb0bac2ec5a556ad1c746fd366a0ff996`

```dockerfile
```

-	Layers:
	-	`sha256:a2c8d1b0dc8c641c388f3b469525e4b408ab3763160733777d77ab813bab5e06`  
		Last Modified: Tue, 21 Oct 2025 10:04:38 GMT  
		Size: 3.6 MB (3621168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f9f4347c49c3f1aec9a718987888bd63c4c590162962798776b02af4341e497`  
		Last Modified: Tue, 21 Oct 2025 10:04:39 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:553e43e53a56c3dde24a9bbb78098075040d6886de6a4c9cef232f591cebd194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35c1e370554a3a1be92f32a2aadf2b5584c4a068267ad23f42424fcbb660285`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ec35973f4a2d99ac59065b0b3a76ccf61878c4035566ec7226e8c1a16f9fbf`  
		Last Modified: Tue, 21 Oct 2025 01:52:15 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d79fe3261152875e088761667f23cbbb0c7bc678af758e17524c48a5626c1e1`  
		Last Modified: Tue, 21 Oct 2025 01:52:15 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7b5f1a07ae7aef949331e1f7c66d270c23edd48267ea5112bf9d71de3ede27`  
		Last Modified: Tue, 21 Oct 2025 01:52:16 GMT  
		Size: 6.4 MB (6442299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa343725ce34f11f1d661376e1b675f60b3336b9ebb598144472c7927bdbe395`  
		Last Modified: Tue, 21 Oct 2025 01:52:15 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1ac49a6bcb51038c49019c0abb68458b76f9125f88b11022ec36af86c56388`  
		Last Modified: Tue, 21 Oct 2025 01:52:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:8baf939a665d9db0cb7f60f6b0fedfd8876ebacb4f3bd3ff9bf48edd65af146e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73814ac040f615b0cf68bd461b9c9bc0b2d3b101dfb244fec16d4456c6f018f`

```dockerfile
```

-	Layers:
	-	`sha256:80aae5fea18a4a63bb0152031d6d8720d742620f7c07118ce785b7c0aa97929e`  
		Last Modified: Tue, 21 Oct 2025 10:04:42 GMT  
		Size: 3.6 MB (3620261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b5b37ab9421c37e53a02bd3e1a958aa1bffed7b744347d0fa6d3e050c1b3a6c`  
		Last Modified: Tue, 21 Oct 2025 10:04:43 GMT  
		Size: 15.0 KB (14988 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:1457fa5a06d52cbb254a7ee14c53a2cd5dc8d12aa7d5bf393e4a1bb8095420b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535605a065eeb5f3c419e60e0d2de8d0eaa41cfd34ac968f318f89c921646f89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44054336467e1569959a00bbc7049678901da87ff3a54b41ea8294c854b949`  
		Last Modified: Tue, 21 Oct 2025 07:25:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efa6a797e0143d9c518486389146bf98076a17915dd8a0b03cb2c0b83c2e9e7`  
		Last Modified: Tue, 21 Oct 2025 07:25:34 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84aeffc46fd6599b7ac43836934ae7eba4c02a998d05522f0e9bd059c18247`  
		Last Modified: Tue, 21 Oct 2025 07:25:34 GMT  
		Size: 6.8 MB (6840157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be975fcd442cff75d724de67baaaf972bd45f1c6c2b5d59ed6253435dd9b33a3`  
		Last Modified: Tue, 21 Oct 2025 07:25:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5f224657c99661027656ec4de48199d2c49a0b84f889b16c5749dec10b5cfa`  
		Last Modified: Tue, 21 Oct 2025 07:25:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:464b024d2933016fbf4fbf8e5b3009bfa5560511917ef9d9acec1f4827ca8a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e459295b28984810a7f9ddeae98b638df235d8f5ef66b367630fd8f472ee8a`

```dockerfile
```

-	Layers:
	-	`sha256:60f3f57b7162196b0edeaf8df251ed42b142d6ebee9c3b6c53a8838b86a25a9a`  
		Last Modified: Tue, 21 Oct 2025 10:04:47 GMT  
		Size: 3.6 MB (3621869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e4158a5c1e2ee5cd5fd10200b13751d7ee1b1e5f6012bed46a0c96bc258db3`  
		Last Modified: Tue, 21 Oct 2025 10:04:47 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:7004f59a14e65493d89d02012617e4685f705f645959559227290584c7da32b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57db3066c8da0560c596ad9830d9e9d916c732311869e057ec28751c6c95ea6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2eca7a0881779ed75b9a6df9e9c73f4e30a2545b324835ded643360d27d8cc`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f2808be96be6277f0f38d8010c29a85c6383d14b6f87ab8b25267c049edb2`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ffa6796bebebbe0e033f44c2862905348b86b654f6796e30afac6e530d4277`  
		Last Modified: Wed, 22 Oct 2025 17:58:57 GMT  
		Size: 9.4 MB (9358258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6357568a94aa6f06730895e5dae1afb3df5610b097001d226a3f77165e34f`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b644b84d3f1a2b591c927fa6de5e0189e84eefcff0f41ec2a3f44187185c0d`  
		Last Modified: Wed, 22 Oct 2025 17:58:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:5c5c3dac2a6b922d04f583d01b94567b074f27f995ce52ec74839d9912349909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a636dc3ff00c7130929694628709b79af7b1fee5b8a10375831363195b017596`

```dockerfile
```

-	Layers:
	-	`sha256:06533fa6c4fa5d87ac9aa9b94a962ef7605ef017f0c5582d776f1d8052627da7`  
		Last Modified: Wed, 22 Oct 2025 19:04:39 GMT  
		Size: 3.6 MB (3613275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d421894b349a0bc498ac33059bfe41875507a74674a4b14aefd8a88b3e1a41`  
		Last Modified: Wed, 22 Oct 2025 19:04:40 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:b286a9297f3b6f6d41e14f240b98569b984581e3b577798c4d847aaf9f26fa7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35961281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6df0f7aaa6b7e5543ffa071d253b1a0d0e864c30b4cacc596e690c60ab3b87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Fri, 29 Aug 2025 17:20:00 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3t64 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 29 Aug 2025 17:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
VOLUME [/spiped]
# Fri, 29 Aug 2025 17:20:00 GMT
WORKDIR /spiped
# Fri, 29 Aug 2025 17:20:00 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 29 Aug 2025 17:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Aug 2025 17:20:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961b918949ccb05039d664d7e1cd9791303e0393feda1bf323a315eac045f7be`  
		Last Modified: Tue, 21 Oct 2025 12:10:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe3083e3b003a40325152f2e53fa1732f9ffedfcd84ff6e79a95ce37851e80`  
		Last Modified: Tue, 21 Oct 2025 12:10:46 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512acbb5b71d660f4402e2993331109cbed8085bbc7ebadfd4a62bb6fded45f`  
		Last Modified: Tue, 21 Oct 2025 12:10:46 GMT  
		Size: 6.1 MB (6121657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a638d0a341931aff5366ab9e604f9472515c2e87c5d65deeec73b78f471b691`  
		Last Modified: Tue, 21 Oct 2025 12:10:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e71d019b6e9a83f9c1f254760b23c3be61b514a25be9414f2e4bea61147ead3`  
		Last Modified: Tue, 21 Oct 2025 12:10:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:bdcadb601d6404d64d0321e088ec1f1ea2520b66f2d441c2a5730e2ceec84458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e5fbd77f5339e6628e12f846661c9af06657c4e2ef8d2278823925e07f2a5f`

```dockerfile
```

-	Layers:
	-	`sha256:4d89285d5f5720a56d288696f65f17a67cc1a118b25260d4263cdecaca0a00db`  
		Last Modified: Tue, 21 Oct 2025 16:04:42 GMT  
		Size: 3.6 MB (3618495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62117ef2297c87147bec8c9acbc2386ae161555b7e8af650ae56e8c430ba96f3`  
		Last Modified: Tue, 21 Oct 2025 16:04:43 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json
