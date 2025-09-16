## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:5d9f34d7e4f1a382cb68a723b97fb194da8ca68a0a973fdf3ff63034a1c3b1e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:949edf272670123941d68692ea612cc9695f3209b1fbe2a1ab4f6257b191cae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178044036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d700fef4c2a747acc326fd6bcd85f2d574504b4b33f5c370895dc614e850c1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bd097d50d91d9079b863d48585856bcfe1226afaf88c87c9401ddf39f9a2db`  
		Last Modified: Mon, 15 Sep 2025 23:25:10 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830364eb1927cccff2e640a336b9e3fd92891e2abdacd56bf9574404b44b89f`  
		Last Modified: Mon, 15 Sep 2025 23:25:15 GMT  
		Size: 69.6 MB (69556690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f326e877e1e20827f64b1c91b1c0ee2d69304ee34ee72fc8ff84b40248479d90`  
		Last Modified: Mon, 15 Sep 2025 23:24:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2c1766db4b6e689f07c7d9b8751d607675dadbcebe7640a54ef026fef7ed7abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a23015eddb8c0aa52134ffb89d8f06100b90285f56199f4b7509c2ba3e12f09`

```dockerfile
```

-	Layers:
	-	`sha256:46831b11857b20c1aefcf2aeca8f45dd5b61a3f40bd10af4bfcb462a786a8ad2`  
		Last Modified: Tue, 16 Sep 2025 00:47:47 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aaf219005353dc9578a15c90a283b2ab7f80209038e4cdb86c0687fd5d31346`  
		Last Modified: Tue, 16 Sep 2025 00:47:48 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6cd55ff6b4b9ed9a53c4275fc50d80d39704b204a2b798a02dd75b83dd5af8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175768693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b30bcd50d0c631bc30646f361eedc92c2c1ae8ccd5e54091d07a0606d46f0a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fb745d07b3773f637e4dab362713a4f2c21469689c788aa3db30bfda6212f5`  
		Last Modified: Mon, 15 Sep 2025 23:25:13 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a731ee0730ebf4b8f6b8ca389ff76f3c5dd70d954666415c8bfee38ab2072fbf`  
		Last Modified: Mon, 15 Sep 2025 23:25:16 GMT  
		Size: 69.7 MB (69684073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a87a39f150ad3a6369df7c1f80b45e885d4ac98c47852ce897121796777548`  
		Last Modified: Mon, 15 Sep 2025 23:25:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6f689294fccdb449c6d037cb867283176cc9084819e6527c1a14c9fb12d31d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b62bd1a50bd2afacbc889000d0a756c08f517b78140be59a40c75ff382629c`

```dockerfile
```

-	Layers:
	-	`sha256:d790ed98fc988af049767b248d901d91f6a49cc1ef16c065ed6c72ee69c1a966`  
		Last Modified: Tue, 16 Sep 2025 00:47:54 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:877b3a4bc664398e3dacc79566c19444fa0d084b70e562d7ddc1013bae04de6a`  
		Last Modified: Tue, 16 Sep 2025 00:47:55 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json
