## `clojure:tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:6b28791430fdd66cff469c034df4389edac707963d0d6bf23e83005596534900
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:12bedc8b5cac4f34dcb909c2d5132d709783cd2935ce966dc51add4bfeb68600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227090073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0ac0e54ab2cdc19fe78a8e33f1f847e109616abd526dac8023a2cb30d01fb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:57:35 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183003a54bd0704ea3971054ada12f8eb7d539a0c269062a37f327fbf5e33997`  
		Last Modified: Tue, 24 Feb 2026 19:58:13 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eb65c8cf822d78c0ade73a0b5f6d3708067c7ead944869ac3f79c6bd174dbf`  
		Last Modified: Tue, 24 Feb 2026 19:58:13 GMT  
		Size: 85.5 MB (85539617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d847eac25f740aec42a529de8ec33719274210b7b7856d33746c373accfb249`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d74348cbba5343610d16a1fb2ff362440dde0c03508a00886288c2abb67def`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:494e096395359bb38147b2550562866aac449a82fa3767da1786ac3b5ba67644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c9721522438e196fb0f1c61a5ba7af54d22f064acfb55d12fab3abb189f98c`

```dockerfile
```

-	Layers:
	-	`sha256:c010f0b9cf5dc3463449be40de2a1d53fb1f4ad5952badee7acfceb9be558c69`  
		Last Modified: Tue, 24 Feb 2026 19:58:10 GMT  
		Size: 7.4 MB (7437146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f54184ef983d5759ffe5b5c0bb839f06d18e0cd7f4ab2eb142b5e998c6348b8`  
		Last Modified: Tue, 24 Feb 2026 19:58:09 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c7d3649f44f21d93e1bf78c904923899ab74d9c3877385016813fd2f1de5017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226306740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f589c273b3f0c4fa87764d7efa92d215620879b15acf1a4bfaaaac522331544a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:08:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:08:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:08:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:08:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:08:11 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:08:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:08:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:08:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:08:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:08:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71f6343d802bbb11ecabfac7757348ac81fa7c44c7ef053b81d1159f2280c0a`  
		Last Modified: Tue, 24 Feb 2026 20:08:54 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925d6e9f957b451c20e4f1ae8d7118b87ab0149a4f15f4ed02deeaa059acb04e`  
		Last Modified: Tue, 24 Feb 2026 20:08:54 GMT  
		Size: 85.4 MB (85365258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc34b0a297203da4c53b43c828326f26ea8a276c29d36439182899b34f9b1117`  
		Last Modified: Tue, 24 Feb 2026 20:08:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9faa434027fdce9b3b444248d27d505d922665abdde01f69a2fbf2077578424f`  
		Last Modified: Tue, 24 Feb 2026 20:08:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2515095560fdfe4d2270365833d7ec699bfb6ab87aaa48e43d60a80e9a1d8736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c114271bb4e97e233b99ed1cd0b03102c33a78fa42958e21f6eb8dfdecef0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:60426bb0da078f8e400a86b23ae3ff7bc602f5231bb4b8c12b9048440ea7d89f`  
		Last Modified: Tue, 24 Feb 2026 20:08:51 GMT  
		Size: 7.4 MB (7444197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2b03a1237d52f91239538626546ae15389a3ab51929cdceb5d54eeba50187e`  
		Last Modified: Tue, 24 Feb 2026 20:08:51 GMT  
		Size: 16.6 KB (16556 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:af2a86a89d9fe491a4a090029a2db4f562052c9b8ac6cdc9f0940b39ff3c94cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235702769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddd10d69d533a8c624ebad8093fa9de4b08c777f078941cccb12cbd8ee1b612`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 02:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:14:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:14:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 02:14:50 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:19:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:19:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:19:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:19:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:19:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898bd9db475a819ec030b333968ed33ad54a305029d5289784462edd831f227f`  
		Last Modified: Wed, 25 Feb 2026 02:16:20 GMT  
		Size: 91.6 MB (91632903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546efa00bb9dea82d6a9c931ac2e95c22934b0f3a9f50f9b99a7adf1282e279c`  
		Last Modified: Wed, 25 Feb 2026 02:19:44 GMT  
		Size: 91.0 MB (90956561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7e32b1c2312dfd7c935fcbebb08755f65b6ad7764a99802991022a38a37e17`  
		Last Modified: Wed, 25 Feb 2026 02:19:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9f9c7446291662a229068687acff115bc1bbef7f94d5293cefe06ad47d101a`  
		Last Modified: Wed, 25 Feb 2026 02:19:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:723fc5f0d1302482ea252d8af78b7147873be66a00c5bf9925019d8a9767afc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ad571c5eb9f7468687949e575e9b92bba5d57029ff3ab85c2451e3beac52ba`

```dockerfile
```

-	Layers:
	-	`sha256:44f6adb064c534a0a4493322b76bb45ea4319a69d643a74244d3ef90a7749108`  
		Last Modified: Wed, 25 Feb 2026 02:19:41 GMT  
		Size: 7.4 MB (7424891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb3485489930beb1d91f268c64e4ccf43059e1204336ce4cd894ebaee078c8b`  
		Last Modified: Wed, 25 Feb 2026 02:19:41 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:75d42edf6a911f433be6ba1b3ffd292ef4fc55d41d1636eac8ca56c2c9ddfee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222976456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f534d2176a7d7ce3d3970157c24c7190fa2b9bb56d997fdfec8ddbee2d6b25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 11:49:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 11:49:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 11:49:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 11:49:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 18 Feb 2026 11:49:18 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 11:52:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 18 Feb 2026 11:52:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 18 Feb 2026 11:52:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 11:52:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 11:52:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0c08292c273f6fa94290477f212196176e148c5443e72d590aa78d4b504c5d`  
		Last Modified: Wed, 18 Feb 2026 11:56:49 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e5dea3ba31bbf37ebe3b3414bdf4258e0621b6aab164e9c2752fe0d6b1f786`  
		Last Modified: Wed, 18 Feb 2026 11:56:49 GMT  
		Size: 84.4 MB (84425223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7f7c826b217e95fd4d70b6791c43150f39357961456e4054c4782eb6bcd45e`  
		Last Modified: Wed, 18 Feb 2026 11:56:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e84ba204c8d259db90bace7fcc313ba1fea0b94a0dc26859f7206a9e9ceb66c`  
		Last Modified: Wed, 18 Feb 2026 11:56:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:587c106994e2521c67971419a361f0613cbc11e348e24e05ac0852586bee188a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b538e779102728ce651b789a1760578d4bcf9613d5d73da63a9e04d1c43ed279`

```dockerfile
```

-	Layers:
	-	`sha256:1f3210e0b07d1ea50cdd2a79dd4f3e4bcfebb64adf507e58cb64cfb04c0b917d`  
		Last Modified: Wed, 18 Feb 2026 11:56:26 GMT  
		Size: 7.4 MB (7407084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad1045cae8dc95a5e5d67d3d7d82b8194db34f4943cca8cd294e33026c772878`  
		Last Modified: Wed, 18 Feb 2026 11:56:23 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3e1a13fb62f2eb3eca5be13227a6bda13b223318637e0fc050aa488ee5171d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224103853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b1ae290f42668f6e87e8cc3b68cf22597c2eb4e65f9e8b0e9094ab5c880098`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:26:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:26:20 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:26:22 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:27:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:27:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:27:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:27:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:27:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eb195b5aba9a96256c78bd1353fee477acdeab2f0bd579a2906ba761aec182`  
		Last Modified: Tue, 24 Feb 2026 23:28:02 GMT  
		Size: 88.2 MB (88233866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de11cda0388242d50c09880796bf0952579920f6e9b592c322817e6003ab49ca`  
		Last Modified: Tue, 24 Feb 2026 23:28:02 GMT  
		Size: 86.5 MB (86514411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1eeff22a8bb09a2f9a744a36eedca67bb06375f8918fe60b788b12626f74ad`  
		Last Modified: Tue, 24 Feb 2026 23:27:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f89fbf49c1a486d77890e6db98e0755e459b393302847420a555dc1ad0ca500`  
		Last Modified: Tue, 24 Feb 2026 23:27:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0f4e8a5dfc9bab75c4996847eb307cac0885752cb73443b273b46c141688e30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58835fc9b43fad0bcf38cce9baf9417057ba30c2c6c682c95aeb75a948fcd20a`

```dockerfile
```

-	Layers:
	-	`sha256:429781cce452577d53796985671b0ed20801141c4ea647ed0cbdf1b403dac1e1`  
		Last Modified: Tue, 24 Feb 2026 23:27:59 GMT  
		Size: 7.4 MB (7417630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de9331a9dddc8da37e806f8e54979df8306ba36ed7185aa9e4de9a1a3b50ab4`  
		Last Modified: Tue, 24 Feb 2026 23:27:59 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
