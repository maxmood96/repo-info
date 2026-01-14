## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:0ddc5129807259c1e0f8f4dceca146e3942d4b8ddd72609b7fea4f592da38526
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:272600affc46d5ea5d6f797e611d73432cd7037c631a271c90decd9eb2b32d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207921364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4484f70d20f7b888749e60059503e6a7072a9b5102884aa8720890a1070f9106`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:27:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:27:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:27:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:27:23 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 02:27:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:34:32 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:34:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:34:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:34:46 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:34:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:34:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:34:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:34:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f2da96b7de746ba174dab2a39ed6389e7e90314f090ff0cd1b0e2022fd62b0`  
		Last Modified: Tue, 13 Jan 2026 02:28:37 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e915e27d6d1d151b604fa5756e4dea99872a1051c2ae0a755f24f457c5baa41f`  
		Last Modified: Tue, 13 Jan 2026 03:35:06 GMT  
		Size: 15.3 MB (15318682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e94fab2381bb6214a829a1259d93092d32b3a3a33d068dae4ad8b3543c25f8`  
		Last Modified: Tue, 13 Jan 2026 03:35:05 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36249f2c30c315718eb8668744f92322a3ec4a5961a70fe81a14a7ab916404b`  
		Last Modified: Tue, 13 Jan 2026 03:35:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a80ba35af434fd25c67d44806bd6e229e5251823db96d681ecb8adf2a286c838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3038614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0b8fca25a8bc332d86d2ce5b15c45598f98f3586c11e0f199d1493237cf12`

```dockerfile
```

-	Layers:
	-	`sha256:7855ab3020cac067d07f5384b0fd0b88da648ff260ba0e48026a8ad31b9b82db`  
		Last Modified: Tue, 13 Jan 2026 07:43:25 GMT  
		Size: 3.0 MB (3021012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5edbaa0911cab280a494451ced8a4c17b9c71108ea6deb537129c174b22191a0`  
		Last Modified: Tue, 13 Jan 2026 07:43:26 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9936d1bb7ee606714df7aec099f9b8176fd10289e8a16a0e5df6fab0cfd31c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204680079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee7d56d6873901ccd0a03d5f611a33622d6e2a0021a33bdb62b85755330dd3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:38:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:38:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:38:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:38:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:38:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:38:27 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:38:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:38:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:38:40 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:38:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:38:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:38:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:38:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3340fb9bc41dba6d9c64998e81ad5f91b4b3a00ee9ea37aa467576a8059970fa`  
		Last Modified: Wed, 14 Jan 2026 13:21:19 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d242cde330fd3cf755a1fc90ffb7117470b443c77273d7f3e86a86aceb006a`  
		Last Modified: Tue, 13 Jan 2026 03:39:11 GMT  
		Size: 15.3 MB (15305804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664df7c354d14145b35aeb4e1e0aee68934376dfa4f12f7dcdd7f9a22559d8a8`  
		Last Modified: Tue, 13 Jan 2026 03:39:10 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5292d485aba4104a402428adb18fb283f52660cbadc554146c55fc13697161f`  
		Last Modified: Tue, 13 Jan 2026 03:39:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d153bbdf578a380a0e26721380325411c5f65734cb0a27d4d444a02e83ebf086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc814e6f38206052a29f4b309e52b3de37ad2bb3b3f028bb25fb7a94a9d57b96`

```dockerfile
```

-	Layers:
	-	`sha256:4120444a99ba5e864c268d70f27e8d07d9845b1ff7eed668e012dd65d6cd1260`  
		Last Modified: Tue, 13 Jan 2026 07:43:31 GMT  
		Size: 3.0 MB (3020621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885a86605fd737eeac0c6cfc15abed354203038f0d7ba54c1e78f53e10aee902`  
		Last Modified: Tue, 13 Jan 2026 07:43:31 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
