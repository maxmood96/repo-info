## `clojure:temurin-24-lein-2.11.2-trixie`

```console
$ docker pull clojure@sha256:a54951c95565450c4cc7aae062dcdb552e748ac224a54a41ed942da638f34a68
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

### `clojure:temurin-24-lein-2.11.2-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4f0745923f0f104ee475ec2891e8d87adb32339d4040026c0440d1f0b7fb9f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210246082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc179a72ff904e5367113fd35fa9d25e8231eee7ec0ef1e03d685bb3b6cc58b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a862a741c4a8c9476b3f8169f085a59370e44326dbe38a1854b138cfc335db04`  
		Last Modified: Wed, 02 Jul 2025 04:17:38 GMT  
		Size: 90.0 MB (89952014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda5d9c547db28b8b8c4136658cb597b42638ae1d2c2ff71b7a1dd2582e117e1`  
		Last Modified: Wed, 02 Jul 2025 04:17:34 GMT  
		Size: 66.5 MB (66515628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c121f940ad6522de26030c918537465e46469d9c7821620f2879af1db510e`  
		Last Modified: Wed, 02 Jul 2025 04:17:27 GMT  
		Size: 4.5 MB (4514134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a814e6cf0e91c23bd6e9315d7c031a2aca9265877c38271700ee1130b0211482`  
		Last Modified: Wed, 02 Jul 2025 04:17:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:022457af48a91b86e595fa9d38be315b4fb2c40d56085fa4b42396af650f5617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6416949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a535a261f857ccf7b8450e1351a864f8c13791eabb4d9f738324e9b7bb3ba8b`

```dockerfile
```

-	Layers:
	-	`sha256:6b9dbfc0a0fa428027788126c65ba215ecf61513979a4ae72c524f47809e1200`  
		Last Modified: Wed, 02 Jul 2025 06:41:44 GMT  
		Size: 6.4 MB (6398553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bccd1f68e15879422a5477c94233ba5be079c7deb8617d1e816a1899f184853`  
		Last Modified: Wed, 02 Jul 2025 06:41:45 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc1f989b5fb066a9963e5c5ffc3708345aedad12cbceebd2db3d5a44c85bdcd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.7 MB (209697605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3029a15232acce637ca9945260ae37bed2c6a610b964bd527f1bd4c6215f961`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3201e1aad33692d11acdbc8c155e37cfea431ba1a1deccc85ed3e689d8a5db`  
		Last Modified: Wed, 02 Jul 2025 12:59:39 GMT  
		Size: 89.1 MB (89091225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7dbc09fe929cb1286413455d6db2b5aed8fc20534ac3b3e4500af4f2c6a675`  
		Last Modified: Wed, 02 Jul 2025 12:59:36 GMT  
		Size: 66.5 MB (66461662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3f4514b0cfc800aa1323ee28d8167c42c974558aa42dfb9d6ebe882bb713c6`  
		Last Modified: Wed, 02 Jul 2025 12:59:25 GMT  
		Size: 4.5 MB (4514135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14715ce47974494e00138c2d2441472c6655fb7cbf3fd62fa169b36cabe02d00`  
		Last Modified: Wed, 02 Jul 2025 12:59:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ed9ee061c9da4a9d83f69b598ecfff417d52e316581b9638f3bf1bbd3921028c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c605d2711aa2259857361ec99b338a8c33652f39d1d48e7f75269ceee04bd539`

```dockerfile
```

-	Layers:
	-	`sha256:394f661b79f42dcfe9e46ff07971b2d33805806351c03e92314ee70f76ce31fb`  
		Last Modified: Wed, 02 Jul 2025 15:42:50 GMT  
		Size: 6.4 MB (6405513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:431c22ea8c83d980f126b9de48550768db7b65a79c207b7071d5c39d78718f23`  
		Last Modified: Wed, 02 Jul 2025 15:42:51 GMT  
		Size: 18.5 KB (18517 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f72e4f4fb007ec0dcfe5de99416a093901bb6db62c0b1f0aef08af34d7dc52a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219053509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8159412dfc7fb953ce795d57a2b4efa8c99a4b4ace27c36fdcd44334079857`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3bdb985c0e5b4213fe25f1bc15fec160dfdbf3983ad4f63719fbaf61f76363`  
		Last Modified: Wed, 02 Jul 2025 14:07:30 GMT  
		Size: 89.9 MB (89920272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cfb209375fdf2fb210a0a8040fcaae0f20e0e9e748105c40bf1ef91297f675`  
		Last Modified: Wed, 02 Jul 2025 14:07:24 GMT  
		Size: 71.5 MB (71521411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810f8dcca860a2b9d3e79b73fd9d7faccb4b19a6a77b20e18fe7e7ca02057db5`  
		Last Modified: Wed, 02 Jul 2025 14:07:11 GMT  
		Size: 4.5 MB (4514162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2646886d7c2064aee7abdde184f2655e2a9bb7ad01637b44de58f164e7cb776`  
		Last Modified: Wed, 02 Jul 2025 14:07:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bc64418df46d89422326c05a7c41a17b144ac6b5804eb7e293c6c68efe49ef79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6422399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5817817f121d724071ef7782781497f848756bf3f8d82ea9589dca3be288b709`

```dockerfile
```

-	Layers:
	-	`sha256:a587a7dc810448c3ed52011635e732b65da81b4c50a2f332c3a7216f661e92fc`  
		Last Modified: Wed, 02 Jul 2025 15:42:57 GMT  
		Size: 6.4 MB (6403959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b44fa404e34d0d95c20987c702e0069bba3887ebfd62f672d83ca1a244f4af7`  
		Last Modified: Wed, 02 Jul 2025 15:42:57 GMT  
		Size: 18.4 KB (18440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:7b1f5c5418bc796604df5e1da2c40a826764464f37bce7520500abfa4724edab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205520143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678ea0903c6320d5dd113a896655caf2e89f75d8feb91648406d022c48240877`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f120b17727d388dbdc6b555b4871b73604f60d8e50666c67171b05dec72894dd`  
		Last Modified: Tue, 01 Jul 2025 13:21:46 GMT  
		Size: 87.6 MB (87622163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b007c8716844c00be475be4bbdc72f5ee222bec67bd3425ab55450403226494`  
		Last Modified: Tue, 01 Jul 2025 13:22:12 GMT  
		Size: 65.6 MB (65633151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58055c8d9fc82b14f9a2f01b67b73d89204c4b54732f959ff7e561a819fdbba0`  
		Last Modified: Tue, 01 Jul 2025 03:32:10 GMT  
		Size: 4.5 MB (4514243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a713ddba6e019f0f7adf2c13c9dcc91a0d04b21291a9cf3f01c79c6188ec9b87`  
		Last Modified: Wed, 02 Jul 2025 09:28:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5f700961067f504bf89d7903d1715e80af5ff35c8eccc4755146ceeb8c90a748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6404811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa7f61fb60cb68d714495628e72af09b15797b05e3a2ca5134443a84bddd89`

```dockerfile
```

-	Layers:
	-	`sha256:8b49ae09d68e7739d4a2f06c83156ccd52b0050badd1101220ea7a5b5b893ccc`  
		Last Modified: Wed, 02 Jul 2025 12:40:29 GMT  
		Size: 6.4 MB (6386372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8943cd74b56c468f75e7dfd3a77ffaa0d0736d9a89a7ca63d6350474d162c6da`  
		Last Modified: Wed, 02 Jul 2025 12:40:30 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:53a9d440aaa7862a867a84f80f7a6c0d224e79cbb8960d592f1eacd80650dc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206567629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c980b507b502ac7b53969ebcfa5540e69c4b3d93724c6407f7d75e23d759fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc4f9cbbad9b79641e4f5ac67263deac9aa43001430d2662bc7db69f2fcfe7a`  
		Last Modified: Wed, 02 Jul 2025 06:58:54 GMT  
		Size: 85.2 MB (85216805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0389efe5572da439519964e43461ea7a66e5828bf12fe3257f2952ef87074732`  
		Last Modified: Wed, 02 Jul 2025 06:58:54 GMT  
		Size: 67.5 MB (67492543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3076a5a9eb04af364f8eddf8a505f28a136ca84953641f7209d7265a04aa355`  
		Last Modified: Wed, 02 Jul 2025 06:58:48 GMT  
		Size: 4.5 MB (4514192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f3950a1203accc2344862da7a5d40d4065877c48704c8409f3f15aad2723c0`  
		Last Modified: Wed, 02 Jul 2025 06:58:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:feed48187c27bfcbb3dfa451472b5910b96f5661c805b9692ff6edea0cf5d884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6415473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f955ee27d4af8430ca75409dd9c59ee705c4962beb3533e2f22f98d4864a449`

```dockerfile
```

-	Layers:
	-	`sha256:f17df1b418d08a7b3b1081d6efe634f978a0b01414963022c50411566ae56f46`  
		Last Modified: Wed, 02 Jul 2025 09:41:08 GMT  
		Size: 6.4 MB (6397078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213895f0de75226c7e7a8fd441b96caf5ebfb0cb0a513c475e43b509a2fd039a`  
		Last Modified: Wed, 02 Jul 2025 09:41:09 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json
