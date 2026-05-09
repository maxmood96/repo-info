## `clojure:temurin-26-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:dd04f537181d1c1ae593fe17ddd59f1f2233783c2c9dfe059fad88377437bc78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:db66d79a51904812f25bbf9213342f1e0bcd334386be0902f57d04d5280272fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144570654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ed0b4576b43b38d69363c5681986902603fc5d26d85f7f8a0425d30a5b1cb0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:20:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:12 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:20:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:20:12 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:26 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7120785b359a34c6f31445bf1b899f5275c8a5735f9c47aafadd89d4c71c2f`  
		Last Modified: Fri, 08 May 2026 20:20:47 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9faddb39a25cb20523f402ee77ce167d9f909f989d6a539b13e9959a60235a4`  
		Last Modified: Fri, 08 May 2026 20:20:46 GMT  
		Size: 15.3 MB (15338823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af9bf08c4d55df969d1345fa98c515e6bdafe05f4de8260fe0b8c7e99aadc50`  
		Last Modified: Fri, 08 May 2026 20:20:45 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb767c641ffbb031122efb0781bf7721edadde7788a84f6fb0e792337ef9ee4`  
		Last Modified: Fri, 08 May 2026 20:20:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d86874b9e087c3cf1d435d3683fc4d6e062d03a2bf93ea79d2acce311999e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5dfe837ec2bc73834f16edc6ea42b9b30fc1eb31d6fc38c719b48a11e58bced`

```dockerfile
```

-	Layers:
	-	`sha256:2a35c0b5b9c2706ec71cc360bc9fb103002f3f92b56cf76bc43db1ba287c2fb1`  
		Last Modified: Fri, 08 May 2026 20:20:45 GMT  
		Size: 3.0 MB (2993086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9471acee4065d1dc44aa0884d92c6e191618df649233d89d6e5150eb881d77f4`  
		Last Modified: Fri, 08 May 2026 20:20:45 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9e06885b0f1f33ad33ff95ffa933a865478f15d4ad990e532ab3ec4ea5a115b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141983126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e2f6576ac4e6557cd99e2c318347662ae6348b2d1e5c6db3c71d3d73a54cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:24:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:21 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:24:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:24:22 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:24:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:24:35 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:24:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:24:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb130dbff6c49733f9e912bad8030d5827829bcba29a63166665189d84332927`  
		Last Modified: Fri, 08 May 2026 20:24:55 GMT  
		Size: 93.4 MB (93395166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b17c17b2347f66bee23ab1e7d8626fd9b3408b8177ec5a197ec4fbc6e85e88`  
		Last Modified: Fri, 08 May 2026 20:24:52 GMT  
		Size: 15.3 MB (15327236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3d8dbc274da3c5a3fa849fec7a8fc1070f006bbcbd246e5758be9e4f267ec9`  
		Last Modified: Fri, 08 May 2026 20:24:52 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f15a27428634c8b0819cde328e3d0fd5fc3bca17cd9cb64948e3ebeaf3d144`  
		Last Modified: Fri, 08 May 2026 20:24:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b00d9b244275e0b423c43267ce9058acdce660e9b2643b329bff163ac3983c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6511361f7ec5b7c2a439db749f5fc60936da619a34970cb0974fc13f3b7a13e`

```dockerfile
```

-	Layers:
	-	`sha256:f276fe9e4f9eb38e8510b1260ebfa4a108e07fd5a7a18a1ddc37846d31683d3b`  
		Last Modified: Fri, 08 May 2026 20:24:52 GMT  
		Size: 3.0 MB (2992692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f3e2b0626594db41c583dfc67800eef6f93b85320c60410229cc84bcbc59ef`  
		Last Modified: Fri, 08 May 2026 20:24:51 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json
