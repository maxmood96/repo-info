## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:0ffa7932254d56a6673f34bc6c04fcf1534991c64f157095f160e3e6a31a6251
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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b5926d17d66edc54c4f8848f7faa38090592b404a29d222b5bb9d84f02b0eff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196372725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25750820e5693524428ae30db69dbb3f576e1ebaf5eaa3f72fe74023f2b4a68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:54:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:54:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:54:49 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:55:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:55:05 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:55:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:55:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e777bc62000a14ff928256f311b85eb13d55bfc517a3945db6224f6ce2cf01bd`  
		Last Modified: Tue, 24 Feb 2026 19:55:24 GMT  
		Size: 145.6 MB (145628747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51edcb83980b3ed5b5044eee255b1740f91224631f90113e8cc260ad086ca4e2`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 16.4 MB (16447209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b40ba88bd3d18c5e6038aed25b878f112a110f96e14e30716faf149117a6f81`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fa003994e7505474379f93cd04175918e2d1f07fb76817111be74bb97a30ca`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:999ba12e44524305cd7e2cb3149422e84fcaa5d67b204e4b568c7597352f116d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d287721985f250cade5f879fb68f40ef693becc42fba96bca3b76e882a44f99`

```dockerfile
```

-	Layers:
	-	`sha256:3544e75572bbcef8cbcf643eb940e34fcd74801b7eb403ac33d73099cb88cb2a`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 2.4 MB (2364752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f24dca4a20d463666313164641870b0615d86edd84782fd4124f873b23b13607`  
		Last Modified: Tue, 24 Feb 2026 19:55:21 GMT  
		Size: 18.4 KB (18385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66de2e9d8e51a585ad4f12f812f0ecd7fd0c548b653db9810df0a5ba9b9ce641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195508086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4f42f6aeae40a5a7826e1fc3889c36355ce5ad35bbd2af8e53166c2d44e83c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:05:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:05:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:05:42 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:05:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:05:59 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:06:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:06:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471b1f1cd9501f26c0762e43c28d87df4e14438ac69b6b1a5458935c2047590c`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 144.4 MB (144436238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9be8413c6b2698fe8e44e333df2327646235cc8eee913e9ad55f44c5303eba`  
		Last Modified: Tue, 24 Feb 2026 20:06:17 GMT  
		Size: 16.4 MB (16413600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1065aade25ada88c57e6fdc07cbec457e9451a7bd24378715dd16e972a1acc52`  
		Last Modified: Tue, 24 Feb 2026 20:06:16 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abae0d12f23a3547ca8fd68dba1c780c4b18bfe8b3e79230060fc2f2b4241d93`  
		Last Modified: Tue, 24 Feb 2026 20:06:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:571b1ef5eed96a20eff5d356a7df63ff310e03468728ca37517625970d42db48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533cb28aae2fb714ba905260fa620629ed10d689851abf2fe351a8437c4e3f1a`

```dockerfile
```

-	Layers:
	-	`sha256:7a5bc36cf4706550a82d3f859dad4378906a344d14b8dd860d18c6edc182185d`  
		Last Modified: Tue, 24 Feb 2026 20:06:16 GMT  
		Size: 2.4 MB (2364370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aabb3da34939dca7bbac8bb5c3324371cfb490233e7253dd86d6f73597df3d66`  
		Last Modified: Tue, 24 Feb 2026 20:06:16 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f366657e3dab4b013d75accc6952c23cbe27f9cf86fb02f0d6460ce646495deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200041393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9651d0902f0d5f64b0ea2431b80a9d1f3b1b52b0357b95afe8c02ce9d1d8851`
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
# Tue, 17 Feb 2026 23:49:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 23:49:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 23:49:25 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 23:49:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 23:49:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:49:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:49:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b4cabddd66d71e97ccb04d7861e4511a418edbd43a9f1a73ba473b7207138b`  
		Last Modified: Tue, 17 Feb 2026 23:50:19 GMT  
		Size: 145.4 MB (145438194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7465036c90e665493aec51061373f7e455acc1f9f134c4003ad5a2772e7c811`  
		Last Modified: Tue, 17 Feb 2026 23:50:16 GMT  
		Size: 16.5 MB (16484871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51914d5b3a05eaebc403d794d1805edc59ddca8181ce33390a7192b8bb89e8a2`  
		Last Modified: Tue, 17 Feb 2026 23:50:16 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df268c77bf962061f5d5e37bea4d1d29b0a9f07b00d3faabc29c6d16acf49084`  
		Last Modified: Tue, 17 Feb 2026 23:50:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36bbc96f3fa091827d6ec6f9f4b46d454d4ff68dbe8734acc01dfac8b3e845f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc954a050e8fefa240f380460cf434dbe144b2c33962e2337f3c9f2849803b6`

```dockerfile
```

-	Layers:
	-	`sha256:84396efb9176ff3b95ece5cf81f3fee02750a0811d52eb598a3f3badd7038721`  
		Last Modified: Tue, 17 Feb 2026 23:50:15 GMT  
		Size: 2.4 MB (2365732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88b571aff3b434e66d59b2801892770ad4091dd00aaa90af48759299f332ad97`  
		Last Modified: Tue, 17 Feb 2026 23:50:15 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:739c30d87eaeda8a976b33c356162fd94834ce0a6d1354b9e30fda16c261d969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191855713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c76ad41b00f3c28fa92efdad9c49200eab9c60ccd0350326b293abd712f30e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 10:26:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 10:26:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 10:26:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 10:26:35 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 18 Feb 2026 10:26:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 18 Feb 2026 10:26:36 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 10:28:10 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 18 Feb 2026 10:28:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 18 Feb 2026 10:28:10 GMT
ENV LEIN_ROOT=1
# Wed, 18 Feb 2026 10:28:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 18 Feb 2026 10:28:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 10:28:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 10:28:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111103a58980758fcdb9577cdd1fcdb21280530f3d9c80e1e1c9faa138061546`  
		Last Modified: Wed, 18 Feb 2026 10:32:31 GMT  
		Size: 142.7 MB (142663128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0d82f7ff75815feab2d63a94bac883f7a75b822dcb35b3546865ee9f73a6f4`  
		Last Modified: Wed, 18 Feb 2026 10:32:14 GMT  
		Size: 16.4 MB (16397969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b881d6f0c0ce8faebd66df289ed4293ca70b2d3c9174b678b79538cae7cedacc`  
		Last Modified: Wed, 18 Feb 2026 10:32:10 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad1c12476ea7f7cf1af973f433b89f7d9ff8bc7a984df94797690148002ef6e`  
		Last Modified: Wed, 18 Feb 2026 10:32:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3551d66568283d3fa1d8ad9a322457fc78b9d062c2eb0e701b3e052c921686b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154d5bac2c59059060c24c1aea5e2a052928ef34c940d930d5788eb131256616`

```dockerfile
```

-	Layers:
	-	`sha256:565f4e36e26cf78ec59e11eb2987e72b01841dc5f0b3b69c2c8b715b175d148b`  
		Last Modified: Wed, 18 Feb 2026 10:32:09 GMT  
		Size: 2.4 MB (2354881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bbda6ccc208ff9f176d637c03d9f4722cb6715fac84d99f6db329d8c485717`  
		Last Modified: Wed, 18 Feb 2026 10:32:08 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fac1c4f99fd7d4518c3cb1e4bcd71884d9aa5424dfa7e91c1bcad11213f0783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186467046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77639c61fad6cfa93779892e5015a0bddaf9f264a552178f5b207282896fcd5`
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
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094f54d5460e31ea8945cc291a2d9832adafb12b5a3dc29f5a20e3454ee7fe79`  
		Last Modified: Tue, 17 Feb 2026 22:08:46 GMT  
		Size: 135.6 MB (135627116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d933b736317699f99275a0d07974f8b904fe7a46832647649149603c55ab08de`  
		Last Modified: Tue, 17 Feb 2026 22:08:43 GMT  
		Size: 16.5 MB (16483595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eede91a645ddf1e5d73d1a622a1511ebc2eb949406bf1150383497d36a823233`  
		Last Modified: Tue, 17 Feb 2026 22:08:43 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69df11e74b8801046460c8fbaca61a87239e1a95e78d105fb582e8823b0cd918`  
		Last Modified: Tue, 17 Feb 2026 22:08:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d6e637cf839e376534176167a1e87e02b1e964bf47dd186a504e74fbd552d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f387b0624c0ddd57c5bf497b2b81ac968bffc825dad21bdc929e19ba1fcb9023`

```dockerfile
```

-	Layers:
	-	`sha256:6c70db781e3cb47c06a4248305b425ce0fe1f6998e2af45097e748b643f464f3`  
		Last Modified: Tue, 17 Feb 2026 22:08:42 GMT  
		Size: 2.4 MB (2361179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8891cbad96b0c59f8a146c094d93f00e0c4066e9b922bf62c89fe568f37468`  
		Last Modified: Tue, 17 Feb 2026 22:08:42 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
