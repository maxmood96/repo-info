## `clojure:temurin-25-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:c587456b45107b1eb194a471582b2ad801a7d6ea67dcd406f80bc222d55c2904
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

### `clojure:temurin-25-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:360453ab1c30870746d70b3d9c4488ff73668f887e62af23c6ca7fe7437bd565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165066171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d2890084e3ab9997a072f39bf56e4c496f204151caea07573e92dae6dbf34d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:16:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:16:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:16:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:16:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:16:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:16:37 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:16:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:16:52 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:16:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:16:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe1e0bd5b5c8fe64ce083f7bc3ca49aa5113fd74da92e5c8c551558ffcb3952`  
		Last Modified: Tue, 07 Apr 2026 03:17:13 GMT  
		Size: 92.3 MB (92256301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a398a967d8bdd9c169d62f289230ba4bb2bcfe227cba3967407e6e069414cc`  
		Last Modified: Tue, 07 Apr 2026 03:17:11 GMT  
		Size: 19.8 MB (19802868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3ac8a2b93a028d4ea9e740dde721e44e80a3903cb801b63fd1cfd10ef9c135`  
		Last Modified: Tue, 07 Apr 2026 03:17:10 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d5181b9088dc8ed6f699a4c3b028a16d87a04d33ad6fdb6fd9877c8c0f91d0`  
		Last Modified: Tue, 07 Apr 2026 03:17:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7ce1e812bcf058773fe8d91cb80ef5b37e2b0426c71bb2f1c68693ad920ec23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b245e8293c7f2a17a97e1e76a53fc1f2e3088f61308914b9325c1b6594bd22`

```dockerfile
```

-	Layers:
	-	`sha256:3c58deb5fbd69b0a5b2d43e41bcc7547784b8870c3ad390553cbb8ff01d1886d`  
		Last Modified: Tue, 07 Apr 2026 03:17:10 GMT  
		Size: 4.3 MB (4251027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fd86f7d4b2d589bc231c44415f80ecae02aa6d72def8a5a6ee009d18350da9`  
		Last Modified: Tue, 07 Apr 2026 03:17:10 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6c4b3cb4390ef27905c362014a0148a1a20d5be9d46f1c09b07f773a2637787c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163812504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54175a1404c1e63ac4fb4d186409656d519877207e9646e9ef4cf4682bed690`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:27:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:27:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:27:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:27:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:27:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:27:21 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:27:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:27:35 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:27:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:27:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3acd372f57eeab1ed9cd713175d0bf7e4c3b892726ce0dec1d3bf637fcfe443`  
		Last Modified: Tue, 07 Apr 2026 03:27:58 GMT  
		Size: 91.3 MB (91288270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e8f0a01c71d412c27d42ecbe9d00c711958df8f0bee5772eb58e9d811bb110`  
		Last Modified: Tue, 07 Apr 2026 03:27:56 GMT  
		Size: 19.6 MB (19632820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60de5d4269bc4d9f3e3f266103e036a10c2177dd7791fd960a529cb32d53c0e`  
		Last Modified: Tue, 07 Apr 2026 03:27:55 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53095fae702ad19b94f7c743d705e7bc02eca26fb902fad0e2272073a675e06b`  
		Last Modified: Tue, 07 Apr 2026 03:27:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6cc5d6d20c2431bc8c287a95d5cc132ef3ba364cf8836ce43810f8eb1e41ae5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc4eb9de155160b6f95378880e170adf3a4a56123952050c6533c1078fa3e7d`

```dockerfile
```

-	Layers:
	-	`sha256:05258444936c89c2e08873c08c7cc06384fb6ae33be375884fdf08760019bba6`  
		Last Modified: Tue, 07 Apr 2026 03:27:55 GMT  
		Size: 4.3 MB (4250711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d986ba753a603ff5e3ef0f98cfe51d51fe96b4c8b7e0a47760191ddb5498f563`  
		Last Modified: Tue, 07 Apr 2026 03:27:55 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:58cc074f85ecf6c8b5e852923d69ce1b62083f15148c4e153fddca20de81b5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168511471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a803687d15943cda4d2e5782beacdcf4226c533400f9daa47e880c142803fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:03:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:03:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:03:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:03:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:03:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:03:56 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:04:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:04:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:04:37 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:04:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:44:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:44:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:44:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81438db6b066b5319caf43fdad1d2cd4324d06132f04193db065dad00c8bc101`  
		Last Modified: Tue, 17 Mar 2026 18:06:02 GMT  
		Size: 91.6 MB (91632940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbb7e0a4408fd05d90beb04f1c7387137fa2b4b6a0805400ed94ee63a9d2443`  
		Last Modified: Tue, 17 Mar 2026 18:05:59 GMT  
		Size: 20.0 MB (20023636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66ec7b7df251db8f61f857203f7844ef8845574dabd5a355949632b6471a1e`  
		Last Modified: Tue, 17 Mar 2026 18:05:59 GMT  
		Size: 4.5 MB (4517770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed50f9d8e58b0d259beb1cbcfca7a0974d440e30c772690689e091968beb65b1`  
		Last Modified: Tue, 17 Mar 2026 18:44:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:99d73eacd25013cbb39ff4f8e83312696ffc55c318ba5bfaf07abd56ccfc4828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab14acfd1372ba457d9752eb9226d84e9e9308ca2c223493a6eebd2db444fd90`

```dockerfile
```

-	Layers:
	-	`sha256:971c814f6adc56098741aec1940169f073fb934eb25bf77d71404d11e8dff9c4`  
		Last Modified: Tue, 17 Mar 2026 18:44:50 GMT  
		Size: 4.2 MB (4236236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8e4b50db99ba9c769f1085eeade72fd2e6d43c087afe8d2607e22d75026944`  
		Last Modified: Tue, 17 Mar 2026 18:44:50 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:66c18bef94d84e9d704594989cc4862eecc68a80fcef8ea630853b5d3a956b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159363271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2434e4437dae3cc3cfa77eeafd6f925c0f1aaa19fcf91cf6af511461a1b98a92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:38:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:38:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:38:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:38:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:38:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:38:40 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:38:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:38:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:38:53 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:38:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:46:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:46:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:46:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6336049cfea2fb1bf6fe937dfa06a3231de1bcd109cc0d07cc3ba41fd378402`  
		Last Modified: Tue, 07 Apr 2026 05:39:45 GMT  
		Size: 88.2 MB (88233804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94d5138627d9e4edb404122d05597758714dcab9e5b88c41aa2fe814dd04b85`  
		Last Modified: Tue, 07 Apr 2026 05:39:43 GMT  
		Size: 19.5 MB (19463188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c53efa365a3be02bd634a88ae7bd02b5fa2c28b559bb0375684b4319d37eee`  
		Last Modified: Tue, 07 Apr 2026 05:39:42 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0f7d62fd23c30452c16a29ff17b1dc20dfb8f6ca89a10360d33b68e96bc47a`  
		Last Modified: Tue, 07 Apr 2026 05:46:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:eaf792a2933e69826856e055815187a06c2945c67c87e4f1a884a6ac0aa6482e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fb3ad3bd67f68136a5552d0928289357f5211ca58a927f64d07e6abf51ba49`

```dockerfile
```

-	Layers:
	-	`sha256:f4840977f44d427da0e3c3de5a7a72b6487c6404dd3c3a203d406b4dffb9a2a6`  
		Last Modified: Tue, 07 Apr 2026 05:46:39 GMT  
		Size: 4.2 MB (4227403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bed1c66d1f655fc2792fa7d2bc17515b9f65202cac83e3815df1d61c4d61b36`  
		Last Modified: Tue, 07 Apr 2026 05:46:38 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
