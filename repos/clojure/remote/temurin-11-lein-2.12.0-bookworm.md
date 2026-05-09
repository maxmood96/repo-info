## `clojure:temurin-11-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:9d2992fe8e81c6a44701ad81e795a17e812aff6385285db25a3b78d76782339a
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

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5f60c80d0f47f7eef61fa0bc1b20f2dcfc0e69c2a00515b0721bf28cdd176de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218699243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbad9cdcc524c70feafb0175b17f4f4e787d3c195ee97fb8303d95ac7742f6c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:15:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:15:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:15:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:15:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:15:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:15:38 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:15:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:15:40 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f47c1a719f2473f5f28427de07761e9e53a87bd5af15d38e6ea99d6b4e3310`  
		Last Modified: Fri, 08 May 2026 20:16:01 GMT  
		Size: 145.9 MB (145886193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50d87469cfb87a13bdaf6b8c26ab601b408332e10fa3ed3c1a3864399f17a95`  
		Last Modified: Fri, 08 May 2026 20:15:57 GMT  
		Size: 19.8 MB (19806585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d649dda57749d593521d06afcd6d951e74f529031d694517bf9e84954afa4e47`  
		Last Modified: Fri, 08 May 2026 20:15:57 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6c883f89ee4c53bc6920b2a791e75ff5eb5e6dfb56518f3db93a391dd9a73fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8124145c711b9d15f2c71c8297e313bfdb1302e5feb79b1ca20fb8f0ea4b0d1e`

```dockerfile
```

-	Layers:
	-	`sha256:cc7282e2efea4be70379aa169470fbccb875c9ff710667de6cfc183ce646c31d`  
		Last Modified: Fri, 08 May 2026 20:15:56 GMT  
		Size: 4.3 MB (4301874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bbc69b3d868cfc20d9fde3908fecc89b9acf4404515d451e086b2c453a79b1d`  
		Last Modified: Fri, 08 May 2026 20:15:56 GMT  
		Size: 16.5 KB (16535 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:52d42ba8c952b369d4058794afa7bd5a56de0202c9acab3c57e6cccb6fb69f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215110169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8bc7bcaeb111b47caf00bf1fb38d532c4c0f932c75c032bafc29ebfc2da0f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:45 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:59 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82caadc6c696330246c7b835ab41fd4e4202e75aae88198f5ed856799aac2fc`  
		Last Modified: Fri, 08 May 2026 20:20:22 GMT  
		Size: 142.6 MB (142582223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087a0214cff1cdbf1cac827d2897422da81c72d009ba46a40fc75ddf3d2374c4`  
		Last Modified: Fri, 08 May 2026 20:20:19 GMT  
		Size: 19.6 MB (19637007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e204f0ddbf65f1975b98a80004cb9e3482181456c5dd75f28cda8e5810e1bd64`  
		Last Modified: Fri, 08 May 2026 20:20:18 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0b476dde0b50af60c93a73a66fb2bb73f6c7bad77e0dc1d779aa6c96579cd1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ab1d6366a72b6addc3eeb2298d1793f69db991601161ad8ada334a08aadf7a`

```dockerfile
```

-	Layers:
	-	`sha256:795e7f05d06242df6be24b59d13f11941a66030cbd8abdbcef1ad61d8702a61b`  
		Last Modified: Fri, 08 May 2026 20:20:18 GMT  
		Size: 4.3 MB (4302107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d57a932fd2567b7e0bf0b2420b21f64a39f09197a609c08d1bdc13ea2ab246ba`  
		Last Modified: Fri, 08 May 2026 20:20:17 GMT  
		Size: 16.7 KB (16657 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:2c891ee0e0e29591b9be894b3f28bd7ff9d87aeaf0b583221458748a110ce65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (209995123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea3cbe4d5f76d34538b9ea178ab692db59ec2ab5ad0ac19925b64a896703669`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:32:03 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:32:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:32:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:37:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:37:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:37:50 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:37:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:37:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ccb486cd38d4bc6e81d6a758dc0756e8388df36970ae898570b04b2565a95`  
		Last Modified: Fri, 08 May 2026 00:38:30 GMT  
		Size: 133.1 MB (133110145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09edfdd545d7fec8fecd3717f397b9df8b54a6121e3c8fdfa4d287881c515a12`  
		Last Modified: Fri, 08 May 2026 00:38:28 GMT  
		Size: 20.0 MB (20030449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9154703084701f557390ceaff8d4290c1d9361cc530a515595ec50d3f01815`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:29aeebb380b596053addd8714f9384a8eb2fed574e0fa0a49817cc21355e8fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79158202f3875157ed6505fbaa02cc066473a98ffc89e34f9252c30d13e822e0`

```dockerfile
```

-	Layers:
	-	`sha256:335a8ecd935d79d36f82e7e598c7e5682c48a003e817b0357f088e52041aed44`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 4.3 MB (4303120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:597d54a2bcdfe268ed84ebfc48281ee0babaee70cbd93fcbe8f8c48d7545f872`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 16.6 KB (16580 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7a545f5578fbb8dbe33dbe188d24f082f355aeea3676efb5a351b1263f89f56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197784275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747f11ba6645408a9aa2294bc2ae6fb23cf6d57e3344e3240a8a192078fe4661`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:12:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:12:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:12:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:12:55 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:12:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:12:55 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:13:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:13:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:13:06 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:13:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:13:07 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70190c1a78cafe191cd85d9c3387ed7789d3847f12bfbd93c5484a305c7602f2`  
		Last Modified: Fri, 08 May 2026 22:13:32 GMT  
		Size: 126.7 MB (126651715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d3ece0f7076d4163853a81118be14274c36cc9bfa20d9f9bccc5e95df9faeb`  
		Last Modified: Fri, 08 May 2026 22:13:31 GMT  
		Size: 19.5 MB (19466793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba53ca821f6d632a1c695cb9659baec4496183e16730b5e1b6ad577eb5551a5`  
		Last Modified: Fri, 08 May 2026 22:13:30 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1d7b8e7995906e743d9cae853a01dffdd4ee7b38bb91867e29317f0cc1066797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96b186e0c753d84de7a5b43986ddb9632536ebe0da41909b61d0323c24b4713`

```dockerfile
```

-	Layers:
	-	`sha256:21d7d33696bcd5654b0fb98396827dedaf411dd03e204ba5ba2d277a89c1490c`  
		Last Modified: Fri, 08 May 2026 22:13:30 GMT  
		Size: 4.3 MB (4293692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b8d9fe31040c714674cb458962a44441d32e3e487659d051560d88c26c320b`  
		Last Modified: Fri, 08 May 2026 22:13:30 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json
