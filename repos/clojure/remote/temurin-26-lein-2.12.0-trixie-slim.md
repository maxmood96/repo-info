## `clojure:temurin-26-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:6ba89095d85c854239ae24ab443e5d3875762ca69eebb45739ec643eb7eb4280
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
$ docker pull clojure@sha256:40da87b89f3ab029ba338c2fc52bd0164d4ae2ecc44309e8e409ffc32607477a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145270599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f937eebe268cb42a1081fbfa97725d5d6f88b3428ed6746d877a6236dc522467`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:02:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:02:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:02:16 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:02:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:02:33 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:02:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:02:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cb911f0c1363c8994a0a917d64c8f1ebe6c145420049650de30cbdc51e52cc`  
		Last Modified: Wed, 20 May 2026 00:02:54 GMT  
		Size: 94.5 MB (94524374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1a0c2683575ac34c697666a090c2140da0c0fbf8112a686ef91cd366bfb96`  
		Last Modified: Wed, 20 May 2026 00:02:52 GMT  
		Size: 16.4 MB (16448162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a424002eaef46fa0aa54915f5c0e6227b2a763088d8021c42d5c32256faebe`  
		Last Modified: Wed, 20 May 2026 00:02:51 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc793a03998acd8560730b3b618a81dcc83e93c001d86c21479867cb43a7d2c`  
		Last Modified: Wed, 20 May 2026 00:02:51 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3598917b90d812cb80d515118c2d62a3e20a094ea5e76315ee0fb21cf6f2f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863f46d5a124e5aadf24d106533b9e930ad011a138dceaad3cc275c8288bb6c2`

```dockerfile
```

-	Layers:
	-	`sha256:d9da0c06656e6b00f676e447b9445462f64991fecd6414ecd10d5455d70af6e9`  
		Last Modified: Wed, 20 May 2026 00:02:52 GMT  
		Size: 2.3 MB (2330348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1422134aa269f12c84c6e5d20cad7d380eaa6291be44d674de32547e9ae2b03f`  
		Last Modified: Wed, 20 May 2026 00:02:51 GMT  
		Size: 18.5 KB (18534 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f408c8ade27f7c6821250f1f1afab8360134d513fa69f0592fe55102f1e74681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144578643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df70ba03dc08ca7f0a3507a32d876d20350559240256c1c2c02973709a9e781`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:09:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:09 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:09:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:09:09 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:09:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:09:24 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:09:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:09:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538fc7b5ce7b1642fec46bd62575d1627c7d0a5ca0e35d3fb785904dd61b5672`  
		Last Modified: Wed, 20 May 2026 00:09:46 GMT  
		Size: 93.5 MB (93504347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bc0aa8477223e36568eab6aa030ac9e37fa02919dfb55eb47d4a6a48d93633`  
		Last Modified: Wed, 20 May 2026 00:09:44 GMT  
		Size: 16.4 MB (16414208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ad0fac1087f30e52a07ae60469f1dafab44c80153fe460488b9430701f361f`  
		Last Modified: Wed, 20 May 2026 00:09:44 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83375e397a0bc7eb3a56f1673a955910ea21c803500bfffe03da0281ed6f414a`  
		Last Modified: Wed, 20 May 2026 00:09:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd787fb029629d9e40275a91f04c220e3d4ea9cf3a276634ea066a703b3b0672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2348609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2044ec6c05c6f6cb1cd26693776820b2df3d68d91eb4d2b689762af90794b94`

```dockerfile
```

-	Layers:
	-	`sha256:ec27302b5f2cbc5c10a4dab090f68a870d3c44b64a1b0a43eface547c2319191`  
		Last Modified: Wed, 20 May 2026 00:09:44 GMT  
		Size: 2.3 MB (2329955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c79c45eea3d172179e13e52d0951eecfa190c2776482dcdac27f2029bd5fac3`  
		Last Modified: Wed, 20 May 2026 00:09:43 GMT  
		Size: 18.7 KB (18654 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e0bbeef1005d6cdfe50ef7c2b62ad7142c8c34861c449ed35d98a3fba58d2ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148503691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f6579cff2df26646d7e20246e52701ee7904495a4509292188b911196d70d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:48:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:48:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:48:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:48:47 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:48:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:48:47 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:49:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:49:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:49:24 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:49:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:49:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:49:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:49:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f8ab13e6d21adc6f6b5e2937ae339405e46ec097e90a97ff0de0b57189e749`  
		Last Modified: Fri, 15 May 2026 21:50:11 GMT  
		Size: 93.9 MB (93902067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55bf8dcd0ca0858031094124914e624100604d684fb4938d6fd0c53e31696f7`  
		Last Modified: Fri, 15 May 2026 21:50:09 GMT  
		Size: 16.5 MB (16485388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0b6bbcb2bae1403bcbf9a8ede8470b2693553977dfca2c1a946074868b0b5`  
		Last Modified: Fri, 15 May 2026 21:50:09 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b4665ade97a3224477bf33edbbed97acdad9ede06e99635b939c13cacb642c`  
		Last Modified: Fri, 15 May 2026 21:50:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d13f7741ea133bda692a9333929bd0eef95510e0e08739116027c4c01250cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6691a3e3aa497d842953add456ce9b1451e4e09b526b55cc7bd4f275ab87d654`

```dockerfile
```

-	Layers:
	-	`sha256:3da8b4c6e0320a9743e0dad3630056f7318b8e568209c3f7b87a4b0f94eef0c5`  
		Last Modified: Fri, 15 May 2026 21:50:08 GMT  
		Size: 2.3 MB (2315222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b878c4a24532daf1ac383568dedad60a941416aa01ae3bd049a391be01a01523`  
		Last Modified: Fri, 15 May 2026 21:50:08 GMT  
		Size: 18.6 KB (18578 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f0a17ee6f3d62a5289587583793b16a42a51cf5133769c4f3f7215c7ceb435aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141385320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2947c8055ffc39598bb2e8f7036e07c83413d9d6b334178ce79e17fc3db3822b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:49:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:49:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:49:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:49:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:49:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:49:23 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:49:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:49:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:49:35 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:49:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:49:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:49:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:49:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f28ec650cc3670cf225cb9ba6ae9fc5cb2ad7e45efa2a6c00995e79e4c5ae07`  
		Last Modified: Wed, 20 May 2026 01:50:04 GMT  
		Size: 90.5 MB (90536967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e658c46330ae0650483f62a63862fbdda6852a5812f381f4bd9a88746ecec8a`  
		Last Modified: Wed, 20 May 2026 01:50:02 GMT  
		Size: 16.5 MB (16484277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6a625e1343e7c966ab1404bcc22377535b48eb9056aff6880a3db2572a4369`  
		Last Modified: Wed, 20 May 2026 01:50:02 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf683d850c4e97c511f857cff0e058cae3c4a6c1ea28a4a7ac2de6b0572b3eb`  
		Last Modified: Wed, 20 May 2026 01:50:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:19508e9d2909714e652d2bf930f09e3be70c161e5c59c404936a1d3aded513f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfd6d983488b5bc56b8db53495f141fe3a0df3539952fab00b8d46a02dcce24`

```dockerfile
```

-	Layers:
	-	`sha256:5c7487bff7a2fc86550bf3f1bab1b1f615c5c6bd7f76b884f5cd008c89b06573`  
		Last Modified: Wed, 20 May 2026 01:50:02 GMT  
		Size: 2.3 MB (2311961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4a61f547854045ba2c982d660b3e868ad3e85f671bc70b2ecae64bcb8e319fb`  
		Last Modified: Wed, 20 May 2026 01:50:01 GMT  
		Size: 18.5 KB (18533 bytes)  
		MIME: application/vnd.in-toto+json
