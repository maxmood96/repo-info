## `clojure:temurin-21-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:816f4b1f5b6e58293a682e992ccbb1da12bc4aa672843de3813f89efbd13c628
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

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f2c36d7cf7283c884ca7623221a46822a4b2bfd886331ee857fbfb97c02e8973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f208dde12fb33be54e1887546748658f5ae65ee336d7dbb53ed5bf3fb4c610`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:43 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:43 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:59 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e72bb403d9782bb56d35711d545701e6745ab31da83fa0baaf4bac1c44b438`  
		Last Modified: Wed, 22 Apr 2026 02:20:20 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ca8ad8a750b4b700f28f3b9014cda09d0ccd22dac7e5b097944897ce223a45`  
		Last Modified: Wed, 22 Apr 2026 02:20:17 GMT  
		Size: 16.4 MB (16448023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3501434d406c3b5b5754836cc2719281b941f356ed2280e2d959141a0da0fe30`  
		Last Modified: Wed, 22 Apr 2026 02:20:16 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a37e7d98c2401dd4e0e3b748628cc1ec1bfadd930394b72aefd9389f60ba8b`  
		Last Modified: Wed, 22 Apr 2026 02:20:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:846551bf079506d922bc7165a14b97eb30e4e8c685d508564e776d8a86091902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd516b178d6159f2f6ca665cd093fabad10ec7fa77e4f03d9e473d01a5e731e`

```dockerfile
```

