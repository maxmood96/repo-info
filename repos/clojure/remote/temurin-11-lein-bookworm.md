## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:475ba59ea1d964ad129321a6fb354582ef963591ffba05f3183db194745cfd70
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

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:cb44e0670311ad434aa09a029678627d088d9e44b98fcf050250f948d9415afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218619974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1279faae5c2dc3b254a181b0411277f4af838f361b021b39eaa147a5f731709e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:01:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:01:59 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:13 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d5ec9542abeca9108d89330a7ab97ea1ade9d2e82ec4fc72d0f3bfe8cdc2c5`  
		Last Modified: Wed, 15 Apr 2026 22:02:35 GMT  
		Size: 145.8 MB (145806832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd470e0f7ed9c414aaf16a08570f0528a40c6d14df4c371d1b38962f1d013f48`  
		Last Modified: Wed, 15 Apr 2026 22:02:32 GMT  
		Size: 19.8 MB (19806528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764b22bdd3a9d5a1b796e665362f3b1360e3572c2773167242c859b5fd67acb5`  
		Last Modified: Wed, 15 Apr 2026 22:02:31 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f8973befcb76c351d189f3328d383dd5a896031aa40f2db3973d7fb0df3dd21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a4f51762a0828f2609759e44a26916aefce659207eaf46815ee1556538309c`

```dockerfile
```

-	Layers:
	-	`sha256:9253cf4732ef529b9a9e862dfdf313dd54ddab190ac36468bf31668df8eb8feb`  
		Last Modified: Wed, 15 Apr 2026 22:02:31 GMT  
		Size: 4.3 MB (4301872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7797aa5f14365e0ef7c47edb95c180667faee5897e6f5572487a7ff937409567`  
		Last Modified: Wed, 15 Apr 2026 22:02:31 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea94ad15106ea7665e92fdef58ed1a822811f9adcb7ad910cf3627600adec524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215028915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa16b5a776eb68356012fe912ce4f656fa6848946791997517144c22129710ea`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:13:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:29 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:13:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:13:29 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:13:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:13:44 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:13:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:13:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c09ef9f443ddc64e7c80a46484bad1fb4bd8cb83c927978b1f19c12dbd90b8`  
		Last Modified: Wed, 15 Apr 2026 22:14:08 GMT  
		Size: 142.5 MB (142500804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e519c6c5370b4cf280a227a88ba0d0632166b35179af7b34df93e55d093b0c`  
		Last Modified: Wed, 15 Apr 2026 22:14:04 GMT  
		Size: 19.6 MB (19637094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a966ee085c0ceefd9ce099aeef2c205fc44e70e24daf8a47d937e874a756950`  
		Last Modified: Wed, 15 Apr 2026 22:14:04 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:deff0efaf8923462e2c5dc746a8db36c91155decd7d6b6e4f8716c34206b6f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5317c57d529f2f3ad465695bde3c1c37740d71421e9f11edcf73e1dbe3e1faf5`

```dockerfile
```

-	Layers:
	-	`sha256:b39911dcbb69d7c2eb89c8e882863a2d53c6a0ab377233b6b86fdb55c1950d81`  
		Last Modified: Wed, 15 Apr 2026 22:14:03 GMT  
		Size: 4.3 MB (4302105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09c2f642b1c7ec70d078931eccf128a46ce25e85f95d224ba76c41020978a7b7`  
		Last Modified: Wed, 15 Apr 2026 22:14:03 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0f74a04f5d2ea18cfb599fa6d3f34e5ef9f6a356fb0b47e04d4e7af2298bdb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209876211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03ca114ede0ea259254e5138b4151ac05b3a5fed7864d8e7159453d8f41490e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:28:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:28:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:28:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:28:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:28:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:28:31 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:29:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:29:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:29:10 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:29:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:29:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1061aa781fb4b7c36cdecd69fd6ed87373d79e2a52e43dd17a688e779d38977c`  
		Last Modified: Tue, 07 Apr 2026 14:30:00 GMT  
		Size: 133.0 MB (132997676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad11df42e74974fca803ac2b476cf9b9cab0a41e29dfbf6999cdc7fccf9f27`  
		Last Modified: Tue, 07 Apr 2026 14:29:57 GMT  
		Size: 20.0 MB (20023812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656a16a55db662b8d07b53e837d07e152a8bad7f22d63485410ff8f8a576417c`  
		Last Modified: Tue, 07 Apr 2026 14:29:57 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b4ed5f16bb5cd110a96cc1764ddd5da791d8e5dda4b55141a8ff9a88621f26ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89c3b99200ba52fece4cffdcb0ac36093c4b6e31c0f21e32acd40f9721d229`

```dockerfile
```

-	Layers:
	-	`sha256:63051bb8f104709c841022078ad9cbbac3b0dee513497186265fdcac59ca820c`  
		Last Modified: Tue, 07 Apr 2026 14:29:57 GMT  
		Size: 4.3 MB (4303118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d0a4fef1e6844d0a05d7d6989e82325589f759e7bd6f82fe0fcfa22e0ca39a`  
		Last Modified: Tue, 07 Apr 2026 14:29:56 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:36d9e255c5f6b8429f433aaed689be33edcd3ad88994e37d9a9d80720cdf9d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197694824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f542597e27d4d15509499878a763117c133c899e2087485cafbf7d01e229653`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:34:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:34:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:34:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:34:54 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:34:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:34:55 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:35:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:35:06 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:35:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:35:08 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3353cdef4b198536bdfcee818f3b5b34ef7f61508865540779831ee3c355b04`  
		Last Modified: Thu, 16 Apr 2026 00:35:37 GMT  
		Size: 126.6 MB (126562151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d9a19d970cbba3ac261c794b297223592a0bc60293ebf9cf8a88f407b6c6aa`  
		Last Modified: Thu, 16 Apr 2026 00:35:35 GMT  
		Size: 19.5 MB (19466815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef07f36d6478c0298964b2b096e23a03c90bc8b1d3afdc2661e9f4c0b176244`  
		Last Modified: Thu, 16 Apr 2026 00:35:34 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:febd722d9f71ff5f3528a9977817f51f861881c28800a7d7668ae24fecda1c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e38fab549150cd8c5f3452fece6824411cc2afcd494506c07affb28543ec82`

```dockerfile
```

-	Layers:
	-	`sha256:713674b8aee12dec64495579c8f0c64ab3c4d74e3ec7ad32bfd7fb27a9d75ddb`  
		Last Modified: Thu, 16 Apr 2026 00:35:35 GMT  
		Size: 4.3 MB (4293690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8229b783cf03eb7bed6b54461b6a91fd228c074650c55f4ac512e3a52ebf4cbe`  
		Last Modified: Thu, 16 Apr 2026 00:35:34 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json
