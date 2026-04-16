## `clojure:temurin-11-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:2d29f2cfb8f2a1137f6955010480c3f5b8adaf9f3bccce8142dd1d61c9abaadf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ddcfbb0111242f38d6f92d729476c99d59ff5455813e28da4035f4dc2308dd58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195921397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11ecf67aad77bdf2590267803c8745c6eed6670da42c42ec4dabf598d99aebf`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:02:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:20 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:20 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:34 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5005f1c10bfe40891fcf1dc7c312dae85700e0aeb9520d6b13563f7423653b40`  
		Last Modified: Wed, 15 Apr 2026 22:02:56 GMT  
		Size: 145.8 MB (145806832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cc091317a785f55665e983b51279f2ab36ee784aca0c0ac0adc42a4feca34d`  
		Last Modified: Wed, 15 Apr 2026 22:02:54 GMT  
		Size: 15.3 MB (15338800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d52535042b491d71aff0da674276ce3e22268cd812dcf50da2cc7ba29d985a1`  
		Last Modified: Wed, 15 Apr 2026 22:02:53 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:550b450f321174901cfd5e01c98e651f07749fca5487e416f3f0a4d55bae6629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0247127ae2cafcb91e5aef661597503a96cb3928b1000553c692db2aa90bc76`

```dockerfile
```

-	Layers:
	-	`sha256:a090c19bd989f6a3bcf5e0a3a195686c3ade3a7b8c0b1ea57d9e22d78ad2033c`  
		Last Modified: Wed, 15 Apr 2026 22:02:53 GMT  
		Size: 3.0 MB (3047723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad9ae85fcfd0ee1be29bac4b1550ba82cf7a738c651854e33f6ecc8a8f30719`  
		Last Modified: Wed, 15 Apr 2026 22:02:53 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9cba10d89b02c7a3312391330e65ac422480ca786ffd86f86a4046996f1fb381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191090500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d27cd9ec8b98b1170477e339bfa8c21a22915192aa92b8d528aa2e2531b5ce`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:13:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:13:38 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:13:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:13:52 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:13:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:13:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d018da6e9f937163868e385a92a9dd5798bb293d905b146faadfc17f901a15`  
		Last Modified: Wed, 15 Apr 2026 22:14:16 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539be53b48db36bb5d233d4d5a0a3975e0959826d0a5d8daf737a031062fbb00`  
		Last Modified: Wed, 15 Apr 2026 22:14:13 GMT  
		Size: 15.3 MB (15327217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac3e0bd657bcd345c5c32838299fb67dd80b0b4c276fb221d492fe379f42dcc`  
		Last Modified: Wed, 15 Apr 2026 22:14:13 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:648a837a514c7e6a152ff497acff3ccdec5464e364cad7670ead636a810b1452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f2d4900a3e6d1aaa9b212a06492d20e266f9b960e045850293a8aa54a4bba7`

```dockerfile
```

-	Layers:
	-	`sha256:07289bfa84470f20becb0afd9fa39f5992369a63430dfa433df5c25c0d362a58`  
		Last Modified: Wed, 15 Apr 2026 22:14:13 GMT  
		Size: 3.0 MB (3047950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a271a97f0bf9e8013174054c4c2714581f08158fa1e8fe9202b249ffb902b0e`  
		Last Modified: Wed, 15 Apr 2026 22:14:13 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json
