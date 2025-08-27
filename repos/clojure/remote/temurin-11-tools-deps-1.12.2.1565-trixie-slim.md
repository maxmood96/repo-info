## `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:01a95c3d12a33c66b82a53cd9d1a79540d07aac719b63a6d5c76920bd657603f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7245b22940650c41418ac25b5b3b0b850e9df849ef46d2aeaea2a73e330b4b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247414975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5fde8a4aa74fc51efd3e86aa0757072912a3678bb765ee279cc306bef67893`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7317ca72d8b623cdca20b6b0ee6bac7abdbd3cc2b7b0f6b69af48e9a911c1f0`  
		Last Modified: Tue, 26 Aug 2025 22:54:07 GMT  
		Size: 145.7 MB (145658140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5710c1295bbdcfeeee72c37df4eae307e8450b6c409e4297cfff20cad6f68aa`  
		Last Modified: Tue, 26 Aug 2025 22:54:05 GMT  
		Size: 72.0 MB (71982905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2ff70e4d928665e4a5a8f44ec7df5fae0c42b51bb56d340e1e9cebf6f00a9`  
		Last Modified: Tue, 26 Aug 2025 22:54:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e4bb0ed4623b9cba0e7427ec22e945ef6a87dfa32791ebf8c2b5e410b474250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d929041dd652af5c4c99fa5fa791d1fb7a90049292550b8fbfa9ee978ed72cf`

```dockerfile
```

-	Layers:
	-	`sha256:89bc6c58b039b5fdeb419b00f40b7594d75ca5a3aa4e198a1e690498be7a05c2`  
		Last Modified: Tue, 26 Aug 2025 18:36:44 GMT  
		Size: 5.3 MB (5275378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:417f96f97111afce640c6f7198467145767d2f4b6ffd30bd13c13420754cb19c`  
		Last Modified: Tue, 26 Aug 2025 18:36:45 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ba662089d24a8da9407f67320329ef69f824a265c9ab53d2399f49e2692cb77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244401015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2368f5377fe433510b0eac759a9846a71aad459838b5cb712f651819f966531`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575fc3fc33f3212c68f0b4bce5426cd5a68295ab95b0f84cdc65794583043dc`  
		Last Modified: Tue, 19 Aug 2025 04:00:33 GMT  
		Size: 142.5 MB (142460557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f5eb6fb037fcf5bf1da5787e8a845cea470eff8bf42db6b5cf16797fe04243`  
		Last Modified: Tue, 26 Aug 2025 17:40:22 GMT  
		Size: 71.8 MB (71803769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be3f990d9174a9e9c67973296344f3f6c40d08c9b7f4b7a4d8e88cf1549a02`  
		Last Modified: Tue, 26 Aug 2025 17:40:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af6e5ff9e6c6a6980247bef9c95bbfc34dbc0f93ed128d001d3421fb79740675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee694cf8df6f6711f83bf8752dfd82e49c766c56470b73a9d67c09fcfe990e25`

```dockerfile
```

-	Layers:
	-	`sha256:a26d855c95f81fe02388f84ec6282419f63476fe18c2711666c32030a37a00af`  
		Last Modified: Tue, 26 Aug 2025 18:36:50 GMT  
		Size: 5.3 MB (5281765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3937a43a1776a270a43370884ab632a853412d8c5903a31ec20caf4d6f9a8485`  
		Last Modified: Tue, 26 Aug 2025 18:36:51 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d3b9f1d4b8b214976553ab1dea8eec0d738a93905206058c6826c9e7da85479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243836953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cadbb3a360615d3b278ab30bbc1d2c636b9fb17bf929a16ab0a3efa06458b24`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d40da39c1e05974afe8d7dc7c9ee044827e979d78538852469cea98a61ef8ff`  
		Last Modified: Sun, 24 Aug 2025 06:19:53 GMT  
		Size: 132.9 MB (132853302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b925286cb7e081b4b8b05e18cca4e8112e43cdcf86ed21f836f6b0fd0b44e07`  
		Last Modified: Tue, 26 Aug 2025 17:51:49 GMT  
		Size: 77.4 MB (77388791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb168031d7dff9f8f2988384a67f2b30e186dcd0f56c1d30bd34efebfd06810`  
		Last Modified: Tue, 26 Aug 2025 17:51:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f30db2465180fb040e0696a59ddec9c80add349d7fade8b1d27de83e9c4d85de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b966c772220b4779b3d5c7d3697b267de0d2243675d0f1f4fea5b357b16a57d0`

```dockerfile
```

-	Layers:
	-	`sha256:7b1519ee0a3761eade276c3ab8b6ded6514c6c31d8e48ac399b191b8510a1dbb`  
		Last Modified: Tue, 26 Aug 2025 18:36:56 GMT  
		Size: 5.3 MB (5279134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81435949029dec1a446e185e1338c54b29ab6ef7258bcf29e65e474d90f467fb`  
		Last Modified: Tue, 26 Aug 2025 18:36:57 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7ed14fa96f65d08598c2c9256431cc7f143a1ff0509ce21a80a440012dbc1362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228405707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc202761178496dc14dd4e1681ba95527d1b31c2f75fac7fe536c40f76d7a7c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1941fd0e14005c4b3a4ceb8cc960f8885714e1070af13e09c47c856d2a283b`  
		Last Modified: Sun, 24 Aug 2025 06:20:46 GMT  
		Size: 125.6 MB (125622148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb311665e0ad134792bff4ac312d7c052ca73f10dd3a6bd3c8e7288beb3ee3de`  
		Last Modified: Tue, 26 Aug 2025 18:02:40 GMT  
		Size: 72.9 MB (72949853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5aa42f9258b96d9c6c69d0ff6f731dbabdf3c0b8a04be14c04af3f91eca614`  
		Last Modified: Tue, 26 Aug 2025 18:57:49 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e8e0e01c74951d17ccdb4c64c0abf44fd6bfed44660a8bbfd0675036496dd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688d8682fdfb3b6baf0e5015affbaef9b1cbd0b0ef8a2703d19aa0ff0149eca0`

```dockerfile
```

-	Layers:
	-	`sha256:f7dc44112556194c1ff42245692fe28f4492bb31c540ed3e643dffd4ee875746`  
		Last Modified: Tue, 26 Aug 2025 18:37:02 GMT  
		Size: 5.3 MB (5271306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ee2a062a4511eec1e146303e8ea04a7831344aefaad975dc19bfbc59670d4e`  
		Last Modified: Tue, 26 Aug 2025 18:37:03 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
