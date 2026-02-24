## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:f3b4b832f6a49f2c354bd74dcd14980dc26d455ff559a4ba8783bcce803c15b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8240cd660729f809353ba1d983fa0f9dd63eb8bfc835e88d482a6e32c85e668b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195921709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9ebe55e743ddfb31fa7e2ca9aab8446e546bbcbeb8cad10ed3bfbdb5317a75`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:26:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:53:40 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:53:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:53:54 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:53:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:53:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b774018ac372017ba46a5a8faebcf0569ece034205384171ddfc56750c6c3c9`  
		Last Modified: Tue, 24 Feb 2026 19:26:51 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c655a1d5a059ac232b16e7153e11d00a26024fa9df5112e3c4fabdaa2538de38`  
		Last Modified: Tue, 24 Feb 2026 19:54:03 GMT  
		Size: 15.3 MB (15338839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07466b211a6d6cfa5df3347c4c8ae3b7db10b8772923495bae4f827b45988bce`  
		Last Modified: Tue, 24 Feb 2026 19:54:03 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bacba743c52da6129bb5b43bcbadbdd540d417be2e997dc09ae913f066c68d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbbb36679de5b27ff3463cb274ee0e95788d056eeab364002440bb37426a774`

```dockerfile
```

-	Layers:
	-	`sha256:fceb279ddaf56321211f30e51f402b2f91c9f6473592010713907548b85468d1`  
		Last Modified: Tue, 24 Feb 2026 19:54:03 GMT  
		Size: 3.0 MB (3049347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1045f73e8a71096ab4dce28790141c3955848f980adc7f832a6e2ed9e1ef5236`  
		Last Modified: Tue, 24 Feb 2026 19:54:03 GMT  
		Size: 15.6 KB (15611 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:39895b9474be984aac3a24530a370cb48b7ac783f2c0da8829bef6550de046bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191090903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7c908507ccf687f5647b981d61ffc2e6ec3968b6eef32c3e03ea86dae84b1a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:04:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:04:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:04:16 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:04:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:04:29 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:04:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:04:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87261ef607de5b91a3b621f96c355d2776a1ebdd5143bb5a9540344e58f2ab6`  
		Last Modified: Tue, 24 Feb 2026 20:04:50 GMT  
		Size: 142.5 MB (142501445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534edcb76f5958daa0d66f6fb9a9e3975ae7bf73af0f34b0e029cfab384c690a`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 15.3 MB (15327212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207075f5c44b69c8196ddc40c9733f24493c3787a8b9ab3d7287d093b268549f`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f44be69a26e5c78425aa9e8a508891046025acf0686844fe57d1b22db770747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3971f6ef5c941b49d03eceb657073bf05f935efaa71180605e6faa64e1f1b52`

```dockerfile
```

-	Layers:
	-	`sha256:1ede17b0051ffbb3ca089c09dca107fa884c71c06b862b129be17ab3b778a708`  
		Last Modified: Tue, 24 Feb 2026 20:04:47 GMT  
		Size: 3.0 MB (3049574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c61d5fd7332679c16637827aa74223b841db3702c1960ee1ec10e34e664cc5e`  
		Last Modified: Tue, 24 Feb 2026 20:04:46 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json
