## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:020cb2023c3068825724ad20c0c37c10ff62517b6e1345e283fe042a5e270530
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:df49b1392291cb57bc33ef4174aaa87c12a19bf1e17eb6779a593983fac03154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235552035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64570b1a55f8b01edfaa4798a49a43b66c18e5db3c89cbe48f44fffbf7207950`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b66f3049b6623cb6563a4773cd5043736e63053efe8fc32026dd51b0b1d437`  
		Last Modified: Tue, 02 Jul 2024 07:07:04 GMT  
		Size: 145.5 MB (145504892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c6bc41f0b4cfb51d570b97f41a0fe69fce02290e652d1386b10f14922657bc`  
		Last Modified: Tue, 02 Jul 2024 07:07:03 GMT  
		Size: 58.6 MB (58624214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb22c18c9acd55f924e5a8d7968f295bc8e7c1acdc11ba4f0d9b62d00f8eaf9`  
		Last Modified: Tue, 02 Jul 2024 07:07:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:07b5ed501eac0c89440c69768cfc24b5088273705d21063837b1ab0c6eaff439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4923209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95355ab36e76e805b54ce791bef4ef9c3fc373877030177bd4f264c291230641`

```dockerfile
```

-	Layers:
	-	`sha256:fe0ec5d08cb50c01afb3c379820671c61bc72bbcfc240fe9cf96bf932c439fb7`  
		Last Modified: Tue, 02 Jul 2024 07:07:02 GMT  
		Size: 4.9 MB (4909272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe95a700ff1b7ce3bb731ab785b8e949cae36604a1c2e821036e8175d2384b9`  
		Last Modified: Tue, 02 Jul 2024 07:07:01 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:857746ddca9d03dca4f7e827e2705af34b5b6199fe831eb0bfdc9ee2a8320428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231118251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5c2cb06f6139d9d28da350eb05c7c1c4c9ef3b396d93a60636181a8c0e7e47`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6dc203474b2aa45fbe7304424a3a4eae19794c6339cf0f3b64cb52937c4f82`  
		Last Modified: Tue, 02 Jul 2024 09:21:45 GMT  
		Size: 142.3 MB (142304047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab70ac79ca020b62168273b1023878e0233015f431a660da63d87cca82c8c7a`  
		Last Modified: Tue, 02 Jul 2024 09:26:23 GMT  
		Size: 58.7 MB (58743945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d730b3a854ee6e764af39f00831fe29d9b4ccb29989531eec835f27072a387`  
		Last Modified: Tue, 02 Jul 2024 09:26:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38fa48156780a99d67126e843465c5efb869222d922098c61c969396cecce4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d21aa7c71caef57d8eb38c4e92e44f97a463b1715111b9309d516b3dcfc5a8`

```dockerfile
```

-	Layers:
	-	`sha256:400619bc4450a951b95c7ce3161bb2d1abac72de92e945bc647962e2d8562f6b`  
		Last Modified: Tue, 02 Jul 2024 09:26:22 GMT  
		Size: 4.9 MB (4915628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9feddecfa77197e1a7dbc1776c75a89ce82b00331a576654a11cbb722844510a`  
		Last Modified: Tue, 02 Jul 2024 09:26:21 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json
