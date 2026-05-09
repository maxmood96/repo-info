## `clojure:temurin-25-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:2afde82e26143ef6169da12594ac3a1f8438291f49a8e40063b307480c78e722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ece216637666bf6787d9766bea5484970e0de7d376727abafd38b31d02d05451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143088535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30de1503f03670bb441070ab712e4ab0ece95173e5ef32bda1968f8b3c61cc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:01 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:01 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:16 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100a9ace8dcbc40a26712ecee68a42394613c9b46b75f051f35098c1ca07482`  
		Last Modified: Fri, 08 May 2026 20:19:36 GMT  
		Size: 92.6 MB (92574572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29051eed9fb1afdaa1c903c501819d6bd39ec29e40466ce7238b166648f7e962`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 17.8 MB (17759535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03615be620330dd99527f684063c841e19b580d0194d6380b795175354199063`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4334086f140183e683e44e19af8c6365bb59ba4db14f77f5d3f725070bb57`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a90ec20239007702d8bd6ade9521bbc7be90bdd3b90986209363dd6a0db42af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31559863a54ad9357349366a3e08ac6761982354a6489fde34e18a70f80cca7f`

```dockerfile
```

-	Layers:
	-	`sha256:540f4ee2f9ce073ff8d96cbded0f78c80902090043d24604cce741583a8ab577`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 2.7 MB (2698733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc09bad3cf40669731b46e513bdefec20ecf736eadddd885b86efcb157368c6`  
		Last Modified: Fri, 08 May 2026 20:19:33 GMT  
		Size: 19.2 KB (19210 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ffbcacbf4057e6922522b450f0f02263db32d04153e438d4cc5c5967607e77ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141769608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6834dfccaea725a99469c8760b12c140ab4ae681d7c14deca5a05c19b747fe44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:22:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:22:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:23:11 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:23:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:23:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31052a2c6c7a34e6b9841ad35dab1dfaa0c49a562e795b25b45ad29662637d1e`  
		Last Modified: Fri, 08 May 2026 20:23:31 GMT  
		Size: 91.5 MB (91542268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171a044cd60c186883611bcc2ad0839cb0a5cdd0bbf063368f9169e594c49f7`  
		Last Modified: Fri, 08 May 2026 20:23:29 GMT  
		Size: 17.6 MB (17593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2a3065777327d25d03beac4d370bec181c30e2b2c8c750478f51d92a88cc63`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd623b46acadb614f19e5e3b6976fa4e09ba670a5b55f404e1e75a9106df7e2`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:343ee3b1225217ebf1fe08aeb2aa8151360d1506f099ef187a19c8a821211c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3072dd7a28d1ed67618c59f6c7caccb1aaa929b60f7d84ed8f005ba837cbbe13`

```dockerfile
```

-	Layers:
	-	`sha256:05b63ca7c7cbb471ac51bfc1867a338c92d91f64c6482483a842fb6343ea457d`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 2.7 MB (2698369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbf81033b192fcf2670b6568379f2732e2417c3ce0b243b50a9f38ae14c539f`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e1061b778f649da1afa496cc2ec32e96dcbeefbaafbc0d4b13658d252f4beb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19112901749489d98c7099c6e2af3464644a8e241cd078a9bc09826ebda34ca1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:42:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:17 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:42:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:42:17 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:42:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:42:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:42:42 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:42:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:42:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:42:47 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:42:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d1c7548cf004fea430b1528d91b72c7b0058d926919d1835a7b351081faec`  
		Last Modified: Sat, 09 May 2026 02:43:20 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72f726dbab0d412bbda9472c0073bd1341aea89726fffd61da3ea62505c86e2`  
		Last Modified: Sat, 09 May 2026 02:43:18 GMT  
		Size: 18.0 MB (17961357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c5a90e4f55a043054c6388223147a0fe339e684eaef63ec768029465e45581`  
		Last Modified: Sat, 09 May 2026 02:43:17 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee804b89bcae8a135057f59b186e797d594850024e7a2d73d9b841a2d7c41653`  
		Last Modified: Sat, 09 May 2026 02:43:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:55d9e28eacdd32948e5a732d795e61c44bce9122a9431155f4b63e6cebd9d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80570d07d54f0c712d012965d032d4342bcf756ee16a042bd62b7234da0494e`

```dockerfile
```

-	Layers:
	-	`sha256:ae325d08b80e328a3ea7bfcad35ebad7ce8c1eade0468a326ab55aec67e23090`  
		Last Modified: Sat, 09 May 2026 02:43:17 GMT  
		Size: 2.7 MB (2683890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d4b516a5996caa6a6060fd00123a4a59392d5e625a2e229f9d5b94f4951f30`  
		Last Modified: Sat, 09 May 2026 02:43:17 GMT  
		Size: 19.3 KB (19267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:74463311f88999e00e3eb5ef5b4230acb974a51c787fd2bd9b8c752faabf53f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137252085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb803ee88b11f73ef7bb2eaceca123a88c7f6c96bbab92263125b85dadd4a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:18:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:18:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:18:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:18:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:18:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:19:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:19:09 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:19:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:19:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:19:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:19:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2a98e90054a6c9a3c4e497f6656030195d43c38235d9e7c561af6ea94fc09`  
		Last Modified: Fri, 08 May 2026 22:19:35 GMT  
		Size: 88.4 MB (88420316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3966c37e95f2cef5eeafdb81c76199edf31dea2be63d090f3771d693622c33`  
		Last Modified: Fri, 08 May 2026 22:19:34 GMT  
		Size: 17.4 MB (17421981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152785f569a9939cd3e65cdf6c919ad475c171c11e693f92a315cd29f76dde1`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bd3ce40ed185361313ba94973634d7070666209fccccd5266fa1257939ab0d`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba102cc0ed7d0f6e8fd3037833904629132721b993579802c6ab930472541adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a629e9fb78cb3e0b827531a05a7c861589644b92ef1044351d9382399246a0`

```dockerfile
```

-	Layers:
	-	`sha256:be6054c2a0f3d8d4ca5264f7e22f326ddd533e42be93ac740bbbcf3d64a50a35`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 2.7 MB (2675109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fb7ac65835c86af611540df28585460429c758aeb81f7437e5696b17c5e1ad`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json
