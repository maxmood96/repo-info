## `clojure:temurin-11-lein-2.10.0-bookworm-slim`

```console
$ docker pull clojure@sha256:51cdff0e319da0e129c47f2eecef08ad2853172bde8395b146717e78e50c5b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.10.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:158653af892b701e9a092b045ac40b526153edf01d733630c02ff7a715e5e04f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193817205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc619f59a7e4cc84eaee7bb9e0ff6501c1782ebc2f9702a1f96cc87e1e04a802`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 09:54:40 GMT
COPY dir:d20aeb749bf0b3fe533952f7903b6aa08724fe8bf03e369130d4e2a6ff71bd3f in /opt/java/openjdk 
# Sat, 02 Dec 2023 09:54:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 09:57:40 GMT
ENV LEIN_VERSION=2.10.0
# Sat, 02 Dec 2023 09:57:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 09:57:40 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 09:57:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Sat, 02 Dec 2023 09:57:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 09:57:55 GMT
ENV LEIN_ROOT=1
# Sat, 02 Dec 2023 09:57:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Sat, 02 Dec 2023 09:57:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4050ac330d97fd84a1d6329cccff3c6d67aeace4dadb496e6d7467c8568e3c1`  
		Last Modified: Sat, 02 Dec 2023 10:14:01 GMT  
		Size: 145.3 MB (145266397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0fa602000635e3c4f7cf129a589aa4cfe2241f3c42876bd5151ac2f58f236a`  
		Last Modified: Sat, 02 Dec 2023 10:15:23 GMT  
		Size: 15.0 MB (15001667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b424b3ffb1d3477b380cfde06121f7e1d733bed44d118e13957e0e5ef8679419`  
		Last Modified: Sat, 02 Dec 2023 10:15:23 GMT  
		Size: 4.4 MB (4399233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.10.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:049dc33d8709a0519d1195b90261aefd13d51e4608347a82cb63b4b4a3c8efaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190404125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f208676d913067686837a3e1c1698248b21ec324971a3edf4ce6f88123065b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:45:02 GMT
COPY dir:201fdbb3aef6b177b9038d3dd5bbe865568281c78c7bc0c153b57943d571a0b6 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:45:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:49:24 GMT
ENV LEIN_VERSION=2.10.0
# Sat, 02 Dec 2023 08:49:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:49:24 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:49:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Sat, 02 Dec 2023 08:49:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:49:38 GMT
ENV LEIN_ROOT=1
# Sat, 02 Dec 2023 08:49:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Sat, 02 Dec 2023 08:49:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499cde67ef4ddbbb49efba4d14e85c99ac1dcc40592a7b8c7cac48b4f81d299b`  
		Last Modified: Sat, 02 Dec 2023 09:03:55 GMT  
		Size: 142.0 MB (142001789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced489f65956ea2649d515cf27f204250cf2612e837f425099f22a22f6c2e971`  
		Last Modified: Sat, 02 Dec 2023 09:05:16 GMT  
		Size: 14.8 MB (14823778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76273bc8024932a666f9997c57b00669ffe78fbc0ccbe70929f2c528ffadb2e3`  
		Last Modified: Sat, 02 Dec 2023 09:05:16 GMT  
		Size: 4.4 MB (4399281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
