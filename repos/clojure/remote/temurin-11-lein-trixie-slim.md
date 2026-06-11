## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:245302236e341bdd18dd8aeef6d44097ddd8de077332ba7bcf2547af58f3526f
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

### `clojure:temurin-11-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8641d5358f59dc261b671d23fb73f313bc1fc9ff588db9084df0ba64dac73c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196637638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa8512e4cf5a368994cd8840c08f2645a1bafe8a3226d169b4d873b981dbb3e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:17:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:17:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:17:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:17:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:17:40 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:18:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:18:00 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:18:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:18:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d35630145fe290b78ef60808a3f5ab6f6421c2d648852aa86afcd680ce7bc89`  
		Last Modified: Thu, 11 Jun 2026 01:18:21 GMT  
		Size: 145.9 MB (145886255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8e53de87452e8780729e09ac0a6712e216e5069cb93ab09e8144bc55daddba`  
		Last Modified: Thu, 11 Jun 2026 01:18:17 GMT  
		Size: 16.4 MB (16448222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc11293f71aaea106072edd570a1401bcc898929358b4729ba681ffb119811b`  
		Last Modified: Thu, 11 Jun 2026 01:18:17 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a5b6196c57492c34e9877a3e40a1cc3b7ee89e92a3e77eee65a62dafb5d859f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0c47afd050cf18a3e7e594aed6ccc7971723c70f12cc994d95fed273ba7ad3`

```dockerfile
```

-	Layers:
	-	`sha256:fff36c3a2d18a6f185aa8f68cd06e31308b16c3a1d85da3fd8cc573384f8ddfe`  
		Last Modified: Thu, 11 Jun 2026 01:18:16 GMT  
		Size: 2.4 MB (2384973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae74e6615aa3b83a7be045a23d39cc747d8b4646f08cc7dbfe2595652c8bd832`  
		Last Modified: Thu, 11 Jun 2026 01:18:16 GMT  
		Size: 16.5 KB (16547 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:35389f583b68ecf5a9cb739ba5a4556bb39a91544a19cb16627319f729ab02cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193662737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46631a490bd4b8412191fc7901ef62a9aec1ed7c238ee7e015452d3777d37c1c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:21:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:34 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:34 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:21:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:21:57 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:21:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:21:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c68b697ff8720314718c638a48533dc54f24eaac06249c1cd75cb512a3aef6`  
		Last Modified: Thu, 11 Jun 2026 01:22:21 GMT  
		Size: 142.6 MB (142582229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a54d8f7d69839aab9216392094690c5373259c25ae8fae809c78ad5109d13b8`  
		Last Modified: Thu, 11 Jun 2026 01:22:17 GMT  
		Size: 16.4 MB (16414182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760a05e71cd6837fae4790915cd96a211bcf58c52e9df0b6de5052aac8f775ff`  
		Last Modified: Thu, 11 Jun 2026 01:22:17 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:132aece3529a6f40c7fbd82a7b9b940c264f744d6750562d15ab9f9f9a16b28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95a73a2e1ffbd8c6ace6e93b68140a9df89966321b2998ddd5efd829d6c3b01`

```dockerfile
```

-	Layers:
	-	`sha256:96322e671b5039c427d37e25b323c3e797accfef963a04bc96ddacdccbad3192`  
		Last Modified: Thu, 11 Jun 2026 01:22:16 GMT  
		Size: 2.4 MB (2385201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f04e5886a2a94b8761aed171d56fa874945919b2409f7c13b6415cc3270d1f`  
		Last Modified: Thu, 11 Jun 2026 01:22:16 GMT  
		Size: 16.7 KB (16669 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0d62ff3f2ffb75e52b3388b26c79a780724ad48cfd7b2c3be99481965da68f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187720317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfa2d169b7794451ea9f1f4d9d25abda69b5422474c581d7686058a90a7dbf4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:24:10 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:24:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:24:11 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:24:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:24:47 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:24:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:24:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9054a5ac768834a10d14169acc177113311408987ed6c5625592f8ed37e45e6d`  
		Last Modified: Thu, 11 Jun 2026 09:25:29 GMT  
		Size: 133.1 MB (133110170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2feb70c51e00669d6213a211efba499f2e342b073be487f24d1d2c1126e8ee`  
		Last Modified: Thu, 11 Jun 2026 09:25:26 GMT  
		Size: 16.5 MB (16486017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e58a2b5d70a38a7396fc3f2c90ea37a0769efa09c13ab956e1da7a37552a56`  
		Last Modified: Thu, 11 Jun 2026 09:25:25 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:76f5e9c072f2ad70fe292b467201959db1a7565ac786e197684b1e4f61eb7257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20665a9c1d71e7779e741adf491b72edcf1e16a8a5a5170be68b318620b3ee82`

```dockerfile
```

-	Layers:
	-	`sha256:e15309830572cc287c07e6f137942219efcf8fad58eda7bb1d5a5b2d18d6ab9d`  
		Last Modified: Thu, 11 Jun 2026 09:25:25 GMT  
		Size: 2.4 MB (2385338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37439ca957950f0362b50d72376a0a90d2a7762c65ef012b0dd1271bd9124d48`  
		Last Modified: Thu, 11 Jun 2026 09:25:25 GMT  
		Size: 16.6 KB (16591 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:12635e74ef4b0beb80990472602f95fa3468a408023adf892fb3bf85d0beb747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177505071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b7194230a028291491ddf97f2e50822c6ffaead3f9a5270e2ab940ef5e076b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:07:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:07:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:07:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:07:28 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:07:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:07:28 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:07:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:07:45 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:07:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:07:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5802eb9f5d41feedb6c258a1f1f2df21baf827b10fc2b57c1794f8c975245ec2`  
		Last Modified: Thu, 11 Jun 2026 03:08:13 GMT  
		Size: 126.7 MB (126651744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f9760ef5036d1a48970c429f2df3a4593d80bc873d171ef53bbff98c0f74af`  
		Last Modified: Thu, 11 Jun 2026 03:08:10 GMT  
		Size: 16.5 MB (16484195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bf6af21d501f3c5917ff20b989e785b03e6afbbfa81d6a7fc6dcd990644418`  
		Last Modified: Thu, 11 Jun 2026 03:08:09 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb648eb2453b768e3ce5210dda1df871edf886afc262c24152b872c407667bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e10291fa52f1976a1511be70c9869c581084e1c9c4c8f39e6df3d3680a16098`

```dockerfile
```

-	Layers:
	-	`sha256:6901449f644f691cc8283038c0887e77157aa29de8053db6923542b729f356f5`  
		Last Modified: Thu, 11 Jun 2026 03:08:10 GMT  
		Size: 2.4 MB (2381404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9ee7cbac0750d345bb70eb254cc7568b269c9d5d886d030709f6a2e783aaf94`  
		Last Modified: Thu, 11 Jun 2026 03:08:10 GMT  
		Size: 16.5 KB (16548 bytes)  
		MIME: application/vnd.in-toto+json
