## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:fdf4d5206b1d89f0d3a137635b0d148d4b433976044c97991a3b0a69bacc19a1
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

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:78671a6310a7bb46622ee8d36638996671dc63d6d0a9542c1712126c89d4dc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218197657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f651b837c6af2b59f84d817f7a0808cf0e8682c8a1c76cb6dc4f9bce05a2862`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:02:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:28 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:02:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:02:28 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:03:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:03:22 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:03:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:03:24 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ebf691c4314a22aeca8824ddf7db4a9bdd4a5b230fd5c8bfa1712afc053b0c`  
		Last Modified: Thu, 05 Feb 2026 23:03:44 GMT  
		Size: 145.8 MB (145806888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78adc18fcfbee3e9bdb4de3183d0c328eecfa9956a3f4b8e7db651ba046f60b`  
		Last Modified: Thu, 05 Feb 2026 23:03:41 GMT  
		Size: 18.6 MB (18580059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ed4da666d05d378f0440c8f6dfa3bcf84640fcdd6b364fc1db46e93a87c214`  
		Last Modified: Thu, 05 Feb 2026 23:03:40 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:00666962bd2917c82eaf3e29bc46e574a1b5fbdbb9b2f0e5010b2be17c61a1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a015a3017078a5d1681a8844c9d11338e1046340780896ea65d897b2a71cf2`

```dockerfile
```

-	Layers:
	-	`sha256:8817530e06d22d7fc66d183359fbfb542f85004c7210219d9a94ed9879b355a2`  
		Last Modified: Thu, 05 Feb 2026 23:03:40 GMT  
		Size: 3.8 MB (3835632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219919c0eac324de530938071477be30406cb23fb2634e9ff8668a7b2774dcd5`  
		Last Modified: Thu, 05 Feb 2026 23:03:40 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85c2b25d77bd11c13d34329506a74ef352abfdafcda5681c0708ccd0cf24fcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215212119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a82a9275011cb00d3328c65c3403303e842fff4bbf6ca1f0c45f3d02a975649`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:03:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:18 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:03:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:03:18 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:04:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:04:13 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:04:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:04:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0de5ff7f4201f94926e57dc815ec622c47b088e70642cff93dbdec62f40a71e`  
		Last Modified: Thu, 05 Feb 2026 23:04:37 GMT  
		Size: 142.5 MB (142500831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c284f9bf3eb395a4e8d7fe23ba64514415c0825edc7dfdf6cbb651d9c8c6727`  
		Last Modified: Thu, 05 Feb 2026 23:04:34 GMT  
		Size: 18.5 MB (18541498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c05b2a69e1f612cafb3a8fa4dc2b4f59f3e5172c32bc94e13e0713e94a8cb1`  
		Last Modified: Thu, 05 Feb 2026 23:04:33 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9a2a9b24d57850ffad8d45e8d8109c6189aa2b8f8f3902666c7fd5b9411d11c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9be41641344e67ae9b24bb33b7833367c59e0335bd4ccf273c4d4e46e233e0`

```dockerfile
```

-	Layers:
	-	`sha256:33a40a4505fc1a14783b42be02b82c0839fe8c51d24eefc89e13c2a90383ff02`  
		Last Modified: Thu, 05 Feb 2026 23:04:33 GMT  
		Size: 3.8 MB (3837127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ac119b6bc401e6d3187b4d21e3beee27a707e4cc42d01edcfab781dfb20c03`  
		Last Modified: Thu, 05 Feb 2026 23:04:33 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:eaf4e620ce52b8fd25d344bdbcaa2e6fc762f9af6306d82e5be18ca4f4b261c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.3 MB (209264318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7eef6594913854cb0465605192cad37ccf0797dd5fbff360f7ecbc69a2eb5d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:12:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:12:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:12:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:12:45 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:12:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:12:45 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:13:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:13:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:13:48 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:13:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:13:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9196ca82c2237253cd105f74ebc47ce2f1292126825ec1d20ea1c7d414806`  
		Last Modified: Fri, 06 Feb 2026 00:14:35 GMT  
		Size: 133.0 MB (132996872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1443e44515f446963632f23f54350960692d2bc515c29791905044de48a0b4`  
		Last Modified: Fri, 06 Feb 2026 00:14:32 GMT  
		Size: 18.6 MB (18637537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d50800befafbbba5b1f8fcaeb2b02750f53ee9727ceeb879f9e52e55c5e3227`  
		Last Modified: Fri, 06 Feb 2026 00:14:32 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eabf6f1aefccfedcc08ce701ebbafb1d12275a35503efea6a3bb046852ae8712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b232a50e06bf5871d0d07c6a35adcc6026f10127355ff127991708cc6e95e43e`

```dockerfile
```

-	Layers:
	-	`sha256:989514de91b095b9f529e5abfafbb616c0470d2720d4e22df622c3a5eaf3c776`  
		Last Modified: Fri, 06 Feb 2026 00:14:32 GMT  
		Size: 3.8 MB (3836017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e53935dff0ad9b146031b71dd764e2503a3ad3d8a6da9401cfa9b3740f0064`  
		Last Modified: Fri, 06 Feb 2026 00:14:31 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a2f1ca5f3b33c5a563c9bc8d80ae9d9edd7e2ac42dbdaddd758b4732863af742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199055451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249abc64bc8cf2f09f7c22abecfae3e46126282b0f50fb9a6112022900dff48a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 22:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:59:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:59:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:59:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 22:59:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 22:59:27 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 22:59:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 22:59:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 22:59:43 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 22:59:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 22:59:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b198bbce5234d6c6418a67ec8420254720961b6a7485c3877bdf6aa827e27`  
		Last Modified: Thu, 05 Feb 2026 23:00:19 GMT  
		Size: 126.6 MB (126562163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fc844cef4afa8fcdc810e0a324217425d722f6ca5bbf60d8e956cd494d39ba`  
		Last Modified: Thu, 05 Feb 2026 23:00:13 GMT  
		Size: 18.6 MB (18621127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b31e271c6959ff19addd5f23874df833efd58b76a367be5c922e59844cf6c2`  
		Last Modified: Thu, 05 Feb 2026 23:00:13 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2ef8362c4d55298362ed0d2bc9f0ce5512db9ec4e9abc238805105037c59b364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ca8fc378379a14616b4ff88ef29ef5e05011c4d8097a511fe3d070933a14ce`

```dockerfile
```

-	Layers:
	-	`sha256:820fd8a26d4eacd4fe7a767cfabf991d7b5ef51e451c7994ed05f9642f606489`  
		Last Modified: Thu, 05 Feb 2026 23:00:16 GMT  
		Size: 3.8 MB (3832063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b4b4b46496a9d1e59c8bf4e6655d18e296e2326ab274b22e23915bd472c96ee`  
		Last Modified: Thu, 05 Feb 2026 23:00:13 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
