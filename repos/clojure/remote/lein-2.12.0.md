## `clojure:lein-2.12.0`

```console
$ docker pull clojure@sha256:0a7686254a4018854f5f8abae27e7c107f550a91ce089503c738aac1dc7e7d90
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

### `clojure:lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:30a98c595902692a084a39bfd83e8a81753143921c2f7211d439133685e3e414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165388022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e5f6f936d15949b346dc107035b8ad6b639e68f7f518487a9075c84cb65d0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:53:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:00 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:53:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:53:00 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:53:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:53:14 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:53:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:53:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a83e027a563374d7ff9c4765e6372a552451fc66cb16c1c2ce2b343cd790d17`  
		Last Modified: Thu, 30 Apr 2026 23:53:34 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f7e65ba4e6af0ea04dc452a488cac9841cc136753e77f0754b2411f1785a38`  
		Last Modified: Thu, 30 Apr 2026 23:53:32 GMT  
		Size: 19.8 MB (19806610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc724d746c6313f1786ac96da38ddbe60e1ebe772a10d565ca6d49fce107758b`  
		Last Modified: Thu, 30 Apr 2026 23:53:32 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ff11bd8c48c516ae99a187b442b6714c5423c0d3f3f52c42ceb5728fdc2a2c`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:acb428e68e55abe7563a2702352abd8b13a546a94218e66b2da267c697151be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a922209a5a60a7647c0e207cf0ab508c59d90b6626824396358127f30db0a87`

```dockerfile
```

-	Layers:
	-	`sha256:ec5bb169b373ff42232f501507575c6adb57b2cced926080335025986b0aa41e`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 4.3 MB (4251650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb45ecdd80b2286a7b9e66cd9a24243349b8e56eb90dee4ef5bada4544d6ca7`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0` - linux; arm64 variant v8

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

### `clojure:lein-2.12.0` - unknown; unknown

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

### `clojure:lein-2.12.0` - linux; ppc64le

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

### `clojure:lein-2.12.0` - unknown; unknown

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

### `clojure:lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:d7348e80f4468f3b9b44758e83373b0d753a13bb6cf1f5396a4315f73d3120a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159553161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57bcd30908320e6c2a4dd07fa7246a2fbe35619cfb5a826e0c51045693c874f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:49:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:49:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:49:45 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:49:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:49:45 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:50:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:50:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:50:03 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:50:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:50:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:50:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:50:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f546523e17144e6adf96648f2aab96177c22f8992d4957c2ac55d515ef040136`  
		Last Modified: Thu, 30 Apr 2026 23:50:34 GMT  
		Size: 88.4 MB (88420323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d3e5ef4db21ba91e38e66753f81b031cfc833ab9a643bcaec15bff86d8a702`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 19.5 MB (19466693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93247ed19dae32474786717333324e6d2f1110fedaf834fc803291b99f086508`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836ba836443fe4c82176244d3ad0764503f10823c34b592581135e5ae45975fa`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:d87a9235cdd3aa55617230d1a525bd23a29f510ad3cb2e74ae0c88742291dce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbba0006245804f1c1bf3d84c42f6eab609fac634da1a90cf71c267143d41011`

```dockerfile
```

-	Layers:
	-	`sha256:e28d8b32a2e01a894835b56eb7e22cd336b8aa32d951861baeefd0dfa3b50700`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 4.2 MB (4228026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14c6996aa4149718f8623653e0c647f6c5b4cd397fb23e6c4d161a52115e3439`  
		Last Modified: Thu, 30 Apr 2026 23:50:32 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
