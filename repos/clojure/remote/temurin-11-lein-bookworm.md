## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:4390b6063520e327e6542470f98c61925e3eaff737ad5c5b6e389bb66b049e55
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

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f8f277721f11b5da6c812119d8ed7f6b9f998cdf804793a674f4b215df8d31db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217768748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c410b4a4939b38e19c6a7e26f248844d32aaa2d02ecac0bb7bc438fa71469c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:19:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:19:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:19:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:19:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:19:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:19:16 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:19:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:19:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa3e1a0276cd163749eea093535db253feabfad3dff55aee6c5931ac5d629d7`  
		Last Modified: Tue, 03 Feb 2026 03:19:39 GMT  
		Size: 145.0 MB (144966615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5754b8c5ccc1a67311ad97b9382e65d7013f62a4b3f589ca5eca49f14a39621`  
		Last Modified: Tue, 03 Feb 2026 03:19:35 GMT  
		Size: 19.8 MB (19802906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff07d73a5b71d23f54ec25dcbbdad63c8be7d0540d10e83566a2073a93673ed`  
		Last Modified: Tue, 03 Feb 2026 03:19:35 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cadd32993af4c0ef538ce8cd3bf5fa5d566f5cc96a0a32f8d8bf11897c321afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4317000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf167bd1cfdf0168a1bfa81eea2301eacc9ba6e4963149dd480d429f1a5c4bcf`

```dockerfile
```

-	Layers:
	-	`sha256:2db0a9b9f848ff16a56cda957120eb36f71109d86126a2e76fa6b94911ce2009`  
		Last Modified: Tue, 03 Feb 2026 03:19:35 GMT  
		Size: 4.3 MB (4300618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:054acf9e7785ec72968dc6847a4064a244f16725b831c45c366d7187b12fbc2f`  
		Last Modified: Tue, 03 Feb 2026 03:19:35 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bbb23e7174e72a90993c7efcc72d4bddec52626ce80091031b8aa1ee4f881023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.2 MB (214246391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4dc551ee5e685e62c65f7df2600ab02f329fdbee30e97d1cfdc32bf6e3f385`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:21:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:22 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:36 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:21:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:21:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429eab8eda95872f5414b3e6643bcfd70b51d4f99a1ab813c0774784f480da93`  
		Last Modified: Tue, 03 Feb 2026 03:22:00 GMT  
		Size: 141.7 MB (141729869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02eb86807ec04cf1c664f1dc389c3dd6c38a1827cab68d582b36762667a3e28`  
		Last Modified: Tue, 03 Feb 2026 03:21:57 GMT  
		Size: 19.6 MB (19632811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8812bba9fb70f142fcf0999d132ce5aefd1b16687a4897bd518ce82040db811`  
		Last Modified: Tue, 03 Feb 2026 03:21:56 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e101e20ceb70bb152171d7d415a8b7cc3957bf6804b45e4fb00b54036b26fd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4317354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef59da9eee3b318340439a279e108dc5a0e68fe37302a790ac28a36f4acc1e1`

```dockerfile
```

-	Layers:
	-	`sha256:61ae9e8ff00d68722ea6036c08298268c90f965be07d713b4f72684f164406ab`  
		Last Modified: Tue, 03 Feb 2026 03:21:56 GMT  
		Size: 4.3 MB (4300851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e3b5d8b97fb2a644b401f0a8c4af200eb1268e7311d6a5800042d84d27840c`  
		Last Modified: Tue, 03 Feb 2026 03:21:56 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9fc9f88ef3ef30ab8991205b85c4be1d088a4a73a288277baf0e5b6ca2c67dea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208948560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b5dd888e3b291d6bcf70c99472873879735cf6e83b516e7dfff5ac04d3307b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:33:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:33:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:33:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:33:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:33:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:33:50 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:34:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:34:22 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:34:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:34:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95141f17196f7720a48f3cf693760a0ac2298db7ce875915601dbb6e7658990c`  
		Last Modified: Tue, 03 Feb 2026 09:35:07 GMT  
		Size: 132.1 MB (132079737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e98320a3bd7efb0529ef7cd1a6db151df89f796f428351f0c5daf73ead6ad05`  
		Last Modified: Tue, 03 Feb 2026 09:35:04 GMT  
		Size: 20.0 MB (20023761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8ff1ab9b5aab1418885942f0c31d4eeb667ed7a61708df0b54066245655a5a`  
		Last Modified: Tue, 03 Feb 2026 09:35:03 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1d1adf439291d0ec5e126c9edb7eb65c6c378b11ecde95c94c3f0ceee0a01dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4318290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96457e5d9aa63663351a1587e9476bf4b8c9f786820361de1901e65b38ab7590`

```dockerfile
```

-	Layers:
	-	`sha256:dceee6e9af553bfc75ea20c6924fef1931f1a8b5091074e7434c0f99da315576`  
		Last Modified: Tue, 03 Feb 2026 09:35:03 GMT  
		Size: 4.3 MB (4301864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be599690a272a8c70c44eccad2f2a8788a34f295ebf335261a63ec98bc5db814`  
		Last Modified: Tue, 03 Feb 2026 09:35:02 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:1fd63becc91510d7b63548a618341926eaa0e70829fb0fb8785118fb68f00e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196814192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0405080f4827a31c3886460a1338f98f6e98fc2366111e8b3574ce4995645958`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:59:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 04:59:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 04:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:59:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 04:59:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 04:59:31 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 04:59:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 04:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 04:59:42 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 04:59:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 04:59:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b5b602abea3a46935fc3430bcf9dfab66fdf49ca5f43b3a73eb280ca32a7c9`  
		Last Modified: Tue, 03 Feb 2026 05:00:15 GMT  
		Size: 125.7 MB (125694835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30739c9514f080a8e1c8f82fa094429bc81019824f3107d32e1e35e8e30d73e3`  
		Last Modified: Tue, 03 Feb 2026 05:00:12 GMT  
		Size: 19.5 MB (19463242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce6d7d95f85dd29c87db5bb758376681e9f70928521cd5c08a2b1b71afeda37`  
		Last Modified: Tue, 03 Feb 2026 05:00:11 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c314f42155ab2deba0fee9cc1112f97c5e428b843e0f10d8cf985859014252c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f127fdac8cd8f02a7fa9c2c0f6c8fa9f48ff873a347e069967ee949c3525fdb`

```dockerfile
```

-	Layers:
	-	`sha256:cda2eb20ea4ba3d81ab89e629b7f06ec9e418b57a7918fee9dd5fe813cf13906`  
		Last Modified: Tue, 03 Feb 2026 05:00:12 GMT  
		Size: 4.3 MB (4292436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb103d8ac851cbd3630f52cc0b8d21bcdc755bf6327dd9bf6b7f8465da57715a`  
		Last Modified: Tue, 03 Feb 2026 05:00:12 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json
