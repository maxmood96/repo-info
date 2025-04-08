## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:f2b044cf87a378579d45ff5c4e7d219e0693f700213ad43f9c0430f7fdd80455
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6e6f226576947dd17f9beebdc71ed46ec3bf0a88602c193ffe4e8a4e887c4d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255621030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d693f4ee527c05d855bb9d0c27ea243bc493220c4c050ac523dc8a3002e2fde6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4049016e7be50dcd232e5420632591bb71e18f93aef98d81234d8a3505af9dff`  
		Last Modified: Tue, 08 Apr 2025 01:36:17 GMT  
		Size: 144.6 MB (144566594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6cbfe94b27c6b1a5846f380b649d3aa493785647c086378f1d3d185216c890`  
		Last Modified: Tue, 08 Apr 2025 01:36:16 GMT  
		Size: 52.8 MB (52791262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f37129df0189edc7d42194ec02249f2e077c4a7e40618827d6a418f618f2ede`  
		Last Modified: Tue, 08 Apr 2025 01:36:15 GMT  
		Size: 4.5 MB (4514216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0e1db2bf8fb2de027907067643e1d19d80d0c415be88bb6c15f59e29b1e5f`  
		Last Modified: Tue, 08 Apr 2025 01:36:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:95b941db021385e9a7934c3ca88c3f00c6aa51ed6cdd8f09228d11c5d05f54a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6640125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b784474387d95e02352f5f5cf41d61e404eac68f56e8907d0b530f601d6983bf`

```dockerfile
```

-	Layers:
	-	`sha256:8ece4a9c0d1486644bc89465490c1a270bfc3eeab45f1a4d8a1f8a317d0753cb`  
		Last Modified: Tue, 08 Apr 2025 01:36:14 GMT  
		Size: 6.6 MB (6621702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6753a17bc861be5fdecdafd05d0425f4ad04e29ccce5ec98dc3e26527050a599`  
		Last Modified: Tue, 08 Apr 2025 01:36:14 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc19aab21cc9e81ad31cf3bd152c7727595ef46539d2fced3de98c13ef32f1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252842937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfd8f131467095532546d55ae30074a98707ba2dd9630bb6678231712d0073a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 08 Mar 2025 19:45:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Mar 2025 19:45:48 GMT
ENV LEIN_ROOT=1
# Sat, 08 Mar 2025 19:45:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac5f7c6c7c6220bb5761ec89c55fd2dae4d63edf89128d22e1e53d7cf650eab`  
		Last Modified: Tue, 18 Mar 2025 00:00:21 GMT  
		Size: 143.5 MB (143454700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7915f0e5dcc1bb398b7e120653a0f1f930bf035fbe19ec7a1fd7c89382ddf6`  
		Last Modified: Tue, 18 Mar 2025 00:05:37 GMT  
		Size: 52.6 MB (52625223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988a27038c9249ef0b8ec9b9e2e85518e4139bfbdbbf603cda231e3816a03c47`  
		Last Modified: Tue, 18 Mar 2025 00:05:36 GMT  
		Size: 4.5 MB (4514192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2816b22b2c04bf72d7ba8a2edc59591bd4ac1b66a8f5b9633d3d2d9ca5399db3`  
		Last Modified: Tue, 18 Mar 2025 00:05:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8094c0b40e2a5e687a823a8043f716862f6a7e8cd74a8511dfd2296a94386095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6643331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6268ea076f79dc11f1a0f9be12765e1f5a69519077daac4e6837bddce869ade7`

```dockerfile
```

-	Layers:
	-	`sha256:b589ce40e9d42b467bd4745bb77f94909e9cba0212369d6e0a693ba5820010bd`  
		Last Modified: Tue, 18 Mar 2025 00:05:36 GMT  
		Size: 6.6 MB (6624787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ffdfcfd3dc2cfb4e56c5e291f89ee64ef1d9f7024ec9e2b2db0ba73f0b1c59d`  
		Last Modified: Tue, 18 Mar 2025 00:05:36 GMT  
		Size: 18.5 KB (18544 bytes)  
		MIME: application/vnd.in-toto+json
