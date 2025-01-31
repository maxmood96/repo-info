## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:d33ef838690645bb4a794f45c4a158833933531e925bf9f1aea261ca5069be92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:18acce21aea03c34805fdab03d1284eb9de41a1465a197d89843b73ca1889135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280499705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4dd7b8337ff929b2aa196463d4c2f10baa71febd8017909631439b71a34153a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593cf18e65985d775125985accd97e7443c2a169a9bcffc8d003bb7a2d6ff706`  
		Last Modified: Wed, 29 Jan 2025 20:27:45 GMT  
		Size: 157.6 MB (157568670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9054253656cf412dbf7e7bba66110e18615a7ed2babe779d202d75a2e8cf1d77`  
		Last Modified: Wed, 29 Jan 2025 20:27:44 GMT  
		Size: 69.2 MB (69190829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0481fae1c3a360402a6d8b2f2cab1a4cce0af9f02852a73a39326f9ad48cb55`  
		Last Modified: Wed, 29 Jan 2025 20:27:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6d3d2c8de082457503c9857eb47d65710d5c16b0b324608b2e0809d9e1178d`  
		Last Modified: Wed, 29 Jan 2025 20:27:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c2388a25db49d53f0be8d37d1a85bd12900591167fdb8c5cf101a68424ed40ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1f72219912fd48fc7435853bde317f6557783adb3be386343a76b37fc532b0`

```dockerfile
```

-	Layers:
	-	`sha256:c6481516f70bede6ad9b3c601fe87a8033a9ade991230e57fd494d64a2fa5b02`  
		Last Modified: Wed, 29 Jan 2025 20:27:43 GMT  
		Size: 7.2 MB (7208335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a70b71285eef8fa87d777de828c45daffe3473255022d866c5556bd0424abc`  
		Last Modified: Wed, 29 Jan 2025 20:27:43 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8255790296851cf955bf0575b3f7aca2b59f14b697a869bb8f3a6ff660060605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277351643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbea394417977cbe8f9efb26bee5fbac87ba6b56c49873428e2ebd772f7e752`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eda5fd7e4740de452e0eb0971c85821bbb430f489028d0235cb971ae002be3`  
		Last Modified: Thu, 23 Jan 2025 02:55:26 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579f96f92a2a9601abd72debc2cfe9ba5f1889ff8a86a7995568280aeb6f716c`  
		Last Modified: Wed, 29 Jan 2025 20:54:31 GMT  
		Size: 69.3 MB (69311473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde023fed25ce6a98b1470726270115d84b6fb9af43aa4abd17c9859fc54c29c`  
		Last Modified: Wed, 29 Jan 2025 20:54:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aed9b8d6aea149b9ee318e985bd0cfdce882a3f33c7e0829d2715f8653778fb`  
		Last Modified: Wed, 29 Jan 2025 20:54:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6ab50153ab8b1bba5904ae862a4df1a7ae8d0030cce978926024bce8d009f239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8d622ceb8ed59c916aa534b503344d9fd4d2674dcd52cf9a8c5fb5c9f073e7`

```dockerfile
```

-	Layers:
	-	`sha256:3ad0ae91b2aa3e70d491e920b58b10744524b49105a6e6d9f839cfffd5560e7e`  
		Last Modified: Wed, 29 Jan 2025 20:54:30 GMT  
		Size: 7.2 MB (7213458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828983d8cb5d579f5454fb04091e23431f82abc543bd7e5dce532c99cb551dde`  
		Last Modified: Wed, 29 Jan 2025 20:54:29 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
