## `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye-slim`

```console
$ docker pull clojure@sha256:d8b0de3df085c482c5664ae5664a635be6b2a1a446795f2d1379c5152d609cc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:34b6da90e3252975bb307ba00afab0b467d682f363b97f9ca82a452e67ed4510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235242606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f5ffe6fb1c1c0258ecbccb2cefb671633d00f5553fbf70ce3c026e0ca83335`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:46:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:01 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:01 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531c01a82261e861f6e33a853c3b9346224dae7ff6ac9ef2f1a093efac749acc`  
		Last Modified: Mon, 02 Mar 2026 19:46:36 GMT  
		Size: 145.8 MB (145806697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf0947610ab127431522a15726b76502602a3d1391e25e6dd6c6c8b0421bf1`  
		Last Modified: Mon, 02 Mar 2026 19:46:33 GMT  
		Size: 59.2 MB (59176884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78d1e8ff0a90daa065ec615dac519b77f86f4b26b1b79e974a63e2bd0a0298d`  
		Last Modified: Mon, 02 Mar 2026 19:46:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2658fe16c23cb527320350b6623fc4afbc12d57777bf65a2f74fba948618bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42197f34dde6b18148b6e1438d68ca56399070e589c8f7d1fdf8b4f22089df`

```dockerfile
```

-	Layers:
	-	`sha256:d7ee03558a4a6cae5783f5bfc23b0bb68459787daed2e9e782c037f06d7c6ee3`  
		Last Modified: Mon, 02 Mar 2026 19:46:31 GMT  
		Size: 5.3 MB (5341818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63feb07de2d140b47970fbd72fc6b3cfde720bed9b9d770bb18f3ca08cde3643`  
		Last Modified: Mon, 02 Mar 2026 19:46:30 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05d4eb8fd35b99c1b8d7f911729a8aa556f3baa9fb857ba4261c266c28d62b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230564029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb01e1e59b580b05a4d16ba9fd41ad8e0953bd7e7fdbcb2b5c99117937d1c0c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:45:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:55 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:55 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7b1f25979feb8eb8f8e676391390ebe6a463954e11cba0aaf693932290f57f`  
		Last Modified: Mon, 02 Mar 2026 19:46:31 GMT  
		Size: 142.5 MB (142501444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9aaee9f35d8bc870faae6a1484d2c596b4ca71dd4a0bbb5d6f0261fd3afb6c`  
		Last Modified: Mon, 02 Mar 2026 19:46:29 GMT  
		Size: 59.3 MB (59317469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228b24b91e25b9cc9775ccc867bd43737f86102e797fbc00fb078088e0a6dfec`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1607-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e2c7a02e5470f8be7c65e317248faeeac8a20533a2392740f93b7d2c04954a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a55b2ab47c59cafe12807cad5688f801fa8ffeb2e3b887c7ce7f8a61e061bb`

```dockerfile
```

-	Layers:
	-	`sha256:6c5aaa59d4753f57f90216ac1d885a5b4cd2b52122dec11955aa45b9a550dd6e`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 5.3 MB (5348168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78ccf93e5095c485bda9eb1a380d3318866623a80d4a609cbcf679f8871828d6`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
