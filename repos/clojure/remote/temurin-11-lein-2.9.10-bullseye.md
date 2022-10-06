## `clojure:temurin-11-lein-2.9.10-bullseye`

```console
$ docker pull clojure@sha256:18b1a01c3a45f70176e6a31a946b364301648380719ad7893d17399c68c5df4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.9.10-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c210a0bcbfd6a65d158794fa2e27a8959a9d9eba6df75d0113d1197f096e911d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271836053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5409f7567e1d9cfde30048629b83d11da8eb0d54e5c8df46fedb248c4179b887`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:50:38 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:50:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:52:58 GMT
ENV LEIN_VERSION=2.9.10
# Thu, 06 Oct 2022 03:52:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 03:52:59 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:53:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 06 Oct 2022 03:53:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 03:53:15 GMT
ENV LEIN_ROOT=1
# Thu, 06 Oct 2022 03:53:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 06 Oct 2022 03:53:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3983f63d3e4b8776b5231e0bc9c49c468ccec1c53f32fc062195bdfef9cc693c`  
		Last Modified: Thu, 06 Oct 2022 04:08:30 GMT  
		Size: 198.1 MB (198125022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf555a933c50ac1c67421af7002e02e9dc5ccd87b22d237420844b915ce6bd0`  
		Last Modified: Thu, 06 Oct 2022 04:09:39 GMT  
		Size: 14.3 MB (14266082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad49d8a5719c9cbd3a72345c8a689dba04adc256721b1766113955b0bbf3450`  
		Last Modified: Thu, 06 Oct 2022 04:09:38 GMT  
		Size: 4.4 MB (4398701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:221846433cdf4c2ada0c76449de4069736e2209d7cb38f3ffe90e66df043e0a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.0 MB (267014081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e4f42433c55911435b7bed457844a55d4e70ae3dbedf27fa97c116b3faac94`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:31:52 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:31:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:34:12 GMT
ENV LEIN_VERSION=2.9.10
# Thu, 06 Oct 2022 02:34:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:34:14 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:34:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 06 Oct 2022 02:34:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:34:47 GMT
ENV LEIN_ROOT=1
# Thu, 06 Oct 2022 02:34:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 06 Oct 2022 02:34:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2152e7f09463e6c7e89c91d7854a893cfa62910bf4ac2cd6ac8b299794427865`  
		Last Modified: Thu, 06 Oct 2022 02:57:06 GMT  
		Size: 194.9 MB (194866576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69e8def07cef06b9db872083e69570e84723f221a3bb8c5433b3671da07e5c3`  
		Last Modified: Thu, 06 Oct 2022 02:58:25 GMT  
		Size: 14.0 MB (14048270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000fe6043a91419f3ed67a3487160069d193ec42f3bc250f4b80514e6f72dd4d`  
		Last Modified: Thu, 06 Oct 2022 02:58:24 GMT  
		Size: 4.4 MB (4398610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
