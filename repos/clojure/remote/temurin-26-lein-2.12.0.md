## `clojure:temurin-26-lein-2.12.0`

```console
$ docker pull clojure@sha256:f8de8d95d96ae51e7648d80c10fef0d4e5ce866d2c3a5bf655c616d3ca08233b
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

### `clojure:temurin-26-lein-2.12.0` - linux; amd64

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

### `clojure:temurin-26-lein-2.12.0` - unknown; unknown

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

### `clojure:temurin-26-lein-2.12.0` - linux; arm64 variant v8

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

### `clojure:temurin-26-lein-2.12.0` - unknown; unknown

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

### `clojure:temurin-26-lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:c5aab51f7bac51f838b85feb54027a81c9c924c95b5a64e135ab81814c9c2ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170787573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1f1ad988ccc28449cd9c2ffe29daca414c7dc19406db5828f4b7cd659bfdd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 21:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:45:51 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:45:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:45:52 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:46:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:46:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:46:31 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:46:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:46:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:46:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:46:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fd299d196bbbb90b619a2efbdb555a0daabbf409ed235c488e800b3c6f94e4`  
		Last Modified: Fri, 15 May 2026 21:47:13 GMT  
		Size: 93.9 MB (93902030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85259e91d1e2a180ff5f15897dc4bb3bfc9e1b6823b3e072170a9ad5ab067cb7`  
		Last Modified: Fri, 15 May 2026 21:47:12 GMT  
		Size: 20.0 MB (20030625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81dc3eafb3af0dc8e8ff945e9c409f3bf664e43d391036540b615af67aab51d`  
		Last Modified: Fri, 15 May 2026 21:47:11 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959630a46c3b6b8af807068726d066211e84fe83d4b4aed4f06d9799e305bc2`  
		Last Modified: Fri, 15 May 2026 21:47:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:4e9d7cf1cb8691b6387d850eeb0f99984325edd54b987f7bf0da8cafd345e513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c548d5c01cf6662099fa58237ddeab62825a921589a85ea8c501e5af413f4b`

```dockerfile
```

-	Layers:
	-	`sha256:eef8cd863e9fddf56204faffc71af3a21cbf13841895207de1a9370a0f9743e4`  
		Last Modified: Fri, 15 May 2026 21:47:11 GMT  
		Size: 4.2 MB (4233708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64abcc93826dcf61c73c093eb104b2f8e9390d33fa367c6d2b8d0f3fd6b4dd40`  
		Last Modified: Fri, 15 May 2026 21:47:11 GMT  
		Size: 19.2 KB (19219 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:fb17e39f9e3752550a1430e8b920225602b2237d9ce580716e166f56e0cc11a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161670315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e7123b4c3c5d8a29bfa2fca134d0bdaf2ceee1148416766f1af9d19f14a795`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 21:27:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:27:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:27:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:27:32 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:27:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:27:33 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:28:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:28:28 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:28:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:28:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:28:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:28:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a95f54df64ce481af97f579c751c1b86f729330e08dbae614ee3e3b1f85f596`  
		Last Modified: Fri, 15 May 2026 21:29:15 GMT  
		Size: 90.5 MB (90536967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed727ae28599f9006b9511bc81c7d608a5ee52847ced926f43b4a5bf0d0a429e`  
		Last Modified: Fri, 15 May 2026 21:29:13 GMT  
		Size: 19.5 MB (19467109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb524b7b82f4afb76918554cb3d98214c3df050e4514b3ee3ede6a533dbd6126`  
		Last Modified: Fri, 15 May 2026 21:29:12 GMT  
		Size: 4.5 MB (4517785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a05d2ca8b5f4d54e8743aaae19d8743febe1854417a824d28ca12e283a0555a`  
		Last Modified: Fri, 15 May 2026 21:29:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:1f7983fb171e704755598c2be478e8e78a75beeb4b3f8a3e7e086a7a11b6f2f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d67bb1492553709e8f2341bba52e226ac04a9c4f80d900b9fb5d72d2c4a7eb`

```dockerfile
```

-	Layers:
	-	`sha256:1a5f6ba535cd928fed6e2cc33aac8d59c5ba5127237b0f2ac432b298a73b294f`  
		Last Modified: Fri, 15 May 2026 21:29:13 GMT  
		Size: 4.2 MB (4224899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55167ec7f4b866aa9cb686bfff16623468d61ec204ed22c4ecac7aa0bd49e6e7`  
		Last Modified: Fri, 15 May 2026 21:29:12 GMT  
		Size: 19.2 KB (19165 bytes)  
		MIME: application/vnd.in-toto+json
