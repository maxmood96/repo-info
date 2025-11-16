## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:3d1f35ec04a45eb926c462c7e2a3af8716eec9e488a4884a7691f9040c37b9ea
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
$ docker pull clojure@sha256:2ddf10da34a080ce5006fff9527040c1696ec4b3a0a03aa74934a08ccf4e4529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217230885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fb2f1e9fecc18694dcd7f8afee3e95c4345d2765ba39a74f7bde4bdad4e832`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:52:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:49 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:52:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:52:49 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:53:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:53:06 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:53:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:53:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:53:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:53:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1bb44c1f21d7784190b27e2c46bd3e6cf424d43e2e49aa63fb993dbbe89b8`  
		Last Modified: Fri, 14 Nov 2025 13:21:25 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97eff72b8679759f3cfb0251b5783ed136e81d5b164c77a34682f1f6513685c`  
		Last Modified: Fri, 14 Nov 2025 00:53:34 GMT  
		Size: 18.6 MB (18579166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432086bcddb7a9dab8de032493a3ea1eb53ba6fb48814171be0b0dca94b01570`  
		Last Modified: Fri, 14 Nov 2025 00:53:33 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b330dfae3e6eb5bd1d77aac0f8bd4191d3f50b920f505f0f80639635e2617e0`  
		Last Modified: Fri, 14 Nov 2025 00:53:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c63fe8017238f702c2f321aa378244e67893de206544e935db291278f61a121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a128b5e52d02fabab92329010593aa57fdf65576c1bd55dc34e9a4b89787531f`

```dockerfile
```

