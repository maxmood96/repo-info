## `clojure:temurin-26-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:f26b2fc3103ef6561a217982cf16505272f09af36437c25696d3c319f57e60f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3b7ba0180f2c360dab2a6707a9535c2e37048f7243b0a54c2e52be8ce65ee4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169366545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5177d50c08ee8bde5be5fdf197bb914b8158f339dacc70a9cd605af438e30c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:36 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:36 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:49 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719594b4b334fdcf1d74851ebe01c3f01cc57ac3daec2df2d7527bef9b42b0de`  
		Last Modified: Wed, 22 Apr 2026 02:22:10 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267df5b6f8d39796163f9736dad18e68132a65cf44c2e01a8ce8f3430fdd1d64`  
		Last Modified: Wed, 22 Apr 2026 02:22:08 GMT  
		Size: 16.6 MB (16629515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24425020e5d3ffb45826363450d4bd39b6149ceef82191f7dcf134d106f2507a`  
		Last Modified: Wed, 22 Apr 2026 02:22:07 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91dbbe67c9604e7b473808a866c6acb1ee3b71b058f4e6cbe50efce61c7ce3`  
		Last Modified: Wed, 22 Apr 2026 02:22:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8eeacf6fed980b3cd4982a0072b4d78ce68c369b516238a40c0c1ddcbf2f3f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99937d194dd9b0751b364157e30d91a1c163f5072256ef4818001453ad52bc4b`

```dockerfile
```

-	Layers:
	-	`sha256:609081720065cbd55aa726a3d70c390f0ecaaab4a563d9901c470eb986b53c2e`  
		Last Modified: Wed, 22 Apr 2026 02:22:07 GMT  
		Size: 4.5 MB (4451366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc87b14c9d23251958705e160579684b68492d228d84d2ed7b8a93c960dba6e1`  
		Last Modified: Wed, 22 Apr 2026 02:22:07 GMT  
		Size: 18.4 KB (18361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:95e38b09543fff88c110425f53302d3286e565c3511a74c41faf1adf52cb88e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166782860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb37d1d4a9f49910650f6c3f925c1a52ac2140f500b54d35fcd80fc9770aed5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:24:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:36 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:24:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:24:36 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:24:50 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:24:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:24:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95eea0e258b40c7b7acaa0cee73e4e53ec137479bdfa4a71d4c09cfabc247a4e`  
		Last Modified: Wed, 22 Apr 2026 02:25:12 GMT  
		Size: 93.4 MB (93395167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f227e3b639842418a3b847eb4ee69dff04f28de43c3acf875b81d3283979da`  
		Last Modified: Wed, 22 Apr 2026 02:25:10 GMT  
		Size: 16.6 MB (16616561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e777339573063352e559885d9b2ccd7c71f0efe602d9a003d751420ce45c469`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a677b73046419993dac4d5fce2b3f61ebe0167bbd34167d5a8772e1cbb092f`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a1c9c9a2cafe2dc8204252575a7a7fd56ed67a5b745f37ee063ef5ba28e5fac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75412582811cea8e61dd9356bc0c2d072adc6957646a3ced7e02789c181fca01`

```dockerfile
```

-	Layers:
	-	`sha256:63995a62b1b437af209a033b8407fa32e983306879e3d9daf08cf99cd8d724b3`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 4.5 MB (4450337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07cbb3626e42af19b6df98111fecd655b8185f8c9621789082aee739fe474df`  
		Last Modified: Wed, 22 Apr 2026 02:25:09 GMT  
		Size: 18.5 KB (18482 bytes)  
		MIME: application/vnd.in-toto+json
