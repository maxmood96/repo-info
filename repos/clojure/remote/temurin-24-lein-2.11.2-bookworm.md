## `clojure:temurin-24-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:0e5323b22fffa7b47c33dadcf8291426a0cbc85e36d4865c08aa46e2c9077897
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

### `clojure:temurin-24-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:168cfbff764730f88e67ac71ebd747c5e6d3088e5f6e032699e59e44d5fe2a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205026079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266976c626a8ebeb09c00f9916c4d7d3fde01c59184e2c79070ad1153d34623f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a64631b9b4737c7d634dec48c422a3a2349dc5e4ce3ad7c2e1a2273fde4bbd8`  
		Last Modified: Fri, 09 May 2025 13:15:11 GMT  
		Size: 90.0 MB (89951991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b418e643e3ffd6920eec2a258cd3dccf09e1a9d1d4ce965a9a483e90c2d87e`  
		Last Modified: Fri, 09 May 2025 13:15:17 GMT  
		Size: 62.1 MB (62068310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634071ced12223fe93436f0bff863e473225ee13b93cbef7b9e07c1caafa37ea`  
		Last Modified: Fri, 09 May 2025 13:15:06 GMT  
		Size: 4.5 MB (4514151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1be8cee2e8deef123aec7f2ebdf5e91a2cd875724ee707a28c5dd3eb2e44ef`  
		Last Modified: Fri, 09 May 2025 13:15:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6c066d28f388f2d5e37421aac0967ddc2e0f0c8dd33159f3777238f169e90dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d12cd200ccebe4346b857dd77f5ecde8309e58e8f1a6086636446c92ac6e11`

```dockerfile
```

-	Layers:
	-	`sha256:eb25b147b53c8a37666f64825495682e802ce24c1a6f19778d5b5a2f703dab36`  
		Last Modified: Mon, 05 May 2025 17:08:01 GMT  
		Size: 6.5 MB (6486939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd90d6c8569acb27c60b4c9284e9c1b0cb105a703d53af6b3a16c8a44fd15a4`  
		Last Modified: Mon, 05 May 2025 17:08:01 GMT  
		Size: 19.1 KB (19066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8aa5947a2a16e6efa17ffeaed51c18199ece7968f327a0c36b66af7ed07d9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203969060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411014632d55a14af2dfbc95f6f375ddb5a9023a9092c91bc5cc9f7b549e4723`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289d29a9fc32a83e7866e7172e5148e804d7fa6b5e264bedd1edcbb3907d41e8`  
		Last Modified: Sat, 17 May 2025 17:48:01 GMT  
		Size: 89.1 MB (89091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f207d52eaca656e1e388d7f8915c95a41fa3060d8cd6723a06c6acedba7a01cb`  
		Last Modified: Wed, 30 Apr 2025 04:50:19 GMT  
		Size: 62.0 MB (62035563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a2b14ba3594a3b68b3fb43eb5b5c9f179b43cc3ab6f0afb8a98c87e6b0f945`  
		Last Modified: Wed, 30 Apr 2025 04:50:17 GMT  
		Size: 4.5 MB (4514190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666cc9ed956d464f3073cddd7eb59ce9d32ff9e26569354967956b00552619be`  
		Last Modified: Wed, 30 Apr 2025 04:50:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d6775c1901d0d1b298ddfebe49146d634c49ddba30b45aac36884664cec11885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2064c2ac9d713ee3010ac850391e8315daa86518f23d91efc0871584b7f9efb`

```dockerfile
```

-	Layers:
	-	`sha256:72f70fdc4ef48c2315ca0329ff619bad1f3f92dc1d2286ab7940d295cc9ab66b`  
		Last Modified: Tue, 06 May 2025 00:46:57 GMT  
		Size: 6.5 MB (6492654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277a0b5412b8d29c39386e9339babb8db11786bf9db628a64578c53b54895412`  
		Last Modified: Tue, 06 May 2025 00:46:56 GMT  
		Size: 19.2 KB (19210 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cb427a98e0a03de1d69062a98837ef74ea51e7dc69b8f89f28f334e360639d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214071794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed1f9b9338fb617b2bad8644f640a423ffe34c86345f0879fb29e77cf347b27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667e2c75575ea3101085eedee6465ccbd4328518899a2687f5acfacb51334a63`  
		Last Modified: Tue, 13 May 2025 19:30:24 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757a298d8d04038019a6eef7d797eea52bd7679b889d6d64231680b2475bd0`  
		Last Modified: Tue, 13 May 2025 19:30:23 GMT  
		Size: 67.3 MB (67304827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400da0653ff02a19abfd50543de64e35c163137faa1560a07835dfa599265f17`  
		Last Modified: Tue, 13 May 2025 19:30:21 GMT  
		Size: 4.5 MB (4514164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002cddc8a0b61656fb41d9fe6e6a4fef9cb2f97cf205c4db9d10b92d1d81013`  
		Last Modified: Tue, 13 May 2025 19:30:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:52dd2a3a5952c1754874cb1ee92f796bcd545c584badd39065ce002eef70d846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6512093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9748cdce957a3be41948c412f8e015afc05d82816e8bc7c5f90cd2511cfe9ce9`

```dockerfile
```

-	Layers:
	-	`sha256:845ec3303a2c717463d79555cc47e94a6f9dff5184801c48a3da14a6d2d18d71`  
		Last Modified: Tue, 13 May 2025 19:30:20 GMT  
		Size: 6.5 MB (6492972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfcdf1a62ca3082c0e81a08088a0adcfa14149f8cd449ea75333ac556b32798`  
		Last Modified: Tue, 13 May 2025 19:30:20 GMT  
		Size: 19.1 KB (19121 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d3e6bc09ef98fc79cacf7750388bd5f84b372a92c6daa9c6a087a4489ce3eaa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197963220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d543639ee7242b730b1f8640d0780586c184860ec19f9e6400ec2287ea6edd44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5543a7e7f181a87f4b54a4806466f043c954887fbd8349c3543edf7cd2f7ab`  
		Last Modified: Tue, 13 May 2025 18:34:02 GMT  
		Size: 85.2 MB (85216805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54854578a2a71a7a24f30e5551700c767d7851e8966eecec28a02f9c1146a20b`  
		Last Modified: Tue, 13 May 2025 18:34:01 GMT  
		Size: 61.1 MB (61080493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691c05593b7126e42e1153875b6ffbbde1a20f6ea08e7b1ff8f1b91b75039c65`  
		Last Modified: Tue, 13 May 2025 18:34:00 GMT  
		Size: 4.5 MB (4514162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f96da5a3671329032c7f98f6f55df1f6af27d7f4252d9b40df69cd0184932d`  
		Last Modified: Tue, 13 May 2025 18:34:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c30bf067e8b5998fcbe2f57bd9e65150a5192dcefc47b72604ff5417c436de8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6502821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20304de31f546b801c6641da15aa2a87c54e9c0cef18342b6067c3dbcbab02bb`

```dockerfile
```

-	Layers:
	-	`sha256:9c98cb0092b7fb16e98a82dc5b44a4a589e216890f318add0a5a618f28bd62c8`  
		Last Modified: Tue, 13 May 2025 18:33:59 GMT  
		Size: 6.5 MB (6483755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1765c813bd0cb531d72197ee0da368796c8a1c063a16eb871a13f964fc715338`  
		Last Modified: Tue, 13 May 2025 18:33:59 GMT  
		Size: 19.1 KB (19066 bytes)  
		MIME: application/vnd.in-toto+json
