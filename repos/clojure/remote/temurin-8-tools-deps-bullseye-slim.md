## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:fdaa9f5bc75a0f1fc658111c8ce07ebc0c99145fa5d6ee57b05dad89161e50d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ad71d529d7eb31dc778b0f4dbcadbd6275b0e09d7725977c96a038c8d59e0a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144142251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0165dc2eb46c24dfcf8ebc73045854c6ed232c784ac26c0de817a1a0f80a8162`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:19:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:19:44 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:19:44 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:21:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:21:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:21:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdde6dd3d568f99e2e1cac45dc22139c5734427aadb2afc3d95ef2a1d068226`  
		Last Modified: Tue, 13 Jan 2026 03:20:23 GMT  
		Size: 54.7 MB (54733365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c24ffcc5dd662c4c7b2905a2f5b3a4d7eb4abc85cd9df92b17fe6fd536d14a6`  
		Last Modified: Tue, 13 Jan 2026 03:21:32 GMT  
		Size: 59.1 MB (59149746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4ea35de65d77a696f444db6c96ad9f5a9daa200ab05f0ebfb8466abeee115a`  
		Last Modified: Tue, 13 Jan 2026 03:21:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba111ab02bfa695f22a9c0b2c6744bef51559803e2480f60d9a16a26ea2ebf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f985dca738cd6acb22c879fff3fbf3448fa21dbab01164aa39cb7fb6667c84`

```dockerfile
```

-	Layers:
	-	`sha256:49e68ba28852d1e974cfd1c5befc5f6633b4c6eee7ccebf941b61d7181cfb93e`  
		Last Modified: Tue, 13 Jan 2026 07:47:57 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d163c8a0e16dd45f18cee301b9d45086cd54f6287a5b30dc72bccb0ebea18c4c`  
		Last Modified: Tue, 13 Jan 2026 07:47:58 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:496860f40c3c84b966edf060a200ba0f34220f2a5146d047cf84d104fa0b4835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141848033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b25a5fdb39096b37985f4db6f37a1f96b568497b7b41d66ed9ad04a7941f76`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:27:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:27:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:27:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:27:43 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:27:43 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:28:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:28:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:28:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d66b29b89581f642ede25d15ff8ce699a231346b6b2f56758aefde5fc72b9aa`  
		Last Modified: Tue, 13 Jan 2026 03:28:24 GMT  
		Size: 53.8 MB (53815012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77996fc79366366456db788b378764164f02f926883252f7d4b61ac874520a50`  
		Last Modified: Tue, 13 Jan 2026 03:29:23 GMT  
		Size: 59.3 MB (59283859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305481e110843d23cba4f8594309f3de7dec0dc74210b83567d923f39c8dad7b`  
		Last Modified: Tue, 13 Jan 2026 03:29:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7964c63a0deea627c88171a8f3afffd2799a38efb37947b8ebac482607dff40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c1ff983fc53dd725d3394b95df7ab9bdb84d4edc2a50d1385732ef86015ee9`

```dockerfile
```

-	Layers:
	-	`sha256:12575160f48967e4ed6ff47c6e9d5c621f38b60d78caad783df2e6082d3b7295`  
		Last Modified: Tue, 13 Jan 2026 07:48:04 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d038162e5c53afc8f0a89965b14625338ecf57824be179d136d7335d274b1a4`  
		Last Modified: Tue, 13 Jan 2026 07:48:04 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
