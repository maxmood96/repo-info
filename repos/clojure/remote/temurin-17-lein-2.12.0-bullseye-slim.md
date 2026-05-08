## `clojure:temurin-17-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:32a5e62ca7bda1298701f495106fa0fd5610f8a9e457eb631c90f88e5951c650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5848ee73661d7302be8eff0f3ed6c1875efeac6c81af8baa353e1611db10b724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196020440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d139c55a53f2be6ef0e7b236f14809c25b729ffdbf82a42aa3eb32b9da1724da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:07:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:07 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:07:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:07 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:07:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:07:22 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:07:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:07:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:07:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:07:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d25fa090e5a723ad048576c600a747a1cfe745579ec63d396530f5434f877bc`  
		Last Modified: Fri, 08 May 2026 00:07:44 GMT  
		Size: 145.9 MB (145905487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85adb3e41fd1d4da63c0ab6f86cdf196892fb7cd290975d5d73a353fdb46f29c`  
		Last Modified: Fri, 08 May 2026 00:07:41 GMT  
		Size: 15.3 MB (15338870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b622c02a11f7e2744a462b87ccc4b38f2ee6c234d7ed4a1eb8b5affee18db7f`  
		Last Modified: Fri, 08 May 2026 00:07:40 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a8593178922b8854ed90eac880fe9d1331813d0b4b9391f902110113073726`  
		Last Modified: Fri, 08 May 2026 00:07:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58c162084cf02a83b5ce882a42afc2d8f8df68fea66f1b32c99493b7a3eb6141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652777865a191679e3c3c9af62f02879049439a5f0bfed84b15ac4c6601a7084`

```dockerfile
```

-	Layers:
	-	`sha256:f9f3fd8e32c4c8a8769eabd5abad3c9231b2ad34ac077e51e23a3316df4081a4`  
		Last Modified: Fri, 08 May 2026 00:07:40 GMT  
		Size: 3.0 MB (3028209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ebc9efad0c97be0ca5464496734d4b7936b6c467e053bf8508a7fe629ba3d6`  
		Last Modified: Fri, 08 May 2026 00:07:40 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b00ef8c0515eb9a2115da8b1df4e86baeedf4160f55c7e4be50089fbe6d6cf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193312186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6740af9220c82a919928a3268f6327a7d4268dd69c04719ebae50711ac76ac2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:09:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:09:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:09:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:09:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:09:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:09:20 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:09:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:09:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:09:33 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:09:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:09:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:09:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:09:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f83b5ec1f6091696f43cd2b637ebaecedb4134c5a3fe59a85a66eec0ef4c2`  
		Last Modified: Fri, 08 May 2026 00:09:51 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbdb2ade25c6acdff6e908b45895131f87a0b443342199dd1e438cfda195143`  
		Last Modified: Fri, 08 May 2026 00:09:51 GMT  
		Size: 15.3 MB (15327194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192a4ede87ad2ece3d20b113fe878d0cbeec076613fd65455744daf4160de9dc`  
		Last Modified: Fri, 08 May 2026 00:09:51 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c7838f46ba433419626bb19bab003f23723c8219b08b487041e8c53bb2404c`  
		Last Modified: Fri, 08 May 2026 00:09:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7efa95ef3c902d37e8dc94cd3d4e53b946a3705b293fb9522c39ea6442098227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa68850891c7d84338ab44d116adb22457a648b83ecdd0932d113ffcd80e560`

```dockerfile
```

-	Layers:
	-	`sha256:3664268531f2b554c931bf62a4d52f9655d264638cea6b431003932f9def7217`  
		Last Modified: Fri, 08 May 2026 00:09:50 GMT  
		Size: 3.0 MB (3027818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:069b925a97accef7c0fde8c1bbac5c99330b560102bf0fb641b989c285de33f0`  
		Last Modified: Fri, 08 May 2026 00:09:50 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json
