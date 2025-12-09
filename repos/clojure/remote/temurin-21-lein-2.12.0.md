## `clojure:temurin-21-lein-2.12.0`

```console
$ docker pull clojure@sha256:88f829c4af320cf0663bd2f0bb3d2fb93fd3f11063ab8da736b45cf9549970d4
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

### `clojure:temurin-21-lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:d7c1590880012fc39022c148ec801d5e18a9129e9c8a1ad91a5c797f6a3000d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230627913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bab19b902e42bb929e95137c7c470801de50b3322ec9a27ba9dfaf19d210f09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:54:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:54:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:54:01 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:54:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:54:01 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:54:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:54:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:54:14 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:54:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:54:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:54:16 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:54:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3586222b5ec7940e8317771f395367b6615c33cff9ff6828c248fa06cdc84e21`  
		Last Modified: Mon, 08 Dec 2025 23:54:37 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93f066363047997d911364895451eaf5a49c0c6d26572a5cc1e6ac26d4b40e`  
		Last Modified: Mon, 08 Dec 2025 23:54:44 GMT  
		Size: 19.8 MB (19803036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982d375016514f37840bb56e5305291d26aef5776e3286c3d4cccb1b572e1fb5`  
		Last Modified: Mon, 08 Dec 2025 23:54:43 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae071ff79e4ca1b96f78b273f982ed29b18a712a640e5cb969d846e84e30bf61`  
		Last Modified: Mon, 08 Dec 2025 23:54:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:6a6a92bc488e92771ed1adc2b851e75af048121ae8d24003776c231a519c1e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c197d0a32087767ac4432a947909ee27db91d356028f1c5accf16a931a91b`

```dockerfile
```

-	Layers:
	-	`sha256:53f696d9019289455e5db9fdb9108190a94e496c61cf4b3046ebc92c5c2d4351`  
		Last Modified: Tue, 09 Dec 2025 04:42:53 GMT  
		Size: 4.3 MB (4283588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25fc5eb56da6ee869460c158b632b43c0bfa378a8c542954ec600213c249569c`  
		Last Modified: Tue, 09 Dec 2025 04:42:54 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3523222433b9bae11bff38f837cf73ea7e8f9d3e0c87c1f300777bfe657ededb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228617049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42797323db7908b34acdc3449bdb2764e07d7972b5c9ae2853ed35327f843584`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:01:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:01:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:01:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:01:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:01:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:01:38 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:01:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:01:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:01:51 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:01:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:01:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:01:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:01:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e85e305488bd1383fb2eb8c211cfb96f76ee9a795b14e09d60f121891cc63b9`  
		Last Modified: Tue, 09 Dec 2025 00:02:29 GMT  
		Size: 156.1 MB (156107651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b6c2207b35d9b66a03492301e9f74613960552f7d2ab7e9288f3af899e4e9f`  
		Last Modified: Tue, 09 Dec 2025 00:02:22 GMT  
		Size: 19.6 MB (19632159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54420aa3d41ec6ce9b82b565fbedb1ec2dd6123215e7374ad969026295922545`  
		Last Modified: Tue, 09 Dec 2025 00:02:21 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f75d4d5a72ee7b72ff3ddf1ec1e641ae10f6d8954a4ad9a796a0a210808d40`  
		Last Modified: Tue, 09 Dec 2025 00:02:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:549a32cdb4b4d7258790452ee403f7738c8659c87303bf5b8a7ed3224fac9e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c512f6cfa2307ac45c8e5b745444167532f45c0fb72f4a41478ba8fc80d66fd`

```dockerfile
```

-	Layers:
	-	`sha256:83ac304389796f1204a6e6468904268ba754157dfb7aea90ac954e1903814d98`  
		Last Modified: Tue, 09 Dec 2025 04:42:58 GMT  
		Size: 4.3 MB (4283227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893c1f4313864e16f34160d6210e76a16097818adfd221200dc314e3aa5c9234`  
		Last Modified: Tue, 09 Dec 2025 04:42:59 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:9538671482e04802378da4630c22efdd460f3e3500e72803f626e4d44544e16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234809731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1ca27db2be08e89dbddcf61e80ca6253890ef2bd7d27ab794d5d97ae49b1ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:44:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:44:05 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 22:44:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 22:44:05 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:44:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 22:44:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 22:44:38 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 22:44:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 22:44:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:44:43 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:44:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84193563598712b437e18d1f55a29d0760b80aa62c9cc1125eb6b86822607f7b`  
		Last Modified: Mon, 08 Dec 2025 22:49:33 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cc24c9cce496ef73514731238d92506e4ca425b414fef1e034e69e2809dc82`  
		Last Modified: Mon, 08 Dec 2025 22:45:40 GMT  
		Size: 20.0 MB (20021630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c85d88eaecd4673f28b0ab60ad08f01fe4155d82e01b90bcfe334b68d34d41`  
		Last Modified: Mon, 08 Dec 2025 22:45:36 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29424ff691d360cbdce12420d22a33f11a04073f81fd981113c41ab50561ab39`  
		Last Modified: Mon, 08 Dec 2025 22:45:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:0236b99c16d17856253c72862d44afc434c18faf7760c6e4e1a21392a40b53b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4d717db4e7443b1aec4bd649401e9f29df24a2d14a8194efbe7b0c82f7c7b3`

```dockerfile
```

-	Layers:
	-	`sha256:d56d83043619bac01653237297859ab9404cb648220546221c87a8a963831b2f`  
		Last Modified: Tue, 09 Dec 2025 01:37:40 GMT  
		Size: 4.3 MB (4285459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ac68d36f447434731b6adfbcc107aafbb608e7b70fdd20b1157b344e47b73d`  
		Last Modified: Tue, 09 Dec 2025 01:37:41 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:59ca1d75287fb425f1333df3859b89476d60c4ba264a158d7294056a9598f211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218186407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79531a31d788cd97020b33bcf8822b7019c3719e9dcb944b3e2543e61b986ccf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:30:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:30:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:30:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:30:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:30:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:30:38 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:30:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:30:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:30:49 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:30:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:30:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:30:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:30:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0989d7c9aea3b9e5f8aa3bfd4c0ad22e264c7b070ed172dfa35b1bac1415808`  
		Last Modified: Tue, 09 Dec 2025 01:31:52 GMT  
		Size: 147.1 MB (147069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9c94d7a92afcfd05222ea84bd35bc04a11226c7c0cdf9399b7f8ba333d9d1`  
		Last Modified: Tue, 09 Dec 2025 01:31:30 GMT  
		Size: 19.5 MB (19460721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e75969d252c765065c650fb488da096900b20d469f79b4989e9b05c6c5cc26`  
		Last Modified: Tue, 09 Dec 2025 01:31:27 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae28392708126d195356d79430b03f9955215e8a4f7f9f42acadfc48b10f1028`  
		Last Modified: Tue, 09 Dec 2025 01:31:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:922d32cbaa20b7a7aecc6a415e30de5f347483041f901f961e39b0be124d3ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2673b64caf39f10709bc7427457c31cdeae3d6bbb6c4d04280ecd604151b5f`

```dockerfile
```

-	Layers:
	-	`sha256:da8204c52a4a8d25b9851fe8206a464e4b1a2f33991b2f58330f3cf051233a5b`  
		Last Modified: Tue, 09 Dec 2025 04:43:06 GMT  
		Size: 4.3 MB (4275402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41e4ec0a720326ff33551fc0752aa34ac9c9c40424673a7cff6d6901963d055a`  
		Last Modified: Tue, 09 Dec 2025 04:43:07 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
