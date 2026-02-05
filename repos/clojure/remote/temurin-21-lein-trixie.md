## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:140d8d16cab9d9066bfd174a8fa4804aaef4b56713da897f3236c67a185c4fee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:06be86b01637f55eb3f389da3a74c82aa3855158e894c35390bfa0dd81a0456f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230217274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fdd1d9b30116d88eda3f4954c670eb7ff1c661c12bd8affd376f4f9cbd1fee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:21:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:30 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:52 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d500251f85815d5b1bfb3b60db782a080ce74d4a6a6b09bf7412bd3d4d0d5d`  
		Last Modified: Tue, 03 Feb 2026 03:22:25 GMT  
		Size: 157.8 MB (157826055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2256d8e1207034d4f8f5c5bc8a9704f7c1ebb40c3b9131d71e6e71c78085ef44`  
		Last Modified: Tue, 03 Feb 2026 03:22:22 GMT  
		Size: 18.6 MB (18580088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbcf8ed43ec53607207ccc3f7a3d308a490387f5d82f6c8617eb262cad886aa`  
		Last Modified: Tue, 03 Feb 2026 03:22:22 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30e4705948c05fd205324d62d8258fcf5d3e6e2d85a8decd651d6e66707a5cd`  
		Last Modified: Tue, 03 Feb 2026 03:22:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:235291573e466238321d20e3c495b14d10b47be389bf5c8c46cc5a21bf66ee9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae30d9afcae9b58ada0719769d927330700acfcb667cdb8736f3ef4c0758a4`

```dockerfile
```

-	Layers:
	-	`sha256:96e9db2ea074cbddd087b7e9d22c08d51fe3a8d8ba5cdcb518948551e77399ef`  
		Last Modified: Tue, 03 Feb 2026 03:22:22 GMT  
		Size: 3.8 MB (3817341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35f2eedd77ee8850f5894d0b9dc2369af843d72f4bdd9dd1be6fb846ceeb8f`  
		Last Modified: Tue, 03 Feb 2026 03:22:21 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7fa28684b74a5f88c92ec68e2af57fc9d43497f198923fb68da6f5a5c9923446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228819302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a352640a8ac624043e03c68977551d4f78281045e272aac454bed4436598069`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:24:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:24:07 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:24:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:24:23 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:24:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:24:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee447c22cfcf7aa978d4d42a3bd1ba7f806de37e774986f0d901518075c725f`  
		Last Modified: Tue, 03 Feb 2026 03:24:47 GMT  
		Size: 156.1 MB (156107672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0e3b5db012c419c3106006531bd95dfa0508faa8c253aaf6f8fe041d33f84`  
		Last Modified: Tue, 03 Feb 2026 03:24:45 GMT  
		Size: 18.5 MB (18541467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7f17f3dfde84c2e7eb4fa73b239459581f99ddb5d7dcfa7cec5d267d5c7b5e`  
		Last Modified: Tue, 03 Feb 2026 03:24:44 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6741e6261655c02846bbdc7e66f56ce0a405b55035749a0cc29a013a3be3ce57`  
		Last Modified: Tue, 03 Feb 2026 03:24:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6fc18c40b14f3cba549fc492a4d71cb08c432329188664389f7709c80b5e540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c6b13ff32fee7226cc767e77714e19e46360a14f07708e33accf46c88e8a19`

```dockerfile
```

-	Layers:
	-	`sha256:b6787328f7c7eed89a83c7918a18096354eaa8686ad8149222b638a51eda1027`  
		Last Modified: Tue, 03 Feb 2026 03:24:44 GMT  
		Size: 3.8 MB (3818218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bee98899d6a54b4bb55af46574074d2e4c9302f7043c503a320f5c43d441e01c`  
		Last Modified: Tue, 03 Feb 2026 03:24:44 GMT  
		Size: 18.5 KB (18472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0e6f6f8b960e2929fc2628d75ec0283325091b06c26327c9ce6ba26f7d15563b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234210690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733d022dad3914be913cc05177741f60306cc51548b5f86076d0c38dce6cc28c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:47:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:47:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:47:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:47:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:47:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:47:48 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:48:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:48:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:48:26 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:48:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:48:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:48:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:48:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073ee443853c23a0c81f2e493bac340b7fd10c67f60104022a9bece7ae4e7d7`  
		Last Modified: Tue, 03 Feb 2026 09:49:16 GMT  
		Size: 157.9 MB (157942921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddb46952b6ae68c4e819573c2880d0b350cdeba0109934e9674b4d6d2e19976`  
		Last Modified: Tue, 03 Feb 2026 09:49:13 GMT  
		Size: 18.6 MB (18637475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c529b8e004d80770f9be8b2f740a339730d054b3af15f535d1923bcb909c22a`  
		Last Modified: Tue, 03 Feb 2026 09:49:12 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845006d3e2f6b11fe836970cdf5e5d19adfe6fc864d2a55da806f5aaf456a4c0`  
		Last Modified: Tue, 03 Feb 2026 09:49:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:afa816196895897f9d1571e11c8a4791aed9ccf6d5b5424e615b150570410109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d86dbf7b273af3a3351d2de6630daf239e597855a806d643c3f230ed7b96019`

```dockerfile
```

-	Layers:
	-	`sha256:7c2d7db2b941af720fb2e003ddd6cd1ab6507a7eb20ad95935c9977ba17b9b3c`  
		Last Modified: Tue, 03 Feb 2026 09:49:12 GMT  
		Size: 3.8 MB (3818341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4cc6a6383a2cb56040ac1423b8d1d81c3e5099332473ac2700acf542d6597fb`  
		Last Modified: Tue, 03 Feb 2026 09:49:11 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3af124487137bcaca19e8728b13ebb7a105c9b971b74890e09bf2d754a39d22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228021149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72320e57ae442445adca1176c3d39e2d0a1b6979570f4d2abec2125de6f09afa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:42:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:42:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:42:20 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 20:42:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 20:42:20 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:44:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 20:44:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 20:44:51 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 20:45:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 20:45:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 20:45:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 20:45:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1cdbd3dbc058f023650ab2a7a190ceae0ea518397c9e3b43d69e110a89004f`  
		Last Modified: Thu, 05 Feb 2026 20:49:34 GMT  
		Size: 157.2 MB (157194298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef825ed6b4cb815620a413470d1de227b978d18b7374d0099c5274dcd8987a33`  
		Last Modified: Thu, 05 Feb 2026 20:49:13 GMT  
		Size: 18.5 MB (18531867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00598c25a0d76bd3b504515b709e1dfeae9c0ff765b647dc50eb689a10f9ab0d`  
		Last Modified: Thu, 05 Feb 2026 20:49:09 GMT  
		Size: 4.5 MB (4517790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856563d30a478383cbf81b7bb416c8e7bf91ccba3dcc0b3f6df680de2c7bff18`  
		Last Modified: Thu, 05 Feb 2026 20:49:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9ac76fe2468656ed12e3fbdc2fda882057da078ec2f25b5ecd7dad2f7be2cc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eccc2e7c0a12189825e11ee6398e51744cbab88c57d76812d0827107aa8b826`

```dockerfile
```

-	Layers:
	-	`sha256:012b118b71931fb887c507b16d1c4f20789a0410b535d66a78d429b750daf29f`  
		Last Modified: Thu, 05 Feb 2026 20:49:09 GMT  
		Size: 3.8 MB (3807818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11bf6fb819d5a9d367c96601033195942611782304a2a8e4d893e7552333c15`  
		Last Modified: Thu, 05 Feb 2026 20:49:06 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:02e7718559ca71f64c3148505c158fb73856dc86189831eaa1ec0c5fdda4b704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219563494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07d7dbf523df9f8d06a4660c8259dcb7458bb98a244d32121aabf6bf7c1d442`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:04:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:04:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:04:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:04:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:04:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:04:12 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:04:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:04:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:04:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:04:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110ef213ad849aef62022029533be2a09b2a6759b6635f693b2cbce0bee3834`  
		Last Modified: Tue, 03 Feb 2026 05:04:42 GMT  
		Size: 147.1 MB (147069858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603af855b1a3c5556978a6c32b7d5d8643f8dd7f6dac9760474a4768b12e30aa`  
		Last Modified: Tue, 03 Feb 2026 05:04:40 GMT  
		Size: 18.6 MB (18621114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0eb2a937986bdfe1e4ebee545e2b201130f5386f82b039f6d8a4ffd1c2aa816`  
		Last Modified: Tue, 03 Feb 2026 05:04:39 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84836de895b1d4d14ffc23d8f396436f8b0c1303fb848786309943ccb2c6fea2`  
		Last Modified: Tue, 03 Feb 2026 05:04:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d1680189029dd54d28b8b09a6d8f72be723591be5ff86a989bf0316ca54b7e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f776da87d0d253f46c63a26d137ca146e6856943354cb5713274b527c6ead9b`

```dockerfile
```

-	Layers:
	-	`sha256:335323df7b8ebd3dd5740d436800fe6ee77a802398f8ed646a030a8d29f471a2`  
		Last Modified: Tue, 03 Feb 2026 05:04:39 GMT  
		Size: 3.8 MB (3813768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587c4a60de4354ea9b26569629486e8291ed07633c6aacc412e61c33a214c1cc`  
		Last Modified: Tue, 03 Feb 2026 05:04:39 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
