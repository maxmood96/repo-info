## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:ce1be5af504e5019e2b00fb9b03a7a3ab0ac2c335c9224ef2357de4aaf039b9f
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

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e023771f59d98f90f62930f94d936f69c3b09b1887de2b82379d7e0fce8409e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208682856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65859b0379585cbb11b22dd04dd073575ee1c9442fb2b3ceea33de97a1ee776`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:30 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:30 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:19:43 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:19:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:19:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9bf80f0f81bc817aee7303f33a50fa3cf8a5a71e42db5852a5478f39bef653`  
		Last Modified: Thu, 11 Jun 2026 01:20:05 GMT  
		Size: 158.2 MB (158166966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309f6e7c04ba89e38ac954bfd368d6bd36bcd90e457df7181018ae6ad7f35948`  
		Last Modified: Thu, 11 Jun 2026 01:20:03 GMT  
		Size: 17.8 MB (17760098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f96effafbafc33c277d09f767fd91337837ab6687999e52dfecc8157534c92`  
		Last Modified: Thu, 11 Jun 2026 01:20:02 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9eb751d72b34a35a07c8dd4303c2fac8bd21d33539a3b1eb8c38d78495eee3`  
		Last Modified: Thu, 11 Jun 2026 01:20:02 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eca474eb2d08168f78f292905325900baa62db7772ff90d5c9f99b21364e6a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea245ddbda65941ee010500a29accacbfbea925dbd6bc3338838fc797db3a34`

```dockerfile
```

-	Layers:
	-	`sha256:bee1bd2fdf56487ea4b44b4c2266610d096af81ff8fee2bab72177663c4a1e08`  
		Last Modified: Thu, 11 Jun 2026 01:20:02 GMT  
		Size: 2.7 MB (2732565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b44296f9ac7b2e5da821d4b62ff41424fe6c99aed304d27e341a74ee7590ee`  
		Last Modified: Thu, 11 Jun 2026 01:20:01 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83b9b87dcd7fc40a6affe5976dee039d6d9993c5d789353173139f458c310598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206695823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242c4118543e90ae258f0dadc30b5879381d4082f86f4c0760c21ab4ffa70249`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:20 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:23:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:23:20 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:23:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:23:37 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:23:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:23:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b584a7b7da38e9fc408781fea6f36ac56007a7cfcdde7add5e103b699a84d20d`  
		Last Modified: Thu, 11 Jun 2026 01:24:01 GMT  
		Size: 156.5 MB (156461323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0107b5d75ffd464c931413314f970259c47af0f1d8ac0d2f4fb5e6dcd0411b97`  
		Last Modified: Thu, 11 Jun 2026 01:23:57 GMT  
		Size: 17.6 MB (17594012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7afa7e7c94fef9be3ef63edcf08be7ba233e71be29fbc916cdad8fef36085fa`  
		Last Modified: Thu, 11 Jun 2026 01:23:57 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a97dc60c3c1d945bd5dccdb5209a28f898b276f9e82dc3dc543ad276a815cf`  
		Last Modified: Thu, 11 Jun 2026 01:23:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa3d7cec2284e4f925661ab8ce0d4c110eec6855a4c441880aa9a56df118551c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e84e4138b8b3d650b7f59060de5fc3dbc79652bfed732feea9c563634965d`

```dockerfile
```

-	Layers:
	-	`sha256:abfa2daf40c32bdac535b4703bc8e5239c771f32fbfb41a021e98ee088b6cf07`  
		Last Modified: Thu, 11 Jun 2026 01:23:57 GMT  
		Size: 2.7 MB (2732180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c8a0a8db3994f72c597999e446350a80a2359117376bc025eb9b3441a57412e`  
		Last Modified: Thu, 11 Jun 2026 01:23:56 GMT  
		Size: 18.7 KB (18677 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f98fd02e8ebd72370e05b3494c144507e155aab1d13fd9593bef99270b4e36a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212906933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6252a942231febb20fdf929b9c5bd85e08e464c5fb68c9d01d28d07a70bd9aea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:36:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:36:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:36:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:36:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:36:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:36:59 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:37:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:37:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:37:29 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:37:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:37:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:37:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:37:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce7fc17844961c443ec6ff9fc6852d7315d0c5de57330a5cd0dd3369a5a4e22`  
		Last Modified: Thu, 11 Jun 2026 09:38:13 GMT  
		Size: 158.3 MB (158343198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80a95b508789a3d01ab70781cc7e2f715de0726b87d51d91d51f1382aabda3d`  
		Last Modified: Thu, 11 Jun 2026 09:38:10 GMT  
		Size: 18.0 MB (17963624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6babc52f25e93e74a8f3858cff72aac09285b3a116de0fa4d7484eeb559205a`  
		Last Modified: Thu, 11 Jun 2026 09:38:09 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bb9a6c80fb5e34481be9e270c7075ddb79236d13799ee214d6dfd21ac89365`  
		Last Modified: Thu, 11 Jun 2026 09:38:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9766d5883c8c59f1d019357e23dfd179793e3c5bf7ce97abd929116e6703b83a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97d4eaa4617ab2229bcb0a2c1ea29e912d06892299bca1390961150ab9f2d72`

```dockerfile
```

-	Layers:
	-	`sha256:085e2c3d67c8bddbde58b95015bb26548cfa132eb12ed776aa74dd1ce7e8ce13`  
		Last Modified: Thu, 11 Jun 2026 09:38:09 GMT  
		Size: 2.7 MB (2734398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe01f617f43183d4d16a5dd3a55d35f28d80dece567aa5e141df2b9834e6222`  
		Last Modified: Thu, 11 Jun 2026 09:38:09 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:46a80e91f89531284a6433a3ea9bc99861b828959341d7c1453e8614e3555cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196224018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fe1ffb2e2e442837461a66562fda54955203f71b7bdcda6172069198c25a6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:11:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:11:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:11:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:11:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:11:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:11:05 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:11:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:11:16 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:11:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:11:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:11:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:11:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315e35399e5d4547db2084583fbe80262cce5f385bc84081f625e7edec4d8b6b`  
		Last Modified: Thu, 11 Jun 2026 03:11:50 GMT  
		Size: 147.4 MB (147388354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef5de69b664cdde7f301a8693ac3e46944a8164fb26aa41a2c727cbd5a55bd3`  
		Last Modified: Thu, 11 Jun 2026 03:11:47 GMT  
		Size: 17.4 MB (17424004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e511ab3a61a82d6fbb0f317d14c9a0fc5234edb5ab1887b9ddbbe1a67f96ef`  
		Last Modified: Thu, 11 Jun 2026 03:11:46 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9851de999f82a715221ab4209ce3fec4501c3f0cfc5eade04159d15fce42a945`  
		Last Modified: Thu, 11 Jun 2026 03:11:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:50afb9328f06ba65e3dda722259f1deb9aa717bde399f473c74298ccac3993f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d75e56d6e2971bf8c78d3f21a2a413d8acb97b148b9e6fbe3af319f93ed9c5`

```dockerfile
```

-	Layers:
	-	`sha256:fc991e662021220025f081b42f01b7b90ac8b746b6d72dff45dbb52ff160035c`  
		Last Modified: Thu, 11 Jun 2026 03:11:45 GMT  
		Size: 2.7 MB (2724379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19213e7ac201b0775720266b55c54fdb62ec109422152009eabf2900efec628`  
		Last Modified: Thu, 11 Jun 2026 03:11:44 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json
