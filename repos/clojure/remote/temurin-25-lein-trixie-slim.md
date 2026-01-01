## `clojure:temurin-25-lein-trixie-slim`

```console
$ docker pull clojure@sha256:e2a62cb9d3056f0383cb4cb0a4f9c7caa9b7c3fee1dbd69b7c9e55fc107696d8
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

### `clojure:temurin-25-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:03d3c9ee168d16623a71ce79ee288afbe87de12c80f421f4e4c451ce6a1ab681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142787110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f208e042062633c409648c965bd875a919426121ce0cd8095a51438b0270a3f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:07:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:07:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:07:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:07:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:07:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:07:16 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:07:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:07:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:07:33 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:07:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:07:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:07:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:07:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43541c44d959b354253abe94ff28ffbd6742f2898191a667479851de61254c1d`  
		Last Modified: Tue, 30 Dec 2025 01:08:13 GMT  
		Size: 92.0 MB (92045289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b510e04738ef0fd2bb782c6000b26974bb7c0e7e7cb5ae028c0e955dd55af`  
		Last Modified: Tue, 30 Dec 2025 01:08:04 GMT  
		Size: 16.4 MB (16447161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4940f1784b8f56c50750a02bf9ee44b0c2f21965c9835558b2bda3d2c2033aa2`  
		Last Modified: Tue, 30 Dec 2025 01:08:01 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8bae1c9140a0438c35fbeeab839059ecfffcc01f864a2e25731dee84655e7c`  
		Last Modified: Tue, 30 Dec 2025 01:08:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0819e092d39ebdac3e3385190b4edb9a36c84337ab0b4a3906c0a26d07b970b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f231b30979b41c13c9b4415df82b03c528fbeeed3106042f17ea790bdf523`

```dockerfile
```

-	Layers:
	-	`sha256:9cac20b85b459381e5064f8b636761048081d1ba3d32f6bc161627e669e1897a`  
		Last Modified: Tue, 30 Dec 2025 04:35:56 GMT  
		Size: 2.3 MB (2314754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:513c01de261d2a677bd563d14419e31f8d3cf83fbb975f4aeb8e614c3197d0dd`  
		Last Modified: Tue, 30 Dec 2025 04:35:56 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44127a1516cc45f25deac9d681fd8bba2b2f52ea6c2636047f8bdf1df1ad9cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142123126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b899e6770790916d521661d8f627d71437a2b1cfd84f209a448eb87f5f39af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:09:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:09:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:09:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:09:00 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:09:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:09:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:09:16 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:09:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:09:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:09:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:09:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90977f377cbac386759f6d3f7ceeed171ab2c8bd848e81d260ba67444aa5a4ec`  
		Last Modified: Tue, 30 Dec 2025 01:09:59 GMT  
		Size: 91.1 MB (91052511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297a1697d4759b405dbc2d9b4af266d4093f61811e412e3c27dbfe7dd1cdb88a`  
		Last Modified: Tue, 30 Dec 2025 01:09:44 GMT  
		Size: 16.4 MB (16413795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016adb9932e66588b1f07e28074c02cfb44352c330756d0c46433616e8c6ba20`  
		Last Modified: Tue, 30 Dec 2025 01:09:43 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf6be96e62e8d884ac4f47bd90597d80e739ffc14f2bd579d4b9503e695cbcd`  
		Last Modified: Tue, 30 Dec 2025 01:09:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82f956f82057bc95cb5dc393861140cb1420f0f8113c19ce242466176ba1bf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6615ed8b2ed2c1de121ec4f8158e76f93a8da3dcf9b9a6977e28f698f7629d`

```dockerfile
```

-	Layers:
	-	`sha256:3a5323ff6f34c4d3aa6635f45c361ae621be52c5a8b5a2571c579720361503dd`  
		Last Modified: Tue, 30 Dec 2025 04:36:01 GMT  
		Size: 2.3 MB (2314393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a256d053d7b144dced05571ea9baa47836428cb585c99b99aab17be2519748a8`  
		Last Modified: Tue, 30 Dec 2025 04:36:01 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9356d32030ec66ae40dc31741f93b38ae47cf091ed0f1eb1c38db176f3fead36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146211092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc476ed013405c6fb94b1ccaebb54e407015f9de129754bc9c35d600e2b09eb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 19:15:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 19:15:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 19:15:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 19:15:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 19:15:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 19:15:01 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 19:16:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 19:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 19:16:08 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 19:16:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 19:16:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 19:16:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 19:16:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6641751f0ad442566e7584e41ec87027fbbe61b528d316ccc54fec38b944127`  
		Last Modified: Tue, 30 Dec 2025 19:16:48 GMT  
		Size: 91.6 MB (91610756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2562a9f8abc081d569a7c14804d6946dc1e83b76549546e4633da519b733f3`  
		Last Modified: Tue, 30 Dec 2025 19:16:54 GMT  
		Size: 16.5 MB (16485305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9021e43c2857c23eabbd0abd2e524b790adb07cf56e97aaf1a95602e9c018f84`  
		Last Modified: Tue, 30 Dec 2025 19:16:45 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9389402e4b0ee108136758d767bd0b0bf0a80c83b657027690054a9d80e7ef`  
		Last Modified: Tue, 30 Dec 2025 19:16:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93a06c8764ff7e76500ccf748e9b57e30c0988f052b9848881e3bef8fa69c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514ce0f8fd89f864051ba1d449dfe79cf5ddcca2df94a3e4f4975d4e55e1221f`

```dockerfile
```

-	Layers:
	-	`sha256:b3cd9711861437ae625106d4d24aa23ef0ab8d8606bda3fecac75c7af0d80fef`  
		Last Modified: Tue, 30 Dec 2025 22:34:31 GMT  
		Size: 2.3 MB (2317044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64930e90cf0afab6da166abf7b36620502165ff2c62321d72809526bc46fb5e`  
		Last Modified: Tue, 30 Dec 2025 22:34:31 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:98bd97f7da94b04c70f5c690248c396909864aaec16cf66e3cda8180b7a537c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139942042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f956d62f96f6c2d1fc7720a5d66542029874f5988cfbd59c269b0bb5c8d142`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:30:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:30:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:30:35 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 07:30:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 07:30:35 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:32:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 07:32:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 07:32:04 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 07:32:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 07:32:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:32:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:32:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a09886da888ac7f39c6c9f60f721941a5a3cc3ed273e4d20352388b50fb5af`  
		Last Modified: Thu, 01 Jan 2026 07:36:11 GMT  
		Size: 90.8 MB (90752859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809340366dabeee7446bfef1c9430edd6aced6075aa4c14861cdb274ae8b082`  
		Last Modified: Thu, 01 Jan 2026 07:36:01 GMT  
		Size: 16.4 MB (16397836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483da57381707f5798e42be6df179f839c90ea4b2f6c6e7c680e238d5ac7f920`  
		Last Modified: Thu, 01 Jan 2026 07:36:01 GMT  
		Size: 4.5 MB (4517788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b22dcbdce2eb2b0ce5e249fb8a0bd633ba430ee21fcbe4930530bbdbbf8797`  
		Last Modified: Thu, 01 Jan 2026 07:36:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d9867ffb5eefb293d9df5f02d9d933702431d7a48fa8d9e6b942656429d79d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375be7215430e83b634b548dab69a401386d0acd9741d530e4c87047dc276285`

```dockerfile
```

-	Layers:
	-	`sha256:95ad62ba696e7ed6b7f904e40f0cec1913376b2bd8da9a29c2c5033bba16aef7`  
		Last Modified: Thu, 01 Jan 2026 10:35:08 GMT  
		Size: 2.3 MB (2306811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c250f59a91d6e671e1acd6d5d3b283c04a8d5528acba645a7704bc27fed7f74`  
		Last Modified: Thu, 01 Jan 2026 10:35:08 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:818df3e9b149e5cfaff14ce163d5dfc3b65b291db77a68099f50a14ad2472bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139046229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7c0989733e5ba45d3a1b309f89f686fd409535ab7c2982ff96765c27b49f5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:06:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:06:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:06:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:06:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 02:06:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 02:06:53 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:07:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 02:07:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 02:07:05 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 02:07:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 02:07:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:07:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:07:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f373455999c881e0ae9d54247fa76e27724f7219dd5f71005ddbfc519f659e1`  
		Last Modified: Tue, 30 Dec 2025 02:07:45 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abddca3ce0d97efdd7a5a7633eb3e6c0ea6a5cbabf54b5ebbe63b9b6587eace`  
		Last Modified: Tue, 30 Dec 2025 02:07:39 GMT  
		Size: 16.5 MB (16482936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24589acf5eed202bfb8c53a74430e8cdeb4a353a0212b8e29d4e027fb1c021a`  
		Last Modified: Tue, 30 Dec 2025 02:07:41 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bdb6eacd039401f78b49f9fae3f5e02b3476bcef3df1328f4d28caf337ca1`  
		Last Modified: Tue, 30 Dec 2025 02:07:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d2452ec75f56e64e59c6c169e6f588c37ef7ccbcca8bfed02ced82f0c6092171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4c2e6f7af6ead64b8990a8b37c87362c2c0b6aaed145fa6125908ee6edfe54`

```dockerfile
```

-	Layers:
	-	`sha256:571c52347333c2205306b23fe8444ed4820323eba7b4a10415d11ecf0070ffa2`  
		Last Modified: Tue, 30 Dec 2025 04:36:11 GMT  
		Size: 2.3 MB (2313729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d173aa4b643ae6acfeaab3dbeb389f29a286c3bae775c47c9f7fe68eb844b3c`  
		Last Modified: Tue, 30 Dec 2025 04:36:11 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json