-	Layers:
	-	`sha256:f9bc08e318835600c6e0e1d6a296933fb3c8d67d59654fee1f4d8c7a2b1db78c`  
		Last Modified: Fri, 14 Nov 2025 01:41:01 GMT  
		Size: 3.8 MB (3813386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9f0ca9ccb97b59ad062e262229129e351609b5afe5132a11b4fe6239e0d3213`  
		Last Modified: Fri, 14 Nov 2025 01:41:02 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7d5ede8638ac7ecd45f69e697bd8bb235667b120d9b65fa8b8039526de4971c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216388455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb8b17228f72c25c54980f7f41ce24f1ae0bc9f36a46b3c3dd79a3f4a57bf5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:54:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:54:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:54:46 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:55:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:55:03 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:55:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:55:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6fb49782195a5e2a219b5a311f3fcb9917fb2e730cc36c450f0f271c9eb8b6`  
		Last Modified: Sat, 15 Nov 2025 09:42:40 GMT  
		Size: 143.7 MB (143679910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c63d075a072b7fc0dae6e8bf17213b962a1f43d813144686309ba26896c0d7`  
		Last Modified: Fri, 14 Nov 2025 00:55:35 GMT  
		Size: 18.5 MB (18539931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6315f9499a3a14295bc6aa5e7617e0ea8ceddf0e7b5b2e29c21dc5ffe8386e8d`  
		Last Modified: Fri, 14 Nov 2025 00:55:33 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7185a36fee84d0587ab339fa31a6d9cbb12e9a272ffb83134497f01df610b8ba`  
		Last Modified: Fri, 14 Nov 2025 00:55:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8d413ce338fc958541fe75a6ed0df5122c3d64103ebffbd67878259fbc021c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c317ff300332f3232e06790b063c880acd3ee4e3e808e32614792fd6d5c87af`

```dockerfile
```

-	Layers:
	-	`sha256:0edbe00065bc1d1343168b5f3787506a3d2c3acda02b6e9df12f14fa56ae71dc`  
		Last Modified: Fri, 14 Nov 2025 04:37:34 GMT  
		Size: 3.8 MB (3814263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7580e19a3ea46bd7370d213d715338f50864308e0836ada7e211565d4c152272`  
		Last Modified: Fri, 14 Nov 2025 04:37:35 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7f95201214a412cd2a7d1d87f3fc12ff3740d04a195d97a291a85b2978695ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220790085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d5dd8261239e225711ab5d7405cb0496640eb595b86f9e2069b68d8ef68acb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:04:12 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:04:13 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:04:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:04:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:04:46 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:04:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:04:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:04:49 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:04:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006adae81b39e8c2eb6c4f5beac67c9c4f256bd536a083ed9b0394d34fb5b0c8`  
		Last Modified: Fri, 14 Nov 2025 07:05:33 GMT  
		Size: 144.5 MB (144525223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25387b939483973118e02d510b6e859fb0f2c6277f19335800912203165f59a6`  
		Last Modified: Fri, 14 Nov 2025 07:05:40 GMT  
		Size: 18.6 MB (18636586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c932f9aef75fa56e9cc705fcf15fddf2d536fef59a4257ea35c34892d0253`  
		Last Modified: Fri, 14 Nov 2025 07:05:38 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c9ec0986f3d624d5ef8c14c7522d41a7244d9b8bf22d2d779d353995e66932`  
		Last Modified: Fri, 14 Nov 2025 07:05:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dc10a76dd70eea76c2cd8bd6faed412ad29376bb56c6f3069259c958685035b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6320b2da4a313ad22e77487eccbfbb670af4a2b7f713a69125cb220334ec86`

```dockerfile
```

-	Layers:
	-	`sha256:14e2ed137d98923e5da5b16ede142875d48fa751d05497046515f0afbb91266c`  
		Last Modified: Fri, 14 Nov 2025 07:37:33 GMT  
		Size: 3.8 MB (3814384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d3dff53f9fc611e848cbc85a0f1a74aa01ba1ce5d74cab6759de4b3f3f1fe45`  
		Last Modified: Fri, 14 Nov 2025 07:37:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:6f0c394660dbe82ae93af78e6b04d2684ea3d095c312618a09b16078e7535fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215860974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c367b640f2ef9027ba369e7d6133dcc3b12dd62a2d86ba96282306c792d3208`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 21:00:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 21:00:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 21:00:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 21:00:17 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 15 Nov 2025 21:00:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 15 Nov 2025 21:00:17 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 21:01:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 15 Nov 2025 21:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 15 Nov 2025 21:01:52 GMT
ENV LEIN_ROOT=1
# Sat, 15 Nov 2025 21:02:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 15 Nov 2025 21:02:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 21:02:08 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 21:02:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734a358c92adb84badd879c1e293b2d1f8f6cce639f35f64ee300e91fd4043b4`  
		Last Modified: Sat, 15 Nov 2025 21:11:27 GMT  
		Size: 141.9 MB (141889560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4fea357272ca50036d27a1a9eaec5beea28568d79506a859a31f042de9b8e0`  
		Last Modified: Sat, 15 Nov 2025 21:06:34 GMT  
		Size: 21.7 MB (21682261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866708d8d09eeafef1773c534c62e754b1de967ab03d3601d3ba5475f5a75faa`  
		Last Modified: Sat, 15 Nov 2025 21:06:33 GMT  
		Size: 4.5 MB (4517798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba723f2ceca17dcb9df3a3eee4195370d3f147ebbb2d9ce918867d2a3e9ff3bd`  
		Last Modified: Sat, 15 Nov 2025 21:06:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6976b99426d502bf6cb9eae818f29246e09860358ae807c9f962c612d3370475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c6b41faf336991c99680a0cc9f81a0d6a07d45c9c00983b599c224392d4d0d`

```dockerfile
```

-	Layers:
	-	`sha256:a5f0cc85052a3486343e3e0b99c368c46a04457b3e91202eae711bff3485298f`  
		Last Modified: Sat, 15 Nov 2025 22:35:33 GMT  
		Size: 3.8 MB (3801936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fd8f2cb83798a3163734d18992a67fdd6de0f2c353ea549e41a19f2bfe62958`  
		Last Modified: Sat, 15 Nov 2025 22:35:34 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2cdad7faedaff4417320cba74b59291e25b258e15f7b1c9f34a5f4c64da0ed6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207349762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4ff06c42d61399cedd38b2eb043d5fc1f4933c24e6bd007c0af4c321fd0700`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:26 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:56:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:56:26 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:56:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:56:38 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:56:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:56:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bff8e87cb45b3d7167fb65b8d0c1a1a90dcf5a9a1a0b85730e1a46f7b11588a`  
		Last Modified: Fri, 14 Nov 2025 00:57:05 GMT  
		Size: 134.9 MB (134859047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76982e83ce99784cdb736c6ef43125a42d76cd5c2b0f1b2b853e31280146e08e`  
		Last Modified: Fri, 14 Nov 2025 00:57:13 GMT  
		Size: 18.6 MB (18620237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbad305897c1f98da68e9c9d41783f18a6c23d223d8419f59e90a2b5fa357a34`  
		Last Modified: Fri, 14 Nov 2025 00:57:11 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d5f7a8b13f65cc36ee30b318ebb62c069b6d0a392181e4c29d2bf51984347a`  
		Last Modified: Fri, 14 Nov 2025 00:57:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:af1eb8d194d22e45120e906898c3ff9091496d64a942dca2ccd70c4de409369e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55f72ac74b07582080bfe19a87752f49b82200f09b9ddb90297299b07af9b7e`

```dockerfile
```

-	Layers:
	-	`sha256:0e99dfe1ad5d083b0be5deb0b828046f692eba033cc091073480373a2c7d9e82`  
		Last Modified: Fri, 14 Nov 2025 01:41:18 GMT  
		Size: 3.8 MB (3809813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9e24510034ca222ef4b12586692beabe1d0daead5757439c6adc70ce6369a22`  
		Last Modified: Fri, 14 Nov 2025 01:41:19 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
