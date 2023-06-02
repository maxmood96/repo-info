## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:ec46175f465ff0ff6d721ce1753206121fd7e60bbad82ca3889c7f82165b5e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5ca7b7f4854692cc72c70c590a963971a4b0afcdc3ae67dbb979fa61e82bc429
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271858755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77b86ede8860867528e57df78ecad355254dc88b594297e1feb7b6eed6c70a1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 08:07:13 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 08:07:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:08:18 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 23 May 2023 08:08:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:08:18 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:08:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 23 May 2023 08:08:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:08:33 GMT
ENV LEIN_ROOT=1
# Tue, 23 May 2023 08:08:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 23 May 2023 08:08:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a637a166556170916fb88fe2f41e4f73c2a4d05f0bd97e2366c20d1c5a96c1`  
		Last Modified: Tue, 23 May 2023 08:16:52 GMT  
		Size: 198.5 MB (198549521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989cb1194c377ada00fd88e29106014798d49a5108acfc9e6d50796f50b23a24`  
		Last Modified: Tue, 23 May 2023 08:17:17 GMT  
		Size: 13.9 MB (13860926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464504f119b054656a236a3829746d8e843305f7b96153a50b4cfff7e1c20319`  
		Last Modified: Tue, 23 May 2023 08:17:16 GMT  
		Size: 4.4 MB (4399281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b66c65b99d9b59f20bf2f8aee4eae19ca1a147880b35f44afd51dad19a5e9230
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267265397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b31483695de2893e8f533a08ea864296f6f63acfeece332538f1139da66515`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:14:55 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:16:30 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 02 Jun 2023 01:16:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Jun 2023 01:16:30 GMT
WORKDIR /tmp
# Fri, 02 Jun 2023 01:16:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Jun 2023 01:16:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Jun 2023 01:16:52 GMT
ENV LEIN_ROOT=1
# Fri, 02 Jun 2023 01:16:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Jun 2023 01:16:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef10120da7ed1ed5a24c9b69c8e805daf6a8b4d4752ac5ca258e31f04763958f`  
		Last Modified: Fri, 02 Jun 2023 01:24:39 GMT  
		Size: 195.3 MB (195324244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae60e24036d7e002811621c190040160fe1e88cc84b4d373b8163f5fee77fbae`  
		Last Modified: Fri, 02 Jun 2023 01:25:24 GMT  
		Size: 13.8 MB (13849333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a999f436bccb3cc92d7f0fe9fa07e26cbcbe507222aedfd216f2dd33ecc0d5c8`  
		Last Modified: Fri, 02 Jun 2023 01:25:24 GMT  
		Size: 4.4 MB (4399208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
