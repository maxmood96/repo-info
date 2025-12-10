## `clojure:temurin-25-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:95abfcdf2c2f04b85cb3a38069a7d4882402a1cac7cf10c8bfab8e57373baa39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ddc7707bd08b6cc79b59d8dc24e7fddf2611df176504145652c8633ad4c31a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166927425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974298157d90f31042989b8f2cbb6bb69efca4306648de697a8cee6db3b2c084`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:56:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:11 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:56:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:56:11 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:56:24 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:56:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:56:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:26 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469f30affbc6846651e2876c789cdcfa81c0b76491deca304b28740775a815c5`  
		Last Modified: Mon, 08 Dec 2025 23:56:58 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88326b29a2a73720aff1daaf7ee5a9f34eb19454951ac593fc140ccd5fa6cf34`  
		Last Modified: Mon, 08 Dec 2025 23:56:51 GMT  
		Size: 16.6 MB (16607511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d25beada830150eaeefb7ee7828c14c468961009e526ebb4b1b44ff35621a1`  
		Last Modified: Mon, 08 Dec 2025 23:56:50 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd9fc8b3b7386dec2abfd6ca7a31467101af79893737c037380a6926fa6bbe6`  
		Last Modified: Mon, 08 Dec 2025 23:56:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cf5b2d615b8a65521dfde1cd209970ea99983fb10f2e6dc0cdafcfc66623bddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12926034492611a48525579a0228cce00f34990836211259a6a3cd2c3f3b4cb4`

```dockerfile
```

-	Layers:
	-	`sha256:b5164efeb0b4babc2c951efeaf0aa3576373176b01bb4ba10b987b000516afc7`  
		Last Modified: Tue, 09 Dec 2025 04:35:09 GMT  
		Size: 4.4 MB (4427494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d83cb99329886f188c53641b2acd115db1a15f3113b817f02950c02605d285`  
		Last Modified: Tue, 09 Dec 2025 04:35:10 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f113b158565eee3bf250633d4856ec3fc7607c9db876cea55f25ae166ac41d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164423395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec41aea8c296569b8cbe8b20f4441830eff001312857562fad3c52f496e5c233`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:03:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:03:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:03:05 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:03:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:03:19 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:03:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:03:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:03:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:03:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dcfa5187bce4c8528f6900b02ca454c7a05053474f52f15c7e3fbeb1896289`  
		Last Modified: Tue, 09 Dec 2025 00:03:54 GMT  
		Size: 91.1 MB (91052482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a9fbeb1536980c1ddce74bd4a5a2fd32f16395121f09ed72963dc20060808`  
		Last Modified: Tue, 09 Dec 2025 00:03:47 GMT  
		Size: 16.6 MB (16595032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3753a547235768a8ddd6c58f6422fe0577dc51b584dc9ea719b08d3fa274258`  
		Last Modified: Tue, 09 Dec 2025 00:03:46 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c1c67f3e9657520eabf66c85c1074a94e75e69cc9a31a446a6d61fb2b60ab`  
		Last Modified: Tue, 09 Dec 2025 00:03:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bcbfe902b046f34acbdfce207c120f4b53a99c8ce5810cc875af0deb0e94964d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4445637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d7a08c81cd09c9cdb27b3641bb81219ceaaf17f5f5403bfda1eb56deabc6613`

```dockerfile
```

-	Layers:
	-	`sha256:7c0ddc94010faf06138f83af3aabd8ec192b301ad1e06946daa2c396e04d663d`  
		Last Modified: Tue, 09 Dec 2025 04:35:16 GMT  
		Size: 4.4 MB (4426489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623aecbf6c604231a14a7108ce940522811e8512023647bba4845a9b46dd083b`  
		Last Modified: Tue, 09 Dec 2025 04:35:17 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
