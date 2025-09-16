## `clojure:temurin-8-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:c12245a86d7b740bf8dc1011c6430d32d1d46f25d310875945d01445f065d168
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
$ docker pull clojure@sha256:f479219dedba78976e69ae14b06ab2dfb06f93eb8353324a739fb31679c0f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196221670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7a1ad5821dc0bd6f307e4b4586503e6a260ed46b37fd22a3975513493e38fd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d54dd09e62bafd2c468d45ba15c0cc4fac551a0753fbcc6e5e0bb5cee582ac`  
		Last Modified: Tue, 09 Sep 2025 08:52:19 GMT  
		Size: 52.2 MB (52165369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8397a3e729905830bc0c43dc0837902d66ab0ffc11cbc4208a1bd8b831f7fc3`  
		Last Modified: Tue, 09 Sep 2025 09:00:07 GMT  
		Size: 91.0 MB (90951226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0584f5325b725db7a6cc468022c72c0d9a653df70cbd0babda0d6d603f19140`  
		Last Modified: Tue, 09 Sep 2025 08:59:54 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:37c79d54ba65f26ae316b94688f4f55d0981dd951f6751c42811a0479d12ec45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67d8b9c57d3c1af2672c920debc0e6a5d3faeee89b12c4edecc9d1d07dc6f58`

```dockerfile
```

-	Layers:
	-	`sha256:238b15702d3cd07513c5eaf5b513012ccbdd16c233a3f52a1e7e1624a5e43cd2`  
		Last Modified: Tue, 09 Sep 2025 09:38:12 GMT  
		Size: 7.6 MB (7593467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba9af6c2df41b9748eeda324327d21565a6e6f11fbb8cb58d9a60138e5aaa74`  
		Last Modified: Tue, 09 Sep 2025 09:38:13 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
