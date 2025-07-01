## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:bee3c6145944bc8c41d40815809df5f1cd0f31ac006571af85a754a1c525d4ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:63cf4908c8ad06ab010fb7e755b11618649edaaf7fdfdebc789ce032f10dc1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138928240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a8425194b157615eeb725a09de945db8e81fbcb643fbec8696392d19a02c42`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178eb586fcc560f287bcc76b6152afa847c4a7ea4c552e8dc4e7d7a90390fb6e`  
		Last Modified: Tue, 01 Jul 2025 02:36:11 GMT  
		Size: 54.7 MB (54716173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90adb914d3c0c10e1ad4cf070ec58676df97c939505fc44f6a830229ab305a7`  
		Last Modified: Tue, 01 Jul 2025 02:36:09 GMT  
		Size: 51.5 MB (51467683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214fb91eac2be80b064ae684f935c3af8d5ad65593247c631b5435392f758805`  
		Last Modified: Tue, 01 Jul 2025 02:36:06 GMT  
		Size: 4.5 MB (4514209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b2c079af8829cefbb5b101acc8808b8ce4e5a2988fff2291d40134b10c5ace8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4627327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d560bd92cce1d9c555d919fc0c5f236b904beaa2d720b550bc3efcc0a11c746`

```dockerfile
```

-	Layers:
	-	`sha256:f852ba676c9e8aaad5337ff4ecf2d0884269054d2095941a1fc0c4d076c9fb5e`  
		Last Modified: Tue, 01 Jul 2025 06:42:34 GMT  
		Size: 4.6 MB (4610876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959af4ef6856c498dd19d6642d925cbbb201b58bfe6fa608c93f54410d747c6f`  
		Last Modified: Tue, 01 Jul 2025 06:42:35 GMT  
		Size: 16.5 KB (16451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d00018f350704609f0c7060046647efbe077812d6cec0378a9aeea2fe7f2cb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.9 MB (137856119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28abae7de507445057ade5e926e74dc8ab5748b057e4d54916b7ddc281bd181e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad0563892583b6c6ec5d5fbed80818f17182d77b30b2494ba804acaebf04701`  
		Last Modified: Wed, 11 Jun 2025 08:05:34 GMT  
		Size: 53.8 MB (53830509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e3d153798d71c20c826c2297648db7d08600c885cf3ca6cb2387f462cf8676`  
		Last Modified: Wed, 11 Jun 2025 08:05:36 GMT  
		Size: 51.4 MB (51433710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322b745e051ca24408826d5286ff7111bda9589c687a2c5a3fb4335bc81a59b`  
		Last Modified: Wed, 11 Jun 2025 08:05:27 GMT  
		Size: 4.5 MB (4514193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:19890c3a1a10a6d464b4427e571b8c65f85bafb4bd865f61e7c49bca4e0d7f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275724afd2ab9229ca00f8625833e5a527627d750659e8e28c4fa193ccbabb28`

```dockerfile
```

-	Layers:
	-	`sha256:68eecf44bf30120d988272f0f715124cfa15f6098c0d6f8c650a7d6d5fc73861`  
		Last Modified: Wed, 11 Jun 2025 09:43:06 GMT  
		Size: 4.6 MB (4615910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784c2d777770e2d63444797dbb1bcc4452222a429e8f81842158bbd435d264b3`  
		Last Modified: Wed, 11 Jun 2025 09:43:07 GMT  
		Size: 16.6 KB (16572 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:773f72fa2738335153cf9edefbfceea349ce1260aad0f5533047e6422d9c7258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145432761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06872597af8b47493285ceeccc5d74da623541d4c74a39958cbc3f83e1cf5b3f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0942298fc2abdf69cf3e6a970afc1659ec0c0948df86dc3a34aacc3e87a41dca`  
		Last Modified: Tue, 01 Jul 2025 08:16:09 GMT  
		Size: 52.2 MB (52167961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0041adef70b2ebd79f62ad429ca02dbb77456c56dfec8ec36aa14483a4481a`  
		Last Modified: Tue, 01 Jul 2025 08:16:09 GMT  
		Size: 56.7 MB (56677748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbdcf54ac3ecdcb26a2ec918984f65b2a68e35f20e48263174670ea4a63922`  
		Last Modified: Tue, 01 Jul 2025 08:16:05 GMT  
		Size: 4.5 MB (4514200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8198b87b8286b1efc2c821b1833b9038b3fe214617a6b17fe590f6f1918c2ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7d42dcfe3b6aed5b11eb4906dfdb895bff433645ea58a65f683e7bcdd26517`

```dockerfile
```

-	Layers:
	-	`sha256:aa26ff8a296d32f5ea3f60b00f7d55c2b27c326b419f71cc8b1b8e94509de213`  
		Last Modified: Tue, 01 Jul 2025 09:42:14 GMT  
		Size: 4.6 MB (4616300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a8aba3c0904aefcbf53785eac6f84005f14ed73220b0eaccd5801fe5d001e7`  
		Last Modified: Tue, 01 Jul 2025 09:42:15 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
