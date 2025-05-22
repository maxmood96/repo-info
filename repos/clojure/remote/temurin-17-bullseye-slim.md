## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:8f8b8710e47fa987a141abdf301f42f662094c41ee7529af041390ce212cdbbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d6812b31cd7ee66fface65f98cdb44ecef8f0a4dbdc02e8be6d36442fb983d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233886022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043461d731d62d038ea9916c585dc9b2de9d153848f547cef9b62bddb561aa20`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad752d778bea653e830200e896b46c5b8e9e344c11ec9571ef3e28d39700df46`  
		Last Modified: Wed, 21 May 2025 23:33:09 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc74d9e963c0f7d2e04769e6484efebe4ff1c5d20132086a528f80ebf40d572`  
		Last Modified: Wed, 21 May 2025 23:33:10 GMT  
		Size: 59.0 MB (58994084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684ff8e4e7ffb255129f39a0e044a882e2810e05ae80de784e599f1cbbb81e67`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3191b92dcd9b4812b08cbfc89c5ce4fa26e0f50b288073d29a8b8914504914`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb66b9d1f030d6d0462e8018011413c5f94514ef8048e20925f77f02c632fe07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5182869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5e16c9740919e9a6a4d7229a5e685d65fbe39fd77844680ff4364512c42940`

```dockerfile
```

-	Layers:
	-	`sha256:f76fe00bfedeaf92ff87013d0ec4da8392b59b74c76b4b67d3005b32200b9384`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 5.2 MB (5166990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba45d3f97e92298e62d895cf7a6da6cac69206ae7733a8a00c8abc5889475cb7`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3abdd7e7ef084cef93e4f2f48440b2e25feab6484c755c8a161dd1de7ca1aba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231385807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7312dafc6531de0d96ef3028cf9859ab0e4073d30c0213a8fc2db549265bc94d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ae675387ee815f1cf9a4635844bb9773f6f4159669c6ceed3939975ea5d1a`  
		Last Modified: Mon, 05 May 2025 22:03:24 GMT  
		Size: 143.5 MB (143512640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e49d5bf8561b111ab4b32bcf1f994116add29b8ebfe31d40008de774ab8d5e`  
		Last Modified: Tue, 06 May 2025 00:39:04 GMT  
		Size: 59.1 MB (59127482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ad8e135aeb9dfc2d1f9ff84c1c4ed1554ead13e951b3bb4b4e1aafcf8ca35d`  
		Last Modified: Tue, 06 May 2025 00:39:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27944530a67621ffe0a2c46389f78e9ffb3b5851803d74a5af960f7015912cff`  
		Last Modified: Tue, 06 May 2025 00:39:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2ff5b4e4c3919141eecb131f54459188ab66ba5a7b1ee30694cfaa6a0c6105d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdff02a19f2a4a81c16b93dab282872f6600a55860be678e86aa884f154aca50`

```dockerfile
```

-	Layers:
	-	`sha256:7f84c9ff1b7700d267cd83ecac33a814dbf8887b845564c0bf377c449f5dbfed`  
		Last Modified: Tue, 06 May 2025 00:39:03 GMT  
		Size: 5.1 MB (5124799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b7319c31b3e83bb327f16103eda4f4b7a1a1a37f3776241603f653c05b96f0`  
		Last Modified: Tue, 06 May 2025 00:39:02 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
