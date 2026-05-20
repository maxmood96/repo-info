## `clojure:lein-bookworm-slim`

```console
$ docker pull clojure@sha256:fac33bc1dac5c9613d8332f388653bab3f85c7c6fde4b1eee76651ad4fd74b44
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

### `clojure:lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:499bdefaf6b026a5a339320df8e6932af1159100ca3cadc5c8b5554ce7ffe3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143086528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f89b8aa9c5cc400c1f1bb0b919094d8fabaa91c3dc4af5aaea2c8ed61c5c8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:00:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:45 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:00:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:00:45 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:00:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:00:59 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:01:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:01:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ff1f6325c97f1fcdbf05a281f90e6a30aaa9366ab5587a57f896310bbe1b59`  
		Last Modified: Wed, 20 May 2026 00:01:21 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd73868b608d5d6b18e6cc70b1aaf18961bdc420240aa693278ff7720b58928d`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 17.8 MB (17760255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b00cf6572dfd36d3c844ea65e083314ac420744bb711c0e0e01867cbf119d2`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542a5d4d551c21ec4530d2f2f73cde53fe8ab0365ab47bfd1f2e26180e2e4f17`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:661a397aed3e9f1b350c65b117567c604483791dee46b99d8997e4f70baee3dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec570d15587a1a4f05ef4f39ae4c84b8c89ac1d114654e6ca6fbdebbfd12c6d9`

```dockerfile
```

-	Layers:
	-	`sha256:28267f684b988b987f2043abe7b0fc6600a67650acde5c7f61dde4f2f102080f`  
		Last Modified: Wed, 20 May 2026 00:01:19 GMT  
		Size: 2.7 MB (2698751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:571ad892264ee0ae298cf79e2324acd082e8876bfa1093174b980b2253f11eac`  
		Last Modified: Wed, 20 May 2026 00:01:18 GMT  
		Size: 19.2 KB (19211 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3c3736d921823994d04e1fcb2bbd34d8450ccb5d03fa9eee17ec0dd44f58435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141769317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1887029e352f66053a6b60e93597a391093fc15e83f49b48a3bd50801b405f8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:07:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:07:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:07:38 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:07:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:07:52 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:07:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:07:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8dc3ec435dd42bf1159ee0240f038786482394ada4de4ae6caa1f37689d7c7`  
		Last Modified: Wed, 20 May 2026 00:08:13 GMT  
		Size: 91.5 MB (91542260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a755c13ecbba953f9836e30d2f623dc2123e9a33e5d9878f888b45a32a1268`  
		Last Modified: Wed, 20 May 2026 00:08:10 GMT  
		Size: 17.6 MB (17593848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30368fe456046d792f979ac3019b5bb85ddbe51394c5be6fe37cc8b3fae4f701`  
		Last Modified: Wed, 20 May 2026 00:08:10 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779503ab51d0963a0a29465e5c534afd0eb77759ae7c0dfa5b0e3ec5ce9fd576`  
		Last Modified: Wed, 20 May 2026 00:08:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75793bdb5f19ca12a6828e3a92bce050ec337c1bc5557c588575d39f8fb50a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791d30106d3ab9c7d1550a2342cbcef986fef52da26ef4c037cc7fe128a8bed5`

```dockerfile
```

-	Layers:
	-	`sha256:1a822e56f470269171d0d96690d0e8f58e1bb07d2a522c4ecce6d9ebf44bacf8`  
		Last Modified: Wed, 20 May 2026 00:08:10 GMT  
		Size: 2.7 MB (2698387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4939aa6f3ad54dd6e060ac64977747c0a0d18aa6b2f310aff516f6967649b418`  
		Last Modified: Wed, 20 May 2026 00:08:09 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e1061b778f649da1afa496cc2ec32e96dcbeefbaafbc0d4b13658d252f4beb14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19112901749489d98c7099c6e2af3464644a8e241cd078a9bc09826ebda34ca1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:42:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:42:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:42:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:42:17 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:42:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:42:17 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:42:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:42:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:42:42 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:42:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:42:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:42:47 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:42:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d1c7548cf004fea430b1528d91b72c7b0058d926919d1835a7b351081faec`  
		Last Modified: Sat, 09 May 2026 02:43:20 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72f726dbab0d412bbda9472c0073bd1341aea89726fffd61da3ea62505c86e2`  
		Last Modified: Sat, 09 May 2026 02:43:18 GMT  
		Size: 18.0 MB (17961357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c5a90e4f55a043054c6388223147a0fe339e684eaef63ec768029465e45581`  
		Last Modified: Sat, 09 May 2026 02:43:17 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee804b89bcae8a135057f59b186e797d594850024e7a2d73d9b841a2d7c41653`  
		Last Modified: Sat, 09 May 2026 02:43:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:55d9e28eacdd32948e5a732d795e61c44bce9122a9431155f4b63e6cebd9d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80570d07d54f0c712d012965d032d4342bcf756ee16a042bd62b7234da0494e`

```dockerfile
```

-	Layers:
	-	`sha256:ae325d08b80e328a3ea7bfcad35ebad7ce8c1eade0468a326ab55aec67e23090`  
		Last Modified: Sat, 09 May 2026 02:43:17 GMT  
		Size: 2.7 MB (2683890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d4b516a5996caa6a6060fd00123a4a59392d5e625a2e229f9d5b94f4951f30`  
		Last Modified: Sat, 09 May 2026 02:43:17 GMT  
		Size: 19.3 KB (19267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:74463311f88999e00e3eb5ef5b4230acb974a51c787fd2bd9b8c752faabf53f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137252085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb803ee88b11f73ef7bb2eaceca123a88c7f6c96bbab92263125b85dadd4a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:18:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:18:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:18:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:18:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:18:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:19:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:19:09 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:19:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:19:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:19:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:19:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2a98e90054a6c9a3c4e497f6656030195d43c38235d9e7c561af6ea94fc09`  
		Last Modified: Fri, 08 May 2026 22:19:35 GMT  
		Size: 88.4 MB (88420316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3966c37e95f2cef5eeafdb81c76199edf31dea2be63d090f3771d693622c33`  
		Last Modified: Fri, 08 May 2026 22:19:34 GMT  
		Size: 17.4 MB (17421981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152785f569a9939cd3e65cdf6c919ad475c171c11e693f92a315cd29f76dde1`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bd3ce40ed185361313ba94973634d7070666209fccccd5266fa1257939ab0d`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba102cc0ed7d0f6e8fd3037833904629132721b993579802c6ab930472541adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a629e9fb78cb3e0b827531a05a7c861589644b92ef1044351d9382399246a0`

```dockerfile
```

-	Layers:
	-	`sha256:be6054c2a0f3d8d4ca5264f7e22f326ddd533e42be93ac740bbbcf3d64a50a35`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 2.7 MB (2675109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fb7ac65835c86af611540df28585460429c758aeb81f7437e5696b17c5e1ad`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json
