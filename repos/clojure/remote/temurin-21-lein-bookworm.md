## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:0235a97e8d2caf7c1c8d7723f271b1ce289a6acee186f0c75dcff17b0302608b
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

### `clojure:temurin-21-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:978c911a01f815fa61fda0bf03853475c8bac029a2c03e105787f4014d888ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230666613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e0e61a8990363234b761c7c4c58ab2846dcd7d45a8d876dd36484b04b106b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:58:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:58:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:58:57 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:59:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:59:10 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:59:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:59:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930bc417d09576f8fe90d17d3184225b0988d0fd97d77fe8d4a89039591e4ef0`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 157.9 MB (157857094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cb81c6d68e825398e5a40cf5ac3b351e3bbce99483e0e985ef5c731f5bff2c`  
		Last Modified: Tue, 17 Mar 2026 02:59:29 GMT  
		Size: 19.8 MB (19802770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7a93a89efa1f071e10fb87f8f4b467c72580df3ba659a337a76d41e4f78c0d`  
		Last Modified: Tue, 17 Mar 2026 02:59:28 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d67d0ffb6b386dba0d6066be1c4418669280b1fd6d04420d1093c36a7c13a36`  
		Last Modified: Tue, 17 Mar 2026 02:59:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:166a215c999595ee416c4ccd2537d816402005c4c4f68d6d49c6501e65c77181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541a030944c8959311968bedc21befe7d36fd8d2aae31663c1dabb23537d42de`

```dockerfile
```

-	Layers:
	-	`sha256:5725fc82ad8b2fb978c24b83117f896cb89b5ae8b5cbe69404ef68648d0444ee`  
		Last Modified: Tue, 17 Mar 2026 02:59:28 GMT  
		Size: 4.3 MB (4284233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91419f9ccf832b630946b8488c03cb24eb2bfbb431679dbc7e9d351f30a0658e`  
		Last Modified: Tue, 17 Mar 2026 02:59:28 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:63153b3e84bc588df70dc7b02a87484b73095a9e649c38b1a977b4afd71de1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228657110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09aafb3b5fc9eb1e3fb5604d26966d1b9cb524b84c2c434fd5fe7c1c22cb264`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:03:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:03:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:03:45 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:04:00 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:04:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:04:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82faeaf178d6892a9733fed8753cf36fdb693e9b1c18cd729d56fb092ecc6f8a`  
		Last Modified: Tue, 17 Mar 2026 03:04:26 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10618d908006e446b646f467a009b1fbb4122d5dc93e51e820521c2b439a98e9`  
		Last Modified: Tue, 17 Mar 2026 03:04:24 GMT  
		Size: 19.6 MB (19632833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fed25a44e85539c226c19b1362c3584a44203c55404aa0e3e49672d3d4fafe`  
		Last Modified: Tue, 17 Mar 2026 03:04:23 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d412391dda2782e063498737a627815f249bd184614183f971c0c9f54dd110`  
		Last Modified: Tue, 17 Mar 2026 03:04:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8e09dd8f65f1b1a92978107a6dcbed1e9ce1aa01f63cca0ea45901e0962ca344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a18a469e655a88eabc6e74d47eb6f77f31a54c760ca92dcbbe5a93d60e78d1a`

```dockerfile
```

-	Layers:
	-	`sha256:8ced9821c1a2edffedb1e3204d9cf86223c4fb8f1c817ae669b184cd431133a9`  
		Last Modified: Tue, 17 Mar 2026 03:04:23 GMT  
		Size: 4.3 MB (4283872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11c44fcefcbc27d2946a24ec45524998e5f239314d1fa6d4cfad1ce598a4bd8`  
		Last Modified: Tue, 17 Mar 2026 03:04:22 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b292458accc75f9163d3a0a5e03b6fcc6b8899ac4a7acb254ae73bb2a64018b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234856318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cda18ac63cca2ecf2d2f57c8f18e3a9a0e8859b62894a7351b1144da6eeba5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 02:05:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:05:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:05:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:05:49 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 02:05:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 02:05:50 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:06:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:06:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:06:38 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:06:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:06:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:06:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:06:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d3f5e74242b563425489fb40e572f07cd179ee7a7b86fa1a8e8f36a083f08c`  
		Last Modified: Wed, 25 Feb 2026 02:07:30 GMT  
		Size: 158.0 MB (157977502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50285f3786943d6a91a37e64d74f443446f42158e80a09b8b33cf6d04adf412`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 20.0 MB (20023839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c9fde50611b7b0e058750127f821b0236f9e4f460fa1e449f31951064828e`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a61ab8c25662006212920c1d71bf1b69256c068040587a1befe2bc9d5ca580d`  
		Last Modified: Wed, 25 Feb 2026 02:07:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1ae12122672c0c823ccb7de626ad799f412c66e340785dbbb3856a2248869a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d084fda3e220520283f9bb407548502dfbe78e7c0823e616c1f69a78d2c88c`

```dockerfile
```

-	Layers:
	-	`sha256:50219c6784559a6ee65115a400c2d19ec04a1aa047d5adaf18c4461476e0984b`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7cfbd5c3f0bd02fc42afed72d5e230aa4f3425b6c6fd8ef33095ba2e9916be`  
		Last Modified: Wed, 25 Feb 2026 02:07:25 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:bc200876d84fb87e037a5b0e573bb059e8cb3916db85da4911930aab5ae2793d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218234965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b3e6d9dce3e08c0b36a110d3440fa14728228bf7bb880216664c993ae1c435`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:19:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:19:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:19:02 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:19:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:19:32 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:19:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:19:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:19:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:19:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49354e9f0679f3ff8b88e9d693551817e9930dd3f79f0b6470d4ff396a09d7f9`  
		Last Modified: Tue, 24 Feb 2026 23:20:16 GMT  
		Size: 147.1 MB (147105304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d029d48f8385a6e82d6d25771c55cb496ed9963da48ee1585e3bb41256565a7`  
		Last Modified: Tue, 24 Feb 2026 23:20:14 GMT  
		Size: 19.5 MB (19463372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efe4f6cf3aa11e90816c6f6b7f95f4dad94b617ec5249dff28f5ad4777c623`  
		Last Modified: Tue, 24 Feb 2026 23:20:13 GMT  
		Size: 4.5 MB (4517771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05e262fe4905ca17d80c00f3761dbb2bec2fdfc0a8b43f330663e51260607d1`  
		Last Modified: Tue, 24 Feb 2026 23:20:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7c0ba3e7838e22c42764d1a67a23005bb653af20c4904636eaa28945c17fa65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed092d5d7d75031b4f8dfa8c2e22a66a583c21c376b004a13b3f77d234a88cd4`

```dockerfile
```

-	Layers:
	-	`sha256:83f5870f7b5618b413600722db8acfd3be12c09b815a249d0daf734086d73819`  
		Last Modified: Tue, 24 Feb 2026 23:20:13 GMT  
		Size: 4.3 MB (4276047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b089e498d14298be826a99a22260dbfa4e9847ccce1f290801f9855fe005191`  
		Last Modified: Tue, 24 Feb 2026 23:20:13 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
