## `clojure:temurin-8-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:4e60757a14d966ae936f3b6466cb9f83c22403e750c04ec7406c4994fd0d5718
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:903b71978f5d3e420b8009ae861c42e9d352531d1343a1a05c94a3dbed95a7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189544867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f40632b3c304cbcfba7bf9b0745911659ae7d686612acbf7366f119f25f641cb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41ebe8357a2720b33b40fd3bc725e6c0bee7aa97dbc61a76ec4add4f8235cf0`  
		Last Modified: Mon, 15 Sep 2025 23:25:07 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19aaf1112c8e7ba759c35cfa48f714ac2c6257749326f6bad7b2a55e120fcd3`  
		Last Modified: Mon, 15 Sep 2025 23:25:09 GMT  
		Size: 85.5 MB (85533384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c423f987f9701e6ed36f7753043f2b79e228e0590e2c14f2549b58090d25692`  
		Last Modified: Mon, 15 Sep 2025 23:25:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e47a74062a2f92b610650892860004741449453af55a67aa5343299c8f333719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf102ef4715edb429f35f92836ba478303f2a7ecbf76db1d3c2ff48f1229c3`

```dockerfile
```

-	Layers:
	-	`sha256:437d4263f11d027ff703b1c615b834280aeab32f2b675f7f66b8384828109372`  
		Last Modified: Tue, 16 Sep 2025 00:49:48 GMT  
		Size: 7.6 MB (7588455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:607c3a1d18bc2bda98bdea11c2fb93b7433fadd95f3951ecd536ba7295492f81`  
		Last Modified: Tue, 16 Sep 2025 00:49:49 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0d069c257100aa39f9e4494f90823989a677a81a26ddc1e73c537cd68490027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188837160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccf053c81fb27efbce575550cbaa63c6536fcbece09ef1187fbc965253fdd4f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4c4a8eaa76d61f99110e22be4af48eb89f4349f88b3668072f414b34deff2`  
		Last Modified: Mon, 15 Sep 2025 23:25:24 GMT  
		Size: 53.8 MB (53835629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbc4dfa490431f7da26fa7ea1b6171ac6d8623172285f47fab06fe6ad6a7ac5`  
		Last Modified: Mon, 15 Sep 2025 23:25:40 GMT  
		Size: 85.4 MB (85357141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f53ba9d949fa7808b9659df50c0ab4ed8152aed0a34dffed455f5e7a6c8cc`  
		Last Modified: Mon, 15 Sep 2025 23:25:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:960f4e69592419a76c41be9678a69afa194e7c39eed0655efaf186b73b32bb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af41e7a5c781d7b4c7e8c9441a183d7065d498480fda59e28bdf7fb7621ec35`

```dockerfile
```

-	Layers:
	-	`sha256:a2f6f3943e16c7ca4bff17a34ad9d725214e3a9864c91ed284c020633ffb470e`  
		Last Modified: Tue, 16 Sep 2025 00:49:56 GMT  
		Size: 7.6 MB (7596183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d474bf6d9487f96f323925bbc45072540a5f217f79660de72bd7db5b0d8fbe`  
		Last Modified: Tue, 16 Sep 2025 00:49:56 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d16adbde497bcffdde3ac92cb7d6a93b4f12013ae680c8eee8e0be777d092add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196223161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f44100e1eecf2e1599c6e9a75d086e9c140d341fc7b37081f1ff782684920f5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffc46708712e2739dd223f5a5084a3758b7e54dc9a68ef7ee76603b0b823ed7`  
		Last Modified: Fri, 12 Sep 2025 23:49:00 GMT  
		Size: 52.2 MB (52165393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c8ae605fed0f5b73af441215cce25a45c532840f09c61c623fed2508f15933`  
		Last Modified: Tue, 16 Sep 2025 00:38:50 GMT  
		Size: 91.0 MB (90952690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee4f937f3e16f8c6a1f93a6e96f17dcb7718e3ed9068e96c018cefebb84029d`  
		Last Modified: Tue, 16 Sep 2025 00:38:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3868f718a37f39f9d0feed8833ca882d91087a5f6e0c8191de85d5b17efabbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742647225107ab01f41b8744e6ed67b7c7da4665b7a35fd11052fb32bc0a0ff2`

```dockerfile
```

-	Layers:
	-	`sha256:6a64b18b71e793e92abb57a2904c9047c34a3cc6a59632f950b9812489e38728`  
		Last Modified: Tue, 16 Sep 2025 03:45:45 GMT  
		Size: 7.6 MB (7593467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:873f038bce9a55afd66e64700521a0872ecbc2a8270c65f32408ffc391bd3e2c`  
		Last Modified: Tue, 16 Sep 2025 03:45:46 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
