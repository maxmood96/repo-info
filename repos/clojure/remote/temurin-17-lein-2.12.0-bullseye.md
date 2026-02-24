## `clojure:temurin-17-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:b6c4caf2c0d5f460c2284bf5b04d1245b144e412959845a34ae6ee868f51b425
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:80d2c387c8530efab657e65ba1b69a71841c4fe79127014542c18627f542b28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220532864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6b6606c0c0857817dc749f1622d2d9978e6ab406e87e09c08704cefc014ce8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:54:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:54:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:54:40 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:54:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:54:54 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:54:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:54:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:54:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:54:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48565a06d758dc039c80eed53e01ab13b1ef51d24af748a75deabf3691baf81d`  
		Last Modified: Tue, 24 Feb 2026 19:55:16 GMT  
		Size: 145.6 MB (145628702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73dfc173956c9c8efe506dac918b43740b51cc2b7b4db899e2768d4b3f7e4db`  
		Last Modified: Tue, 24 Feb 2026 19:55:13 GMT  
		Size: 16.6 MB (16629561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ec1c7f380ad4d7aaf998cceebe8677c8f2d57d6b47f346ccebf392f9f20f35`  
		Last Modified: Tue, 24 Feb 2026 19:55:13 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88418abb8d1b7f449520133cce14cf14555efabe3a451791c1c27ff66c623cc`  
		Last Modified: Tue, 24 Feb 2026 19:55:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3d4ebae13c6c98e52004637e8cb49d08f027f2e355462aa4d8009f03e9f32ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612fb51332ff7c1878861b115d5cea938a7ad99a5eaebcef2f30c46c1e82706d`

```dockerfile
```

-	Layers:
	-	`sha256:b9bba147986cfaf894ff72623ae5f7213e280b9364d59b205e34aba0d8c5a698`  
		Last Modified: Tue, 24 Feb 2026 19:55:13 GMT  
		Size: 4.5 MB (4487486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f0fd2b4a7392b477ccf879a04fe9908fbeb8aa4fef2aea32c2cb9662469cd5`  
		Last Modified: Tue, 24 Feb 2026 19:55:12 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:efa3c4c55032ce7b8564772fcef25870676bf57335cade31ed3d517835f24b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217829322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5a05fc8be3fb523330f84819ad89fe27f9d9686e3e0b9bfcfad43b9daee9e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:05:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:05:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:05:19 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:05:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:05:33 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:05:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:05:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:05:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:05:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595c7c14f0d2f4ba995ae5aca744b6bc8d3a34e264f1c994e3173038135e2602`  
		Last Modified: Tue, 24 Feb 2026 20:05:55 GMT  
		Size: 144.4 MB (144436238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735f9ebb6a270d6a9c3073cd49ed485f6e84f9d466a623940567d927069c6bec`  
		Last Modified: Tue, 24 Feb 2026 20:05:53 GMT  
		Size: 16.6 MB (16616524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f83998b77127fa09fba9253a688b9730328bd018a731d30fb3d054940cb87`  
		Last Modified: Tue, 24 Feb 2026 20:05:52 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5849f1504f2f0b0e2028f25950e4da911b065ad550be5e904a118cd99b015095`  
		Last Modified: Tue, 24 Feb 2026 20:05:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a5b3440f39d510a91cd73a45bc5de23413eec05577302731772b9b518a4d8c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f575b1e64f33ba11c29d1cc506633feec50202c59bb0c2de8ee345c27256ae`

```dockerfile
```

-	Layers:
	-	`sha256:ba37ec07994c09493d958764412874c00fb406aaba137bd660ba07f13c203af7`  
		Last Modified: Tue, 24 Feb 2026 20:05:52 GMT  
		Size: 4.5 MB (4486460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8043ac1a0a699b291116d3b2be75d04bf1bce42b97b7e633ccd836abd0d13a3`  
		Last Modified: Tue, 24 Feb 2026 20:05:51 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
