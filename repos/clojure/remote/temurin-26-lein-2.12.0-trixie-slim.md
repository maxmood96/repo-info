## `clojure:temurin-26-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:97524fa2fd79e320d75dacde3b93648f091e0091352245bf8dcbd76accea6cdf
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

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a00f79a35b3efe31a2d0b8cea4760971736b273360a520899d0d502d4b565166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.2 MB (148151376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa5ff5c276d8d19e64220a0a09902e960a599bc4c783658d8e7cd0e842030ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:37:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:00 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:37:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:37:00 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:37:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:37:17 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:37:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:37:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7238408d1136ad0dde901634127d41f81ffd06bd7906d6e36ac9e2d7d6c816cf`  
		Last Modified: Thu, 09 Apr 2026 23:37:38 GMT  
		Size: 94.5 MB (94455682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55b643c7c209f2f9e660155cd212a706b3d21222be0a28d16bb55eb75bc175f`  
		Last Modified: Thu, 09 Apr 2026 23:37:36 GMT  
		Size: 19.4 MB (19401915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38d3824284841f0f2120b36b9bda6553559ac90550046e77bdcb750f3800a2f`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311f1d7b25f3a5f033bb10eec540a530c7b9ecee6b1f4504ced7a56b27607b91`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:306e55cea92df6b377a3387be850055682af68ee9592c58f8a55ee38b62edc85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33574faa4fe472762fabbf4a314f854b9fdfcbdf792ef06f252fcf486c6301dd`

```dockerfile
```

-	Layers:
	-	`sha256:44bd1aef07b882d8eb28907d41e745b82239a8a479bf491e2217a01d1415ee8a`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 2.3 MB (2330292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5863b787bd45e7594468b14bc471cee6ee4da2a6883f89398f4d79d6a766771b`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 18.4 KB (18380 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d4c195fe34811ffb38e946e510de189bcbbd5f2923b86fb3a4e0e178220bfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147786747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c69af737178ed122268e02714f500f90e67b30d26d392fc68b7e2b88a3b9bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:37:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:00 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:37:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:37:00 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:37:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:37:16 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:37:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:37:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae43ba1ee948f083a210c0be66728a69773437f80ca2cdbd01f93e6700891f5`  
		Last Modified: Thu, 09 Apr 2026 23:37:37 GMT  
		Size: 93.4 MB (93395169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87c39fdc9f959d8711999619c4d93e06d55ea043089c003e77aa55c755b9e07`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 19.7 MB (19734850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51807da3fa753035b5edef6d0c2864450fbfdd4196b944f4c90661f49ad94e7`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aaba93706e373f645efd73ad3aad69233923b8f8ce9b6dce68e4f4c9d69e1d`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b91ddc0259d90cdbcf4514f551c6f040cb65b1ed8e96c30baf3875866defe25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cdc04f372bc7dcfa3d53448a11375938d655514d11c83ec6c9e44169d83ccc`

```dockerfile
```

-	Layers:
	-	`sha256:25676d8b943d59724f5c1ee59cfe1c204a15dbb70803559f31f09862d327a84c`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 2.3 MB (2329907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f749556e1def8f27ff5f466fe751188e631fe8e84eabce2d535e7eee6940012b`  
		Last Modified: Thu, 09 Apr 2026 23:37:35 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c8ad2f5df50e3df4555299082985e29788e1a6bdbb3b31162f33e8fec9ad7afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151579042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a463f8da126605c62f5b368f0933438737c7aafd7095863d30e1a20b6f4dca3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:53:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:53:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:53:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:53:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 10 Apr 2026 00:53:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 10 Apr 2026 00:53:45 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:54:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 10 Apr 2026 00:54:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 10 Apr 2026 00:54:19 GMT
ENV LEIN_ROOT=1
# Fri, 10 Apr 2026 00:54:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 10 Apr 2026 00:54:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:54:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:54:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad9d78de109af0508c6cea77373f8cb08369c373cf24c72f7da9935301139a`  
		Last Modified: Fri, 10 Apr 2026 00:55:00 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a3210fca8d79f1cc1db27f62cc3cf989202e9c6ea247f650aba49efb4798e1`  
		Last Modified: Fri, 10 Apr 2026 00:54:58 GMT  
		Size: 19.7 MB (19686375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4b0d54f122881561f793d16774b08bcf63cf9a64e2bd9dca615eb5ce11342f`  
		Last Modified: Fri, 10 Apr 2026 00:54:58 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743cad04e5b3d7c7fb3acf83c6b27da564b8be22fdd69a026044d98a9c3a8d9d`  
		Last Modified: Fri, 10 Apr 2026 00:54:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:68cb1eea1a89fe0e5a153c8c1a4341bfca0ebf7bd50fdf59121ffbf83d65f18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f675e1f44db4d41d0b6ea984ab6de8892f659e96d86850bc8bec12b5332beefa`

```dockerfile
```

-	Layers:
	-	`sha256:d73edfd1bd71100e9eed58f3e4e34403a89be0e275731566d9741db870d0045f`  
		Last Modified: Fri, 10 Apr 2026 00:54:57 GMT  
		Size: 2.3 MB (2315208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa7c5d83ff881e5bff9adfcbb7a4c90e9bb6d79f78041993d2e8e696b054c621`  
		Last Modified: Fri, 10 Apr 2026 00:54:57 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9d0c344a1fbe70d1ae3b200e9dba6e57f1b5dff7cdf6f278d45233d9a0ae00b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143991363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2131a10ddbb8e4f1d6d584269d3ffea9c9b9b4dfd5dc7b5c86eb9507ecf28a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:44:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:44:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:44:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:44:22 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:44:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:44:22 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:44:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:44:36 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:44:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:44:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:44:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:44:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d497ec2816b8b56226d37338bd198a7a45726696a0423458803d8542ce4164ec`  
		Last Modified: Thu, 09 Apr 2026 23:45:05 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e87b1c2c1914d37b009de99dac388a1f1cd3d36f4edf4b8dd4f069dd98fcec3`  
		Last Modified: Thu, 09 Apr 2026 23:45:04 GMT  
		Size: 19.1 MB (19090092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c26e7149d51c1f50b55dc11f2c0793b68585ed4b26edf8fb90e74b7f4f00b`  
		Last Modified: Thu, 09 Apr 2026 23:45:04 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b205656e3228959559c2f68a393e59d2cd4d0eae919edc29828aaed6d9b050`  
		Last Modified: Thu, 09 Apr 2026 23:45:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd314646ba8e3d4da71157c4a1fe886b01b8f9e516cefa7938a877ee754911d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6ab4e03c1c3a80161a0388f6f9a518ebd0578b4262e25f872507959945ef5c`

```dockerfile
```

-	Layers:
	-	`sha256:deab0291e2ad5b71bff51d75e133e18a7cabe14b97dc67cbd9380fa5ae508199`  
		Last Modified: Thu, 09 Apr 2026 23:45:04 GMT  
		Size: 2.3 MB (2311905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a0c1a556f34b251f66d1f67ec79691a5c194373fb8c6afb32454ffb952f1235`  
		Last Modified: Thu, 09 Apr 2026 23:45:04 GMT  
		Size: 18.4 KB (18379 bytes)  
		MIME: application/vnd.in-toto+json
