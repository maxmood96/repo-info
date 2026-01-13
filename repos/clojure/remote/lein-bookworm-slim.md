## `clojure:lein-bookworm-slim`

```console
$ docker pull clojure@sha256:3cf2eb42ec89b85e1d594d4af9fd0b56683b9a3fb3c42a7206df0ebcc1f93e1a
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

### `clojure:lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b6bfb292ca3ca6270188957dadb3df332d2cec9abdd6f055fd52ae3dba0a548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142549929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f161d65644ac7bc32291960af7b536fe5340b0726fb916c4ff01b5ddb85134bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:06:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:06:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:06:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:06:23 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:06:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:06:23 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:06:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:06:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:06:37 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:06:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:06:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:06:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:06:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cadd1d04c25c1af3140f14a1cdfc3b2540614c4abc9e48a10b252684db2565f`  
		Last Modified: Tue, 30 Dec 2025 01:07:12 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8688c19b5f812254cf0190de76b682b31c5e52b7efa87886fb119632d7718b`  
		Last Modified: Tue, 30 Dec 2025 01:07:04 GMT  
		Size: 17.8 MB (17758081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc6fac02b1aa5ef36dc9ce96609fd6ced33a6cf88ed950694a09bf8a729c0cf`  
		Last Modified: Tue, 30 Dec 2025 01:07:02 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a24eba45e3bb65f9d6d0352cedde69a8fa4c6f0f57ce894630072991eca303e`  
		Last Modified: Tue, 30 Dec 2025 01:07:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d096846d1c655b5855f0f99b8b49a359996ea83b376dac567a65a4861fff0529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3400c02692be4a7e6535cad07dce334cce7e636321414decae6ed7ed00d1229b`

```dockerfile
```

-	Layers:
	-	`sha256:02f68f8b9e9e160aa6a7af2d3f2371ac36f5dc26bd4597400fffb48617eafd18`  
		Last Modified: Tue, 30 Dec 2025 04:35:19 GMT  
		Size: 2.7 MB (2680112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce938ee09ac355a14e8cfabdfd12b5d4845c8b878bebb22b3b69e9af20cd2968`  
		Last Modified: Tue, 30 Dec 2025 04:35:19 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:24ad57b791cf03d187e62200c3838feb4d7627f66c25daf58979765c357692e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141264007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5565d7c5540324fce7181e4cbd5d952ac15edeb53281d6670402ee2622c7e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:07:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:07:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:07:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:07:20 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:07:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:07:20 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:07:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:07:34 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:07:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:07:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:07:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:07:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3291eb324f97ae7b7f720cb397123184752e792cbecddd0ba01c848269cccea1`  
		Last Modified: Tue, 30 Dec 2025 01:08:14 GMT  
		Size: 91.1 MB (91052500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6460a980d70e8f7f67efbe385ad37137979c9400e9dc58d7e4c27f4e3323aa4e`  
		Last Modified: Tue, 30 Dec 2025 01:08:04 GMT  
		Size: 17.6 MB (17591128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b666a90f66520f7df4b548f8f7429cfa9b3774b273994eabb315e8ebe7f5f0`  
		Last Modified: Tue, 30 Dec 2025 01:08:02 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f327835a51bf2af674a2ea93eb613d28ba2fddc836e807153d88fb7c27f43fad`  
		Last Modified: Tue, 30 Dec 2025 01:08:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b96f226b80b669131e43c3738d268ac8885d887300b337da4ea3fffd7eadac5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a0abb39f81e13a665bb3c4cded3035825748bc81652d45001a63b36fe38547`

```dockerfile
```

-	Layers:
	-	`sha256:057dcc5a589a55083619fa6c8c254adfbb443b714a59daf9b7b4db0895899b6b`  
		Last Modified: Tue, 30 Dec 2025 04:35:23 GMT  
		Size: 2.7 MB (2679748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c89a63136c27423ad32ce6a858175744e7b075a33434b8875cef5a1d644d028`  
		Last Modified: Tue, 30 Dec 2025 04:35:24 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3988f005a19c430e6bb2a7898ffb7ca49621146f90c8c13ce2273c1adbfd303f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146157420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceec6fae77aaec59037be09fd3de8a6b7a09212a0be3c422d7c980241f67644f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:27:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:27:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:27:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:27:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:27:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:27:57 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:28:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:28:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:28:31 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:28:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:28:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:28:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:28:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbdc8c4b3ff1ba34b10d9319fbd72ddd62e70a3e9d93f8bff5484d7ddbc79e1`  
		Last Modified: Tue, 30 Dec 2025 05:29:26 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ce385ef3af18cf8e353ca585425a902b6814393b75b1f5e855cdc81702faa2`  
		Last Modified: Tue, 30 Dec 2025 05:29:17 GMT  
		Size: 18.0 MB (17959606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91994733b8085fab30460ee25e66c1d2cc37f19c335173d1e586a4a7ee35e53d`  
		Last Modified: Tue, 30 Dec 2025 05:29:16 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a486d54c03fef35714bb21937e6087727d1fa2d3b1bf39f17ceefe05d840d027`  
		Last Modified: Tue, 30 Dec 2025 05:29:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3bc7130182f73928a10cc418e076257ef40194e6faef49b4353513582bf94401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005874cec46bd4ad14990aa91a6e1a35d01391f02871c74b374b911ea6fca0a1`

```dockerfile
```

-	Layers:
	-	`sha256:cddbc87e15f95b9a437817016f0bad1b4f19328d80cd9c073a927702d6ebc7fd`  
		Last Modified: Tue, 30 Dec 2025 07:34:31 GMT  
		Size: 2.7 MB (2683255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:808271a17f7a738ea3e15a358972faebf728485c7adc2238746b9af6e74341aa`  
		Last Modified: Tue, 30 Dec 2025 07:34:31 GMT  
		Size: 19.1 KB (19113 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9073ce42ea9bbbf6d630d1eb690d4bf5575d94dbc0f6af1d9e183d9874b0e2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137034108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014102fa617e8f49597b024c27e04c911d7fd25afe48ce39d3182d88964b654d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:08:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:08:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:08:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:08:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:08:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:08:22 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:08:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:08:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:08:32 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:08:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:08:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:08:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:08:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fedf639c136731205d5f1e19fbc4ea363b7ab6ef5576a3c1b39562e2fceead5`  
		Last Modified: Tue, 13 Jan 2026 03:09:14 GMT  
		Size: 88.2 MB (88210715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de96067426d5d0a91a17824c2ad8c3bb0b6ed2745d5b5bc331bdf299ad4f0e50`  
		Last Modified: Tue, 13 Jan 2026 03:09:05 GMT  
		Size: 17.4 MB (17420839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaa151df2a46cc9ca62e267ea9d22ad4e0fd6be6aba7cd8037f0ca99ea83a7e`  
		Last Modified: Tue, 13 Jan 2026 03:09:05 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590ef031ac21ec2a0f866e8f0ff335940219c81ee27f23641884453148458a81`  
		Last Modified: Tue, 13 Jan 2026 03:09:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2fe0d08106bc2f2e0f38e2b67879f7b39e8e84ef097286b92d6a2196da742407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313a3a34bf93fd63c5eba573589735a5e37321ffd6fca41fb7254816401b4999`

```dockerfile
```

-	Layers:
	-	`sha256:1bd300ec88b9fd14ebea3013deeca269461e1a375e41165badb1f7a17c26d849`  
		Last Modified: Tue, 13 Jan 2026 04:35:35 GMT  
		Size: 2.7 MB (2674484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c27800049deb148b4685a0da1cb4d4ee14ff6b91cb2fc88a0df27bd70bb4e1e`  
		Last Modified: Tue, 13 Jan 2026 04:35:36 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
