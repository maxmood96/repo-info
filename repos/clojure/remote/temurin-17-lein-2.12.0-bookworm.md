## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:f509b87ffb30e1681d3347e4f0230ae29dc979bdf71790cec76db86d18f8906a
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6a81d952c8d259f4b1ac86e38d74ab12e527a15ac3b7c2c773cc34df2de82d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218730745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4199d48943dbc8def5b8265f9efa02bde41cbb4322411bd97a15160a6dc7b29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:58:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:58:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:58:06 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:58:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:58:18 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:58:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:58:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:58:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:58:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f077097c336887412e208e7d9a88f7486692d05dadc9e2bfa01ee475548097`  
		Last Modified: Tue, 19 May 2026 23:58:38 GMT  
		Size: 145.9 MB (145905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0b558b0f05e8c35f55380af3c575a8a28b1360d92c69c18c48088c1b48ae07`  
		Last Modified: Tue, 19 May 2026 23:58:35 GMT  
		Size: 19.8 MB (19811661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90d658b459814a6f278adbe801d83e828933b0fbdc844a6539fd997549d8f80`  
		Last Modified: Tue, 19 May 2026 23:58:35 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f36ca9c78119ff425a5a1c4aa950eaa174e4ce6c7cfcfd0491a3ed15818bb0d`  
		Last Modified: Tue, 19 May 2026 23:58:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5a21092ed248b80860feac1edc791e07d4c90ffedbd37713f1ae3ba449605bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9bd0477daceb06df49b48b4fc023b9af262ecf86700c3002530c6ec687fe28`

```dockerfile
```

-	Layers:
	-	`sha256:4e7b627343c0e68c8ef4543d47a34983b6e8486a8ee40c9afab5fad15da806e1`  
		Last Modified: Tue, 19 May 2026 23:58:35 GMT  
		Size: 4.3 MB (4282376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850dcca36894991e1c46fc31567c7f3aa13a9f4db9d032c1bc2d85fc1ea5cda4`  
		Last Modified: Tue, 19 May 2026 23:58:34 GMT  
		Size: 18.5 KB (18521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a89f922ab322c7e10eb6f0f20b6c5e360e5f82c5ea85ad66bd9972e4ec5e570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217263796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1047b668ad85ec0bc6243a1bc7cb5b2af0767567711a4cf2640d324190780553`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:05:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:22 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:05:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:05:22 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:05:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:05:35 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:05:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:05:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:05:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:05:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebea9660d093878aaf48be7395f4821664b2ca82e7aef65298e6e1711831d46`  
		Last Modified: Wed, 20 May 2026 00:05:57 GMT  
		Size: 144.7 MB (144724360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5edd3b23e392ab5b4cb987cca83ab06f9d07d73f7fad9016c1e5773e4f7c8b`  
		Last Modified: Wed, 20 May 2026 00:05:54 GMT  
		Size: 19.6 MB (19641831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0bc5b251dbf66d2104a4fb38d2d9e6cd840fa089ed7ea15706f07efeb60ad4`  
		Last Modified: Wed, 20 May 2026 00:05:53 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bc17c6d38573fc7b42d37f1f6fb498f87f3b5e511f45c8a4663d5a20ed827d`  
		Last Modified: Wed, 20 May 2026 00:05:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e9084439483823bb4c6154e70537a9fef688b96b9e6bdf4b76c219cf9c03d467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e70b1c4f91e159d156628c269a32222b3fcac60b00f1179be4cbb111b1ce35e`

```dockerfile
```

-	Layers:
	-	`sha256:dbe66c6662f97acc6a0bc53be892fa805362c396a38c68ca42ab41e403a6a5ca`  
		Last Modified: Wed, 20 May 2026 00:05:53 GMT  
		Size: 4.3 MB (4281991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2fe03c1fefdd78ae08a360311a91f839fbef25cfa22b59025f447c4cbd51c3`  
		Last Modified: Wed, 20 May 2026 00:05:53 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:4fa50ab23af18624dec30b83acb951ade4f5f7cf46fff433b1ea47ffe28e4b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222657679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f74b1416d7f5d764c711dff91b62f0442a40dd2ba34f542dfe52607e3164132`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:54:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:54:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:54:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:54:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:54:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:54:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:55:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:55:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:55:03 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:55:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:55:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:55:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:55:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6633021a99f451d585b657cbca0d3fbc241ffb487dcadb3e2ad6afd10c777642`  
		Last Modified: Wed, 20 May 2026 05:55:35 GMT  
		Size: 145.8 MB (145766094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec27c4a56dbeb1d63181b9f177af797c25025ff069f49b4eb775add5461d0f1`  
		Last Modified: Wed, 20 May 2026 05:55:42 GMT  
		Size: 20.0 MB (20033240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ab5bdc1dc186ca766d35e44e475f174ce6c5328de4a19f84c34b4a17bc80b`  
		Last Modified: Wed, 20 May 2026 05:55:42 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e6d2d7475c10d351dc31ae658fbc7daf855f4331b41fcdfbe0abef1b4b2ed`  
		Last Modified: Wed, 20 May 2026 05:55:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:66617f872cea71bb5377104f6a49cdf6097dd07d2271417235938cf47d4ebf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ac62465136e990a9314638846abaa258f36a899756174e440c7313166faa7d`

```dockerfile
```

-	Layers:
	-	`sha256:c2d7d7eee9ebddd0df63b5a4d99711c3a6d39c4f1c9e5ca6a967b6f94d5b6b2e`  
		Last Modified: Wed, 20 May 2026 05:55:42 GMT  
		Size: 4.3 MB (4284237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846395447f5691679534a5c36d8deb56c93795937912e8b2e417542cbe1e703e`  
		Last Modified: Wed, 20 May 2026 05:55:41 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a4c1102cf98acf8465e0ee149a728cccbfe47265ec4db12e75be3ef733bec1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207057893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951bc6a2e923bb369fca4faed10d9c06e58b93f780acc1da162e5ef7e9685da9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:43:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:43:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:43:28 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:43:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:43:28 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:43:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:43:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:43:40 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:43:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:43:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:43:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:43:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5e6deaec85cc5be451ebdae33f1ebb1ee8f8afce7f812c0687c0c3ed8574b1`  
		Last Modified: Wed, 20 May 2026 01:44:08 GMT  
		Size: 135.9 MB (135910432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0557c0fac45c0aea14e474a84fa245943cd7a013a808bd4a820d665f8d1b56`  
		Last Modified: Wed, 20 May 2026 01:44:05 GMT  
		Size: 19.5 MB (19473729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2563e4ce3345008be131e6476c0ac5c1bb79db8b44164f89b7cc376958a0b`  
		Last Modified: Wed, 20 May 2026 01:44:05 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7198c24d2fe2e751ceba96d90f47d5542018ba57930f696e630be5b1df50b08`  
		Last Modified: Wed, 20 May 2026 01:44:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6e84428cd3764156b7a86129202109ec19bd7676cff0f532538bce92e456ea58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4292712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74888c01fc4380b881618066c442b0fdaa40a1e2fab50148394694e0d88185de`

```dockerfile
```

-	Layers:
	-	`sha256:ec750e16da34638989e5a2df008de7161ebe8b8b6b29302c5aa8a07ed6b45646`  
		Last Modified: Wed, 20 May 2026 01:44:05 GMT  
		Size: 4.3 MB (4274190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1cf7b71d0c66ac01758d7f00301f9f5370a39cb98dac1d573ae1dfddc834d0`  
		Last Modified: Wed, 20 May 2026 01:44:05 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json
