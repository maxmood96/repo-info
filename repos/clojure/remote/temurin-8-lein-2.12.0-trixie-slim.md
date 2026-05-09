## `clojure:temurin-8-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:f48f1ab24351f282803400ddee1ec9b517967e6a3b5c0fb3e33e9fc88ccfa0a7
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
$ docker pull clojure@sha256:5f10e5425f9a446013860e55b9526d5de4c84c41d3df68f8538416c82a3e3799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105916065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491801137793ecc5bdaafd713869de90de0c2de6929e560f88ba8e056bef8306`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:14:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:14:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:14:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:14:13 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:14:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:14:13 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:14:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:14:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:14:29 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:14:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:14:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a063b69919e37abbccd636e7d0d3ea8cbb4278157c6f9fb2c5425bdc0e7122ec`  
		Last Modified: Fri, 08 May 2026 20:14:44 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d1adb667d16e8280102db038e1d35a8d873f1179e36f2a1a8e4728bdff33cc`  
		Last Modified: Fri, 08 May 2026 20:14:43 GMT  
		Size: 16.4 MB (16448003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321b052a9b65a0ab9d6c332fb291bbd4c20ea4d352782dae99475e1032ff182`  
		Last Modified: Fri, 08 May 2026 20:14:43 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dec2f532757df15cf2edcfebba918ab05876cecce5caf3f10ffd4f5d09304ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69c40cd996ad307f8164971eeba0fd534f351d615fed39a3bd8e23201da4856`

```dockerfile
```

-	Layers:
	-	`sha256:fa64118ce8af16f45c8ca057ea34705601a974fd5a933606907a5e8d89022568`  
		Last Modified: Fri, 08 May 2026 20:14:42 GMT  
		Size: 2.5 MB (2485777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5761b6fdd5e06084868a1db3a04339531f89f46ca73787195cb5efef5f3c3d1`  
		Last Modified: Fri, 08 May 2026 20:14:42 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e8b209b2ffd2de5d8316f280971be4e6909a91dde3de556e2a574b057f623091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105327026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbef278b9a5518cf6e03c4bc1b2479bc08d09a35ba499384c2f13f203921c265`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:18:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:47 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:18:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:18:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:02 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4d4f12b06a4cf04d9d344aab6913173e33af02ad4e1a163c96e0a7a28d8298`  
		Last Modified: Fri, 08 May 2026 20:19:17 GMT  
		Size: 54.3 MB (54251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c80cb38f248db97a1ba9bf5a4471b361e4f332015659897fd2b82f358ee3038`  
		Last Modified: Fri, 08 May 2026 20:19:17 GMT  
		Size: 16.4 MB (16414009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d09cc7b26b2e761802b5d534c7ea03434e416168343a03340399789bf97f34`  
		Last Modified: Fri, 08 May 2026 20:19:16 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72d6eea92e859493a8b22db3ba5e5cb94edd9ecfc3d1491ad61e080da6c3c0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7637c021cee509c01fcc256dab64ff66c08c304ec432134e2f7ef985779dcd28`

```dockerfile
```

-	Layers:
	-	`sha256:2381b91d79f533cccd83e8cd6b7ab71d1fc46c0e003a6f8e80733c7c88d940cb`  
		Last Modified: Fri, 08 May 2026 20:19:15 GMT  
		Size: 2.5 MB (2486095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e0421a9a90ed8000879d1efd2fdb172d272fa0d7449c94eec1b8403b0b77e9a`  
		Last Modified: Fri, 08 May 2026 20:19:15 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:db475156a2931264e8461dc4007b94ef5a2e23c23d1395b4cdba32eb0750d704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107251506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f6df543256ff0f4978c38c5745002a6e098f7f5b1e2a31a46ea440427c682b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:16:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:16:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:16:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:16:14 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 08:16:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 08:16:17 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:16:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 08:16:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 08:16:48 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 08:16:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 08:16:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909dacfd29690d1229d823bbdff4948ce65ffd405125b5cb14537992f61a0959`  
		Last Modified: Wed, 22 Apr 2026 08:17:19 GMT  
		Size: 52.7 MB (52650391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b6dc2559b84bd57b4d994b98f918ce68316730c847d7bbf9ab317d036fbd`  
		Last Modified: Wed, 22 Apr 2026 08:17:17 GMT  
		Size: 16.5 MB (16485321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad176ddca538bd2a919235fa9497da30723aef65261f1c2888c0423a4e31a2`  
		Last Modified: Wed, 22 Apr 2026 08:17:17 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:892793d0b49f5cb5607f3d360d5b71ceed3da45923cce4e32ba4512c456d4ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a322b6666f20fc6c3a1317caecdb2ddf245086fe8874704ed092afd328b48511`

```dockerfile
```

-	Layers:
	-	`sha256:d241b56c373105f6fcad67b725ac3210af21304b881202d102bb9ac61bac0cb1`  
		Last Modified: Wed, 22 Apr 2026 08:17:17 GMT  
		Size: 2.5 MB (2487352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb8804a159483fca7da2f3ddd7b6a197a6710fc5e4fd9ddeb316da0c49272bf`  
		Last Modified: Wed, 22 Apr 2026 08:17:16 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
