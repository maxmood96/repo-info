## `spiped:latest`

```console
$ docker pull spiped@sha256:7e3f6f4919b7f89ff00970c041e80e7dae63ca470f04f741671d16aacba5c734
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
$ docker pull spiped@sha256:fea99c454ce0fbe794959c712b9aa8211a59ec36d96ba4ec47e615983a02df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36828407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61044b76967f0bfbd214c3f0c337a70e34bd5e0113b94ee6aee969afe8ae0c9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc238e6158ba23ca3c78f09a916e5b8debcb8fc98435ef72ed1372e4a10d36f0`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631db32462bfbb6f6adbfce206c84ea557ef848ce2db5acbc296919b1e2fb8`  
		Last Modified: Tue, 30 Sep 2025 00:09:33 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfab92e44961e7c708e76600cd2a58da46309cb1585752de3faf3cf12144b9b`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 7.0 MB (7048278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6723c6fe89d1ee4486ae7f1aba339a847174340058a9aafba610b8f5d08c392a`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638bc283d4e51af75c91b14cfc4325a4b783724ecdd9ac3d936db49437b45069`  
		Last Modified: Tue, 30 Sep 2025 00:09:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9c5b20ad1230caec7f7f817835a32a8e84c0749bb0cec2f1338c9f94d9cafdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39fc5ab26c741f2fadea946a1e3f5f8d5f57b2c46254f39a4cf3dec01016afc`

```dockerfile
```

-	Layers:
	-	`sha256:6162c674076105e040975f2f9084082ad1c95d3491863ccfc1a758ad44af0f88`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
		Size: 3.6 MB (3626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e718aeb59e0ddcdc8ae0d260d22d1e426d5f84484cbe07357ab801c3c2ae2ac`  
		Last Modified: Tue, 30 Sep 2025 01:04:20 GMT  
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
$ docker pull spiped@sha256:9c14d801535964b9856cc995b5cc1d953e664d4d36a29226d0b525ebd12fc23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36375041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3760e5d3e931c335d1ba762156bad16c786221e38cc064a049bffad16061ebf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138cafb84902697aa37bc68f6f860c44a9a11d9b9a83a6c59384a6946bfb5073`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a73645b11d1149fdeaeb95abee773ad6067bb95726c22f35387d4b849d93568`  
		Last Modified: Tue, 30 Sep 2025 00:13:16 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2201eaba239855e7b70ec7db2b53e68c5437be9fc29a5048b5cec95d4357005`  
		Last Modified: Tue, 30 Sep 2025 00:13:19 GMT  
		Size: 6.2 MB (6231836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7b71e07b92ddd3ea16e307a436f84f0862f6d41ce6e60c918112b5004eacd7`  
		Last Modified: Tue, 30 Sep 2025 00:13:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c64c105923c5d37d4fa6700dee51a52780c755bfba3de0ac42ccf55d9c80ce0`  
		Last Modified: Tue, 30 Sep 2025 00:13:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9bc13bf85136708d05c74af3dfc16259959b0610a6cae025c7f9013c1e36d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2eb9ea2712f520f693ab118515cba89588115d9457cb6fc3051b4f69abe0cb5`

```dockerfile
```

-	Layers:
	-	`sha256:67ff2bdb0f88eae236c4d226ffb071064078a72edf0c36dbc9605931b2873702`  
		Last Modified: Wed, 01 Oct 2025 13:04:28 GMT  
		Size: 3.6 MB (3621114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa507c4eeada3b5ef073dc36105783217730a9444ef304a477a6297a951cebe2`  
		Last Modified: Wed, 01 Oct 2025 13:04:29 GMT  
		Size: 15.2 KB (15159 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:3483553c118f803d7dc6a6c85ba75a6757cf336c0fcdce07857d0a1ca40b5054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37739236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fb778095be09981fa712b92b08229fb6c016edeac9681a10e3d7ceaa3d67e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b683a27da0ff4f41706867fe165539c8b1d4170671892b8376bb380a96382`  
		Last Modified: Tue, 30 Sep 2025 00:20:09 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16959a1fc618d2ae9b84f6d83c71e630edc85d191636b48932f2f1aa95ecf3ae`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd39dff5263a0f9cae965c7539aca9f51ec3b9f5224265f80015a145df9f2cc7`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 6.4 MB (6442337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41989a27b3616713951399c9446e9fedc876ac4bae34f2143fa0833b64bd5886`  
		Last Modified: Tue, 30 Sep 2025 00:20:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1e5b5f97c64972331e5b1e53b8a01934b0013551e3c28790fc7e13f0dfebd`  
		Last Modified: Tue, 30 Sep 2025 00:20:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:5c3bc443e4a2f479f89ee155cbe841e2d63cc9294c3aa888fc64457bea94a474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3635196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a6fde58a78a8df0407f92615908cc35805714e3a1671a66bdd5d5353c72832`

```dockerfile
```

-	Layers:
	-	`sha256:480cb796d2b5b5d888e607bb45d255e462c4690fb64e54f2721250e19ed909aa`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 3.6 MB (3620207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a547b0a456597261657868e2d4ae927c47a163fda68183e21e9e32adb52c96f5`  
		Last Modified: Tue, 30 Sep 2025 16:04:36 GMT  
		Size: 15.0 KB (14989 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:c5b3f79371b3d7ff8f9e4bbc41f348539977b5654f1de79061ec53da86a2563f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40441071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab34c773cbd45451d188b0fc586243e9ddabeba95f34d0a3fe2ab3eb9668073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0a521cfb00afa1f22bd5d97b85ad1720879ee5c0b1baab105f52e4860ec7cb`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ff4669d4781473da0924bb50912f548111551b9b5f03299c1b3c476c31795`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77cbf7134214650d99819f0a9af3301695acf4eaa87494d06ed137216f6dd03`  
		Last Modified: Wed, 01 Oct 2025 19:48:07 GMT  
		Size: 6.8 MB (6840251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428f16a31134cd2b56611423f586a6bf111aa53bd8afd8bdaafa3815fbae142d`  
		Last Modified: Tue, 30 Sep 2025 09:58:06 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b21ea73e2977d5c531615088cb9bf1fa9b673f9a4a73159745d3775b9be25c`  
		Last Modified: Tue, 30 Sep 2025 09:58:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:c1257c6861ac64a590f57df8457c5341ce92804291bcf17f2e526d6cf56f30e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a512f85e4c6debb71b1588d50653364b97ef66ecf26e492d16906c6f02d9b5`

```dockerfile
```

-	Layers:
	-	`sha256:2e693f388098945d670d6d7401d2c73d30208c04a9c434f89128a9257051cad6`  
		Last Modified: Wed, 01 Oct 2025 22:04:41 GMT  
		Size: 3.6 MB (3621815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fe9e313181c313debecbb9cfd10ea888761ba52ba83d75c155e7f24b2c4c0`  
		Last Modified: Wed, 01 Oct 2025 22:04:42 GMT  
		Size: 15.1 KB (15073 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; riscv64

```console
$ docker pull spiped@sha256:63c81e7a01da08fe2456c4fe9380a75306824b5e09e202e7c8c48a955ef67681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37636030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d07a35af2ecef1d379d7de3e2682368da4fbefb910ec3cd0543c9702ba1cc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fdd8b049eb029577d94c03617e2a21858508fc5e580623cc21f55413af7350`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2785eaaf3b19c0d99a6cd261f54682df997b7f9e8accbab631417bedbbe11e`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 819.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e4c78f116c60eebba9d5a01de232d21fdc151c6c160765cdd45131ac57266d`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 9.4 MB (9358166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5280abb5bee4d4bac9b5e9874666be22133b46530de1b9bfdf616d9bbefaa34`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415a4b562d5e2bd3a63858fa9ad791651dc993419da3712ec490f3c0437d9c81`  
		Last Modified: Wed, 01 Oct 2025 10:45:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:fefbe28311f558c8f0bd34fd6ae277e561a9fba8dccbb5c370b5ae8d06f0ccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1946cc255ef0e663aba1c9b13f58f3e2ef6b22802d595e60c1a905b7c9f8d81e`

```dockerfile
```

-	Layers:
	-	`sha256:0f8800600e75cda5489b2d17ddd9ec37a58ad1f1223410df7742af5d2f47beaa`  
		Last Modified: Wed, 01 Oct 2025 19:04:43 GMT  
		Size: 3.6 MB (3613221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea670935804f907c5c8108973c916a79cd259c3ef65e26b1505d0e684c44599`  
		Last Modified: Wed, 01 Oct 2025 19:04:44 GMT  
		Size: 15.1 KB (15072 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:0f938721daf08c239ba32eb210482941a1f07269b403c500e3eb132911dcb44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (35960783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a850e3bdd587415e9e20969ef6ce52c0faccac714e602b10f9bf1d2b0dfb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 29 Aug 2025 17:20:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470e100e87fb0737d8813ad701db233de34e7eda3bc7a5e347182edb96fc07b7`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef1e4cab10fc5f2a92736f192b67f9fc080966aa9ed2c1f50b7e11829520c0`  
		Last Modified: Tue, 30 Sep 2025 09:24:06 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df0b2c4d2fdf31e6e7d55fa1d672759b5244e49159f022163b746b96993bca3`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 6.1 MB (6121187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785b089a06826b0a24ec162778fc2d01554cd54c34862516f04dcd2dd9ccd403`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d77df7c01beee6fc002cc7aa3c14a701e7f5700b06926f27e143c76a4b4ad2`  
		Last Modified: Tue, 30 Sep 2025 09:24:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:989260bf82df9044c638bd7e2ffd082c84c055e6978c4b777f7ff712cdd195fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3633466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e624bfadefdc72db4094fd7c89b27c542616642506962d12a9866c5e9c9829d`

```dockerfile
```

-	Layers:
	-	`sha256:e8ce284c6273618f8501626aaf90218d5b7c16d53c5504f820ceb8845d9247d6`  
		Last Modified: Wed, 01 Oct 2025 22:04:48 GMT  
		Size: 3.6 MB (3618441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1078258bc1376211e434d54b32dc2978a4b4a468f55cf19901220469ca2edb4f`  
		Last Modified: Wed, 01 Oct 2025 22:04:49 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json
