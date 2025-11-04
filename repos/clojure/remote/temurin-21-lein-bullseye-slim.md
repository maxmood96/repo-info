## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:80237b0e3ddfe8e9e4e71cf34f56719253cb70ff5e4d04822130e59c6875b95e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6096e21bc0cb0ba8444073c6617ca935b1bef93b5499c1f9d9e5c7cb65a653ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207900189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6744a04e9c99b6864a754a29d5d6dfa7f23d5c89b611c5001637076e8ca9df10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:55:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:55:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:55:39 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:55:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:55:53 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:55:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:55:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d39eed2a0d48666d44a1c50b35fdddb42bd8d7d413481e371fc3e0278bbd52b`  
		Last Modified: Tue, 04 Nov 2025 00:56:14 GMT  
		Size: 157.8 MB (157804741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002c502a229a9348f015c2814b679d2e062de82286907af298ffea15a429b84`  
		Last Modified: Tue, 04 Nov 2025 00:56:32 GMT  
		Size: 15.3 MB (15318713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690861abf22d8d856fb7a5f76373123972c7f03e463be4cb8db8a6105e2b852`  
		Last Modified: Tue, 04 Nov 2025 00:56:28 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac52427eaa3fabeca46eb2ef6c6e4f4ffd71db4b4c50eee1b39c73d81cad2f8`  
		Last Modified: Tue, 04 Nov 2025 00:56:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb5bf0972e1da00b69432761887154b891a02f50219bb17d38e9bf0515daa442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5a69adb1416ef11b2e0cb75d938feb4f51813e05e8e76af55071098858e0e9`

```dockerfile
```

-	Layers:
	-	`sha256:936291edc987b9df94a548e4847c5d8b53c830a68a2407c0ce720a915caba67e`  
		Last Modified: Tue, 04 Nov 2025 10:43:27 GMT  
		Size: 3.0 MB (3021010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c8255cada7f939f9b78fd91da0feb5d5fe5c8fb54883196a826250a54513625`  
		Last Modified: Tue, 04 Nov 2025 10:43:28 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54629594303aa6f67985370728c9b8342089e216f2dccf476d9d8ef5d45a9c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204653814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df9631c74167a999ec45d66b68b4efc2b1ec3abed47e5307b67f0fa3985c268`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:56:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:56:33 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:56:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:56:46 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:56:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b031e840dd9e529831c795ef825053a21959656d5f864cf60cc17eac89a5bef`  
		Last Modified: Tue, 04 Nov 2025 00:57:10 GMT  
		Size: 156.1 MB (156081257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7d282dc6ccfc63ae73fb4c0e9adae79ef7383a62141ca9d133b114eea9fe77`  
		Last Modified: Tue, 04 Nov 2025 00:57:14 GMT  
		Size: 15.3 MB (15305827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c0f20eff0faa1d88907f0c0c74c2180024360ff65881b6b93e1dc5bf9524c`  
		Last Modified: Tue, 04 Nov 2025 00:57:14 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bebba8a153053f7de1d7fb678be12a25ad2979936570f0a16a5734e2373eed8`  
		Last Modified: Tue, 04 Nov 2025 00:57:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:371a1af095330d8fab6e0e4ad07b80228c98c357a81e572d9a16b8abb41e2a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e05fb17044f180d1db92bb33fb7ce0a6eea0ccdf4e8eabfea5e5d1cbcbc31d`

```dockerfile
```

-	Layers:
	-	`sha256:6ad07098de41213f789968fcd318a91765a1d204c85ad27b9537162bb405e163`  
		Last Modified: Tue, 04 Nov 2025 10:43:32 GMT  
		Size: 3.0 MB (3020619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abec305125e65ae31c8aa86b477910cde09c0564e7ba3c2a56b150b07465bc16`  
		Last Modified: Tue, 04 Nov 2025 10:43:33 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
