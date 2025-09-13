## `clojure:latest`

```console
$ docker pull clojure@sha256:b1390fb7277919875cfa7ed75ee5fc7337f8ca53eb7b530e9fc73485cf8ae1a9
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:b8a22869f55d02c31f8017b854e0abfd27afa8586e81f36a21a3df1b09c75c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305674182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb98c3a8c400291bd3b37fce6dc000137debab1c29f169b0c674015e8f3f3d98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcf3f76f0e4ea8ac009315f4d1743517e663d63f894f740d7932cadee11aea9`  
		Last Modified: Sat, 13 Sep 2025 00:38:36 GMT  
		Size: 157.8 MB (157804820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d091147820ee662d2f36c68b597a7d4fb85e70521be305397cc786c93e1327`  
		Last Modified: Sat, 13 Sep 2025 00:03:58 GMT  
		Size: 19.8 MB (19799920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aca08b7fe337039108ddcc1ff99511027090b616d35b992cb6878105ec1b91`  
		Last Modified: Sat, 13 Sep 2025 00:03:56 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574f17061e953f00d2cc2820434d71142d72b982e3cc46a57f5ec9e8322d014b`  
		Last Modified: Sat, 13 Sep 2025 00:04:04 GMT  
		Size: 75.1 MB (75070010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058c454d1e54ce3354ee1c94c13ee6eb72936336697eeb2730a46f5756955bbf`  
		Last Modified: Sat, 13 Sep 2025 00:03:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb65630276a72bca60c2843bd3a62efb97fa95ce99d87f33fe0a727f19a5d79`  
		Last Modified: Sat, 13 Sep 2025 00:03:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:b2a3c9061166fe40b04a1328fd3d9489a119edb449fa72358a2229992d603a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732bf1e34d8fee1240641be4bbfe89cd936e8108295c8036812407a88e921359`

```dockerfile
```

-	Layers:
	-	`sha256:4be24f09d9a1b7f419f49a60b67f8a3389e3ae218adaf9d4fba3092df88046b2`  
		Last Modified: Sat, 13 Sep 2025 00:34:29 GMT  
		Size: 7.5 MB (7470629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479961435e3b3b0f45e75d5ca62a1264b6b4640d216106ec9c3776d306574c8a`  
		Last Modified: Sat, 13 Sep 2025 00:34:30 GMT  
		Size: 25.7 KB (25662 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:98e39abc113895451f5909dc077cecfeb73c85c727824c6d07945585bc2577cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303709316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f046db245d07d2bdd6adb86eac15e92fa1ed89acbb32a20250d19349e3617b16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844afbca6e4c77a670255bceb98a173723d0370a888e5b730d4d22189f85d58a`  
		Last Modified: Sat, 13 Sep 2025 07:00:25 GMT  
		Size: 156.1 MB (156081180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeef265bcc0f601eadd4fbc8d2335ef457a9860d37bb8fcd7147b4b97f420d3`  
		Last Modified: Sat, 13 Sep 2025 00:14:40 GMT  
		Size: 19.6 MB (19628608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0da51a8d3b8d82840122c7f3764aa8ffbd88668096cdac3bcaf39159147e39`  
		Last Modified: Sat, 13 Sep 2025 00:14:37 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f935ffaac8b2cc81c16ba3514988d9c4f112b666147e11f080326ff4206c1a5a`  
		Last Modified: Sat, 13 Sep 2025 00:14:50 GMT  
		Size: 75.1 MB (75121695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e269e5080e18686fe09dff336bbec7a8b823d982af5597dbdae65934260d9c`  
		Last Modified: Sat, 13 Sep 2025 00:14:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360b23c5cf53f9862634049828e1a345d3e7b7d77ba4d45147874934ddb90dcf`  
		Last Modified: Sat, 13 Sep 2025 00:14:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:6213ea2e3b076c69f86aed76a8c2849cca1b492f5592c7bce5f7926b6764aece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c1ef40a69ef6b4c8a577017423dbd3b54fb00b465488414f1a528fb3b418a1`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c55d5cc8a9f189b31eafcb9f032e178fd4a8ef7b5e9edcbf3fa23217e2adc`  
		Last Modified: Sat, 13 Sep 2025 03:34:31 GMT  
		Size: 7.5 MB (7476368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4feedcfb1c1546687c0160ed5bac06ef15945ba371312bdb30f5da6207ee9cb6`  
		Last Modified: Sat, 13 Sep 2025 03:34:31 GMT  
		Size: 25.8 KB (25786 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:7f73b4e49f783ffdf4e2ac9887d33f23744e96724a33a192cd54c1597850742a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315507289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c8e8130a5c7a4ff37ac95af4f73e58654a57f355d3314018bcbe1d6d3b004d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b2ca9ff1a3fccb012f6c51a9f097c6995575e5e55d69deb7d54ac91943ca62`  
		Last Modified: Tue, 09 Sep 2025 09:35:24 GMT  
		Size: 158.0 MB (157963479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d44049f2345d5fc93f110ec14e393e02b339e7a221e9a738b65aa22b6a45da1`  
		Last Modified: Sat, 13 Sep 2025 03:20:03 GMT  
		Size: 20.0 MB (20018975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81df610ae69f6502d6e4f4c380c98b4454a30094ed96dae7d931c73782283d51`  
		Last Modified: Sat, 13 Sep 2025 03:19:30 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714760169ac25d55c691f7f5c22c98fea8aeb7c8c4cbff4cfdddc76a74246e59`  
		Last Modified: Sat, 13 Sep 2025 03:19:34 GMT  
		Size: 80.7 MB (80679182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcd71617b723c5c6b3c4e98835b01098aadb57eaa275f77fe0ff2852aeb13d0`  
		Last Modified: Sat, 13 Sep 2025 03:19:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f6a95a063c86f700ce3a83d557cb84e41bf05d7374c20e7e22cc847b2b132`  
		Last Modified: Sat, 13 Sep 2025 03:19:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:e411afd4988d352a6db66003c6800b333c391621cdd51f5ff9608e6597a86006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41675ef7d728e66db3dfc863c0bd1cb5d9bb3acc1d843eb3df9d488232ed0ee`

```dockerfile
```

-	Layers:
	-	`sha256:afea9411e291c47a8cbbda888eff7cc5acbbaa24821a8bac4ee9382eb90acbfe`  
		Last Modified: Sat, 13 Sep 2025 06:34:29 GMT  
		Size: 7.5 MB (7475831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b962af2858df9b1b6f201fa6c48c3b5e1e17d569ee9c871633c1e617a7e331a5`  
		Last Modified: Sat, 13 Sep 2025 06:34:30 GMT  
		Size: 25.7 KB (25702 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:f396ce8057ceb6022062e9a852b1a5b11b85f8bdedabddd12314ded22cbc977a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292364024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf3682b99c2531a867e4654c4d6d414f1e0cdabe76645c5162045bb34ac7dc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84772536e34edd89b294c09dbe86293a053e24f7d3644f8bc0e4612df16f4795`  
		Last Modified: Tue, 09 Sep 2025 07:01:48 GMT  
		Size: 147.0 MB (147027040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ab2b8177ec9b51a4840afef0d7c5f2194f79b9121a2956bc3d8f590416e0c2`  
		Last Modified: Sat, 13 Sep 2025 03:00:28 GMT  
		Size: 19.5 MB (19458801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f3f1ee53736cb6161ffc9beef70dabc78f8b2f54fb095d2eb1949845fe22c0`  
		Last Modified: Sat, 13 Sep 2025 03:00:27 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032984a1fed120cedaf8647c3100169802be65e0b4f9bd804fd477a2b216553c`  
		Last Modified: Sat, 13 Sep 2025 03:00:32 GMT  
		Size: 74.2 MB (74221815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae85ecc3a82286f9ee0eb18d5619a86fad504fd483af7e437b057034bc406bf8`  
		Last Modified: Sat, 13 Sep 2025 03:00:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d05464aeb0a52539429e9e1a43e88e8a7b7be8522a248b9075ef45ea4fccfd`  
		Last Modified: Sat, 13 Sep 2025 03:00:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:af2f92b7af8109e05396ceec9f85968b86eb484bc43ed3b69c46d6d8e1088aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0dc781d6cb7897b79dd558737c7e9425038e137dac81c702617d9011637f7d`

```dockerfile
```

-	Layers:
	-	`sha256:5bece64bbb00077f8f31621cca02804526265b84de4c9967e767393d5d117390`  
		Last Modified: Sat, 13 Sep 2025 03:34:42 GMT  
		Size: 7.5 MB (7461948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc81fdc5e1c3e18eec3b43900c21fd153b2e45749cd801ec2e99b8caa763669`  
		Last Modified: Sat, 13 Sep 2025 03:34:43 GMT  
		Size: 25.7 KB (25662 bytes)  
		MIME: application/vnd.in-toto+json
