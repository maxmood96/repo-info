## `clojure:lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:c83d3bf2a1a29905e1b20f1528ff37751d15e2a52b55c2c1557f77317f9f7aa9
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

### `clojure:lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9e346fa64668867fc356f334dffd996075fa63931b0d26b05e83286e3657064c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165387890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd16a4183c5eaef2c0f264f064b5fdee7c2e2744c38b7d3b3b2729c19f11613d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:27:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:34 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:27:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:27:34 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:27:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:27:48 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:27:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:27:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08585450ad0175763224caac50b1b3bb60a33ad22571bec1a12a114e2b9b44fa`  
		Last Modified: Fri, 08 May 2026 00:28:09 GMT  
		Size: 92.6 MB (92574624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e60f2dc52d8c7cf66e4409a6e3d774e1a3326a106801bbd0936490b6a3ab57`  
		Last Modified: Fri, 08 May 2026 00:28:07 GMT  
		Size: 19.8 MB (19806506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4effc8ebc0986132d32b112356a3203cb7baeb4ec6745c5db145239b7f243737`  
		Last Modified: Fri, 08 May 2026 00:28:06 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd81ed79e38f8d98765f7f7dc98f2171565452ae107200ffa124240985c954b`  
		Last Modified: Fri, 08 May 2026 00:28:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:836e1fe92465fd7824aa18d8b568dc7ce6fb7f7791e5127cd89e2a0a7fa3d4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bbc2fc01e5d00670b63fce17f71132ad2a2293d3a8ebe51ae2a5d2f55297b6`

```dockerfile
```

-	Layers:
	-	`sha256:66d56d27480314dad09d65e09b00e6b9da7677c96fa0385678f95cd60930ab19`  
		Last Modified: Fri, 08 May 2026 00:28:06 GMT  
		Size: 4.3 MB (4251650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc61b0e78484c61739ad2d2524662feef6c8a4f7ca1aa745d6dd35e8fad9bdec`  
		Last Modified: Fri, 08 May 2026 00:28:05 GMT  
		Size: 20.4 KB (20412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25e9635bdcaf638ad1b58b96b1177e8e91c9b169614754a97af2e4d7d36f4af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164070583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f8576a83b4a68904a913e4d6df758c07f19ed0abe78b0f86946d6638e993ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:26:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:26:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:26:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:27:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:27:13 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:27:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:27:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9cb06ffd0c6390e813d86acf786bcc1eb458fe8c1086e6f5689655dcc93546`  
		Last Modified: Fri, 08 May 2026 00:27:35 GMT  
		Size: 91.5 MB (91542278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9f13cd3e70b440ba938b37abf005bc2655d99636ff3795340d6e7dffa5342a`  
		Last Modified: Fri, 08 May 2026 00:27:33 GMT  
		Size: 19.6 MB (19637064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adbbe52eb7846eb9c03e9e69a0e6ad0c8eb6818edfd10857a6a079bec68b621`  
		Last Modified: Fri, 08 May 2026 00:27:32 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed3043d63975c8bf39d87dfa12751694f2fe736c2fe1f037cfa1a7a508b019`  
		Last Modified: Fri, 08 May 2026 00:27:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc07ab003f986e3c57e1b9a59c5b60df2d9b311b4c96ba1322e6f9bae62919f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3347a722b1a7442979082bb0a3a031a33e1d4b0c4c58a053273090bc597aae83`

```dockerfile
```

-	Layers:
	-	`sha256:5cc84d3e0e8b5f3b5ddfe2d839d012b84a161508771a37a180e05bd13968eafc`  
		Last Modified: Fri, 08 May 2026 00:27:32 GMT  
		Size: 4.3 MB (4251334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77e6e2b8757ee5885deec316d1ea32f2bac594d3764e9ad305ff5f19946f8315`  
		Last Modified: Fri, 08 May 2026 00:27:32 GMT  
		Size: 20.6 KB (20606 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:403dcebf1a2adcd22672cbd1f7d14e79be47fb68cc907f3568f2b51ac3eaa49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168799393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6232452c87c38f9d1afb28a1d7180b39bc2b6605d217a8a5e920ef7db9682832`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:34:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:34:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:34:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:34:38 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:34:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:34:38 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:35:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:35:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:35:14 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:35:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:43:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:43:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:43:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d733e476aa8595c677a7a8e78f0fbc11c82e45660c7657482695df3b0260f12`  
		Last Modified: Fri, 08 May 2026 01:36:27 GMT  
		Size: 91.9 MB (91913990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd71281f76e595b73d8d0c8f07fa830b4a334af9eec5d0149a1efb2e6e272542`  
		Last Modified: Fri, 08 May 2026 01:36:24 GMT  
		Size: 20.0 MB (20030493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed03b88e86956a26e7e85d64d8501f485f4609b55f6d6b475eaa3fc1c096d88`  
		Last Modified: Fri, 08 May 2026 01:36:23 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafaaecadf554c123e98402fc8e61b12c12c1a5e1b3738989f8a0f101c20471c`  
		Last Modified: Fri, 08 May 2026 01:43:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:856cb3e08037617b36d2dc401e7e5a3d1dc015d849bd775331686cfa8ba1aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cfb02d123e710d4810c1493b6a07c43cc982933000b84b685e389ee74ea36b`

```dockerfile
```

-	Layers:
	-	`sha256:5d5f376d8c9793e9c18778b07fe171e509032aa312c3464bb3fc9cda2e1af383`  
		Last Modified: Fri, 08 May 2026 01:43:44 GMT  
		Size: 4.2 MB (4236859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92968f68ba1192f40bbbbad78738cd8e9f9348bb17f899245e3a771b256dd115`  
		Last Modified: Fri, 08 May 2026 01:43:44 GMT  
		Size: 20.5 KB (20492 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c2ee3484e91b3b087593173f217e6edfb8829b1825a1c0f99bf7345da757b70c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159553148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1620f1391f5127dbdae6cec05ce0ce737e30d1a9415fe096ba280baa4fc9e129`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:49:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:49:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:49:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:49:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:49:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:49:40 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:49:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:49:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:49:56 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:49:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:40:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:40:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:40:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439ca7a271e362a7945b93efef6e6eb132b28afbec5dd9a21f35ce6c32acb6e9`  
		Last Modified: Thu, 30 Apr 2026 23:50:59 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f49fc5a549ed1553878c3915c3d1663ee51b316338bb43a8a9219a449809f2`  
		Last Modified: Thu, 30 Apr 2026 23:50:54 GMT  
		Size: 19.5 MB (19466655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf46a4b0ade1da07884078a69b4494442dd6325f8e102fd49e1138abb2fe0a8`  
		Last Modified: Thu, 30 Apr 2026 23:50:51 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afb6832a49b969929a286433ffb6457efc75c990e230f0866ae36f1c90feab6`  
		Last Modified: Fri, 08 May 2026 00:40:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3ad90b8793aa66d3c5b65863b120007f63af3900e775a37fb65c851cd9b15732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fca114069bfac20cac2aba61ed771e0a333e122f70fded91504ccfb69fd43eb`

```dockerfile
```

-	Layers:
	-	`sha256:4cccc318988494cde5a197d15f4cbbefa1af1e0fb1487f9431af0e61722e10eb`  
		Last Modified: Fri, 08 May 2026 00:40:33 GMT  
		Size: 4.2 MB (4228026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb11af55a2371c9893dae0e4b056464c9484b440aa69129b0612cc8179846c28`  
		Last Modified: Fri, 08 May 2026 00:40:33 GMT  
		Size: 20.4 KB (20413 bytes)  
		MIME: application/vnd.in-toto+json
