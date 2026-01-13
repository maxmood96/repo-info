## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:688ff27a4842d5da7a28ea7ba87c72e13a805552331174053c30ad96c0fc08b3
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
$ docker pull clojure@sha256:896a8dc0a2eba53c27556295712c376dcd360066e0d5c13a00f912ff6383f7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217768506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328015e251f8bd3a0dc22b4685c0522d440a8d8b4157f7c3ca398c77684d7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:23:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:23:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:23:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:23:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:23:00 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:23:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:23:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:23:16 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:23:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:23:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2b2540b9d0847be9dbb4faf0972c1e6ce6f44bcc50210c3fe218d19943fb15`  
		Last Modified: Tue, 13 Jan 2026 03:23:38 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3033a694c346dc0f9945c3c7a0e13873f1a9f673c5ef5160db69652697d51287`  
		Last Modified: Tue, 13 Jan 2026 03:23:45 GMT  
		Size: 19.8 MB (19802485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9e3e2baa581d6bd2f21c9e6b5784bf00318ef6b6b4d12d92cc2119e85aead3`  
		Last Modified: Tue, 13 Jan 2026 03:23:44 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:df93bc4ec7fddf76c75f0da688c911f812897d2ca1a013bda06900ab70a6982f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4317000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf09dcf967099e46025c332571d15bbe569baf542490162020ea7cb49371042e`

```dockerfile
```

-	Layers:
	-	`sha256:3dc20f64984cf7fbc4a9c20be56f0694d099c13f1be9ec933e426e8b0da66656`  
		Last Modified: Tue, 13 Jan 2026 07:37:10 GMT  
		Size: 4.3 MB (4300618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad2534658fd9e0d9e61be998bc92d0023476858219fdb10a001f5edf0cb76d6`  
		Last Modified: Tue, 13 Jan 2026 07:37:11 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b218b39c29d1a2c0c96ed648410bccd13bf1de6ea0018f16940805afc207aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.2 MB (214248074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932fe4e545835dd7e86ea7746d7f8f44786f784ee004c40d104cf2b563e7d54d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:29:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:29:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:29:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:29:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:29:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:29:29 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:29:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:29:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:29:43 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:29:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:29:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775f50608a55dadf9437819019187a025737fe48d38f06a8346055203accac7e`  
		Last Modified: Tue, 13 Jan 2026 03:30:26 GMT  
		Size: 141.7 MB (141731552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a5dbe6b8c00e613046c7aebb4028115526fb82403567e322709aa66277bd63`  
		Last Modified: Tue, 13 Jan 2026 03:30:26 GMT  
		Size: 19.6 MB (19632696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b27585fd8f3930053f67195acf0d61503f073700f848a8d0ede64bf01e11a5`  
		Last Modified: Tue, 13 Jan 2026 03:30:14 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dd20863014ee430bfdcff7a285f92d36b03336a0949d6d7ad705616d084a28b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4317352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4faf923d568d5f3047ebaa00bc70fa3c1c3635235b0b3f884942af254f6e13c`

```dockerfile
```

-	Layers:
	-	`sha256:0563612b957d93801723cd9d80015ac3666fe2bc8770676c4d917591bcece2f7`  
		Last Modified: Tue, 13 Jan 2026 07:37:16 GMT  
		Size: 4.3 MB (4300851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2fc532765a08eeda14a6fc451af7128e388952a5f41066b1e5f5726ec4d018`  
		Last Modified: Tue, 13 Jan 2026 07:37:17 GMT  
		Size: 16.5 KB (16501 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d7ecbb8632134b58785309fb6d3e5159335c0fa3dbf27ba29eb5cb06c660d475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208949718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ea95fc4d49a340207d734c13049ba6b862470ef47046828c42502f495c3e4c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 05:35:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:35:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:35:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:35:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 05:35:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 05:35:58 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:36:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 05:36:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 05:36:43 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 05:36:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 05:36:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05ee15f4f80900e39229320dc4a18f31e5467836d53d8648177af2819a8867`  
		Last Modified: Tue, 13 Jan 2026 05:37:28 GMT  
		Size: 132.1 MB (132081995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dce6ebcb841502ab107e1ca916871e843e99cd04a83d96bfd78a4226cdfd7b5`  
		Last Modified: Tue, 13 Jan 2026 05:37:40 GMT  
		Size: 20.0 MB (20022538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab51b789f01ae79383656e0b42291d14b731187d5195ddca8cdf03ad5f0af22`  
		Last Modified: Tue, 13 Jan 2026 05:37:45 GMT  
		Size: 4.5 MB (4517777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2fe3c00f9372593f48b124a7fcab86501f312d1f55f3c4d2647f59664ec2a1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68a461bec460071530a4c6347dce6fcbb8fdb6469566b29acbe033b8611000e`

```dockerfile
```

-	Layers:
	-	`sha256:a5ecf75df21f917bacc11535c91888cfc6b7be86722c1f430c74558e1de9f0e2`  
		Last Modified: Tue, 13 Jan 2026 07:37:22 GMT  
		Size: 4.3 MB (4301864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f500941d449b9e2659c462ae992fdf52a59de96c89af05fc810da6f2d0738c4`  
		Last Modified: Tue, 13 Jan 2026 07:37:23 GMT  
		Size: 16.4 KB (16425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0aaf52377107127d4ceb73f888229e6812372b96408ec48ed28aabca2d5df4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196812611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b76ed2463a2da4b2dff59e59d91e92ec44b9ec5d5dcc889ed0d581e96cfd226`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:59:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:59:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:59:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 02:59:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 02:59:46 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 02:59:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 02:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 02:59:56 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 02:59:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 02:59:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5705437884b10c27b4c725a79af51f738cfd9ac5681ae63412beb31d236180a2`  
		Last Modified: Tue, 13 Jan 2026 03:00:48 GMT  
		Size: 125.7 MB (125694398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fe5c3224f751656da4af72542b3f831c646b63e68cdcbe5277c3ae6c1d6f28`  
		Last Modified: Tue, 13 Jan 2026 03:00:34 GMT  
		Size: 19.5 MB (19462036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50348f7daf98ef234c486d2156936a110fbfea77e485620014a584008273c021`  
		Last Modified: Tue, 13 Jan 2026 03:00:32 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7cea3c8a56a6da44184c317e1d843dd30233bc9fa19ede76fc50b2232f62c9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70fad8af34f73674b7824b1a326e85e846978fa43036db1c5658d2fc72f0fda`

```dockerfile
```

-	Layers:
	-	`sha256:bb02d9620343437151ca57689abbf6198771ec583aec15bbcb0e248b77662119`  
		Last Modified: Tue, 13 Jan 2026 04:36:05 GMT  
		Size: 4.3 MB (4292436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0940588581a2ff45f30a50be79c402d6382c34592a026598bfb6f9b7a255f08`  
		Last Modified: Tue, 13 Jan 2026 04:36:06 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json
