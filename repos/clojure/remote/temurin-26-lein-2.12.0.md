## `clojure:temurin-26-lein-2.12.0`

```console
$ docker pull clojure@sha256:d86af909d4ac7b948a712d011a3b7f2ddada56a76572df7ca6456d63825921dd
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
$ docker pull clojure@sha256:8395e10128607787cb98e12f61e538a7c77ce36afd8886444b7e8a227dc18f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167337686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50a67773653320b06edb2028160e38efdebfa29ced066f31973b33f9d7f2eb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:35:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:35:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:35:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:35:45 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:35:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:35:45 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:35:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:35:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:35:58 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:35:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:35:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:35:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:35:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cacdcc38131b51a9258b2ebc7cc9771ffb773de1989a7edf7003079ded4026`  
		Last Modified: Fri, 15 May 2026 20:36:17 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b94d95ca0773cfc835bbb6f7fc85081167ca52114258406e3e22cb5082c7f8f`  
		Last Modified: Fri, 15 May 2026 20:36:15 GMT  
		Size: 19.8 MB (19806482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d5aa34316b287e84b886be66a9a5556c4ddb2b0f34eb45e064c9352cf6696a`  
		Last Modified: Fri, 15 May 2026 20:36:15 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25786efef5e800b03605fc344f00495ef2a6e7c4e900e021519d52f4642ea376`  
		Last Modified: Fri, 15 May 2026 20:36:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:19854e0919cb0c6ff67e612bf25be9a26f54ca9481b2391837d38fd161e34d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011869290acd2c1b580cfb6b7c72f39904ebdd847fed73a82f7bbda7a3cf44dc`

```dockerfile
```

-	Layers:
	-	`sha256:3f6a3347099ab04f187b9220f7527c6c6123a4b549075c47a2768ffbba1c6f1e`  
		Last Modified: Fri, 15 May 2026 20:36:15 GMT  
		Size: 4.2 MB (4247899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9f351556fa6b5c1964bca19ba9980a7a6d4533e2cba88b7296cf72825f3c4fd`  
		Last Modified: Fri, 15 May 2026 20:36:15 GMT  
		Size: 19.2 KB (19164 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:16a00ff5a125b2fb628359fcfad8340fd31d57ca9fa254ff9e5ea10afc53a87c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166032801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94fab018029b330346b5025ee02a2df81c49cb0890630abeca0b9c10eef25e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:35:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:35:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:35:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:35:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:35:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:35:57 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:11 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7405bb9216868a405b56cc0634aa51965443ef7c830610334ab92583fa3b7e64`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 93.5 MB (93504390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ccbe38548ca31c2a38286a6321e337e032270ba611f638bdb3ecd84ad7782e`  
		Last Modified: Fri, 15 May 2026 20:36:31 GMT  
		Size: 19.6 MB (19637088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61da5b33daed634fa39abd69555401fc5805e159a600f30494eedc3e7c5f4b8d`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ed44f6381cc22a39ee399458ce7612bed386cea57834ee0e2ac2c50a7be21`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:69b067e271007473c8515ff2259fd4f3e52ce4cfcf87ce7989d539b817799a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a31e2a22e7857faa7af0c765adbafbd5c75e52b147b068c5a16a0590216557`

```dockerfile
```

-	Layers:
	-	`sha256:46ac5ec3349f52b6db2aee59296ee44709463cafa76717acd4e35b92a419c383`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 4.2 MB (4247535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b389123c4504c6c07a796c1988467e6a07a8bf408ba3a316a0e54f939ec224b1`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 19.3 KB (19310 bytes)  
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
