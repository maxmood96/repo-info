## `clojure:temurin-25-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:455dc70cf2bea61a61f1e05ffa27ead38d055e9c58bf8d92cd5c215615e62f41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ef9d403234e34515cee793be1eecf3bf780254b7dd07391de2746f8ea6cc588e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142540491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c30f7a8ac030e23f9c4e2c1fdfc9a0f62b500f8d7873f398c8be105728069d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3bd1eca61d8407b6efff932a902c87b0691253ad5731f9d80eb1f78f817000`  
		Last Modified: Tue, 21 Oct 2025 02:23:54 GMT  
		Size: 92.0 MB (92036036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c75b9385b2d54b0b9ebbfca3a17f511c9342168b9a412f979c1e6898d4ff7e`  
		Last Modified: Tue, 21 Oct 2025 02:23:48 GMT  
		Size: 17.8 MB (17757999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0776f4fc7a27cfc0f19158383199d24d0780ada288ce7f535aa8aa07bd3281cf`  
		Last Modified: Tue, 21 Oct 2025 02:23:46 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1019444a6b9a5bcdddb779d6eab4f7dbea3413dca3a30ef04b0eb0ef3dee5d0c`  
		Last Modified: Tue, 21 Oct 2025 02:23:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:57fc1b54bb76fb5647043719a9d538ab87e7010a64c13ec371cda4ab27d37603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ecec986cc02914eb47d8615077cb28587a16ef230cc1724aa82724aed50df6`

```dockerfile
```

-	Layers:
	-	`sha256:cd5d19860d2c0f64b8950ff02873ff8ab99f31e9e747f527e7c208fa2557156d`  
		Last Modified: Tue, 21 Oct 2025 09:34:45 GMT  
		Size: 2.7 MB (2680098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef72b1928c31c5b5451e9f21ba3399834b1fe4ce31600a4d77646046f746a9fd`  
		Last Modified: Tue, 21 Oct 2025 09:34:46 GMT  
		Size: 19.1 KB (19101 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:826e4845789686ccdb69432734a5b53089e20c5a839647316c7ab01a79f10b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141256732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99b4cf7c3c3fb5603dbba69c4b382c9a4ddba623a289ebd2769d13923a25034`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95aa3d36a16a382a0cec92f472702c0b8592bd91137effbad3cebdd51fe6193e`  
		Last Modified: Tue, 21 Oct 2025 02:29:30 GMT  
		Size: 91.0 MB (91045250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0731cddc34ba4cee426a266aeb7e2295b3f9c79ef3f1d76848ca785d6dea0e4f`  
		Last Modified: Tue, 21 Oct 2025 02:29:27 GMT  
		Size: 17.6 MB (17591123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4600f41e4d0faef5d3adeb39beffa3c9fb11b5d08b0588bec1e18ad01d8ce`  
		Last Modified: Tue, 21 Oct 2025 02:29:26 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c17637e9e45e0e2dfaf9a0b0f7f2e3d2cc9058556eb256870e4b8ac30981e31`  
		Last Modified: Tue, 21 Oct 2025 02:29:26 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e07938f8efe45560f33eb07f956f25d1b70f1972d58602c4ae6660e1a7a9c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6eeda03f2ff290c2b84f8182b0bfd708236077824b6d5c2911a9b40b8895a8`

```dockerfile
```

-	Layers:
	-	`sha256:6e4bac982f586c0f96ed6358983bfa6b4b231c82617050a26645f24af47caecd`  
		Last Modified: Tue, 21 Oct 2025 09:34:50 GMT  
		Size: 2.7 MB (2679734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc7c855bb3ffcfa2e16e2d6799ce1d3c3aee894d86986512a19b316a68d09b66`  
		Last Modified: Tue, 21 Oct 2025 09:34:51 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2b30200dfa34da68ea9d0e869ea7000b1548fd3b34f1033573cf227b41336e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146148294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e5724d827d3e81a13b7a54ce322fcf2f1cdcb0cb12ddfdf533477b0abacd2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c466f4d3a516fa0f89bd30e4e6127b11b82109306a6772e28f2a761af3fead96`  
		Last Modified: Fri, 10 Oct 2025 05:52:07 GMT  
		Size: 91.6 MB (91601754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5f1fbcf5a0cb2d05e3aefb192277c482434cc3a0a48cd329d7fe5f633b4310`  
		Last Modified: Fri, 10 Oct 2025 05:52:09 GMT  
		Size: 18.0 MB (17959688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c02932616769767432b0e25faa20bd50f19e1058c4c430bc580cb084385611`  
		Last Modified: Fri, 10 Oct 2025 05:52:03 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99bdaf65d64bb3c00d5d5071e94a90dedc65fdd50ce0475206e6c7fd0e48fdb`  
		Last Modified: Fri, 10 Oct 2025 05:52:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59a48b5a6ba2cd97c06acb82da3b55d92c8010e0e2621fd20cdd3d119dcab43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89158821f5734cbe3da06f4c4aadf3c9c914b58ed2818e3828c9e0fe86abb2c3`

```dockerfile
```

-	Layers:
	-	`sha256:9f72daeccfecd905be94b764a06f5e0e8cbc9c269a9c1f9eef51303714720cad`  
		Last Modified: Fri, 10 Oct 2025 06:35:05 GMT  
		Size: 2.7 MB (2683241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da9b5eef64f31679e7227ec00ead6de58467ffe5f3e7f00797dde3dea962385`  
		Last Modified: Fri, 10 Oct 2025 06:35:06 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2eca67d515e0fa4de60d148f37905d1bee3cadcaf852b6d99d6ee2068e024d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137028657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91927d9aaf5eec9fbcad00b60a0f4685c7f830f8e7ec40b86d019cd262652589`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf250e646c0021ded29154a3e88a34116e2514d2045d76747578c3a6b030dfb3`  
		Last Modified: Thu, 09 Oct 2025 23:44:10 GMT  
		Size: 88.2 MB (88206397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1019860c111bcb9a0f5c86508fc9b528cd804cbe00ea1e8aea6f7e052450d736`  
		Last Modified: Thu, 09 Oct 2025 23:44:06 GMT  
		Size: 17.4 MB (17419761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19db780e67348758942e017df59aa7f9b31184a8b8dd1056ddda78a25fe2f586`  
		Last Modified: Fri, 10 Oct 2025 01:09:37 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d376f447ef391c18fa394021410b0686de6f294c8b672e8d8103de2aab45be32`  
		Last Modified: Thu, 09 Oct 2025 23:44:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bae007fc067251d49e258c8708afee98522064115d64ec11744802b880e8860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e1b5fa0c43c722041906829ccfa666756986949e9e23213096ce690dffe32b`

```dockerfile
```

-	Layers:
	-	`sha256:33c961ac3a75950a5b94056d7a3a125725db0982ea80137ff936573306eacc78`  
		Last Modified: Fri, 10 Oct 2025 00:34:49 GMT  
		Size: 2.7 MB (2674460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc6685e8529c9c04be6938465f0d6e57978d912f7195c4026ff4089e5f4c702`  
		Last Modified: Fri, 10 Oct 2025 00:34:52 GMT  
		Size: 19.1 KB (19101 bytes)  
		MIME: application/vnd.in-toto+json
