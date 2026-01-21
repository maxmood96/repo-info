## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:9b339c3c7b9dc0837b4857a97c73c27ded88fc71ba44c5e87e1a62d81efd2f2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3569a9399603f0d529a0076dbc5ff72885f38406a8ca98491582b90536fb9d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230209569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff61c519747447085a9cac9d12b45daac36be89fcbc0f3560dad2c693620b6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:58:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:58:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:58:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:58:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:58:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:58:58 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:59:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:59:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:59:24 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:59:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:59:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f911dd5e792ce3c14fdab9ad0d326a59e05023204bb4d4b466d40e07adca511c`  
		Last Modified: Fri, 16 Jan 2026 01:59:46 GMT  
		Size: 157.8 MB (157826054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710de88e861e2bbf1a062b7462f9dd6bb7e5e59551887e0d92d112f9f40eff77`  
		Last Modified: Fri, 16 Jan 2026 01:59:44 GMT  
		Size: 18.6 MB (18579719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79212c4e69d7ed3618ba61f836a01a9b1da4dbab55c4a276dcd9be10954008e0`  
		Last Modified: Fri, 16 Jan 2026 01:59:54 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ee64d4d20b1edb700860d119f7e30a8e249a3c385a2a42d60caece409462a`  
		Last Modified: Fri, 16 Jan 2026 01:59:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0308f1569aa486093048c0d9c38d18e6b8706669f5b2fd8ebf868c4d143fbe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbaaa94c3d687b284a408637a54bb2babadd82d6edb24fcfac418329b142048`

```dockerfile
```

-	Layers:
	-	`sha256:bc50588cc6d0077d387725cec310fb9ec4daaf5503ffff60a072ba32067e0a97`  
		Last Modified: Fri, 16 Jan 2026 01:59:43 GMT  
		Size: 3.8 MB (3817341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:753f1915a588c348f9cd673c8be720b68064705679a011896fe88a45c4a352f3`  
		Last Modified: Fri, 16 Jan 2026 01:59:43 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51ee159aa68b36cf12714587191b0541736565d06eab927c2bf1c796ba8ea38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228814628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7973e5e3f1b8ffdfe2784b7ad6b0fbf182b9a559c39d419c693ba6bf73eb0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:03:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:03:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:03:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:03:22 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:03:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:03:22 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:03:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:03:39 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:03:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:03:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:03:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:03:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66b8bf69b9d6ebd16515e528990d7ba71116fd5e0f38e41427a814692fb3626`  
		Last Modified: Fri, 16 Jan 2026 02:04:36 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf6dc1a9d72726f9a15adfc5ac04800ae437d58561e83df4a5687d3a3953b2d`  
		Last Modified: Fri, 16 Jan 2026 02:04:01 GMT  
		Size: 18.5 MB (18540739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2ab3b293d517bddb53646063b727d864afdf8e2ff6a046abfe48c8efc5378`  
		Last Modified: Fri, 16 Jan 2026 02:04:00 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871b2abb2e9d48b0ca3aabad4eed26b4590c320fc4c0ac96a0649f82144ddbf9`  
		Last Modified: Fri, 16 Jan 2026 02:04:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:694623517e0496250f5d6e196fc0afb34aadc0f1c56ecf2dc0237f5681f6e6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a4b78a64cade28c23ecebdb975234b4cac5ba8a82fe7ae3956d1823b3d5eb2`

```dockerfile
```

-	Layers:
	-	`sha256:bac883700642554545bb21c6871d733d6cb3aa47b0d422e2da93748bfc6f2a51`  
		Last Modified: Fri, 16 Jan 2026 02:04:00 GMT  
		Size: 3.8 MB (3818218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301b58a34e0548b9d4f8c12a06a5b5f0e9e0485c32dddb3455acfa3073ebf776`  
		Last Modified: Fri, 16 Jan 2026 04:47:13 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1f48c1878fa1350753daf66b16c5ac2f63ebcdca6ae4c05760950c586842b367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234205369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0156be6a093654e5ecd8ed7307f01bbfbc2de7ea3ed1cdbe6794fcfd12cbc2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:32:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:32:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:32:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:32:36 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:32:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:32:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:33:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:33:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:33:30 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:33:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:33:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:33:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:33:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb8419d04d870182d92f9dd23172b44a59edb435e25623743b58a1807e6008`  
		Last Modified: Fri, 16 Jan 2026 03:34:25 GMT  
		Size: 157.9 MB (157942967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dee7bbf1b22cac22a69c8ba0ccfbcf10b976cf32240c0fc68816298c5a35cc`  
		Last Modified: Fri, 16 Jan 2026 03:34:25 GMT  
		Size: 18.6 MB (18637262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2299a39a28bf48571214a8727db93f37115c77d4272436c15de2f185b7e433bd`  
		Last Modified: Fri, 16 Jan 2026 03:34:34 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd708500d913a6d79da823da8dc786b75272de8baefefd7a3f6b6e92c6473da1`  
		Last Modified: Fri, 16 Jan 2026 03:34:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9e2cfa885caf6977b8eb1fad805158b287c0bffea27f857366062fc261bc3158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ec46e36ce3f4e7aa9f05af3775c0cc29e4abc178a94df446d3d99db8963811`

```dockerfile
```

-	Layers:
	-	`sha256:3c2d576987e55b9455584131c55bd90abc70b41e621f726aee1dafb888e933d1`  
		Last Modified: Fri, 16 Jan 2026 03:34:24 GMT  
		Size: 3.8 MB (3818341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c87424310c5a3881863fc4f224c0988b707213d8ceae8a9e619b345164c45e`  
		Last Modified: Fri, 16 Jan 2026 03:34:24 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:5766e014b31c1158dbaf7bcb5a68c55fdcd846938b0540ce6ca88c9a2b23876e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228015386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329602f907071287a28ec0f4e2d9249aaac8501a588ddef71c55950a73aaffb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:55:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:55:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:55:50 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 06:55:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 06:55:50 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:57:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 06:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 06:57:21 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 06:57:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 06:57:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:57:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:57:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a377be731c175125b38de6ef2031ba27b78ddc0d786d1f6e325bc386ce396481`  
		Last Modified: Thu, 01 Jan 2026 07:02:46 GMT  
		Size: 157.2 MB (157194284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951bf8a4e5129e4b3c92931f641a5621fbc7bf4a373957a00cabb9314d088ebd`  
		Last Modified: Thu, 01 Jan 2026 07:02:34 GMT  
		Size: 18.5 MB (18531729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930cf04678b8428afa8882cac6c96e43a3d84bb3d709dbc4f1ff5693e406a16`  
		Last Modified: Thu, 01 Jan 2026 07:02:33 GMT  
		Size: 4.5 MB (4517791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd8ea7ed2f11bc52f15a917aa1eb8e74dac5be7391682fababefa1caa05674d`  
		Last Modified: Thu, 01 Jan 2026 07:02:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:87b09c00605218b8bf78d2bd3499d773157d7b0105c8065b486aac47e5a70fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3825353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f0b7a06da9bef2df81f20d53fb4f75dc3feeee76741b024d90752236d72c5b`

```dockerfile
```

-	Layers:
	-	`sha256:cd090a7f0d4822528bf3d2a7d9c2ee0f6bd221bc69d96eef3eb98f38d8dd39b3`  
		Last Modified: Thu, 01 Jan 2026 07:36:32 GMT  
		Size: 3.8 MB (3806957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bce7bef8bca1fcea65f8d84f9f79765ef60b5800ecdf732c18a3b8a869d58b3`  
		Last Modified: Thu, 01 Jan 2026 07:01:51 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e3017c7a487d8217690f3ece90553d065ed27a737e95fcf41b86687dbb3cf5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219557501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fe12921c5fad7386200d74df51f984e005772d4e94a396905a922f23826dff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:18:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:18:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:18:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:18:53 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:18:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:18:53 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:19:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:19:06 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:19:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:19:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:19:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:19:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe546673f26304e6e3a7565a4a244298cac2a8e593d48a999166ccef6a08f73`  
		Last Modified: Thu, 15 Jan 2026 23:19:35 GMT  
		Size: 147.1 MB (147069857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cc6f52f8cc6668c127e2c039af1dfd1209d77f9097c4ed417c604959431442`  
		Last Modified: Thu, 15 Jan 2026 23:19:44 GMT  
		Size: 18.6 MB (18620754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4126600cc166330f14e98bf2dd754cbfa8941c9842536c633a1167ae353c8e8`  
		Last Modified: Thu, 15 Jan 2026 23:19:42 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f041d433dd2e00d37215da8dab5bf09f73b10379224543e3d6a28b5c1513fdf7`  
		Last Modified: Thu, 15 Jan 2026 23:19:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:837f20b989fcec39a12b37622b5c16bb58ae2cc6af6c48f03aa86fd36c3f973e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114b35b380b8ff12c207aedb8f43b63f718174502effb44ca61c97f0077678bb`

```dockerfile
```

-	Layers:
	-	`sha256:4a4e798daac8f52c2b20e0945348b4b1a4a51f59e525f69b64b4428eda6e3209`  
		Last Modified: Thu, 15 Jan 2026 23:19:33 GMT  
		Size: 3.8 MB (3813768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c3420d8d83a3f7e0f5452a8273f1099a38a8943c8275b7cf887002499ee1bf8`  
		Last Modified: Fri, 16 Jan 2026 01:42:14 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json
