## `clojure:temurin-11-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:0ef6d93c99bd581c001d200b03b6dcfb7f90afae57517f6c51b212ddc5e7f9be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:772c8e397840e81d957cd3f4cbe39f1dbfc576bb966c3de45091c7fc86138a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229806180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8099f76dd3161bd87c55e216c39bdf2a74ea37b9f426dd5cd21bf6171d0c08d6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05891d5ffcee021a106ded094a772e04d5c9a6edae3f0e29bcee742f382a919`  
		Last Modified: Wed, 09 Apr 2025 02:18:19 GMT  
		Size: 145.6 MB (145598771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed843661ea59151bd169b2e5b128b01960691ff5052875be4ffe5654128f0447`  
		Last Modified: Wed, 09 Apr 2025 02:18:17 GMT  
		Size: 51.5 MB (51465958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f745c262b70c3bdacf50caec8b017905b90660d6c95ec3b67f1ef2a83d1a98`  
		Last Modified: Wed, 09 Apr 2025 02:18:17 GMT  
		Size: 4.5 MB (4514160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7b41cfeabdc0e2f8037c0f59be7f5fc8dad57c493d01e9c21f5a9e873422dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4358429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67184c28ac34a7fbba3f29b7a249a628260f21344437a70cc09c6eb81683d2e`

```dockerfile
```

-	Layers:
	-	`sha256:a0948274c640b43fb8c10c7890d4db1e110638a6dd568245de902e64054eeaac`  
		Last Modified: Wed, 09 Apr 2025 02:18:17 GMT  
		Size: 4.3 MB (4341966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2425c3952ed4735ac2ba4087245b7292ff8065e992a339ab17002c389f6cbb3`  
		Last Modified: Wed, 09 Apr 2025 02:18:17 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eb35cc752820a3f62a534429406bdab00cc975ee91c3830dddef9de42794763d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226395331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c750f5e78a91a9e17c3d1eb2ddbd58298a031b54e986260c2f479e4f2537bd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697a3f27ad7c4afeee00ac973a16df9c78d363eded18efac5e78999071abe25c`  
		Last Modified: Wed, 09 Apr 2025 17:21:26 GMT  
		Size: 142.4 MB (142385576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8550b03c2b456bbe5b64e7e15770512d32a2114152dfa2291b39304f3704b4e3`  
		Last Modified: Wed, 09 Apr 2025 17:21:24 GMT  
		Size: 51.4 MB (51429200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd107f87e3c754802ecc06606e16ff6e4da725b0ac02d26259e78caa6ef7c0f`  
		Last Modified: Wed, 09 Apr 2025 17:21:23 GMT  
		Size: 4.5 MB (4514203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75bfe7116877c40ade710bed3499b218d936147d3c44a437ae6fb0282b37b597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45b0624d5295ce0efde9d4fd723e340f953115a21cad30233d2506e2b2e9380`

```dockerfile
```

-	Layers:
	-	`sha256:389c8aed2c60cf677da3eef4d65fb378168c3a54ce6861f359eab96313ba389c`  
		Last Modified: Wed, 09 Apr 2025 17:21:23 GMT  
		Size: 4.3 MB (4348276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee7dd86bbf2212a8cbafe20ebd9a931615a76625a24a731d4df298988860601`  
		Last Modified: Wed, 09 Apr 2025 17:21:22 GMT  
		Size: 16.6 KB (16583 bytes)  
		MIME: application/vnd.in-toto+json
