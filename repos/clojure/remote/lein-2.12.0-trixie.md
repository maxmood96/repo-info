## `clojure:lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:7680cf5b5f32c37b1788ff37ea7ef26316b3cfdfb0bf78233273d31ac347382c
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

### `clojure:lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:92c73edc684cc6f51f23108895260e09ebb5e826a7661a4152667d4819817da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164647557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227fdd455009cf35d3a1aeee2e9f0d3b083e4d835ce71f9a827b38436abe7b74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:45:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:26 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:43 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5010b1096a8b014ec04eff7fe594570c7c7633d4fa267ad179ebe68ac416f63`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53c229a62547c33d574a77cb5ef33688a3f3b671773fe2930cbc00cfff3ff18`  
		Last Modified: Tue, 17 Feb 2026 21:46:02 GMT  
		Size: 18.6 MB (18580162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8eab5fea27138e9dc754b916f9661b75d247292e2994eaa075c32fbb125aba`  
		Last Modified: Tue, 17 Feb 2026 21:46:01 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024cc52fc006362eceaae49651eb3628e9b843a40cab623159e4cf3a364c635d`  
		Last Modified: Tue, 17 Feb 2026 21:46:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2ef261d803a7ffb5408fda23053b6ae3a9bd32464d1398ed74b82e08a62694f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e290d3f65fdf05c50e4a6950ec814241207d49edfc13ab6eaee885f65a488f`

```dockerfile
```

-	Layers:
	-	`sha256:4c5b57ffee7c455ffb239069a4f3d320b66536639f64815b9bb0b68837fc5883`  
		Last Modified: Tue, 17 Feb 2026 21:46:01 GMT  
		Size: 3.8 MB (3783523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d41267b514ce37beaf4ee79354130e31b2e85cf807f03894be1dbb405b7523b`  
		Last Modified: Tue, 17 Feb 2026 21:46:01 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:02d02848a02d5af772fb0b7bb53ca2e29446306ee9fa7823511b1bf497d3f30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163999911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a090f83406af5985673213002f13b60bd0f7717c676c4767ac1bc86099b918`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:45:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:45:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:23 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:39 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2940c31349527342bc95adf4b59af9c941b56ea72d4399a2646c50a160eec5c`  
		Last Modified: Tue, 17 Feb 2026 21:45:59 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f216dab3b32e1016f926fbfe054ad18f98891c8b6ae2be16da16bcb794127f1`  
		Last Modified: Tue, 17 Feb 2026 21:45:57 GMT  
		Size: 18.5 MB (18541480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed65dc0225c6b512eeafbd711af4f151d0295268882e015d7557a5f21eecbcd2`  
		Last Modified: Tue, 17 Feb 2026 21:45:57 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2ec1540489d771afcf397ae608d1a3f618c69ff7da9c92fda552fbaa1d8f35`  
		Last Modified: Tue, 17 Feb 2026 21:45:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a46fd126931e19623f517ac4ae73c0b052d30ab7108cacaddceb5083c788a828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ff9fa549022dac35b6d51021ccade176f062c104ad2d5ebaed873c4387da88`

```dockerfile
```

-	Layers:
	-	`sha256:515a7136a5d17c0921b88b626042a47a9e78593499ecc5f3da02eaefe1ffa52f`  
		Last Modified: Tue, 17 Feb 2026 21:45:57 GMT  
		Size: 3.8 MB (3784421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5b5d7649cfce03b7afed06e322665bd190426117349b2562de061d87ae08cc1`  
		Last Modified: Tue, 17 Feb 2026 21:45:56 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:67454ff47120ee0b108adf09d409e7a46ac3eb53d03debb4a5cdfb1b32013442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167900700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79acb1409382f4e9e8c2853db63119abfb3e217faaa1286e0c21c5b4db610f2d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:48:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:48:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:48:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:48:08 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:48:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:48:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:48:59 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:49:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:49:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:49:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:49:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230ebb877a1444adbcad5521afaffb1c41773004c4324fe65c2c551a9cc1544`  
		Last Modified: Fri, 06 Feb 2026 00:50:07 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3592aef72592656244b79421c8d2881c7ab4347c4dae6ce8aa981feb882d243b`  
		Last Modified: Fri, 06 Feb 2026 00:50:05 GMT  
		Size: 18.6 MB (18637526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587ba20bb2ee02d46106a001def44a07dbb7cabaa6022d338c73fe3b855b3852`  
		Last Modified: Fri, 06 Feb 2026 00:50:05 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa996e2b368b508e8135f75a167c37d450e8907d36fd8f22e066feb03ed873a`  
		Last Modified: Fri, 06 Feb 2026 00:50:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8f4597096230f9e24ab70aada22493ac548b8bcb75d27ee48192cf965aaabf3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f707393f9d081bee2b320dda6671e47b52211c15747b1ac561578a0c0f622df`

```dockerfile
```

-	Layers:
	-	`sha256:38d1bffe3dcc6f64365a775eaa15cae474b67cad360b59879d3274dc7f59cdeb`  
		Last Modified: Wed, 18 Feb 2026 00:04:21 GMT  
		Size: 3.8 MB (3767847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099a59b2a1d20ad099181ec0bf05a60dd3c2af5f1b868f6f33d424d7f73a69aa`  
		Last Modified: Wed, 18 Feb 2026 00:04:21 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3e87c95032783606d7c77aa50ad0ca2953db94c171bb15643931d454fe2799d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161600199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3128580565d2ef6d07c7e58f2b08167166be19856fc0cfceeb96190c88ff8c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 12:53:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 12:53:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 12:53:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 12:53:52 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 09 Feb 2026 12:53:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 09 Feb 2026 12:53:52 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 12:55:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 09 Feb 2026 12:55:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 09 Feb 2026 12:55:28 GMT
ENV LEIN_ROOT=1
# Mon, 09 Feb 2026 12:55:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 09 Feb 2026 12:55:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 12:55:45 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 12:55:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3877762b7849aab190bdd4be4bec0fdbb7a69de6798289c7ab36fcca52b2c`  
		Last Modified: Mon, 09 Feb 2026 12:59:49 GMT  
		Size: 90.8 MB (90773405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8186bd4c2ba1cb3d722851fcd7dd37d212000ea0ddc26146bd8c8f2d7a2ac86`  
		Last Modified: Mon, 09 Feb 2026 12:59:38 GMT  
		Size: 18.5 MB (18531820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dfc246050a42c83362a509676ae6e68f1d8ffb730ea12947ea6054ea05f07a`  
		Last Modified: Mon, 09 Feb 2026 12:59:35 GMT  
		Size: 4.5 MB (4517780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a685c1cad55d054f216c4a7938c58f9aa2c40c393f6033c86fe347c4758733`  
		Last Modified: Mon, 09 Feb 2026 12:59:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7b3057c4b5950534f52f3766423889bf669eb76c3a03de759f55252c15f4e23b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4ccbb27fd30713cda0e283781a59b5917aaa4514be769c13062245090b58cc`

```dockerfile
```

-	Layers:
	-	`sha256:fb13768ee982649b6e19c71910fb68c93543a52bd29df9b7e17ae032e5ca856f`  
		Last Modified: Mon, 09 Feb 2026 12:59:34 GMT  
		Size: 3.8 MB (3756023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:923605d2f40982806e88acd33b5a352c18ea48b124331f16998eedb80170805c`  
		Last Modified: Mon, 09 Feb 2026 12:59:32 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:9d4ce78a7153217edd140b45640e3965ca250f3973ab64112e860dd0960f850c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160727683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b0c7a83484aeb8baf6e48560f2ef2763a2519bf45234fde40b4f3b637e849f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:17:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:17:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:17:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:17:28 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 22:17:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 22:17:29 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:18:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 22:18:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 22:18:05 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 22:18:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 22:18:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:18:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:18:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca7b05b5ccda20d243b58ab8b79085ed9f5c3430e53a7df4f8405f9393cf55d`  
		Last Modified: Tue, 17 Feb 2026 22:18:41 GMT  
		Size: 88.2 MB (88233849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df998cf0bd029436cafbc901d6b35ee15c64c74ddd4334f0db7afe6e78614d14`  
		Last Modified: Tue, 17 Feb 2026 22:18:40 GMT  
		Size: 18.6 MB (18621271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1ec931e403fce1950e5c926398b71dff1cfa1143022d832a3e4d4db47846f`  
		Last Modified: Tue, 17 Feb 2026 22:18:40 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d852b3ab49881ad751fe77dc587b8315a43c05a2789e00032c45826d3d312cc`  
		Last Modified: Tue, 17 Feb 2026 22:18:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3ff35505138bcf60fb11b3bf626e27ee3b50bd643901c45d78f38b35d36e8da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14831d4f42c421b8d14e53810de68c1dad3bdd463b90b96b0fbea221d9c40915`

```dockerfile
```

-	Layers:
	-	`sha256:0d36486f562cd892e95ee93e28fff6c6656542c1f968e07a1309a2a47df15b2f`  
		Last Modified: Tue, 17 Feb 2026 22:18:40 GMT  
		Size: 3.8 MB (3764512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4d61f969011d096edeb1b8c73221d0bf9af99a5732e8d4d489c40b615913a8`  
		Last Modified: Tue, 17 Feb 2026 22:18:40 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
