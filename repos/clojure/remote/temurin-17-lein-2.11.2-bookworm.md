## `clojure:temurin-17-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:2714443a0180551461d72f82cfed7e70417482548c41c63451844f7e5a3a920e
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

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9be353db073c241a778183d9d927c3c110f5bb86522d022d063e05cd020a9329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259709008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33121874d18696d038923aa2e662d8b4a23a54b629e32da11567abfda7e82bf`
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
	-	`sha256:ea2182e8925a506646f46fc97848a83da8f5c5450771d63d135241702244fc23`  
		Last Modified: Sat, 17 May 2025 13:46:16 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c12b3895d657c8fa66ba7fb88124afc4032728536902d4a5e64d857f2b8169`  
		Last Modified: Sat, 17 May 2025 13:46:20 GMT  
		Size: 62.1 MB (62068208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f22040d1f30e3eca2389d164e5c754c515057f3d5f3a87312b117cf0dc69d72`  
		Last Modified: Sat, 17 May 2025 13:46:10 GMT  
		Size: 4.5 MB (4514148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdbc049464f6338ef1cbcb3a65ed532dbdb2ef848153fbc9c368a8a1cca9f30`  
		Last Modified: Sat, 17 May 2025 13:46:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8cf0c9cd4c91bd4825dac72ae5e7b5a92f6bb6e84197aabe80d2a0a8a286fa36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6554066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9ce949d7b0115e5b8f0055e2887b93ccfac46f8ae75f5555a335e004d69de6`

```dockerfile
```

-	Layers:
	-	`sha256:d905a312d282886866664322087f1a0fc4c4dc3115612c148a1a66cb38deb538`  
		Last Modified: Mon, 05 May 2025 17:07:20 GMT  
		Size: 6.5 MB (6535643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5bfd6cef67875ded4c88c486e1c8ddf47f992343082d5fa857a3bdb0ef2e3fc`  
		Last Modified: Mon, 05 May 2025 17:07:19 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f3ec918fcac1218652c40513c16d524b0d6fa898088318736c525b5a07e2c027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258390817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0c93706d4ef948c1c17b02768b176fd74c2e241ff1d8972d44ed3f0c915b0d`
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
	-	`sha256:e0272c641cc0d4e591dfd5633964da759830a3aa31bb840abf370589a98c0a9d`  
		Last Modified: Tue, 06 May 2025 00:32:18 GMT  
		Size: 143.5 MB (143512646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bb7c7cb4cb39fb9624b8e436b22b4f6831bca73aa53813120f4dba53dd21a1`  
		Last Modified: Tue, 06 May 2025 00:32:17 GMT  
		Size: 62.0 MB (62035883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d075a3b3147f4b2664f5fea8572b2d67b5be3035b81b02db3193cd10d8a30a`  
		Last Modified: Tue, 06 May 2025 00:32:15 GMT  
		Size: 4.5 MB (4514215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c55dc6291ca11f7a5d639df03f84f9e41b352702528cce955beb997882f154`  
		Last Modified: Tue, 06 May 2025 00:32:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:efe7c33d46e3b9f82c2bb83dbae5e04effaad15e76585163ce5b8d03740bec51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1f04010432ca65d7e476a4a302c952b4c2192233acfb9d83792d5e0a04e256`

```dockerfile
```

-	Layers:
	-	`sha256:a31a20df6a81e40fdcd73e3eed9c242f26dbd965b523eca16f432363fed4e00f`  
		Last Modified: Tue, 06 May 2025 00:32:17 GMT  
		Size: 6.5 MB (6541337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce605e8a6ca14b48a1a0811c14748a27f0aa3667d72aecfdafc9bc518b4e8ddb`  
		Last Modified: Tue, 06 May 2025 00:32:15 GMT  
		Size: 18.5 KB (18544 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b3f8b54e05a13105473cb6783270c06a56c1fae8efcb5a082c112cc542ff8aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268431864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a128e1c717ac92801bb51be1e8b054fcb1e4fb1264125c1c5555db68c68ff4`
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
	-	`sha256:81b3d490ea25347d534362b7269da337ce2723a0c555c440f6211ca588075dac`  
		Last Modified: Tue, 13 May 2025 18:48:05 GMT  
		Size: 144.3 MB (144280506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0819a1a61d08a6ea89cc015c4c62a64831a147fcc4f80e5d1dd6b72bbeabea56`  
		Last Modified: Tue, 13 May 2025 18:48:04 GMT  
		Size: 67.3 MB (67304624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70dc381593c3031f2346167abed6534203a142bff7584f78d3fd61c02259533`  
		Last Modified: Tue, 13 May 2025 18:48:01 GMT  
		Size: 4.5 MB (4514175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf6c6ff9bd357d596d7d58681d0f38d78b28292b02f7592c55bcef858af6781`  
		Last Modified: Tue, 13 May 2025 18:48:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bcff40b3d39e2ee20efc2437fe454cddd19bc06a7c035632fa8e66fb961f84c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6558833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7418f89a76c9c805fd53b2c05f8862c80359b3307b4f6995c3934420d24ab02a`

```dockerfile
```

-	Layers:
	-	`sha256:11e13fb1eacea8a9db1cedeeded504f251ebf371677aab5ea6dfa13ba036a68a`  
		Last Modified: Tue, 13 May 2025 18:48:01 GMT  
		Size: 6.5 MB (6540366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc0224f61b4839aa478806d7a78d88ce181fa3d696ed09ae84797e2ccdfcb74`  
		Last Modified: Tue, 13 May 2025 18:48:01 GMT  
		Size: 18.5 KB (18467 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:cb1745010adbc1f454dd24ac3054da03a0a3ae2b184b02b98d5690ce6fbe91e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247420137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1da286421372972c5b42e5b01719caebdb6e39db1044ae21bc1d88f5f91b299`
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
	-	`sha256:6625b6191194fba26629853d9de4080fe3fcd48a079cf660370c1797f2747fed`  
		Last Modified: Tue, 13 May 2025 18:09:09 GMT  
		Size: 134.7 MB (134673599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e06713097d525b433d452478ab1c9ddda7b2514753ed4016fc1070fcedce277`  
		Last Modified: Tue, 13 May 2025 18:09:07 GMT  
		Size: 61.1 MB (61080583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9901af91d69a737a179e4a028ef1f50f57db3a0c0397c33e44d54eb97c721a`  
		Last Modified: Tue, 13 May 2025 18:09:07 GMT  
		Size: 4.5 MB (4514193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54756cc57df50db1afa2baa22651dad7342be0abfdd937c14f38673c6afc5753`  
		Last Modified: Tue, 13 May 2025 18:09:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9c8cba8ebf09e276632e4c0600e627301075f6f02a002f006669b4f5a07218be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6548334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd21b608d48aa21ff5710b610fa69aebda3da3bfc2e484e6e9fa61b12ab9fa6`

```dockerfile
```

-	Layers:
	-	`sha256:7dc1e93d216218e038c5f0ab331e0e2996fa29b46d36c97700b3656f04b9cbb6`  
		Last Modified: Tue, 13 May 2025 18:09:06 GMT  
		Size: 6.5 MB (6529911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c4c7196afc06f5341f82e320be4844397b0632b5f2bdc098322c8601fc6636`  
		Last Modified: Tue, 13 May 2025 18:09:05 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json
