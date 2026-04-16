## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:612e2d19c78df935a89ab251cd945d53a27a2d10f33354fed90b6fbcddd25971
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:283dc91f5e3f369b590af149f67757b4af2c1a955301d6a7b69c917f7b006099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108865389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f91bee8835609aaa08e129c9b620b8b2eb216c5332328ecf91d7a25a12e6739`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:01:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:06 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:01:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:01:06 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:01:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:01:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:01:23 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:01:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:01:24 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b39c97740c91198b20f39caaeb1dae1242992552b706e1239290da40f94959c`  
		Last Modified: Wed, 15 Apr 2026 22:01:38 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8621b6dda2252a4996b02cb363fabaa6ca971fee9450107c355a391ccb788d4a`  
		Last Modified: Wed, 15 Apr 2026 22:01:37 GMT  
		Size: 19.4 MB (19401942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feea2e44cfe3b1f8a1c279a3927eaa072edd645bca1489b8a6559768ae0b7584`  
		Last Modified: Wed, 15 Apr 2026 22:01:36 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5349b7c832825edb5bd036b0c1bc9cf252b1d1f67b9a10d5873aa3687c0169c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c51a021449326759bee3da47d866d0574140482c7efa87d8401526e23a6b24`

```dockerfile
```

-	Layers:
	-	`sha256:6c43c9954c7dce8caec39b239c8274213c87004dfbe986e54f6118a1dada5e9b`  
		Last Modified: Wed, 15 Apr 2026 22:01:36 GMT  
		Size: 2.5 MB (2485777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d997459421e1515dd9f157ca1fe344ada6ef98f9a8dd97ecc7252cc6c431141b`  
		Last Modified: Wed, 15 Apr 2026 22:01:36 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:257e39d3ff958d95d48187380fcb7f9e58cf6f921c9343a03dc77992a4fdab7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108642800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea96db1abf05dee8e24b7ee938be2b387b813d1049889daaf8a95968e0a9f56`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:12:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:44 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:12:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:12:44 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:13:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:13:02 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:13:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:13:03 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520abc514447d54af96ff77b36fbaf03a824f7961ddc24f4be7d6022ef44f354`  
		Last Modified: Wed, 15 Apr 2026 22:13:21 GMT  
		Size: 54.3 MB (54251615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32493e3cbfee603afa20d1cd315ac6cdc053f3e76bb53202eab0be97d5fb78a2`  
		Last Modified: Wed, 15 Apr 2026 22:13:20 GMT  
		Size: 19.7 MB (19734888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b16d6c81153a7f2b94d31fef6798735e4251bc0cd94fb349ef05417247ec0a`  
		Last Modified: Wed, 15 Apr 2026 22:13:18 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b6239569db36930a56cf81ae638622d6d0429e0c7ce3fad9f13c239721befb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ab7a0b6800a41a14322ff3fa77dd8a82ea8cb61218b9547597617a876d27d4`

```dockerfile
```

-	Layers:
	-	`sha256:2a21b0ba1706bb19d03078a18ba308780e485b830e21370c86b491360a6406c9`  
		Last Modified: Wed, 15 Apr 2026 22:13:17 GMT  
		Size: 2.5 MB (2486095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b87017b76c0a886890297a0da4471577f994c11ed700e1ecad7f691e9b520e2`  
		Last Modified: Wed, 15 Apr 2026 22:13:17 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:764a960684dc583bb80400643ef788382dd3070d61203b7bcda3d302f402096c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107246699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46eb909d9283c68b858d7202ebb0886eaaa7250b8bdbf426f91e44833756416`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:22:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:22:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:22:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:22:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:22:59 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:23:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:23:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:23:40 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:23:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:23:45 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de41bf7fd798d7a67da7d6002cac62ec5cd96ebd90175ee55ba10334fc7bac0b`  
		Last Modified: Tue, 07 Apr 2026 14:24:19 GMT  
		Size: 52.7 MB (52650418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446ad49921abfb0e507438e98c17c441fcecbe98f336399b3105baa200514499`  
		Last Modified: Tue, 07 Apr 2026 14:24:18 GMT  
		Size: 16.5 MB (16485462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0cf2e1d3c0596739a602bb256c719dea775e2764c8af5402ac1a483b87d81b`  
		Last Modified: Tue, 07 Apr 2026 14:24:18 GMT  
		Size: 4.5 MB (4517771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a52cd1a7b29b96364fc5718eafefac76feefdfd99fff870ee6659e42a875d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3ad5cef1d5bd9140e9cb20fb095e81497805b0875a09ebbb1a0a2975a5023c`

```dockerfile
```

-	Layers:
	-	`sha256:3361582fda299d5b7d60d92d0edd1b8a8ef2fadb769e35ce10158229f9463d12`  
		Last Modified: Tue, 07 Apr 2026 14:24:17 GMT  
		Size: 2.5 MB (2487352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92388fe441d6e5edcc63d94efe019e197d55904499f62f58c85ad7179239ea40`  
		Last Modified: Tue, 07 Apr 2026 14:24:17 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
