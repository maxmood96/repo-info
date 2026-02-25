## `clojure:temurin-11-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:5745611e0ea3641359409d36bbf0ada33641012d312055c2eec0ffeba66a5100
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

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:70c66704d26d41caee7003db77eb23a64dde410aa2a82209bcb7374a6f9ed50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218616204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41251221ac7de135844b53d2a91a052222f8bd59889cadbeae72c43b9cf8656f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:53:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:53:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:53:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:53:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:53:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:53:27 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:53:41 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:53:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:53:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2816e251eb7a9fa52c5f838df8596e81418e3ee039aacb6a5b392c7f079b3a0`  
		Last Modified: Tue, 24 Feb 2026 19:54:02 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de0699ed30d6789cf4f7f0abef493a7d0c04392e72bc5e3fd9626371d522c95`  
		Last Modified: Tue, 24 Feb 2026 19:53:59 GMT  
		Size: 19.8 MB (19802889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bc18ecc0d0f8fb782d8febf7024f7779110e5f1a7d38fbb44f9cab8faaa3a3`  
		Last Modified: Tue, 24 Feb 2026 19:53:58 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:67c075d32116f0046e90a7b3b9d46f1b5b56277b6692f1ebac19e861210c13d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d19d17ebe272bbe5d831e411ac0096164d899418afa5c397a5659fb641f5b6`

```dockerfile
```

-	Layers:
	-	`sha256:3cffd7439d221402fd9cdcc310b0881fed987c961b97ef70392ecb14afd2c480`  
		Last Modified: Tue, 24 Feb 2026 19:53:58 GMT  
		Size: 4.3 MB (4301872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08f359a7b6948ecc26d556c70514682a33be1864c43f5f430c864bd50f4dea3e`  
		Last Modified: Tue, 24 Feb 2026 19:53:58 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:584d9ce7be09c9c7c9bc65dde4a2623d54a9941b1e905634460a78bde118beba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215025250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a213702834f322b2bb6fc352b23d358698bbc61533f2d5e06855a466c1ba0152`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:04:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:02 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:04:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:04:02 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:04:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:04:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:04:16 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:04:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:04:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acced749a8332ae6df09d834d11f9f48214be80678f89d13bd8e47d267e823f`  
		Last Modified: Tue, 24 Feb 2026 20:04:37 GMT  
		Size: 142.5 MB (142501465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513042287c8772c5c815ca4afa605520881bbba30b21282a59a61b6bdf18760`  
		Last Modified: Tue, 24 Feb 2026 20:04:35 GMT  
		Size: 19.6 MB (19632832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82f326bc9dcc61a44db814c7d893f5153e3dc80b531e620b4c15cff9de8d092`  
		Last Modified: Tue, 24 Feb 2026 20:04:34 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3d10fb124ddb81bd2e98fc13887189be6152a85a7d63e58f9a4cfef631d5996a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cd4e6f636807583ad513e4d787ec139b0e689480d792c8ffb78bf85ea7c249`

```dockerfile
```

-	Layers:
	-	`sha256:eca1b34f42625fbc25774fd6d6d9cde39bbef305f9559a09e66772dbcc9e3b60`  
		Last Modified: Tue, 24 Feb 2026 20:04:34 GMT  
		Size: 4.3 MB (4302105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690886eadd616f923b7a594ef85ddea825e48432e869e88c60e337500fbef82e`  
		Last Modified: Tue, 24 Feb 2026 20:04:34 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:da99ce5719bc487f9bf7aed2e3eb031b3964f2eaf4381f7a3c1f69186d2b6d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209876355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b42a4fbaf679335ed6e134d1afbe02d31ab280d48f9b9ddca7e540a28e99407`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:49:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:49:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:49:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:49:03 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:49:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:49:04 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:49:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:49:45 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:49:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:49:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777e2a7cd2f8867774abc2b31adaed051d2272be9ea6f534e24e079ece86647f`  
		Last Modified: Wed, 25 Feb 2026 01:50:37 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678a7ea392a6a80de11f50a04334a13e00882f4e878c6bfab357eedd3a0aedcc`  
		Last Modified: Wed, 25 Feb 2026 01:50:34 GMT  
		Size: 20.0 MB (20023955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30338f92bb1c937cd39a04c2c7589b038f58cc1884a3eb7c6f5289419abf439b`  
		Last Modified: Wed, 25 Feb 2026 01:50:34 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a5d2b0be382b0351e6ec79077b761ff440f793bd53e50b2ee26ab835bff6eaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c113a4bdfdfdc898930ef0c6305c673e05d4548a5aee230ea5a073ac00a929a1`

```dockerfile
```

-	Layers:
	-	`sha256:32a640452655442dddc2b204474cd896feca69b3e993071092d7c74d1d9be743`  
		Last Modified: Wed, 25 Feb 2026 01:50:34 GMT  
		Size: 4.3 MB (4303118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75c554b2a4e5a7d11a84fbc7d1f8ceecdda218ef4e083b2e77b1678b29abd7d`  
		Last Modified: Wed, 25 Feb 2026 01:50:33 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:2f4c41842391ed6ffb809f144a44eafc0a56b7f6dfe1c4db5efce1b4b23f40a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197691228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698b9d4560bbae4ba27ecd0c2c66254c428b4d5da49a4da4afa963d836462139`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:11:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:11:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:11:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:11:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:11:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:11:22 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:12:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:12:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:12:08 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:12:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:12:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88825d23886aad7630f698fabec26ff327fb5cc56e608c0be4067ab5b8f57c4`  
		Last Modified: Tue, 24 Feb 2026 23:12:49 GMT  
		Size: 126.6 MB (126562035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958b8493406627fb4668909c881b87e1f2d139204c3c5c6f192dea6784abaad0`  
		Last Modified: Tue, 24 Feb 2026 23:12:48 GMT  
		Size: 19.5 MB (19463326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58fbb68647c8afd9f83132e7283c46c1f28198a878859d9bea2af464a58c248`  
		Last Modified: Tue, 24 Feb 2026 23:12:47 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0958650c24eb9af239a5ae50317feafd075f964c33c93e5ebd0ba3d3495994c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4310072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2694230e933f02246006fe93de2130b737a661a01ad429a9cca964bfecf8a093`

```dockerfile
```

-	Layers:
	-	`sha256:edab52e369c7110c0e0474a4756786a54f0f06e66d02ce9c016712948147d690`  
		Last Modified: Tue, 24 Feb 2026 23:12:47 GMT  
		Size: 4.3 MB (4293690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4232b76638401d33a5fa944a45ca237715667e132208bbb3f2c2339584e76a5`  
		Last Modified: Tue, 24 Feb 2026 23:12:46 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json
