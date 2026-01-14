## `clojure:temurin-25-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:2699f23ff11d6c9a3ba5ff4fd8278cac304ee6b6f36e5390aa11f1018b26441a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:375e8b2688ac270c3ec74325b3b0b5d0c94fd9bb1671c83d1b9e7e905810eabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166927331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffe59f35cbbc9ed5ac8f261236aa902117461e4f0be4f5b99928c979ab65bbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:38:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:38:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:38:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:38:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:38:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:38:07 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:38:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:38:22 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:38:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:38:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:38:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:38:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a37f4c2a50fed339bdd342b7e158383f45ebda605e8a5bce396a7679120aedc`  
		Last Modified: Tue, 13 Jan 2026 03:38:55 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f178b5d499ad5a882188559a9512a3faaf218a60324b278947b7ed50ea13a053`  
		Last Modified: Tue, 13 Jan 2026 03:38:49 GMT  
		Size: 16.6 MB (16607462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedcd635ae77d8a457085804700b4b291bf7e62ade1583b72bf5363a7eec76be`  
		Last Modified: Wed, 14 Jan 2026 21:51:41 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f46ac9bd098ce12ccb0245f1625fa9ba980ae37cd8bd2299878d9babedd9dbc`  
		Last Modified: Tue, 13 Jan 2026 03:38:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bab92bcedb32d98a1673368b29388b0a43e0b8337c2f7021fafb2ac74e4c5f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a19a8ca99a42ad8a077a7a25cab91da2a57ff24496d7f1ecb5e337dcc587d7`

```dockerfile
```

-	Layers:
	-	`sha256:6233d1a9562d5560c365cae200ac9812f8f80fe008ee98014255d7032d082dc1`  
		Last Modified: Tue, 13 Jan 2026 07:35:38 GMT  
		Size: 4.4 MB (4427494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da0c0744b92777f335b11e1dcb9dc00b3dc3c1bfd2b4e504946864b543e6f96`  
		Last Modified: Tue, 13 Jan 2026 07:35:38 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5cc96d4000675580f3f043c08383b20a8b2f7137624a712c540f2c343eeee361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164423484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf896b5e1390a14ff175c69421147a1b8f769b98e31f57868600ec2714a4291`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:41:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:41:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:41:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:41:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:41:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:41:49 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:42:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:42:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:42:02 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:42:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:42:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:42:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:42:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc71f2d953cdbdde3033b0b425af33681a37cf01133ebd6af04eee2b95809c9`  
		Last Modified: Tue, 13 Jan 2026 03:42:36 GMT  
		Size: 91.1 MB (91052502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a9cf7ea9e19696081981dd5ecde6d6c7f8b9d0939f822242b50a4684ce3199`  
		Last Modified: Tue, 13 Jan 2026 03:42:31 GMT  
		Size: 16.6 MB (16595041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7feafd67f6ba7fd5113ca637c7edc8463b003e1bea6c83a1c0afa911275a1240`  
		Last Modified: Tue, 13 Jan 2026 03:42:31 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607345c8e128d483fa74435f5218175c3676c2154541f6f1f3744308af72b5f0`  
		Last Modified: Tue, 13 Jan 2026 03:42:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d5b7c50a9f54fbad52bb6b47d71135d25bfb265064bcf27268a2b979a3228927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4445637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc1ca31e7f6110b244614e573ffc7a679a0831203eb41d72972d6ecc623a6a3`

```dockerfile
```

-	Layers:
	-	`sha256:f47165aea03cada5decee27302f3bebaa174b503c23217e754756ac4702212fc`  
		Last Modified: Tue, 13 Jan 2026 07:35:47 GMT  
		Size: 4.4 MB (4426489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4630a961a1b3aa3a5e0b8535a2cfed1c0e2978e02b67d6d1e521385e09f4b9a7`  
		Last Modified: Tue, 13 Jan 2026 07:35:48 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
