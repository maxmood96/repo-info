## `clojure:temurin-11-lein-2.10.0-bookworm-slim`

```console
$ docker pull clojure@sha256:afb4acbfea8c9e28a8d17738578513c8b4f75373b2a3b39ff929d1c0f227dc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.10.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:707a415c2aa121cd230ee7b92292887f425411ce7411a3f6f6ba09da2c384975
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193789739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dce9d3810088d640a180dc1938183d79274bdfb331517df85190b4ca8f64f3f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:58:38 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:58:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:00:50 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 11 Jan 2024 05:00:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:00:50 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:01:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Jan 2024 05:01:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:01:05 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jan 2024 05:01:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Jan 2024 05:01:08 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fbe5aa6b4fe7cefda24d4cc70b9d7345aa6d93be5fe42f5f6c5e49702b33a7`  
		Last Modified: Thu, 11 Jan 2024 05:17:59 GMT  
		Size: 145.3 MB (145266341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aacc13de295f3bdae0f5778f87ca2149e9484d3f915ba2e511a898b583520d1`  
		Last Modified: Thu, 11 Jan 2024 05:19:04 GMT  
		Size: 15.0 MB (14998191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79abb09d8cdfb0d6c5996d963a4ea4e0b6a47885804e7e1b60afb2dc438acdff`  
		Last Modified: Thu, 11 Jan 2024 05:19:03 GMT  
		Size: 4.4 MB (4399286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.10.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0367e22fe40e9719924189c3e9606d413e03c94a237a9be74faf37f44ef7128
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64492fa296bf0e421ea3430e5151b3705604db697fa37ff507e1c69f88c0c904`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:31 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:01:17 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 19 Dec 2023 07:01:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:01:17 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:01:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 19 Dec 2023 07:01:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:01:30 GMT
ENV LEIN_ROOT=1
# Tue, 19 Dec 2023 07:01:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 19 Dec 2023 07:01:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3caa98fe64b6e771f2487121c32bd24ed3c1efe0b70cd6eba73ff5a9db11b6`  
		Last Modified: Tue, 19 Dec 2023 07:16:03 GMT  
		Size: 142.0 MB (142001823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f2782143a6f941cddb513a5fd899dd875be31c5ab7bea0cfb7efe17552771a`  
		Last Modified: Tue, 19 Dec 2023 07:16:54 GMT  
		Size: 14.8 MB (14820134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ecdbce3798ac21b7ef9eb0038a00a2b3f76864a67c4e375ba3245631044d81`  
		Last Modified: Tue, 19 Dec 2023 07:16:53 GMT  
		Size: 4.4 MB (4399204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
