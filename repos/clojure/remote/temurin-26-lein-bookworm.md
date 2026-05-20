## `clojure:temurin-26-lein-bookworm`

```console
$ docker pull clojure@sha256:9bedb1392c7198e1a7893ee37934a7ea0b52f0a1c79f66dc7919933291d736a5
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

### `clojure:temurin-26-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f6c79cc7a207729ee333815e190358210c1603f308e5bf0b84407967d0e3a88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167349593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4f481395740e64ce922021f5bbd363cd197fa219b8691ffae9d2f6b297e1b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:01:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:01:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:02:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:02:13 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:02:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:02:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc81f3ad6419f68e6c9183b3d8be358884da208cb678b67b4770ed64c85bb71`  
		Last Modified: Wed, 20 May 2026 00:02:35 GMT  
		Size: 94.5 MB (94524332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86539f34b8cd47a710c8a333d773a01454328dfa7abeec408527a1825c61c773`  
		Last Modified: Wed, 20 May 2026 00:02:33 GMT  
		Size: 19.8 MB (19811682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f244569b3fb10ab097379ecda73989a1ff690dfc777a7b4d6223c3035980942`  
		Last Modified: Wed, 20 May 2026 00:02:32 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372c45213cd0a968d1dd8c9fe142d62402f9593387526b9a1149cf7b099e8877`  
		Last Modified: Wed, 20 May 2026 00:02:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a19a350c1af52d3a14699eacfcee8fb87a594c481a29a18a7f86cacbf4492187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e091fe57862a40beafb68eef9a9d29b0915713dbe345d132c8f96e8f3e66473`

```dockerfile
```

-	Layers:
	-	`sha256:aab4375fe078ddd4bf4a239be4da843242fd551247afcc2b85ff34f7de739516`  
		Last Modified: Wed, 20 May 2026 00:02:32 GMT  
		Size: 4.2 MB (4247917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b608d1354e26c4be7c280db38ee96ac67c8ed4cc679e46ed6f04803ce0b706da`  
		Last Modified: Wed, 20 May 2026 00:02:32 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23499cd7f21f646b198d2c2c14901e3ed48e02a4a5390f6eec5ec78a7f64321e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166043788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f449d80f006cfc71e297a5b864779c9d413692edcf92d09d1c437301b9d78a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:08:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:34 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:08:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:08:34 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:08:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:08:48 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:08:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:08:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a912e141af15ef5dea2983de28dce2e479e6398c7a0092044c160eb04425e25`  
		Last Modified: Wed, 20 May 2026 00:09:09 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2787fa4830153afb759b988b1427e155bcbf0caf225575d5ea9b17f90598c50`  
		Last Modified: Wed, 20 May 2026 00:09:07 GMT  
		Size: 19.6 MB (19641890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f53208690ffb68e5716f5ae37033fab91562db706c9f52ddd80b5d49e8a03`  
		Last Modified: Wed, 20 May 2026 00:09:07 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55787718ce0494c6fbcdbb9b878645c43f064ffda67183102a1af0c553bd18cb`  
		Last Modified: Wed, 20 May 2026 00:09:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b3384e845c8d62ce225fc508b87e1530c36ab66690f55b57588f4340a057367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab37a3022db2ecda80564e799358582ce6489487e447e76de5282596b269638`

```dockerfile
```

-	Layers:
	-	`sha256:ffed55512bdb903b16faeab153d302b8282a7452f26c0b7a26f6916854ab534d`  
		Last Modified: Wed, 20 May 2026 00:09:07 GMT  
		Size: 4.2 MB (4247553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84074c903995f5f0dc07fd03ce06f63f4b3102dbebfdc557164641cccc7b0880`  
		Last Modified: Wed, 20 May 2026 00:09:06 GMT  
		Size: 19.3 KB (19308 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3665fff8505950da0ce4ce3008b68bd04658b975ef0d429757f38faa47b3cc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170793603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308b6062f2bff7311c3f1ee9be219d82f1eaf601d5c0a12952dc226bf68b7d36`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:10:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:10:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:10:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:10:17 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:10:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:10:17 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:10:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:10:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:10:44 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:10:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:10:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:10:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:10:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a250708f248a2296e18311b56818c5d5e6477c5552cb0d7df7a8d16b02343c`  
		Last Modified: Wed, 20 May 2026 06:11:23 GMT  
		Size: 93.9 MB (93902016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae4802a941d155bc247f6d5010d75d997eb6708384e59cede900b863e68270b`  
		Last Modified: Wed, 20 May 2026 06:11:21 GMT  
		Size: 20.0 MB (20033249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbb17d6b75892e1d15a89b30899e6fc4ed9ebab00e7fa164251b7d7e7b5d32d`  
		Last Modified: Wed, 20 May 2026 06:11:20 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bafdb9cedb0aa77767d9b285cdbb9436e21b2092ac9a3c20b972a66bfb71a6`  
		Last Modified: Wed, 20 May 2026 06:11:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a55dc4eab3104926a5681bda84e2e8c29f065fe342fc221ea64765c20b793534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2577a9e3cdfeae0858e2668a4bbe01742490a051d950f7e4dc1c6ff785598eca`

```dockerfile
```

-	Layers:
	-	`sha256:573d161421455f3fdaa58bd1b475e7f4599cc3c48bf7c2ea54877269d6f03332`  
		Last Modified: Wed, 20 May 2026 06:11:20 GMT  
		Size: 4.2 MB (4233726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a363fcb21df311811263b7b377bbba25c7549d1e070862c9e36772cb177231`  
		Last Modified: Wed, 20 May 2026 06:11:20 GMT  
		Size: 19.2 KB (19221 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:aabea1548c391750c14550d8870d563deffb81770fbc5435bfb6a852aa339b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161684528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04db678db6005467ad7accc2a9d38fd9670f2580724771b1e58f80fc73fcd0c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:48:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:48:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:48:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:48:54 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:48:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:48:54 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:49:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:49:05 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:49:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:49:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:49:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:49:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9ae4ae0ae9e5f83ec5cdac2d66779f72a32acf5bd578b66847f1d4b88f484d`  
		Last Modified: Wed, 20 May 2026 01:49:33 GMT  
		Size: 90.5 MB (90536967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6726d1f53b420dc6aab12078f3dcc9c37ed24ef9f96f2dbfe5887a1720bb55`  
		Last Modified: Wed, 20 May 2026 01:49:31 GMT  
		Size: 19.5 MB (19473801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62e92574fabf82de172afa7fe7feeef21497dd655ef17b41fdd50266b1ad10f`  
		Last Modified: Wed, 20 May 2026 01:49:31 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca8baeafb92361d035db48de9d10c41e4bf6d464a0e822ccadbb463a2c52976`  
		Last Modified: Wed, 20 May 2026 01:49:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:01560fd9ae292cfebd875495666a87d8ebde8ceade06cf076795f6479488b2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de901624442d5af654835cc8f47b0141d787f2020efa25428d6ca07dc6b2e045`

```dockerfile
```

-	Layers:
	-	`sha256:07b28cf395fe5b710445e80c0e2af711e6090a91be5f9cafcd19c82fa1a955bb`  
		Last Modified: Wed, 20 May 2026 01:49:31 GMT  
		Size: 4.2 MB (4224917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fb168df1cd6f148ffb9a0b3f9dbc0607c5ce5050a3fc174e320c0139799d861`  
		Last Modified: Wed, 20 May 2026 01:49:31 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json
