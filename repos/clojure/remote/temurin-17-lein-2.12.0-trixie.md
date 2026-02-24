## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:e354460c369e6b0b3fdf11be558d88fe5fc2175ea9dc8babb997d7f345378a3c
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

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:72144f70c434d4421a086130143278ee28c7bca88caa3b1ea0e214f26fe8f629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218020085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cf3ba6da264cd516f5a8d4df8d1e23c88f539197fd756b27fb2e668cbbca02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:54:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:54:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:54:46 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:55:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:55:03 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:55:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:55:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f0edef257c8c842b866cfc907940e04cd19ad7cf850494eb3e85f93d2987b`  
		Last Modified: Tue, 24 Feb 2026 19:55:24 GMT  
		Size: 145.6 MB (145628796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b911f199ab8eb8a9ae0bb5aac0e98419ffb772ba1c9aaabf1f4295d0a77d193`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 18.6 MB (18580036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b91d4c0a89f49761f4c348c5e2e2458b225319a5deff23bad4fb1e838698dc`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9569c00ef5b60ed580940da297ddc62c7aaeeaf63d5bd3b0a8f0b5977ab86`  
		Last Modified: Tue, 24 Feb 2026 19:55:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:acb84732378083d797bedffc8cf9acbbd4c59be05ead395891b4be19336c6e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef984bea92b0a3add40a879d48dc7755bd58a9f535105236f28c0740b9092f49`

```dockerfile
```

-	Layers:
	-	`sha256:f48fa37ba3dda1358a35eeb01a2afda7e777faa4acbd3f6f5e28bebf67dced11`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 3.8 MB (3815491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304f5cc96f46b9993bd091306d6ef2a4ceb271db6308c8249c1dd14488c5c47b`  
		Last Modified: Tue, 24 Feb 2026 19:55:20 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:252b4e48fd1cd0b3a026a45e00291ef236dda5a7058274b89b6c75f27defb648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217148009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51330f0d349f60c6b748c91dcc4ffee4760ddfe2d86470a03b634d23b73bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:05:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:47 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:05:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:05:47 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:06:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:06:03 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:06:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:06:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c2742c5137d1adc9a98d2d04fc2af2b324f40c2bb44d64cf745d7fc28fbae`  
		Last Modified: Tue, 24 Feb 2026 20:06:24 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dee45cef3262b7948c8da646e53cf28a278bdeac60cab7dc6424069de9dcfb7`  
		Last Modified: Tue, 24 Feb 2026 20:06:23 GMT  
		Size: 18.5 MB (18541452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d90ffd6ae13293757b4d4eb89d640ffa62c92afa1c18e2bf411a496f4c8dd77`  
		Last Modified: Tue, 24 Feb 2026 20:06:22 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7018f407f4e9adb724f16fa226c1e66a3ffb7a399f7a9af3e7d5575d3c231c48`  
		Last Modified: Tue, 24 Feb 2026 20:06:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5f7e7ac9c742169717b17a4daaddf130ff51f13e55199c930376308ffd296743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e136f15ba7190c1152659090f98b64c77ca04c40e62e7ea3e24d5a64690f9a`

```dockerfile
```

-	Layers:
	-	`sha256:10f60057bf6c2ef4eaecdbd0d645cfdf93b0186d6c6dac88c6dfbb7d58c1ceee`  
		Last Modified: Tue, 24 Feb 2026 20:06:23 GMT  
		Size: 3.8 MB (3816368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:720eb6450f84d59b32efcbf353e6409574a380d16c36e10f563dfe9939dfa628`  
		Last Modified: Tue, 24 Feb 2026 20:06:22 GMT  
		Size: 18.5 KB (18472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2770486bd813f0d657529a13729e7547b48a2cdd42d5c3996aaa1bd273919d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221706088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc128e926bcfac7b20ec2fa88948a5489c0d82717cc6cac446d3a7c10a09bd4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 23:48:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:48:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:48:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:48:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 23:48:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 23:48:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:49:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 23:49:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 23:49:31 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 23:49:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 23:49:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:49:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:49:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b4cabddd66d71e97ccb04d7861e4511a418edbd43a9f1a73ba473b7207138b`  
		Last Modified: Tue, 17 Feb 2026 23:50:19 GMT  
		Size: 145.4 MB (145438194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a74da1d38ab9fd424c68a3e12f25ddb974d600c82927e9d6f53cb4cbacb586c`  
		Last Modified: Tue, 17 Feb 2026 23:50:19 GMT  
		Size: 18.6 MB (18637590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dddb11a310826ff78ec40c1c76fedd30191c74df8b23a172303d77aac01907`  
		Last Modified: Tue, 17 Feb 2026 23:50:19 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db724ba36ce43906b94d09b1446b7765819f84bc32b54e5f91d93c69ef6b555b`  
		Last Modified: Tue, 17 Feb 2026 23:50:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:135f8d26ad735dbcbdfacf69a9d889ed077969cb5cda61727b8baba94d9395dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4db223a4492c980afe79a73c31ff852db0055d9cc4afe6e81e23f51f778556b`

```dockerfile
```

-	Layers:
	-	`sha256:07cd91663338c1f3be24f0e4ada30dc432abc3473e9ed3fa6a02faceb1b0ac12`  
		Last Modified: Tue, 17 Feb 2026 23:50:19 GMT  
		Size: 3.8 MB (3816491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4dfd65f16907087cf9ea396511bce3394e9c08291177a01f8b8e9944bc3a9e`  
		Last Modified: Tue, 17 Feb 2026 23:50:18 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:38e0812d23c6f3185b5dd6020d06c3ef968c149e76d04036e769453c62424973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213489851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d86e5b8f82e6e3a1cefe4c805338f0d34b9e74e2f3426732ef6c053a03fadf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 10:19:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 10:19:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 10:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 10:19:58 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 18 Feb 2026 10:19:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 18 Feb 2026 10:19:58 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 10:21:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 18 Feb 2026 10:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 18 Feb 2026 10:21:36 GMT
ENV LEIN_ROOT=1
# Wed, 18 Feb 2026 10:21:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 18 Feb 2026 10:21:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 10:21:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 10:21:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a68b91c900b38b25108404deded7395508254e83b0954c22570460e94fb1a34`  
		Last Modified: Wed, 18 Feb 2026 10:26:05 GMT  
		Size: 142.7 MB (142663031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d6e0b729d3a86f02b8b31a1f26b3d36eea3445f79eb991c2271feec6fd66f5`  
		Last Modified: Wed, 18 Feb 2026 10:25:48 GMT  
		Size: 18.5 MB (18531833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f01918d8ea040e2962384ebf14403fa16d4431a8f6229ddb5dc16b4489726a8`  
		Last Modified: Wed, 18 Feb 2026 10:25:44 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a67ea175a977c6c65ef32e56c70e39eecc8e2d11e4f1bf0dac884af26b17662`  
		Last Modified: Wed, 18 Feb 2026 10:25:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6c619c92399ca0fd0506132dcc5a8b75621090a7991e20e0ae2932180f8b5b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663b7c19edcc5f446a4ec60341d427684db6160e3e3457ebb73abdd75a2ca208`

```dockerfile
```

-	Layers:
	-	`sha256:a81867f5019f1c99c2de76642498b58be7a67ae1b3779e107520b9c733bf6388`  
		Last Modified: Wed, 18 Feb 2026 10:25:43 GMT  
		Size: 3.8 MB (3804049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d920d152e94580043fda5b0237348bdd5baf3463c255ea068e81d6541b95a6`  
		Last Modified: Wed, 18 Feb 2026 10:25:41 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c0bf3ad7658d13389b3de7ffa13335842345408da58e8c481ca241682b7658b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208120968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5167c5b34d414374026d6e91ff2ee1852ef1b5c2a862bae1e0c0df2e6b0c4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:07:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:07:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 22:07:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 22:07:21 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:08:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 22:08:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 22:08:05 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 22:08:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 22:08:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:08:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:08:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094f54d5460e31ea8945cc291a2d9832adafb12b5a3dc29f5a20e3454ee7fe79`  
		Last Modified: Tue, 17 Feb 2026 22:08:46 GMT  
		Size: 135.6 MB (135627116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030d65bcc4da58bff18af73306c8848677fd4b261af862fa742e0693d82633bc`  
		Last Modified: Tue, 17 Feb 2026 22:08:46 GMT  
		Size: 18.6 MB (18621296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f497e721b584d1aefdd7be08832a35877b182028ab0a2191bb5ac83c3eebb4dc`  
		Last Modified: Tue, 17 Feb 2026 22:08:45 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69df11e74b8801046460c8fbaca61a87239e1a95e78d105fb582e8823b0cd918`  
		Last Modified: Tue, 17 Feb 2026 22:08:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f18ef0b0b4191cb4fe97f74c80991b24b9e0a1973f156f7c424eb5ab1fb26d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195414f38cefe841649952e1425b894775daf0fbefd5ca555fda80978b3e2008`

```dockerfile
```

-	Layers:
	-	`sha256:2f3c0431c9beb0dbcfab6311f0b0b5eda077ebae2cbbfc27fcc7bbc37d769460`  
		Last Modified: Tue, 17 Feb 2026 22:08:45 GMT  
		Size: 3.8 MB (3811918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787e46bc48f2cf4d70bf98c760be3d9d02f965587d78755846807c89c9403d8d`  
		Last Modified: Tue, 17 Feb 2026 22:08:45 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
