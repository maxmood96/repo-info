## `clojure:temurin-26-lein-bookworm`

```console
$ docker pull clojure@sha256:9fe3ec26f94fb04daadf4327b1cf01f91787a20e3b861515f5ee7ae0ee1f117b
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

### `clojure:temurin-26-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:90685dcae1bce1e773facb1d0539e3e7b05df93b2d80b8d1e5960a68578a6cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167269204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a65d5b692eec703369f754fd1cf629be985e9a1bee01eca714e2582332703e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:07:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:08 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:07:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:07:08 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:07:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:07:22 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:07:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:07:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe521d4bb446c7d4ca969a7b7f05569101a6c2e431263790948a41f0c238858`  
		Last Modified: Wed, 15 Apr 2026 22:07:45 GMT  
		Size: 94.5 MB (94455692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aea1e885291748957a7f28dec88a505371ee4dbd39f2d3e3b079007d229a1a3`  
		Last Modified: Wed, 15 Apr 2026 22:07:42 GMT  
		Size: 19.8 MB (19806553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4504de4b8eb4acd82323585b5cee6aa7c33e7c23d1d98ba108279be4ed21677`  
		Last Modified: Wed, 15 Apr 2026 22:07:41 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1ecaec05cb9efa9c3da400c616f5f3ef40aa7836e2f12b64bbba646ba1b225`  
		Last Modified: Wed, 15 Apr 2026 22:07:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a8899010a53a5fba1ed6c1ce9911ced3c1d5d52a2dee896bea66ac2edcaf07e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19441a2279168a1e4a4d8737bef36a1c96176a94caacc6cdcb1e304354f5584a`

```dockerfile
```

-	Layers:
	-	`sha256:b3649e78ab9a3a3f6701784e39191fe56666321b69b89faf553cee937a6f1bee`  
		Last Modified: Wed, 15 Apr 2026 22:07:41 GMT  
		Size: 4.2 MB (4247885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eebd0ffaa0c537ad0ea9bf7b7be1218c2c7de3de2a2960bea6076c48459b2dac`  
		Last Modified: Wed, 15 Apr 2026 22:07:41 GMT  
		Size: 19.0 KB (19011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0ec4b3eab94749303c8140c0bf82dab98b3b7079052f73f7841a974b8f353789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165923638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965f47f47adf430045bbd576bf45188d05f71c4f1b3b87cbcecfcaf0249f36ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:06 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:19:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:19:06 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:19:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:19:20 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:19:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:19:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34afa5a1c2d132f4af85916efb2cc7108481fbee27ddbe286ff694564fa4daea`  
		Last Modified: Wed, 15 Apr 2026 22:19:42 GMT  
		Size: 93.4 MB (93395204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4f057e717eb9c36ef0b1f77f3f0e4f83a236dd8fbebbf3dd4259fba0ea2495`  
		Last Modified: Wed, 15 Apr 2026 22:19:41 GMT  
		Size: 19.6 MB (19636988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a20d035f74e534a54aaeaac98108d0f39a6579e1b39d4267234390a912883`  
		Last Modified: Wed, 15 Apr 2026 22:19:40 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8da663d531063991452757d6f912c9e115bcdce90516b5b6d461b8c06b2c5e0`  
		Last Modified: Wed, 15 Apr 2026 22:19:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:88ea13edf325421d9368c1455a8d27bf1d2f1c8c3853220adf80885e1de7a1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767b28701b1144e2d37517f8ab33f2a5671e06f71bdcf9850cf8d67275d98b0b`

```dockerfile
```

-	Layers:
	-	`sha256:7aa39892ad87267e17b9ac2ecb3c7be19842c2510446fbea7fa60f4afa5c9d0b`  
		Last Modified: Wed, 15 Apr 2026 22:19:40 GMT  
		Size: 4.2 MB (4247521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f796a90253d6603690cb4fbdbd930daa40a5ee8aada1cbd0f8eb8c134e82dc3`  
		Last Modified: Wed, 15 Apr 2026 22:19:40 GMT  
		Size: 19.2 KB (19155 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cb317ba14c1da94211849df4d6ed91bfcd98c72bad087ca9f2e3564e12b66992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170667057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a1dfb784fb041146054add29bed7f109d2189b7d1f4fbf709ed53e643f3f48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Fri, 10 Apr 2026 00:49:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:49:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:49:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 10 Apr 2026 00:49:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 10 Apr 2026 00:49:05 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:49:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 10 Apr 2026 00:49:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 10 Apr 2026 00:49:32 GMT
ENV LEIN_ROOT=1
# Fri, 10 Apr 2026 00:49:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 10 Apr 2026 00:49:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:49:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:49:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5bb937b64e28b9440675ccbc228210a99b8d8484e299953df825953180b5f5`  
		Last Modified: Fri, 10 Apr 2026 00:50:20 GMT  
		Size: 93.8 MB (93781433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213dbae337a5455dbabf0e4151c608eab4dc2d1b81e9706f56314a65150c6b1d`  
		Last Modified: Fri, 10 Apr 2026 00:50:19 GMT  
		Size: 20.0 MB (20030503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4198fff1b6a249f71f7f9d6ecea50f6deb671380a8ca8c1c5215373bbf9b5`  
		Last Modified: Fri, 10 Apr 2026 00:50:18 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206a180a19dc4d851f0188da0462b6f41c0aa4db076257034717d005bdb42d3`  
		Last Modified: Fri, 10 Apr 2026 00:50:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:adc8f5dc47d4c34f13a7f2d6d69955c73faa32406432afc72d40038471951df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66bfc359e426ec7ab176f7b5cd0b7639e74a3d2ef1d5283ec65f15252a1562`

```dockerfile
```

-	Layers:
	-	`sha256:6c308741155985bb4257410b0219e2df5a8bdcb757a3e94ced71c0f9e9523aa1`  
		Last Modified: Fri, 10 Apr 2026 00:50:18 GMT  
		Size: 4.2 MB (4233694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f12440292c65141185367979e69bcc0720ef09554d499a480bcadbd8f51c7014`  
		Last Modified: Fri, 10 Apr 2026 00:50:17 GMT  
		Size: 19.1 KB (19067 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:9d74129e6a84ab38cca0a8d55d3b8ea3cdb981b5c9a9e4bb7e2483a3fab7e289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161680752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f5fb48f652ebb39f815eea7e6ce4096f3e0d14ee68663c4ed5204f10e33b92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:43:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:43:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:43:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:43:20 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:43:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:43:20 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:43:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:43:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:43:35 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:43:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:43:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:43:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:43:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4374cefdbacee456d8ed008c1f311f90f13f2b652def32ee01d354d19f349fd7`  
		Last Modified: Thu, 09 Apr 2026 23:44:03 GMT  
		Size: 90.5 MB (90547745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d59642ff6b3f4843ab38e54ef273e79b74047cc6de6059b75170953258b45f1`  
		Last Modified: Thu, 09 Apr 2026 23:44:05 GMT  
		Size: 19.5 MB (19466783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071cb072674d18c110a4955441ee92639783916d21ba03efc67d8ae34586567c`  
		Last Modified: Thu, 09 Apr 2026 23:44:04 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87f09fa3b216f62d7af1cdc7f0009e1348d50ba1b2f5896f2b8bf09ff1fcdb8`  
		Last Modified: Thu, 09 Apr 2026 23:44:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:41dd5c4ef70062fa05a48ca3403105fc4713d38c04949aa4f053088b9949024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4243895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ac5d6c33d6c8dd7adf0a1ee46e2efda2b725c219af87f45c13981a25cd86c4`

```dockerfile
```

-	Layers:
	-	`sha256:4317b3b6a604470cc8ed45467b084f39c87667d090f157930c4b09033fbb6c8a`  
		Last Modified: Thu, 09 Apr 2026 23:44:05 GMT  
		Size: 4.2 MB (4224885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89826f7f1bbeb86fbe380b375012d81b65647229c28ac3dc1e673e1f3b4c6b6c`  
		Last Modified: Thu, 09 Apr 2026 23:44:04 GMT  
		Size: 19.0 KB (19010 bytes)  
		MIME: application/vnd.in-toto+json
