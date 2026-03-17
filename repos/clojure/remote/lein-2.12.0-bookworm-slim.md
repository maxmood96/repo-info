## `clojure:lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:5750d75c8c80f7a5b975b849456f77172e1e0bd9298c4db37e3f15451674e99b
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

### `clojure:lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9118a6c29edc2b99dbc382d2a5aa3320cc2686278c1ffffda53fb98a8d38cb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142769481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75d15cbe71905771ecd4202df43d4ae27b347fe97825873573da502bc66a42c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:00:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:00:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:00:30 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:00:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:00:45 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:00:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:00:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:00:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:00:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d734cb92863bf3fa2e9f3fdc5dc3e71c0f4a4366cf67f9dc0db206a7c9573a`  
		Last Modified: Tue, 17 Mar 2026 03:01:06 GMT  
		Size: 92.3 MB (92256314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109233b7523052c3e1fa3c3ed79317e6e3944b1d2acf400b7fa0f684e4954aad`  
		Last Modified: Tue, 17 Mar 2026 03:01:04 GMT  
		Size: 17.8 MB (17758801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28b22ad47f8a6a7f84abd674357a0d39340474465bd432421f8047254a80f83`  
		Last Modified: Tue, 17 Mar 2026 03:01:03 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660195150a8ff615affd773bd52a15684ff08491330297a4061f65140586f425`  
		Last Modified: Tue, 17 Mar 2026 03:01:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:56cda8984ee118003bfba21fd78b9d339b93db21605b4acce3e3336102e561bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36a66053ebdaac8c6dd22589cf79db425eeb2870dad9d903348e85d44de98e9`

```dockerfile
```

-	Layers:
	-	`sha256:6f87c31d1686feac99a2da7cbf85ed510eaefce4c2c54620428d05544156cab3`  
		Last Modified: Tue, 17 Mar 2026 03:01:03 GMT  
		Size: 2.7 MB (2698110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f405f7227a1256e9e265864606abdb398a1a9fddeb5ac6c4fea220e6f2f06da8`  
		Last Modified: Tue, 17 Mar 2026 03:01:03 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:964b9012275f03dcaaa3f3c5ab9470adcc2ac00e788c52f8772b578976d8c532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141514336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8b0dadd6aecc408993dee47b10503348264835a890ba50d27e775aa2bbd229`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:05:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:05:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:05:16 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:05:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:05:30 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:05:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:05:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52959b05d9e93c66e8f12b48f6edc273043d6f0610e754d2f1c81b2ec1ccf7b`  
		Last Modified: Tue, 17 Mar 2026 03:05:51 GMT  
		Size: 91.3 MB (91288265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8374d0f937b28b79be6666e6748bb0cf842a625b7b24bb746df929f002e2c299`  
		Last Modified: Tue, 17 Mar 2026 03:05:49 GMT  
		Size: 17.6 MB (17591831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f8ebc615b316f7fe9374d70f7a8aa61b09aa172fc0b3f69fb8c122848f7583`  
		Last Modified: Tue, 17 Mar 2026 03:05:48 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df4ad53653aeca9c88df0c6eca7a0c51fff7087b8c0e4ba0abcdcd3ee29d20f`  
		Last Modified: Tue, 17 Mar 2026 03:05:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd871bc84f34829412e8b0861f5aeb39dab1dd44a19603578f4586cd3f990366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de9ab13e0c5bd4242251c4546b2dfc13976d2489a46a3146261ea3b180498df`

```dockerfile
```

-	Layers:
	-	`sha256:4900410e676a131912e993f9538cfc2d22e9ee18c322ebdaa11a891110acddbf`  
		Last Modified: Tue, 17 Mar 2026 03:05:48 GMT  
		Size: 2.7 MB (2697746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2afccb04d18328e2c383d8c9eda0bb1e7008c7b6c52daacfd437a2abb511f497`  
		Last Modified: Tue, 17 Mar 2026 03:05:48 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b8060a6731f91ea536bce6e6c4357dd960cd3fd18de1e46cd069fdfa2829b61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146190607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd00409df887981cecbaf31b4cf67d575930698fc5c0bf41e1aea9033f4aba9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 02:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:14:18 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 02:14:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 02:14:19 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:15:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:15:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:15:03 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:15:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:15:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:15:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:15:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba348ce5bf0fcaa6972e10095c9a06c61641f8395c5fafef888ed9e3e07d216`  
		Last Modified: Wed, 25 Feb 2026 02:15:44 GMT  
		Size: 91.6 MB (91633003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6873dc6208672e7965619b6bf9ce03e1bbb233e6119b6dfb05301a982cbb2b`  
		Last Modified: Wed, 25 Feb 2026 02:15:42 GMT  
		Size: 18.0 MB (17961077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb8bbc08ee5ff289ce66aa27b565b3bccf6ad2e5536b369e307e4cc9d04539`  
		Last Modified: Wed, 25 Feb 2026 02:15:42 GMT  
		Size: 4.5 MB (4517765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39c50e2e450736890311dee5d81f3fe3b6715e20c103b73dc400e5811d843ec`  
		Last Modified: Wed, 25 Feb 2026 02:15:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8fc555c2e797352d89c9063e84d7048b74c77844ccc03b0521f7c397db82af4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017269771af4bcac2370a36ea99dfc9308d343acb84bed4b2f96b60bda3a60de`

```dockerfile
```

-	Layers:
	-	`sha256:d6b7d6b267c5c03fd1780a743e9d688fb626acac2b4e18082dd2bf2204b447b4`  
		Last Modified: Wed, 25 Feb 2026 02:15:42 GMT  
		Size: 2.7 MB (2683267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d044fed378ba3e116056c8817a43c21ab9edf6574717d4652ec19486498809df`  
		Last Modified: Wed, 25 Feb 2026 02:15:41 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:23985aa37fa252826a802933ba7011d935fb2e857f06e4e74c774c1e486cef65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137064744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3244c7c53562c1424c589dc6b6eee787bcb14d4549b33c8b6fd1ec77e7823b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:22:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:22:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:22:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:22:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:22:55 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:23:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:23:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:23:28 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:23:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:23:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:23:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:23:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2c7f155ba43475a58ce53d7548c5de702bcc0cc952b4fe414a2ed67d07e94`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 88.2 MB (88233846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9a3f30508869f9674f86fa6de14e5ded30afcc5aeb9f827dbf24b2c0313e43`  
		Last Modified: Tue, 24 Feb 2026 23:24:08 GMT  
		Size: 17.4 MB (17421191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c6e810204baa620baeb52774b91c5e38691aedbd19f36fab8f0e4e8e5fcb6a`  
		Last Modified: Tue, 24 Feb 2026 23:24:08 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dbac5009380a7762bdc2ad39a9a9cc9599a48379ac6c3df8a3cbdc911f861c`  
		Last Modified: Tue, 24 Feb 2026 23:24:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ef13fcdc1c6d5d08592ffea58ca065c28e8ea0c3f3613c06c653f154ff7fd99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7412a4c005e2313b06e2b90593511f80eeeb9c686fe52776c27915af59aa03`

```dockerfile
```

-	Layers:
	-	`sha256:1e1973a84a2b39d451a7d8823d8a3311f57c17bfc588c82d6863fb74115ce2d4`  
		Last Modified: Tue, 24 Feb 2026 23:24:08 GMT  
		Size: 2.7 MB (2674486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3996807e0e2970505df650c5b7a6b663c17ade60da99b3966ceac352ed9644de`  
		Last Modified: Tue, 24 Feb 2026 23:24:07 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json
