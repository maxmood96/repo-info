## `clojure:temurin-8-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:4a1a062fbbb07463f92db49fa71d3330398051190ad63fdbbfd0a919c841ff9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:209ca788a207378deabd57c8dc02160eb912199975d790b8c3a63b21ffd4fcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105476842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18aa62fe1113b0cee57c3ab65d69e947a724db605a0dd476facca615f124ffca`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:17:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:17:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:17:59 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:18:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:18:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:18:17 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:18:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:18:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5d23877b51c01d1e3dd5916935066d4accc854310db45c2a02af8943165e64`  
		Last Modified: Tue, 03 Feb 2026 03:18:32 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f199767e391467cc5a24ca470f61620af6bb0716fff45bade08d9bf1111f3a`  
		Last Modified: Tue, 03 Feb 2026 03:18:31 GMT  
		Size: 16.4 MB (16447140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdff1876f85010754ce1124c7ea59bb30603d9581fe91579ade3bca9329091e5`  
		Last Modified: Tue, 03 Feb 2026 03:18:31 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13acc05d53e9be63c7cd572a94943e0aea3dc2c19909174ad31c2ee475bbbb6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59c632c60fae60a2879b6129e1c207dc023bc41287a5721290a9aefce080f4f`

```dockerfile
```

-	Layers:
	-	`sha256:1e0507ecb339f881432ba02714af8bc9fe3c92e9991bc96653461c34df5911b9`  
		Last Modified: Tue, 03 Feb 2026 03:18:31 GMT  
		Size: 2.5 MB (2485110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc211fa26a661e1d32419d02d6dcaeb2abaa5d3e84a05cc6bdeb5e466946be1`  
		Last Modified: Tue, 03 Feb 2026 03:18:30 GMT  
		Size: 16.4 KB (16381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e2dd6903e8dd4be9764f3bd63cb9975d4b89b07ae8be80569b5e862d152483d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104886409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978e5c66796462b21245d95eee4dbe968cd81cb0cf0ebf894d91adae5327a522`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:36 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:53 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2047505dae0c83b30a65b712ee6c0a65147c64e896e0370d771362f22c96fb7`  
		Last Modified: Tue, 03 Feb 2026 03:21:08 GMT  
		Size: 53.8 MB (53814976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da3a6f79333945e90551db1ed5faf5e9d019aef8516c624e0c3bec2284966a5`  
		Last Modified: Tue, 03 Feb 2026 03:21:07 GMT  
		Size: 16.4 MB (16413588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a6c9054b39d3ff8b02780f47915d6ff4f052337420a259c4ee9713a63f912c`  
		Last Modified: Tue, 03 Feb 2026 03:21:07 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a291a8cc39e025be5067d772d98fdbb78bd4ec7e52225f615f6e50a00719f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542ff72aee14df4e5be3871735c44dd97087161ffad4fb50b1e7f0ec47f9799b`

```dockerfile
```

-	Layers:
	-	`sha256:d6ae98a69f8f612f147df27d80a3eca501d7aa7791e0b6807a04c558d8901648`  
		Last Modified: Tue, 03 Feb 2026 03:21:06 GMT  
		Size: 2.5 MB (2485426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4227b9d4be160db9e4872509c077f02c4698b8f49b3be09696d3d612ed794a`  
		Last Modified: Tue, 03 Feb 2026 03:21:06 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:06f4dd4b22d20e8e980e5782a2967040df2af3b5b84d6956375bde4e8ddefda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106777913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fa2e68c64e94fd52608bf27a1ccb6f70f623295385bc2f26e52f7a51c4ba4a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:30:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:30:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:30:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:30:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:30:19 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:30:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:30:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:30:56 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:31:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:31:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c819a89e06acae8f0e6e8b0e7165e0365d89135dc37230b2f706d88a3eb226b`  
		Last Modified: Tue, 03 Feb 2026 09:31:29 GMT  
		Size: 52.2 MB (52175143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb12b334e7e19e6a91c8a4fd7b73b3f5f8463def5bc64836595f77129643a8`  
		Last Modified: Tue, 03 Feb 2026 09:31:28 GMT  
		Size: 16.5 MB (16484800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec8f4f511547bc3afea5f45feb3d1af4b8289732d828581255cf03fb5dea601`  
		Last Modified: Tue, 03 Feb 2026 09:31:27 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff5187fe7ccd3e6c983746cd35bf369c00c1d3e4dc8083ba30276b5ebc24b796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a38aceb9e1cdf4bc72fd7c352c1f4648c45847c1051b54c432b6de955786e4`

```dockerfile
```

-	Layers:
	-	`sha256:aa830c82b5e49e6ebd7869d431a6806a283c1a9a98d64014fe0c88c8d1fbb097`  
		Last Modified: Tue, 03 Feb 2026 09:31:27 GMT  
		Size: 2.5 MB (2486683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b695f05a00de8b0ecd6b0618904c057bedbecc4dfdb9ea6f550dc92c89d2e3a3`  
		Last Modified: Tue, 03 Feb 2026 09:31:27 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