-	Layers:
	-	`sha256:4ddab77d943730f05d97ddf6fb3a268e810f28202ae86634522fbbc856494d55`  
		Last Modified: Wed, 22 Apr 2026 02:20:16 GMT  
		Size: 2.4 MB (2366640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333b1de6201f23219e82d85e35167a18e370fb60178bb2ad63f4e77dd082afec`  
		Last Modified: Wed, 22 Apr 2026 02:20:16 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2cf28ff14663f9134c4a7337be8f190069f00b0da27714e1b2d7e00a7dcca4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207208808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e256b631aaa6ed88da818be0167c29b9a723e498f13797843da30e2311fb85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:34 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:22:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:22:34 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:22:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:22:50 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:22:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:22:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52eda08e4497389d8d73c2832713c0f34794fe77e8c51321cab4dc749d9d9e46`  
		Last Modified: Wed, 22 Apr 2026 02:23:13 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb48e6954768401a5f4feedf0d3d8b2116dbb5045e2e157562100b9c71b77ad7`  
		Last Modified: Wed, 22 Apr 2026 02:23:09 GMT  
		Size: 16.4 MB (16414002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7b3045261d1253de652b5baf46fac1db0f8a848b0b73668b15c78fb6b5589`  
		Last Modified: Wed, 22 Apr 2026 02:23:09 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d7c8e9e24fc4474f2d2a51f6bf56603104e91ccad5947462fa484051d49d8c`  
		Last Modified: Wed, 22 Apr 2026 02:23:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce8c1033ea229c6fdd6270f029866592777aaf0058002faf1464b754ca24712e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b021cb5865a002f1d9d9effce7be34323e08e78dfbeae83197a8b969e1f5e4`

```dockerfile
```

-	Layers:
	-	`sha256:4311fde76b01f84b68212ddf2b813874b38496b50c78f989a110d12e57fc9c4c`  
		Last Modified: Wed, 22 Apr 2026 02:23:08 GMT  
		Size: 2.4 MB (2366258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b3a577c4c6337393c136c6524a6880d37759e3af2160bae531cdc8768e1bce0`  
		Last Modified: Wed, 22 Apr 2026 02:23:08 GMT  
		Size: 18.5 KB (18507 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e2ee4942e246f91077d34954357f62f5fc4c79b1e772b9a17071757de83dd74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215775096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f36e9fbf7aa98c040a1aaca694e615fc4db2d7ec382a13670ee8ed1c5c2e54c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:01:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:01:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 03:01:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 03:01:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:02:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 03:02:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 03:02:30 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 03:02:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 03:02:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:02:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:02:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6266996408f18fa5b8afefdb178402a7bc9517ccfdc1fdefe8e27ee9d954dade`  
		Last Modified: Thu, 16 Apr 2026 03:03:20 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc75deb1b6fc5ab1bd9a6b7ac41d868d75a27a0958959f2d25194d84d9a19a1`  
		Last Modified: Thu, 16 Apr 2026 03:03:17 GMT  
		Size: 19.7 MB (19686438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6b5c52cfdb2424a9bbee2b9f6e0ec77a8b53452b12d54424618db7909e1148`  
		Last Modified: Thu, 16 Apr 2026 03:03:16 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09176ed17b2d3ad7e085a5c81d25f156c88befc66d1e73c2eb221f9d4fea8776`  
		Last Modified: Thu, 16 Apr 2026 03:03:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eebab01115af9f43f9554246b3ccadb6aeb1f0109079b8a3fabe6a35c1427b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f3b13f956e2c62bfebac4da71485b2015c08aa375043e07a3dded0907c2749`

```dockerfile
```

-	Layers:
	-	`sha256:712d0b202db80a93d661cbd1da7fb46194daa8c60ce90b9a644903482bc18e23`  
		Last Modified: Thu, 16 Apr 2026 03:03:16 GMT  
		Size: 2.4 MB (2367620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba78a75ebd29d8c57292c6d547afaf0eaadf35e5013b88d6e31a7a9e5b8fb2c`  
		Last Modified: Thu, 16 Apr 2026 03:03:15 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6d565e58aefdda2f77fca6886ab77e40bb206a50ddae6323886435f6dc0c3ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (209028998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32253284d6d19668b70233a709a2aab7a3ab02383217acf4cc045e745de5e162`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:00:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:00:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:00:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:00:57 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 22:00:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 18 Apr 2026 04:49:20 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 04:50:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 18 Apr 2026 04:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 18 Apr 2026 04:50:55 GMT
ENV LEIN_ROOT=1
# Sat, 18 Apr 2026 04:51:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 18 Apr 2026 04:51:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 04:51:12 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 04:51:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5427f8f7357cd1c2f90f35451416b331ea3c682f95a93bd8689b142ddc99805`  
		Last Modified: Sat, 11 Apr 2026 22:07:07 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1d6844c8ff76c85995458ace5cf83f6f635b6892c7867c105283223fc443e7`  
		Last Modified: Sat, 18 Apr 2026 04:53:21 GMT  
		Size: 19.0 MB (19018102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce2e260c6bc09e57439fcc776409ce4622184cbac98cecf32d7c925ca46972f`  
		Last Modified: Sat, 18 Apr 2026 04:53:19 GMT  
		Size: 4.5 MB (4517794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f6bdd89f4afd817db4b45666da9d9372114cd88e0299a93e740b86d613b49c`  
		Last Modified: Sat, 18 Apr 2026 04:53:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dac7ec99a331df71d588a369b369fff167a8a910e5d19c8510577f296f155273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee6d3aab6b2db68d3af9c0b2bf7055b8911a6c7ea49e736cab5601128d05cb6`

```dockerfile
```

-	Layers:
	-	`sha256:e5ec5dc490893371a13e2339eb7d9640060ec0480fcf3c7e5830774652c48b52`  
		Last Modified: Sat, 18 Apr 2026 04:53:18 GMT  
		Size: 2.4 MB (2358688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952d6d8421f425ab84a812b14b4c0d6dc14861468f1f5971c0d7aaf510e0fc9e`  
		Last Modified: Sat, 18 Apr 2026 04:53:17 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ea909dd681f07bb802d8fde14f8fc73e2a75192ac76d59ba89c985273ad1abc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197947580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e15426b516320fbd87bf02ba4d1a62131c58d66ce1e0e29c81c85ed2c91da9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:03:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:03:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:03:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:03:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:03:16 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:03:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:03:29 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:03:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:03:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:03:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:03:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc13e0424f9cc62cbd79bd2740a0337d43290a60f702b3f4c6b3ca57b188dac`  
		Last Modified: Wed, 22 Apr 2026 04:03:57 GMT  
		Size: 147.1 MB (147105211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefd825e80f3756285616747e84d082d20b2c0d341c740af95d744f15dc9376a`  
		Last Modified: Wed, 22 Apr 2026 04:03:55 GMT  
		Size: 16.5 MB (16483893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8dd0e94805bb7cd8aaa97da4305bb82c0b6ab97da6f2c82136f5fae0bbe8d`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3fbf5333dcd457d84d2455b8e21a0a9b5712a390dcdcc0c831f70f6c100f67`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dde72b1e3be0d16fcc6e2737a574177813afc76575d5f38c4f26ec071e527210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36e578312b7176a4c3a92b10e845c8c8b20ba6487dbb7d1d9dbb3a3552ecdcd`

```dockerfile
```

-	Layers:
	-	`sha256:34cd4e2651618ab7d0c60c7888fc663c3a82aef8e4afed7711d51557565e19b9`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 2.4 MB (2363067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6e721edd3d60047d1cdaec0b6a0a28fbd2702d323207baec64002952253ee4`  
		Last Modified: Wed, 22 Apr 2026 04:03:54 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
