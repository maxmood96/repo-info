## `clojure:temurin-24-lein-bookworm`

```console
$ docker pull clojure@sha256:3f874d644e7eeb87c61cdec3a9c6174c49a9d424dc25f878e48cde2474ad0040
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

### `clojure:temurin-24-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:15c2e690f3043d26ada5eeaf5b9148a5165f8cb315e6406e986aed56c5902485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205032598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571d4c78b3126d7b58b05a132dfa420521300ef2384cbcbe0f7de4ff4657b68f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02180bad3221bc5bbd6ca1c5b0859d35853456087347bfa826d66f318ede5e8`  
		Last Modified: Tue, 01 Jul 2025 07:15:40 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af814c54c8dbd91943c706158e9d5dcbc2e4ebf2831a526daff5a5bebd1d8400`  
		Last Modified: Tue, 01 Jul 2025 13:32:51 GMT  
		Size: 62.1 MB (62071734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24281766dcc050b220ac0b69032f67a4306b045f03a489238a4af9933f68a4`  
		Last Modified: Tue, 01 Jul 2025 02:45:51 GMT  
		Size: 4.5 MB (4514148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e247271fafead6b245a24dc1fae7546dc33b240b3c2b78a1df4837a4d5a115`  
		Last Modified: Tue, 01 Jul 2025 02:45:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:275871cbe987e024a27d71190e1d77e4e022ca5be84f660131babb3c5a6196f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f2365d1004c83c55886bbb723e97ebd2b898e5f2cf1a205709b716abe3971a`

```dockerfile
```

-	Layers:
	-	`sha256:5b3150fc805c464f760372dfb787265b4325591bb13cb607db1a23de068199b7`  
		Last Modified: Tue, 01 Jul 2025 06:40:32 GMT  
		Size: 6.7 MB (6654017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a253f87b312bc8acf85a5217962eba117610f6bfac4572f407bcc3cf8b8b239`  
		Last Modified: Tue, 01 Jul 2025 06:40:33 GMT  
		Size: 19.1 KB (19066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3131fd0bbfc531ff80fc3345d54f3669d5eb29a7c9107459b1da9405f57f8314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204002202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c83a3fe1f834fe2be7d684fc6c8879e6fe45683a9fe916db21175190a8bc7e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068915118494f0a1e3d96ea0ed10f769bc409d86b4869da7d353f2b54f9fcd84`  
		Last Modified: Tue, 01 Jul 2025 12:36:35 GMT  
		Size: 89.1 MB (89091279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d93e8614abc6ce7aa9c627525b9cbbfea0841b8ba72d721e41635475acc8e0`  
		Last Modified: Tue, 01 Jul 2025 12:36:34 GMT  
		Size: 62.1 MB (62057548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf40c4bf8551605d62135b9f01461e447fd9944e9bdf7c37ded5a5f773240e`  
		Last Modified: Tue, 01 Jul 2025 12:36:47 GMT  
		Size: 4.5 MB (4514163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b3622d593dff9fa4ba6f6ecde0d001319db634e4383495fa0e654af1e12c12`  
		Last Modified: Tue, 01 Jul 2025 12:36:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:08f6a8a80adbc1183b248137809d9473fe2dbcad3795fea0e99906d330886fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b63349c8c81e446337524d78a2daee2bc85efd56384b97fcd6c4d93b0e17a39`

```dockerfile
```

-	Layers:
	-	`sha256:e3d90b236d13c8501ad481d0ec9e94bd43a3a28a96e5cb9d7c140a92ecd8387b`  
		Last Modified: Tue, 01 Jul 2025 15:40:06 GMT  
		Size: 6.7 MB (6659732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2befe80e80b8898c0f13f6293b6319de59866e9d4358ed5ecdb22cfcb3bbbe`  
		Last Modified: Tue, 01 Jul 2025 15:40:07 GMT  
		Size: 19.2 KB (19211 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:51fae9f0b43e65b59cefeff703c97a2a88da23c1436699f0d94c344a9799cad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214087386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:651cc2324cb7e737bcc7a8d922bc1629470ebfbeaa6a2e2d4c8c9b7bcfea30d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcfd6874f2794612323526d256ad677942a1f220ad172db56959f104717dfc1`  
		Last Modified: Tue, 01 Jul 2025 09:09:37 GMT  
		Size: 89.9 MB (89920248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae42bd2f54b72d251052056dd70a6931d57a85e660ae76aef9aa78eab36f97e`  
		Last Modified: Tue, 01 Jul 2025 09:09:48 GMT  
		Size: 67.3 MB (67315266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18139256be9cc07e78f6b384bc84b595842f88db0e4a67c54b48f4ed26c5cfd`  
		Last Modified: Tue, 01 Jul 2025 09:09:30 GMT  
		Size: 4.5 MB (4514200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d40992217ba3cbb49ea25a66e1f2f2854b704ad4e71a14f8ba7de7b33f9b32`  
		Last Modified: Tue, 01 Jul 2025 09:09:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d3bf65aa20c6032ed453ef30741d9410eca80fe27ce2df6cb15d4f2e0039f91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cce567d48765f6fcb432ecbf05d9425140de82906bdeafc246ce5f4c007b545`

```dockerfile
```

-	Layers:
	-	`sha256:7efe1d10ac0e7a7a8e01694b01ead266f055000ce991db965624040b9157bf78`  
		Last Modified: Tue, 01 Jul 2025 12:37:29 GMT  
		Size: 6.7 MB (6660196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bb4213869cc9f54c74d0b8175fe12483ba3effd4dc2733aacf84f4222ada6ba`  
		Last Modified: Tue, 01 Jul 2025 12:37:29 GMT  
		Size: 19.1 KB (19121 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8a6264ca00efa57f880bbedcb6d62c04d2b7e73e97aa0bdc19216dbaa0ec01ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197981619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7b214f88c1d563418cf72ffa5c31b12e700cd21103bdd47910cce5c9c11454`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ae874c9bbd580e7c558a716e38196ebb26f775bf28a7ffa76aa7fe9c1db98a`  
		Last Modified: Tue, 01 Jul 2025 13:32:54 GMT  
		Size: 85.2 MB (85216780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c05a7013661158b8faa89a77b4757c74a4337a97165b487f0b1f60b7724c66`  
		Last Modified: Tue, 01 Jul 2025 08:25:40 GMT  
		Size: 61.1 MB (61100960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cc0b1c447d13d623cf85bb1386abe7897f4c6f5f4e88266f8b9e32bc2420a7`  
		Last Modified: Tue, 01 Jul 2025 08:25:02 GMT  
		Size: 4.5 MB (4514164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ab2f573db9bd9758a1723ee3496e3f358a9312a583cf8f601f8c94b87fa14c`  
		Last Modified: Tue, 01 Jul 2025 08:25:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ed1da176bbff9838528d604d49dce8a227c76cb84028aa4a98a167e32356d564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025551e22142f565f033144bdc72d81326151077dbb82b0c71395bbc69f19740`

```dockerfile
```

-	Layers:
	-	`sha256:0acf242d196f63b9ad528ee0733c4c0042dc8258d0f6b63516b8c11f9f2adccd`  
		Last Modified: Tue, 01 Jul 2025 09:40:50 GMT  
		Size: 6.6 MB (6647941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711960fae0518c2e4f4a1ae496d811dbbe40bf04b5b2bff32e3cf0c701ba2cd5`  
		Last Modified: Tue, 01 Jul 2025 09:40:51 GMT  
		Size: 19.1 KB (19065 bytes)  
		MIME: application/vnd.in-toto+json
