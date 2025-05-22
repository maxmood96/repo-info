## `clojure:temurin-11-lein-trixie`

```console
$ docker pull clojure@sha256:5c7ec8023e464cb220dda534ceba0f0a618ebbaca4f42181446395caa636ed49
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
$ docker pull clojure@sha256:72d4c08d057d58e272136f5bce095b1a764811733acd42b8f42994a02fb8dbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265824625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6f25068bdd4be2c8b8d798d8b3ee9e8de4d24f20f0420b92c5b4cea053656b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dd6a4ee94245d6f0d02f096786793894d9415ccbbe1306f89680ad82bf9fb0`  
		Last Modified: Wed, 21 May 2025 23:32:29 GMT  
		Size: 145.6 MB (145635719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467dc9684a13945bb9713cab38bed22c99e018c2eac70a8d8f7bc5f4ff330078`  
		Last Modified: Wed, 21 May 2025 23:32:28 GMT  
		Size: 66.4 MB (66427763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26687e658acce8ab087942814fc4862e9e5e32f6f6f3d2fb381b7e4566d7b580`  
		Last Modified: Wed, 21 May 2025 23:32:27 GMT  
		Size: 4.5 MB (4514203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1a3dc40602e53a4c6b71d98d792dfb74cbd57d86ad40ad21fc7859e159928a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6369764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911a24d4aa426f45b26b86e7c23e0316cba04e5bf1f56d87dfabbdcb88f1307f`

```dockerfile
```

-	Layers:
	-	`sha256:f70eb00a421b37b91e3f474eb4f901850259ab420945578281cd7b1adaf71cce`  
		Last Modified: Wed, 21 May 2025 23:32:27 GMT  
		Size: 6.4 MB (6353345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d795a78054143fedb91d766a06af048bb113a5e2caef65fca07d21499f9daa`  
		Last Modified: Wed, 21 May 2025 23:32:27 GMT  
		Size: 16.4 KB (16419 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:addc8800ddf319bb4037664dde89415da4199d0d31ee71c264d29459535f1944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263015932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49baa4afb426d4caa99da7011e40d0b9401b9d7c5bd5468ab678bea3fa3f112b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa81e2617996b590287af40ced269fbafb204b4143062c93006401b1b1e34c4`  
		Last Modified: Tue, 13 May 2025 17:57:09 GMT  
		Size: 142.4 MB (142420736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e76af499736aed70f6dc035bb40cb351abcb1b41ec8ecf253b61153d0cf8fd`  
		Last Modified: Tue, 13 May 2025 17:57:08 GMT  
		Size: 66.5 MB (66456836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d7b1099e52dfba8cb19b24e0a545240bb49d08d16a37c453654f4f384b90c9`  
		Last Modified: Tue, 13 May 2025 17:57:06 GMT  
		Size: 4.5 MB (4514210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:75d0712023a10d84cc8a915deb5fc0feabf3292698421ae36ac749d85e9ab977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab99e7aa985b47b267cd3ca94600e65fb0e84efdfd75c2a4ea954e425ed7bd4f`

```dockerfile
```

-	Layers:
	-	`sha256:b60a7129405e852415a0e5bca28bf820041396db4532380c3af14a89ee209a55`  
		Last Modified: Tue, 13 May 2025 17:57:06 GMT  
		Size: 6.3 MB (6312958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5908894cd6b62943c60027f12e5fcd6e66036e02735cfac2ceb7bda18e8a9b0`  
		Last Modified: Tue, 13 May 2025 17:57:05 GMT  
		Size: 16.5 KB (16540 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d4473a635e299fadd148e670496924819bc319b123c16e3e63a95ea92c1398c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261902349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5ff9adef3329121a5fb7aa1d7589498cb8061932c9b1249b960133343a4855`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cae647bc37778358b907d22b7bf35eb9da015bfb7b8a8800a879a20173b410d`  
		Last Modified: Tue, 13 May 2025 18:34:18 GMT  
		Size: 132.8 MB (132809833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c90060580e27738b033c4ee605daa0bbfcb6ee12f17b0ef71d4c842d5d5d18`  
		Last Modified: Tue, 13 May 2025 18:34:16 GMT  
		Size: 71.5 MB (71505787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25c92bcc16969ce7c9ed74c555aaec51bfbf7db699cec7a209f170f11dd9fc0`  
		Last Modified: Tue, 13 May 2025 18:34:14 GMT  
		Size: 4.5 MB (4514145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:14e9abd82210f2f9b87792422ad05016cdf06f8501a33d391c309095f731d86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6325179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19858226099baa3c5e7d676ff31fd27d14593f391b5b0fa397c2dacc4309cba1`

```dockerfile
```

-	Layers:
	-	`sha256:e4ac7c1ca2551d361c4400420ba5c69ff35416389fe6e0271e77b35a568379ee`  
		Last Modified: Tue, 13 May 2025 18:34:14 GMT  
		Size: 6.3 MB (6308716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7e8914301e93df755a8038f320f49eb12a632522f7bd8fc1482465e20e624a`  
		Last Modified: Tue, 13 May 2025 18:34:13 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:251ed03013a60adc952229fe102092ed568ad20af05910e9167ca0a29d5e74a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246922793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1faa164a999b24ed0d5323c9a80de320fd433e45b99a46544ce1e5d180e12bc3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5926ae25fe9817c3fc9b51b369a326f72c3940aeb3cce1e885d54af89199e4`  
		Last Modified: Thu, 22 May 2025 03:40:46 GMT  
		Size: 125.6 MB (125585847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17774bbc8469d41e85e68cb00bf7899ec1b66971da37b285deb03ca31936ec98`  
		Last Modified: Thu, 22 May 2025 03:40:46 GMT  
		Size: 67.5 MB (67500487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d233ee4ad522cfe29c38b7cfea94a7c4ef8dc989cc48c62bbe520db1274f15`  
		Last Modified: Thu, 22 May 2025 03:40:45 GMT  
		Size: 4.5 MB (4514200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:385b40b9e253bc44248e7b04513310b268db9586d6e3e15b00f4d5eb5f63f89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6365744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12646b9d3d485fb0209fe2fe1d7bad2d71f140dd0caa5d7d01514411fc0b4aa9`

```dockerfile
```

-	Layers:
	-	`sha256:bb4354607fdc46ed42b2260265c846333e17ec675edcdc6018c8c7ee4136285c`  
		Last Modified: Thu, 22 May 2025 03:40:44 GMT  
		Size: 6.3 MB (6349326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d67e95ab059eef8d774d8b7d5d56c6657c103a34bd8df3b67586f18e63062b`  
		Last Modified: Thu, 22 May 2025 03:40:44 GMT  
		Size: 16.4 KB (16418 bytes)  
		MIME: application/vnd.in-toto+json
