## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:cd672670842c9fce79e17e74b682cb5c05b7baee6e69b23bcde6f1301fe46e8d
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1589436c7f3b699e0bca40a197f3d9eda222ae04bde4e70d0e00208afac71693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218718796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056e3d271d473c809de4db9a76f6ea458585e69a97bb071a604f236313d2a1f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:07:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:07:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:05 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:07:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:07:19 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:07:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:07:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:07:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:07:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f526ccf870dcc5ba5bacf69624a30eb9f0060c0af00af833ec527f8f2ea6ef20`  
		Last Modified: Fri, 08 May 2026 00:07:56 GMT  
		Size: 145.9 MB (145905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c7a980f6769f2ac4896e5ad8c267043165bcb8b66b4c407a85cf29e6da96f3`  
		Last Modified: Fri, 08 May 2026 00:07:39 GMT  
		Size: 19.8 MB (19806513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4082c1e51faa9a7406c81bb558410a2f83785c808d46194af454059b72a5ac9f`  
		Last Modified: Fri, 08 May 2026 00:07:38 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ce6ca0de69d56e32e9efd28eb8f5f8134643750ae6d44fc989053fe7144ded`  
		Last Modified: Fri, 08 May 2026 00:07:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:daa5f639da4319e51fc39c7778a70e18958aa951956ba1830900211e096f7fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3ff28e44f434b2350dd4f8d986952bcbe9a8f8afd1edf28cd5bae2f0e9aea1`

```dockerfile
```

-	Layers:
	-	`sha256:9313889a14d7024c50785d6e08c69c296408d9e116e375a3f7acd6be9553a05d`  
		Last Modified: Fri, 08 May 2026 00:07:38 GMT  
		Size: 4.3 MB (4282358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ac9a2e0a8d8cb52974e0c45be0f811bca5363ed07cc071935dcab1e38329a6`  
		Last Modified: Fri, 08 May 2026 00:07:38 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c0191cf7a76b26621b14d59a50da629da52d9bbcb0cad750ea46197471ecc6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217252604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31977ea5553e2eb9d3081953b2edd7658f2c7c048d9c704adbe47b5738040a24`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:08:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:36 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:08:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:08:36 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:08:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:08:48 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:08:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:08:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:08:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:08:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2afb7290c6f0e6371103c0b0b34522435a82cd734fa3aa911fc15187c6ee982`  
		Last Modified: Fri, 08 May 2026 00:09:10 GMT  
		Size: 144.7 MB (144724305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb27efa9fe006eece16d3a67d3c0fd4d3df9bea29a5b5a2fc1e708dac3ae813`  
		Last Modified: Fri, 08 May 2026 00:09:08 GMT  
		Size: 19.6 MB (19637039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c9fe0dfc58994c3dff17959aaef6920dfa778d31af0b8e4af17c8102f8f58f`  
		Last Modified: Fri, 08 May 2026 00:09:07 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ab2a046d389469b31f6ffadb3118f23771017a8a0d5f7ab35614e456305e47`  
		Last Modified: Fri, 08 May 2026 00:09:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f2e384e87a8d377250b05f1e3152b9c5de20c41aad1471d0ec2ac9e0d87e5241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf5c42c71cdd02672a8d419758665b6755a9701dd36819083c3c5e74df5e4a4`

```dockerfile
```

-	Layers:
	-	`sha256:516d63527b2a1e2c2a9c5942996ca07ce15d80888281fc5536f4267d89c55e9a`  
		Last Modified: Fri, 08 May 2026 00:09:07 GMT  
		Size: 4.3 MB (4281973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3267c7e3baa094ce8c5162fd3631ffed6f79a8ea8826ed8d474711b732ff22cd`  
		Last Modified: Fri, 08 May 2026 00:09:07 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9a943b4e3cbd17409647fc61e2b029b3f71f812a9c397f5746e64736c696b48c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222651666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9deb79d9c24d2ace3307969056a1ddd804d75d2974caa1728c7c27bc939603`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:43:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:43:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:43:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:43:06 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:43:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:43:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:43:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:43:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:43:47 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:43:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:43:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:43:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:43:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1a630844f3ca330b4aeb3cf62ea83634554dfbe591d28cdf3d1bbe7c2c4aa2`  
		Last Modified: Fri, 08 May 2026 00:44:30 GMT  
		Size: 145.8 MB (145766245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419e191c7ec4b8ec3cb4ebf0d56a17bdad44e0f536b66424b1152ae26f2de926`  
		Last Modified: Fri, 08 May 2026 00:44:28 GMT  
		Size: 20.0 MB (20030506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a883e733f7ed5810bed9ad730543ab1e9fa9dcf21f414b765bae147c277196d0`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4868052b9600bafefaae8a0a1ec28b16a4ec94dd4727eab9ee656adccac2719`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5a43a0e686d129dd5a06b985f1786f788ffb9ae25e390db9c9e39a5f1d498220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfe995cc87badbfa918db774caf2549e49d7f6b9b1eaa8aa5ab1c46a20cb209`

```dockerfile
```

-	Layers:
	-	`sha256:4b96d5e5ec89d694389ed472c7e1eb33cf0316e20483a29885f654a83607d42d`  
		Last Modified: Fri, 08 May 2026 00:44:27 GMT  
		Size: 4.3 MB (4284219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df0ebc9e962434ac2e531db4a1ba520486ac84785ac4fdcc2f917e8eb141476`  
		Last Modified: Fri, 08 May 2026 00:44:26 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:16cd68f40894e4fc637c1b165f9a1b12516dc552897273d8aff2e2a2ba721f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206759867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c569086028104b6664acc2c6aa5f837d19205ccd8bfa3a328eec4979e83d874c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:00:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:00:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:00:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:00:34 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 04:00:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 04:00:34 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:00:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 04:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 04:00:47 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 04:00:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 04:00:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:00:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:00:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046564bc8b79a0be58c4ba63f7db980f118576e0890ddd62ae27ffc38620ab70`  
		Last Modified: Wed, 22 Apr 2026 04:01:22 GMT  
		Size: 135.6 MB (135626974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17727c8a34d4d9c960c82e23c4c326c06b40a4e34870c31b22b0269c77abd285`  
		Last Modified: Wed, 22 Apr 2026 04:01:13 GMT  
		Size: 19.5 MB (19466746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e8d069ce62f03720a6c3a5724f451b1d5a383090359388a220fe9c4f42f6d5`  
		Last Modified: Wed, 22 Apr 2026 04:01:12 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0a88ca2b3fb4eb03f7d795d394732221f48678b8d41f32929c48a53b2170dd`  
		Last Modified: Wed, 22 Apr 2026 04:01:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ff59e9ce03a74acc091f2ad1ad685e06c0b89217e47d53a4f4d570f0fc7e075b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a24f28c8c78933156fe68f737b08fcac6d9cbbafb603f27f40a24febb32bf2`

```dockerfile
```

-	Layers:
	-	`sha256:832601923eaff17b9f0490b7822a98a291f085c97e4ab2777b4eb93d61194936`  
		Last Modified: Wed, 22 Apr 2026 04:01:18 GMT  
		Size: 4.3 MB (4273545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef39021d1058ab07fad9fc64b10a75c2794a6b39bf7c6832757a2537ea219711`  
		Last Modified: Wed, 22 Apr 2026 04:01:12 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
