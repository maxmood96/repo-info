## `clojure:temurin-8-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:87b1a316d751adcf448281650adc5f0021ca78581b8de0c7698e77a0606ec03b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c65ca9e0212b9f1fc9766d65436a4d004a8b088cacb7dd114c398c8de1768d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127534896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b094a3b425dd9431a347cdd77c742f3e13e2468d0dbc42041e23fbaf3929415`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:48:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:48:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:48:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:48:36 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:48:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:48:36 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:48:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:48:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:48:50 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:48:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:48:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faef215933c28196d285cce12ed12d8c2b976a4bc0041a8a8ef6a8cffaae2eec`  
		Last Modified: Mon, 08 Dec 2025 23:49:21 GMT  
		Size: 54.7 MB (54733391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a37d3c6684bf064fcae402faa474146c0fd9544fe3d2fa959fcbb7601477e21`  
		Last Modified: Mon, 08 Dec 2025 23:49:16 GMT  
		Size: 19.8 MB (19802974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ce60df359eb47a103ddf565a8613c83f6209673ee8f228fb9d9980428a8f87`  
		Last Modified: Mon, 08 Dec 2025 23:49:14 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5563fc17ea10d64e1c28157dc7074096070e10780f3f13e8f480812045f04e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4417816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ed7e61420d1ba77a57cdc481a4ea9a1591c5dafbf593959b24688b7c18c7fe`

```dockerfile
```

-	Layers:
	-	`sha256:267e6efb4352cfe78fb756214828e63198964d4162501b7bfb1053b95dae784c`  
		Last Modified: Tue, 09 Dec 2025 04:48:20 GMT  
		Size: 4.4 MB (4401446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71e961a1eba75cb61ecaea6f2f45496a616f90f32003a44f026df24a96a9efc`  
		Last Modified: Tue, 09 Dec 2025 04:48:31 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a619e189b1fa9249cb3944b12e4173ab79505064e4c2ca03893b9e55fb00011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126323989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43e69c02629cf507ed6ba65412dafab08d5e1730a44283fcdd80951ed1ac77b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:57:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:32 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:57:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:57:32 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:57:45 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:57:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:57:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51290555ee3100897419a250bd2dcc2e8cf6c0ab52b9dd3b88f5be7d5b37e240`  
		Last Modified: Mon, 08 Dec 2025 23:58:14 GMT  
		Size: 53.8 MB (53814992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d416856703540b9fb51220cdd26b26a18135a67c1831dc4d95c79aae421da`  
		Last Modified: Mon, 08 Dec 2025 23:58:10 GMT  
		Size: 19.6 MB (19632186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed395779234825464bbca04be6ba1206625eb1f6598d2c0461939aa5240750da`  
		Last Modified: Mon, 08 Dec 2025 23:58:08 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9c9021180c661ae428d6da59e67ae0f9d7c47a6910e4a693b55c3c939264d0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4418250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b977bef2a458790bc077707d96cd10cc1498ad96e1551539e641379f9e16f8dd`

```dockerfile
```

-	Layers:
	-	`sha256:1d2bab8db5f7d647e38f8f0773899ad5d454f965a9406b737793541408a039f5`  
		Last Modified: Tue, 09 Dec 2025 04:48:35 GMT  
		Size: 4.4 MB (4401759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b02c1b54ae425c0f48a598436552c16026c064a95dc808ef889ff335a0c9b96`  
		Last Modified: Tue, 09 Dec 2025 04:48:36 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:24e4b040fd2208ffa772b863f93dc7a23bf1bf73e7b0f396bd513560997041d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129041513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35773c09d48c7c6b31082dbea3ac85efcbcff8757c4c97657fe4dfec73ad7b2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:37:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:37:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:37:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:37:07 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 22:37:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 22:37:08 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 22:37:32 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 22:37:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 22:37:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a51c77f8794a7a48d981ba475763915c444e47af96f90a51cb42c060ef190d`  
		Last Modified: Mon, 08 Dec 2025 22:38:19 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cc427d4c98452752d4a1a1886e4342ef668c5b453bf35d1b8515a63120b865`  
		Last Modified: Mon, 08 Dec 2025 22:38:14 GMT  
		Size: 20.0 MB (20021614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcee64c3f3fc26310b8c5d7d3ed2e1c39540c4e24030bf1997f9ed401a18123`  
		Last Modified: Mon, 08 Dec 2025 22:38:17 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:94f103f6e60401508f69df36f8b0de7d70177dac3bb739e9f92c90c628ed982f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4420312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5beffc6357d0ccef41ab5b8d05588ac918f96c92f8248f7e309cc48209977056`

```dockerfile
```

-	Layers:
	-	`sha256:c99bf1d69c0a86eeed6b2f2d51148b68b0a92eebe5cb54bb7a4334eeccc48036`  
		Last Modified: Tue, 09 Dec 2025 01:39:59 GMT  
		Size: 4.4 MB (4403898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c10c846dcb51ec9cdb6fd5df87d7391febbaa9c11a43a4d082a8bb82324ece3`  
		Last Modified: Tue, 09 Dec 2025 01:40:00 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
