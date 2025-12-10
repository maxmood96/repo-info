## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:72aac3d86af9b72939ba991ae4c1f84cb30a62475c67e47af42557cc8c03a602
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:99b2ee950717d61b9ab0125757b3c494062bfd21d358ea6addcf3d8fd3341de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208567764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1c1419b23a424c35d678539b7eaf4c2749ecfa577da7da14cfb51464cd9d59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:54:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:54:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:54:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:54:54 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:54:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:54:54 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:55:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:55:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:55:10 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:55:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:55:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:12 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d974c063f21030a11891ea31c9c7f21e6c4c68e43c850c0fabd168133b06`  
		Last Modified: Mon, 08 Dec 2025 23:57:43 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e5c4a25648fb9da41f122de66c10bbaba189c4d64db477eb5a93365bd7f8b0`  
		Last Modified: Mon, 08 Dec 2025 23:55:44 GMT  
		Size: 16.4 MB (16447122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628acb87a705206ef8c461971a443ceb9f951535970d4d10042f341d85e178dc`  
		Last Modified: Mon, 08 Dec 2025 23:55:41 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fd5a695a0cb293da116791202ccde8abf5a480a95c9e6c25809e8164b1ba45`  
		Last Modified: Mon, 08 Dec 2025 23:55:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b27b0fe1510cf60d50117cda05bb9c55ffa6b7802436532aa509605edbc9860e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6417078b992e7011d736a45111af3f4785e756478b5698f20745722d9880754c`

```dockerfile
```

-	Layers:
	-	`sha256:5787fbb832cab183c0db92a38de995a1f4f11486e1ca858cf01b2703899e18a6`  
		Last Modified: Tue, 09 Dec 2025 04:43:52 GMT  
		Size: 2.4 MB (2366540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3386ba5456abb2ebd4b8737b8224363fe480928e0f879b3f1b69c71a23df6652`  
		Last Modified: Tue, 09 Dec 2025 04:43:53 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:439b4aa613bb04594c64118027fe64ed90d99a6b9289018f6901c8bf14e46987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207178219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b558dabb69c65c25784a797d13d3855eadc3039bee8a59ec5fa94b92666737`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:02:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:02:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:02:14 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:02:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:02:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:02:30 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:02:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:02:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba6e99349c2ad77e628685ce93274852bbe1ace7d65fb01b069b4146cc8fe6`  
		Last Modified: Tue, 09 Dec 2025 11:21:49 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2525073fc739fa3958006a76d07199baf271ce4b88cd43c10cb1100d22686265`  
		Last Modified: Tue, 09 Dec 2025 00:03:05 GMT  
		Size: 16.4 MB (16413828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e2222cb457fdf7356055d33ad9b53ee8971c5b89974e6224ec767483c13d85`  
		Last Modified: Tue, 09 Dec 2025 00:03:03 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967ff5c95fe12eeebf5cff70fcf3072bfe913e20a404281d763388e9384d6f11`  
		Last Modified: Tue, 09 Dec 2025 00:03:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca747aeee9fc63575489899268bb7ad69f3ae9279cfe7c8915b56eca504f9db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2908dc483d402a87b223815c95644b7c396a2e4305fa2914fdc437b3d6b8086d`

```dockerfile
```

-	Layers:
	-	`sha256:7b4fb642b44de0106e71086c052d43001dae256f6a337f963df01df690793cb3`  
		Last Modified: Tue, 09 Dec 2025 04:44:00 GMT  
		Size: 2.4 MB (2366158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc2596b6426e3a4982f7ee1d64159c785a94cfb50a4bc776da314c0b7485a54`  
		Last Modified: Tue, 09 Dec 2025 04:44:01 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0bb1abab1e395d5a87dd87d676c76a10b68bbf4bd017086438434ad3c809b749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212543348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e61ed4a7d682282b4a00d0a30b8afa278e40653be2f644e2fc97375f1f78410`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:53:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:53:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:53:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:53:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 03:53:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 03:53:31 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 03:54:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 03:54:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 03:54:15 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 03:54:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 03:54:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 03:54:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 03:54:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1738f5a3e98755bfb9425681189b2a44278e8171bee65caa143a42717b2cfb8e`  
		Last Modified: Tue, 09 Dec 2025 03:55:01 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c7dbfdbb76de8651dab7a60bf9d5c12e2c4e64ed7c7e7700ae2f32b2128112`  
		Last Modified: Tue, 09 Dec 2025 03:55:09 GMT  
		Size: 16.5 MB (16485328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12d4f06f05c56e1bb14963e63eefba0dc48b5e90cf52993fb5a79c178dbcfde`  
		Last Modified: Tue, 09 Dec 2025 03:55:08 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53a9b58cfdc6ce93511ec14a97b05ba14eb77a891b7cf682bda1f15337d2775`  
		Last Modified: Tue, 09 Dec 2025 03:55:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:57ae000c165b2ee7b504a6320d80f1d5a6e7ccb0828e30a8de35d8746de7c291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e22b031848b8664224a961fae7fa92d0d40d69cc502fc58cbd00202e164cb0`

```dockerfile
```

-	Layers:
	-	`sha256:09955538c70136e1d9d756f8da2a1318b23d560e441c8c591cdaa53b4604098d`  
		Last Modified: Tue, 09 Dec 2025 04:44:05 GMT  
		Size: 2.4 MB (2367520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5910d93111fd22b097e457eb073cae6b680834234bbc205d98095a510486460`  
		Last Modified: Tue, 09 Dec 2025 04:44:06 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:896f6f2fe624bd55917e6a11f2bb0586df36d5f5d8706d8197ea93b98e6aa147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206383549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2363ec9486cdf23032eadf3e02707145ed720df2b73ba5ebd9a95461d48805d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 18:27:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 18:27:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 18:27:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 18:27:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 20 Nov 2025 18:27:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 20 Nov 2025 18:27:05 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:28:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 20 Nov 2025 18:28:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 20 Nov 2025 18:28:35 GMT
ENV LEIN_ROOT=1
# Thu, 20 Nov 2025 18:28:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 20 Nov 2025 18:28:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:28:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:28:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516f07972228dcbc55c70b87824ef60b8072c90f8a8787a93b8e4054d62735df`  
		Last Modified: Thu, 20 Nov 2025 18:32:59 GMT  
		Size: 157.2 MB (157194320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d8e837cc89855d17c99b22159f005e8903ac23af850d4b1c1c6fe833a47e0`  
		Last Modified: Thu, 20 Nov 2025 18:33:09 GMT  
		Size: 16.4 MB (16397875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44afa0f681b4791914704d576f7287e4f9881f79ee2b4d7a253bf5c29a97117f`  
		Last Modified: Thu, 20 Nov 2025 18:33:08 GMT  
		Size: 4.5 MB (4517798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47719f85e6dbd9f2123c0040575d5dae2b838c7234f9e436722ad1df7fb43f7a`  
		Last Modified: Thu, 20 Nov 2025 18:33:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0f7ae7af418e406de9fe99ef975ddb335fe53ba82ca4f96603b1505559aed2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f250977491e97a239f81f8354f4527bd07d93d5b8512156e9714e363456c6d`

```dockerfile
```

-	Layers:
	-	`sha256:3763c1bac6e2163888af09e5a3b63bc0152f2b67de8870c88ebebb1229d3b1d0`  
		Last Modified: Thu, 20 Nov 2025 19:36:55 GMT  
		Size: 2.4 MB (2358588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f73c4b270794e831adaa870289aab5c2b2892e9241af425fb7799efb327091`  
		Last Modified: Thu, 20 Nov 2025 19:36:56 GMT  
		Size: 18.4 KB (18430 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fe0e92f4e7f89df25a6baf82993202aa7c176ef55cb4c4ebdb1bb9816c2c381e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197905370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4086130ca14d718c74bc8e19b41f37ca76b66bac60fdf5e37cbc9c5462d609`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:31:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:31:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:31:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:31:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:31:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:31:13 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:31:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:31:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:31:26 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:31:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:31:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:31:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:31:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ad8af80bd1fca505a458dadc68d16da2d131f0ace69cc71fe587e4b3a2a78d`  
		Last Modified: Tue, 09 Dec 2025 01:31:58 GMT  
		Size: 147.1 MB (147069847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036861b739fa9e1517d84070eaf22a622265752fb0a99be958c61efa232411f6`  
		Last Modified: Tue, 09 Dec 2025 01:32:06 GMT  
		Size: 16.5 MB (16482998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583e6f614cc344c237cd2dc7faa59329de6bba34c23db3a69efb70508e08ea3b`  
		Last Modified: Tue, 09 Dec 2025 01:32:04 GMT  
		Size: 4.5 MB (4517699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264ea6c94208f4699e90619db2bc4ab5376dfae83e042a86408ddcc690294216`  
		Last Modified: Tue, 09 Dec 2025 01:32:04 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8b1cdac0c4c3be3902c539585367c4c910eb5a07c0d82fa4b82f580662b245b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb57c8a41e94a92dbaf31a24b2e4abd6de4ccf62e91e89922cbdc90e763485f`

```dockerfile
```

-	Layers:
	-	`sha256:bec0c43865e80f67299e388be66c8c925e403526e297312a50b8be88b18c3de2`  
		Last Modified: Tue, 09 Dec 2025 04:44:13 GMT  
		Size: 2.4 MB (2362967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d9c40e7691ae3b41afa783d9290c4e1f2a174dd93fbac213b2bdb08b76eee6`  
		Last Modified: Tue, 09 Dec 2025 04:44:14 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json
