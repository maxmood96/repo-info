## `clojure:temurin-25-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:0154cbff071f8b571124daeb06a0ac81f1ddef5da74328538bbd5e14ded32fcb
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

### `clojure:temurin-25-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cced695a837c20dbe1e348d011fde1ec3d0f015fdfdf119f9fed5eefb7b0cd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142770402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e76f44525f4c651512a203ad3a21de7316e35171d15df1bff02046a18513408`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:06:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:06 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:06:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:06:06 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:06:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:06:22 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:06:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:06:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f6dba04eee038f02864c661b4a98791c3a408eb09c299dae4622ad54d0ae0`  
		Last Modified: Wed, 15 Apr 2026 22:06:43 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998e280b99b7fe558786a47ae3f6b53968e883d4ecfbfc7f8bb9c0ba39cecfe0`  
		Last Modified: Wed, 15 Apr 2026 22:06:41 GMT  
		Size: 17.8 MB (17759554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2916d19decc9a17fe1271a114b3e07401129d80d63b491909bd12b5785e5e0c5`  
		Last Modified: Wed, 15 Apr 2026 22:06:40 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7e5e435d3c083955495f05e55910d25d8192ec0f735a82718d0327695289be`  
		Last Modified: Wed, 15 Apr 2026 22:06:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0aab0e39db3122f8b4099aa9cac63d424e4e67e8ffb2e069b9f886c45326ec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4464e1c14f8cb5746469cdb9f1bf49e804431bfae1c8fc8ec580afa48bb39c5e`

```dockerfile
```

-	Layers:
	-	`sha256:e1f94a0c5886be4de7d004968797075401357a6a0bd421b22885eb2c09d257ce`  
		Last Modified: Wed, 15 Apr 2026 22:06:40 GMT  
		Size: 2.7 MB (2698110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699bc4e36172af37b9ab0dd0ea40b387636703b90466b2d61238fabf91ca941a`  
		Last Modified: Wed, 15 Apr 2026 22:06:39 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:532641fcbe4d4ac2beb203bd2d73b5648cf7b75543ef4a4149aef97d41ef6566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141515687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0083a05db458c21258e0257427870363d6b064744d6b5d87265d41d8be8641fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:17:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:17:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:17:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:17:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:17:38 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:17:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:17:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:17:51 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:17:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:17:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:17:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:17:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8fd8f67623a70843f8e287173fea45394ae5466b307cc51e1cddaa86cf63ec`  
		Last Modified: Wed, 15 Apr 2026 22:18:12 GMT  
		Size: 91.3 MB (91288279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d122daabcf243ea4cfc83fff199de69563a7a216fadbd94cbedced7a45a21d33`  
		Last Modified: Wed, 15 Apr 2026 22:18:10 GMT  
		Size: 17.6 MB (17593067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baebf321373d0f624371d5126b766b77f4f4bc391a9b8942630138d5c09755a`  
		Last Modified: Wed, 15 Apr 2026 22:18:10 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9372655c4c516adada04aff9034797fa22b4043b60c91c20682b3b6d9d4b140`  
		Last Modified: Wed, 15 Apr 2026 22:18:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc97cff5156e8a9d5010ab2dada54ea30487c0c5f9fd1802fd49b1efd9b3719a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abbd99bbc487c6972cb48f9917097ce82c4c3460463d2f452b35852eab551d1`

```dockerfile
```

-	Layers:
	-	`sha256:c2db008764e3e1a5f970343f134fc07c61a64fd14e375a5fc1c549aef61d5bc5`  
		Last Modified: Wed, 15 Apr 2026 22:18:10 GMT  
		Size: 2.7 MB (2697746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfba0c8ba4ba05805dc38be86d908ddcb93bfc87d2a71d414be0fc8f627b0b9`  
		Last Modified: Wed, 15 Apr 2026 22:18:09 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:66e373c53ce7721aea6362ef05691d1e094c88d011588c56ac45c564701bae51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146190787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07317d314a8d964b115f92f0d5fffbfa2516b86a77dacf2fd363ad6e39e740dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 19:13:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 19:13:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 19:13:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 19:13:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 19:13:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 19:13:50 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 19:14:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 19:14:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 19:14:27 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 19:14:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 19:14:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 19:14:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 19:14:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186825ad1954e238f9d41fa43dbe8881cdc35374805d5861befa0e42e394c10e`  
		Last Modified: Tue, 07 Apr 2026 19:15:05 GMT  
		Size: 91.6 MB (91632990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c136c5e4d1b39849f44776d5c465f6e4f9bc09426c43d7cb81f4d42618b2d`  
		Last Modified: Tue, 07 Apr 2026 19:15:03 GMT  
		Size: 18.0 MB (17961133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e59a45118f3cd04c33c341632c7480a07080f8521e1fe191324e9a4c9dd5fa`  
		Last Modified: Tue, 07 Apr 2026 19:15:02 GMT  
		Size: 4.5 MB (4517771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefeaadb79b63b4c959c7885773e62927a2c55a294280f73a36d4fd7957f0bff`  
		Last Modified: Tue, 07 Apr 2026 19:15:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16654e263ef1455af78e8bfce0771b9a0b07670415e43aa9584866b47c7b011b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa6d28e37593df2201e91cb8d007c3388913105e98d4ab19f7bbd8f854914e8`

```dockerfile
```

-	Layers:
	-	`sha256:ce8f6f7922eb0013f486ca6517b1320a85fd663c12a3c041978d08dc903e895a`  
		Last Modified: Thu, 16 Apr 2026 03:09:01 GMT  
		Size: 2.7 MB (2683267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f3d329d4fb0478225e1e4f0f36e27dcfe60cce19215ce3f8dd290a7a33dc5f6`  
		Last Modified: Thu, 16 Apr 2026 03:09:00 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3bc62e23efbf3387e980adcf4a8c48a15330b26c662818029b2a04199098b1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137065558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28a6b2d9c6c036504fbafe3997e11a41c67c0410b57ab09d9ac4055e2bd4619`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:43:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:43:49 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:43:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:43:49 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:43:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:43:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:43:59 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:44:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:44:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:44:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:44:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a78ac609f8f046c6a31d61cf5e496d160fb1bf38a5cda92b8f538e5fc85bfd`  
		Last Modified: Thu, 16 Apr 2026 00:44:26 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a67819005e77ddd06986ae67c0ccd3091ca5e711048eb60e7b10d002925525`  
		Last Modified: Thu, 16 Apr 2026 00:44:25 GMT  
		Size: 17.4 MB (17421953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d75d761d5d852217df00f1190408da4febaf56d2e33678fb9150c5cc593558`  
		Last Modified: Thu, 16 Apr 2026 00:44:25 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2f3b16c66be45988135bb546e0f1f7911e7c2017c76e0973aa960b02ca8c42`  
		Last Modified: Thu, 16 Apr 2026 00:44:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58ea2760e8c52bda5d2c9f9d6cc5b8b2324a5b6887e51859519405e09f56dc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c183c23635bd82f4702b6b63eb79eff1dd5c0de1e03e4c3c948eb131a44b23d9`

```dockerfile
```

-	Layers:
	-	`sha256:072fb13acfce5d2bbc9775f3f54b9151f84824b45b5126dda238c139b84fbcaa`  
		Last Modified: Thu, 16 Apr 2026 00:44:25 GMT  
		Size: 2.7 MB (2674486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc1d11b3e38ce8432382793dd5cda307aa10530183db899ab48fca2d9fcc6f70`  
		Last Modified: Thu, 16 Apr 2026 00:44:24 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
