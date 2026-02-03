## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:b72f7d7f096d48efe7e1c492d0647fca810515ed8ee2efee0b9ad7450d3f90c0
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
$ docker pull clojure@sha256:9f43425a94c5d2787bfa5f77ebb28f4c82ee58fd051d7f918ff7c15af12423e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217357376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a92efbf710d11fe87ed9b95afc036c79d122571e1ba7171235ab7e7d07807f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:19:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:19:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:19:12 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:19:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:19:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:19:31 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:19:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:19:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8453c7bd6b3077a63443c92fdb746ad1fbb8946a535606c1e0621cfdfe28e558`  
		Last Modified: Tue, 03 Feb 2026 03:19:53 GMT  
		Size: 145.0 MB (144966643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5655bd6f3ca0c8662cdf27662631181aa66469148b8f7be744e5a704a7dff9`  
		Last Modified: Tue, 03 Feb 2026 03:19:50 GMT  
		Size: 18.6 MB (18580034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b6b61aeaa211ec88626b96a759a6328c7de8bdb3ca34c3cdb849c9447f6a7f`  
		Last Modified: Tue, 03 Feb 2026 03:19:49 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:34765b05bf9db31b1c02b6f30d972f3b1d72bcefb9c5966056d8754c347748a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f687b4df6aa326735028e541fe61fa23bed77964369e72bf5783050163648a8`

```dockerfile
```

-	Layers:
	-	`sha256:be44ebcd814fa58444ddcd2f0d46b3e9d7eb74afd672d683a663fa37f78b6ef4`  
		Last Modified: Tue, 03 Feb 2026 03:19:49 GMT  
		Size: 3.8 MB (3834378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b1082c93e00b7d014722c4f227d4c5fb7d0737011eccd25edf4126ad9059fce`  
		Last Modified: Tue, 03 Feb 2026 03:19:49 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:76b1c9043d2460eaca11064fc605e0d407e7fed53124cabc0021941bbaea4303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214441140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e042506431779fe826663d67297853d375f2911428c4164031a049295d41779`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:21:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:42 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:21:59 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a1def3147761fddf05a39c7a50a65cf76465307a6a4e10540e678260dd7c51`  
		Last Modified: Tue, 03 Feb 2026 03:22:19 GMT  
		Size: 141.7 MB (141729907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4898c8c50db3cbda207949766ecb847c849ac85472a5fef7363a68beb65277de`  
		Last Modified: Tue, 03 Feb 2026 03:22:19 GMT  
		Size: 18.5 MB (18541464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41cebfc4d4343723b2781169faa3276b0054ea070df86230e26b2959c300da`  
		Last Modified: Tue, 03 Feb 2026 03:22:18 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7af42f13670cfdc0a02f7a448aaf93b639b926388f761b0a5c1104a887abac98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dae927ea086ca4bfd0032f3bafbf490418a209faad807b1f7556383a1e6b4ac`

```dockerfile
```

-	Layers:
	-	`sha256:9b27ebab18602b2fa73357ee097f6929455ecbbbb6321e4918156648552c906b`  
		Last Modified: Tue, 03 Feb 2026 03:22:18 GMT  
		Size: 3.8 MB (3835873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d49f8939690e4672508b3d8b86e87da28e26f3841e1e59e7e3c35a079ff76018`  
		Last Modified: Tue, 03 Feb 2026 03:22:18 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:da4c0d10885d79878d543de10c49acda83130b5dcd25e7955e95f09d8605303e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208347081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cd2eda5ec09b3c8f57dfbff3dc4b8ffac52ee6ef417ce2fff91b7273648c36`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:35:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:35:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:35:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:35:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:35:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:35:22 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:36:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:36:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:36:00 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:36:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:36:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d550e8e3e84307a53a865255ffa7934eb6a2d4a27cf9304f480d6e6b94183b`  
		Last Modified: Tue, 03 Feb 2026 09:36:41 GMT  
		Size: 132.1 MB (132079737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c438d31ce1757eb40db0b0b220549400e5095ebfcc26ea7c6b55c3ff91cd08be`  
		Last Modified: Tue, 03 Feb 2026 09:36:38 GMT  
		Size: 18.6 MB (18637459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f96a9adf9b4767b3a463f3266518df1f30482b4c5d147d6aabdccf022a6e96`  
		Last Modified: Tue, 03 Feb 2026 09:36:37 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d95b0ffec85a192f740bbcf709534b8232429a7b5e0a5148db4ba808cb1e2336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c301356f2cf8fb70ecbc296a57a9b6863676a076dc0599b6eacb973862610ec7`

```dockerfile
```

-	Layers:
	-	`sha256:caf1090d488b4914ea76e1e18bad1608aaa36c4794935b13ac4fda540f4395b3`  
		Last Modified: Tue, 03 Feb 2026 09:36:37 GMT  
		Size: 3.8 MB (3834763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e522927df4dd0d612ea202bce9ed1a9f93e6b36439b0a510e6f09e6ba6b93c4`  
		Last Modified: Tue, 03 Feb 2026 09:36:37 GMT  
		Size: 16.4 KB (16407 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8c9ee36635cb9e31ec43a23f903c20138406a44108f8438a6e2ae22323af8776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198188111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e52db41edfa266b2bce5ef6470e0016c8679787356b02615415739176d8e52b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 04:59:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 04:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:59:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 04:59:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 04:59:56 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:00:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:00:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:00:10 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:00:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:00:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc79570d0434267dfc1c3c1e2bf2c0aeed5bd16edce07420e924b763e62dc668`  
		Last Modified: Tue, 03 Feb 2026 05:00:38 GMT  
		Size: 125.7 MB (125694888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4c62e0715889143fbde4ba3245390cfcfc9171116d9033b9fe414ed54bf2d4`  
		Last Modified: Tue, 03 Feb 2026 05:00:36 GMT  
		Size: 18.6 MB (18621061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a536cdff004a88c4b131556ed4af5aeee43656d97dfa670e1d758436ac8b3b`  
		Last Modified: Tue, 03 Feb 2026 05:00:35 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:293e07f0af0ea7eeca904b01597e4d29d917f583bf7a15c5e374617e0199145a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9600b79275d3bf183e2a5d3e62ba6f9d1187fab2815bdf0c4b9c0dbdf49fec4a`

```dockerfile
```

-	Layers:
	-	`sha256:b2116f4c1e0d9407eba8392a2167105b26e907d5ec2f4b6cee26c545247c1f3f`  
		Last Modified: Tue, 03 Feb 2026 05:00:35 GMT  
		Size: 3.8 MB (3830809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55af954e10ae8e3e9f229237564d2ab1b5de6f73ef5bd3c887202ebb454d9473`  
		Last Modified: Tue, 03 Feb 2026 05:00:34 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
