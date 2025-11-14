## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:429bd05a2e9df550a090405371254d7bbfb2ec06bab13def4755769689ed1934
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

### `clojure:temurin-11-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fc6d11b719d2308e4ad0205e17c97bc2de0fb44696c9b8cfd2ac380b3da351fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217349175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94315441ee2780f5f5b1d9df88c35b493ff71571ec38a5e67caa7ee74a2b298`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:50:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:50:51 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:50:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:50:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:51:08 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:51:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:51:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc2d520c1e99ff71ad1b8e5d2e62521194caf3c3748a016f685b6b71fe72e2`  
		Last Modified: Fri, 14 Nov 2025 00:51:22 GMT  
		Size: 145.0 MB (144966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a72f2eb7b875f1f9d50233d0fe2a10a805d8a91c50a3a5780e86f17dbfaba3e`  
		Last Modified: Fri, 14 Nov 2025 00:51:36 GMT  
		Size: 18.6 MB (18579159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd415e99825a12c0979072023dfc596406c025af62a9e2ec118df6e6dc5bea3`  
		Last Modified: Fri, 14 Nov 2025 00:51:33 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:62190be21b331964c053c800e8f6f06d162ecf5c3c10b1a9189e54cd5278d4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3849887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa27aa2c3f8dc88304762a5139c68bedab3daf7fdc16990118656e71d4deba4`

```dockerfile
```

-	Layers:
	-	`sha256:ae70787574f6a2c6dac2a5cd0a45d7d6088d5ce5bcb50fe832e12c0321147377`  
		Last Modified: Fri, 14 Nov 2025 01:36:57 GMT  
		Size: 3.8 MB (3833525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4403afe034ec5cfeaad3b65b5393668c523d45c65cc55afd748147f3864463`  
		Last Modified: Fri, 14 Nov 2025 01:36:57 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:62e9cd3dcbc505df978fc34bbbb8e39c28a2ef33baa77ff3e09a01a93120f32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214439630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e952a970b7cf4e0dc42143f96350a481392bd29d5aacaf385af085f1182ef481`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:53:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:01 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:53:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:53:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:53:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:53:18 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:53:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a107ddc908046070d9b9a64575ed7cc2e6d5e84ac9c28388ddbdece39ba61648`  
		Last Modified: Fri, 14 Nov 2025 00:53:43 GMT  
		Size: 141.7 MB (141731503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd1af4a23bea878f8bc901218c5a05d6a96b5e99d64119b33a8eca6834442c1`  
		Last Modified: Fri, 14 Nov 2025 00:53:52 GMT  
		Size: 18.5 MB (18539945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc3fc9dcdb34a6521ee3b3d823eaa5b60318609ef95f71a823e6f46c63f26df`  
		Last Modified: Fri, 14 Nov 2025 00:53:49 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:92a3d304adfc55b6c99f5c196d37dc0f7bf13bc4a8e5685e101f93f96a6d8df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c610c4b028a5856390b7704a14be2c197da844d63fbe3a6963896bf24ce159b0`

```dockerfile
```

-	Layers:
	-	`sha256:599624c25bf7a700dfe0939475f20e3afb87d298d64b25a252f0948cd42fa1a9`  
		Last Modified: Fri, 14 Nov 2025 01:37:03 GMT  
		Size: 3.8 MB (3835020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53f416c802d95c5af36c38eabf78532328a21260680d6453243fcd305508bde`  
		Last Modified: Fri, 14 Nov 2025 01:37:03 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:066e1ede7c689def0a7bd46a2612138697a45eed05e658ec28d7bb861b494bd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208346458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929c5554d1b28ea6d210d9d865f45a3e11d9ef11356699e973129a0306a5dd0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 06:46:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 06:46:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 06:46:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 06:46:38 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 06:46:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 06:46:38 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 06:47:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 06:47:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 06:47:06 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 06:47:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 06:47:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5a3b6c6a00a022bc990deb9832b7b4f14089026526f7793cbb341460c5a679`  
		Last Modified: Fri, 14 Nov 2025 06:47:48 GMT  
		Size: 132.1 MB (132081986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3623a949c1ba58aade8cb46f320a7ed2fcf53a9e9d099ad7285ad8ef8cbd943`  
		Last Modified: Fri, 14 Nov 2025 06:47:54 GMT  
		Size: 18.6 MB (18636556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aca6834ffbfe83cf770bfdfa6777315b068b4e2d4863dc5551c4e9c2df6e1e`  
		Last Modified: Fri, 14 Nov 2025 06:47:54 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b84fed8b5da3a04aaefee567e126d05f9dc48f4c39c77a4992b9f2d55a0b87fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf04472136e647d7a65d4ff42d0b0ca14b94a20a2ca6a9af49f37d1f7d48fbb0`

```dockerfile
```

-	Layers:
	-	`sha256:205cfedfaaec22b005963debd8d16d697a896242da9a828264147b73d1628d93`  
		Last Modified: Fri, 14 Nov 2025 07:35:34 GMT  
		Size: 3.8 MB (3833908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27980c87920d069fb8d46a5a03f3ac8b201c608cf4e58a8edbf54a89e0dcbcce`  
		Last Modified: Fri, 14 Nov 2025 07:35:35 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:67d0ed6424527bfbc43965d4bcad4ee3d3c30fefdd3c08657af21cd3f39ee95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198184766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e51d29b28f7fde30fa17fa1a4a584a66903f6a1a6181540553927e67728b83`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:52:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:13 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:52:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:52:13 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:52:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:52:28 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:52:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:52:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a213f18554008fe4500d07244be8d9e9a685b476789161282afef051ba3355e0`  
		Last Modified: Fri, 14 Nov 2025 00:53:15 GMT  
		Size: 125.7 MB (125694467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fbf31b0ddfecad5ffe400229e4fbe47d65b3c914f68c87bff63df8188e44ab`  
		Last Modified: Fri, 14 Nov 2025 00:53:03 GMT  
		Size: 18.6 MB (18620211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a78370e18a290c148168725486e2119ce1c6b63e76b65cb172cd62302be5b6`  
		Last Modified: Fri, 14 Nov 2025 00:53:00 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f64c648898b916e8aaf9a21b234f0abf2ca6494bbd8ed7e7c7d0d4de74fad4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a396589cbc021284d9a9f895d1d12e23c3c98d994251c9b40df3d91ca4fa157`

```dockerfile
```

-	Layers:
	-	`sha256:1c3dc5297a12cc4c950f20864fae1c5139d185d1cd620831ca4169265fda161a`  
		Last Modified: Fri, 14 Nov 2025 01:37:13 GMT  
		Size: 3.8 MB (3829956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e427bdb21fa7f5716b8dadc9cd66c847eedc17d683d3ab2edefbd67a82b43fa6`  
		Last Modified: Fri, 14 Nov 2025 01:37:14 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json
