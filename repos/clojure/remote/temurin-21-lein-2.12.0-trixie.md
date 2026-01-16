## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:bd7b71058ecd3d951bbb0b9a8552858e2cbed661309a4ba6e0e5e6cd98a89866
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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:383efa68c7a97fbcce1b32d4122b95f0bb819a92ca3476ad310494c3b7850e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230209503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8b8122b2482b075a540f2923c8d42e240441783ab94a246e7a4c6398d1a18b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:34:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:34:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:34:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:34:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:34:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:34:56 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:35:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:35:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:35:11 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:35:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:35:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:35:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:35:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc1e0c19d888088c5f66a0600022e09cfd522b2211db22c381f31958098f9d`  
		Last Modified: Tue, 13 Jan 2026 07:44:06 GMT  
		Size: 157.8 MB (157825981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf1aa9f05f09030d29f6f8f094f96e97f2900336c76888c03bb4dfa1e25faf2`  
		Last Modified: Tue, 13 Jan 2026 03:35:57 GMT  
		Size: 18.6 MB (18579759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd1bd8e791722a130d01500e15bd6f33c61aa51b198d777a6cd7bbda0fa4b01`  
		Last Modified: Tue, 13 Jan 2026 03:35:42 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5d55984a93575c326a9ef352c903d7e7c64cbcc51ac1a5980da3646592e447`  
		Last Modified: Tue, 13 Jan 2026 03:35:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:29757704338808854e334fe29160dba8174033eff778ae0f7d13408401fe51e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9141e5462b00c62e35eea37fe2c7357ae64dbd9905f3626a881cc8d10a9665`

```dockerfile
```

-	Layers:
	-	`sha256:3cef7893a519001c7c26d7bd64ccabc794c744255f694cfd3edeb391ef4f61b9`  
		Last Modified: Tue, 13 Jan 2026 07:43:38 GMT  
		Size: 3.8 MB (3817341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d246f09fc8ba4e2ddb126af8fabf37123f61f0b8b370f2d003701327517be3`  
		Last Modified: Tue, 13 Jan 2026 07:43:39 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9dca2ad2f7a573197d3d6603717007d8432cd54b62893ed6fbeb28a7218be8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228814603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7fcb47ce3a8d578bc1fa0fc157aac35f578e6bae663e88a51b6d369c575fa7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:38:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:38:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:38:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:38:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:38:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:38:26 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:38:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:38:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:38:42 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:38:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:38:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:38:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:38:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3340fb9bc41dba6d9c64998e81ad5f91b4b3a00ee9ea37aa467576a8059970fa`  
		Last Modified: Wed, 14 Jan 2026 13:21:19 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915e681bf033a69bcb71fe8b91e95a3c8228688be898d3cb95009f0039920a97`  
		Last Modified: Tue, 13 Jan 2026 03:39:12 GMT  
		Size: 18.5 MB (18540762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9094fd7dafd8a685494d0c7b61f671b4c919c33f9dd8242666e9f48d42318e98`  
		Last Modified: Tue, 13 Jan 2026 03:39:11 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2f3d12b1075420cb649293886b464d811fe683fd757a6a76c31fbd23299740`  
		Last Modified: Tue, 13 Jan 2026 03:39:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:237e8faa015a9c094336c914573f1f6b8bf497cb02c4ecbebf16ccc930d289cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3384eefd97ea76db435b530bba137c7602166dd1a31ef0fb703be2017a2e6d`

```dockerfile
```

-	Layers:
	-	`sha256:057df9c78247234d26e6868ed0fe918a1865908bb4ed3a72f41dba5b0e5771c1`  
		Last Modified: Tue, 13 Jan 2026 07:43:44 GMT  
		Size: 3.8 MB (3818218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6c0ce316fb084aa3bd9e12c915ee5a931f2274b2813b397cf12021e86115a9`  
		Last Modified: Tue, 13 Jan 2026 07:43:45 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9496496fe99a3ea1e0d8fabd1ccdb4240696e938e2d126468365b2cae8fdc763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234205322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416d584a11f6377e61a228279a4398dfd0f49b0a10cb1536b67a28ad940632f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 12:22:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 12:22:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 12:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 12:22:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 12:22:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 12:22:56 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 12:23:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 12:23:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 12:23:45 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 12:23:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 12:23:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 12:23:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 12:23:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb1fb4376f306eadaef720e8550fee0db4e7f2f64a3c535d26f70b6366bf18c`  
		Last Modified: Tue, 13 Jan 2026 12:24:34 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f860c041f3fd717f53d81ee2b1838495ad6449144671466a2bc8b4f0d24d5d35`  
		Last Modified: Tue, 13 Jan 2026 12:24:42 GMT  
		Size: 18.6 MB (18637229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb88288856b3c0bc7db58f32c338ab45384528562160feb367efe718202659db`  
		Last Modified: Tue, 13 Jan 2026 12:24:40 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937b3f58c847d34671688723577e9816cf29017537e569453276b6a2956b3c1d`  
		Last Modified: Tue, 13 Jan 2026 12:24:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a4413cd1cfebc653ee03409ddd12df328aed368f076464312e9b0eb43313d0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9999ba863d3dbed160d7f25476711fbcdf0cc8e6c2b0aed3de8c440661f067`

```dockerfile
```

-	Layers:
	-	`sha256:4b641a1cc08c34f597ee8fbf5825ef2206f6df049911c28639be08398f918b8f`  
		Last Modified: Tue, 13 Jan 2026 13:36:32 GMT  
		Size: 3.8 MB (3818341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0dceb9eb12d9bfc622a6f29ba65985957e0e14c00b7f552712540c53127d956`  
		Last Modified: Tue, 13 Jan 2026 13:36:33 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:5766e014b31c1158dbaf7bcb5a68c55fdcd846938b0540ce6ca88c9a2b23876e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228015386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329602f907071287a28ec0f4e2d9249aaac8501a588ddef71c55950a73aaffb9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:55:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:55:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:55:50 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 06:55:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 06:55:50 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:57:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 06:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 06:57:21 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 06:57:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 06:57:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:57:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:57:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a377be731c175125b38de6ef2031ba27b78ddc0d786d1f6e325bc386ce396481`  
		Last Modified: Thu, 01 Jan 2026 07:02:46 GMT  
		Size: 157.2 MB (157194284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951bf8a4e5129e4b3c92931f641a5621fbc7bf4a373957a00cabb9314d088ebd`  
		Last Modified: Thu, 01 Jan 2026 07:02:34 GMT  
		Size: 18.5 MB (18531729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8930cf04678b8428afa8882cac6c96e43a3d84bb3d709dbc4f1ff5693e406a16`  
		Last Modified: Thu, 01 Jan 2026 07:02:33 GMT  
		Size: 4.5 MB (4517791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd8ea7ed2f11bc52f15a917aa1eb8e74dac5be7391682fababefa1caa05674d`  
		Last Modified: Thu, 01 Jan 2026 07:02:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:87b09c00605218b8bf78d2bd3499d773157d7b0105c8065b486aac47e5a70fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3825353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f0b7a06da9bef2df81f20d53fb4f75dc3feeee76741b024d90752236d72c5b`

```dockerfile
```

-	Layers:
	-	`sha256:cd090a7f0d4822528bf3d2a7d9c2ee0f6bd221bc69d96eef3eb98f38d8dd39b3`  
		Last Modified: Thu, 01 Jan 2026 07:36:32 GMT  
		Size: 3.8 MB (3806957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bce7bef8bca1fcea65f8d84f9f79765ef60b5800ecdf732c18a3b8a869d58b3`  
		Last Modified: Thu, 01 Jan 2026 07:36:33 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e3017c7a487d8217690f3ece90553d065ed27a737e95fcf41b86687dbb3cf5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219557501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fe12921c5fad7386200d74df51f984e005772d4e94a396905a922f23826dff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:18:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:18:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:18:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:18:53 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:18:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:18:53 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:19:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:19:06 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:19:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:19:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:19:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:19:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe546673f26304e6e3a7565a4a244298cac2a8e593d48a999166ccef6a08f73`  
		Last Modified: Thu, 15 Jan 2026 23:19:53 GMT  
		Size: 147.1 MB (147069857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cc6f52f8cc6668c127e2c039af1dfd1209d77f9097c4ed417c604959431442`  
		Last Modified: Thu, 15 Jan 2026 23:19:44 GMT  
		Size: 18.6 MB (18620754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4126600cc166330f14e98bf2dd754cbfa8941c9842536c633a1167ae353c8e8`  
		Last Modified: Thu, 15 Jan 2026 23:19:42 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f041d433dd2e00d37215da8dab5bf09f73b10379224543e3d6a28b5c1513fdf7`  
		Last Modified: Thu, 15 Jan 2026 23:19:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:837f20b989fcec39a12b37622b5c16bb58ae2cc6af6c48f03aa86fd36c3f973e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114b35b380b8ff12c207aedb8f43b63f718174502effb44ca61c97f0077678bb`

```dockerfile
```

-	Layers:
	-	`sha256:4a4e798daac8f52c2b20e0945348b4b1a4a51f59e525f69b64b4428eda6e3209`  
		Last Modified: Fri, 16 Jan 2026 01:42:13 GMT  
		Size: 3.8 MB (3813768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c3420d8d83a3f7e0f5452a8273f1099a38a8943c8275b7cf887002499ee1bf8`  
		Last Modified: Fri, 16 Jan 2026 01:42:14 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json
