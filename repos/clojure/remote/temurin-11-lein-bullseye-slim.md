## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:8214e0e41bcfacb5be3ab89edfb691745402ea097ce5bc8ad17120ba57eadd84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b51312fe40285dc56d382a94602d1466dabc3ac6738c6685024f0627230c3a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195061526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2816afdb1b98391fe148dc66b3ec32b4c5ce4166521e5388ba0759d2625335bf`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:24:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:24:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:24:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:24:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:24:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:24:36 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:24:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:24:50 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:24:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:24:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f17022b9ead5c10b4f6402516879a4a51d4d5d60301e8e7c19b27c5076046f`  
		Last Modified: Tue, 13 Jan 2026 03:25:33 GMT  
		Size: 145.0 MB (144966609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db4b6bf2315bbd60e4cc7d364df11b22d65e2ffb34c719731292295e401450d`  
		Last Modified: Tue, 13 Jan 2026 03:25:09 GMT  
		Size: 15.3 MB (15318659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515472cdf4a1716b674c1781f458420e95df55fde2480f6c142306a70a6680e`  
		Last Modified: Tue, 13 Jan 2026 03:25:19 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:931a99be8e415d388ff144c97701554e3a5d5a502a922f1491b0281394a60549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dde214c13a81290974acb6bc476c91f7998030e6b2e315628e56ac5b12e070`

```dockerfile
```

-	Layers:
	-	`sha256:dfd2c5bc7cbc4e65427dafe92ee075287373fc403dc4ebe43ba8cdbe147a5a44`  
		Last Modified: Tue, 13 Jan 2026 07:37:34 GMT  
		Size: 3.0 MB (3038049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329238c2a467d77e8674a9cd01302a3cb7e0b3817ea910b607cbe13089978839`  
		Last Modified: Tue, 13 Jan 2026 07:37:35 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20dd1d388155c52d4f3230ca271c75b0ea6c64c6cf2594dda8e9bca4b7031659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190303701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5677902fd034b1e8e266fde9895a8c729f7793e0f0215f339501b97f813baf6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:32:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:32:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:32:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:32:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 02:32:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:29:34 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:29:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:29:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:29:47 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:29:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:29:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3b0a0079547cca6f4cad851516b5185a1da2ce9d4c96eabc458a76af99307e`  
		Last Modified: Tue, 13 Jan 2026 02:33:31 GMT  
		Size: 141.7 MB (141731575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c643140d864c300d9fea101b2932723935e283427cf7fb4c8700c391927c8478`  
		Last Modified: Tue, 13 Jan 2026 03:30:06 GMT  
		Size: 15.3 MB (15305821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000178f32f8a99402c7aa98d429e6ca65d37557a7a09b88f1b77261b1cc3fbab`  
		Last Modified: Tue, 13 Jan 2026 03:30:05 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5504d71d2719273d459c59b625f34222531cf489697d52360a1191a2d6fada1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa57602d7e0f521767327cc1b278a4ac47d57ec3e4e3da3a83390eff7032149f`

```dockerfile
```

-	Layers:
	-	`sha256:aa2deb125331cf0bea886fa1276bdd7a98ea61212e5deb2836a3c02599cc13a0`  
		Last Modified: Tue, 13 Jan 2026 07:37:42 GMT  
		Size: 3.0 MB (3038276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ac99d81ee5673d96b3f0bccb556edd654baf34a6955996dc6ae2f9dcf173a1e`  
		Last Modified: Tue, 13 Jan 2026 07:37:43 GMT  
		Size: 16.5 KB (16533 bytes)  
		MIME: application/vnd.in-toto+json
