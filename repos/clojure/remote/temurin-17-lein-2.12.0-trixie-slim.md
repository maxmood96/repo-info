## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:a54d34bfa105f9183e10f644a85a800004bb8599c91cdef697c75b0746382c00
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
$ docker pull clojure@sha256:e89a3aa87432495207659e249911620df8247986f7dcd2f7039b60f18609df09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (200041460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c17abac7ae8839587013430a233ce19aceb3135670caa3465ad79062c86e8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:59:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:59:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:59:46 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:59:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:59:47 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:00:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:00:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:00:29 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:00:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:00:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:00:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:00:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93d40c272f62556f73a8f185bdb3534d9d5498e1326e609b9e0d6c7e31c711`  
		Last Modified: Wed, 25 Feb 2026 02:01:21 GMT  
		Size: 145.4 MB (145438250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62db194d31c9f4d236875156db4e13ebeb783b8052617fa83cbef31f0cfaf5fc`  
		Last Modified: Wed, 25 Feb 2026 02:01:22 GMT  
		Size: 16.5 MB (16484835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ac4d0c65d6bf3c6ae89b681e4c60259d5885e16b8a52966908032200471bba`  
		Last Modified: Wed, 25 Feb 2026 02:01:19 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc92de180dedacadd41806891039f8e51975126a65be5507f0eccb058343d0c6`  
		Last Modified: Wed, 25 Feb 2026 02:01:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d73897cc9fe73eec646235f464d18ed3d71559232cce5e74d2540986acf537a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56c276a1f2a5e3839c5927c3f40a68d7161a887f5eef36a0bce88d4e4e682c4`

```dockerfile
```

-	Layers:
	-	`sha256:3bbe42b3ba6d423c02816aafd1fda130777c8e0de7f752f255e2bc28d65ee055`  
		Last Modified: Wed, 25 Feb 2026 02:01:19 GMT  
		Size: 2.4 MB (2365732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11c5fcfc234cea41b98cb66c97438af719b37aba03c51fda502504d89a5684c`  
		Last Modified: Wed, 25 Feb 2026 02:01:17 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:dbff749b7c6e54db54fdb55cf65dddf0491e2692be2481a5cc176c43e7438505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191855591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3e03ccb6d9de6b3a7804afbcc020c7a06e8397e0f62cbf027365985f60274c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 21:27:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Feb 2026 21:27:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 27 Feb 2026 21:27:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 21:27:32 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 27 Feb 2026 21:27:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 27 Feb 2026 21:27:32 GMT
WORKDIR /tmp
# Fri, 27 Feb 2026 21:29:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 27 Feb 2026 21:29:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 27 Feb 2026 21:29:06 GMT
ENV LEIN_ROOT=1
# Fri, 27 Feb 2026 21:29:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 27 Feb 2026 21:29:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 27 Feb 2026 21:29:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 27 Feb 2026 21:29:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09e3a601e9732dcc8a0f82d761fe91f0f721e0c071867bcb2447d017285e0fc`  
		Last Modified: Fri, 27 Feb 2026 21:33:20 GMT  
		Size: 142.7 MB (142663031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5c339fdd318d03c7f649f83cb09e06cbf2c11e03d5d86982b057697696a7a6`  
		Last Modified: Fri, 27 Feb 2026 21:33:02 GMT  
		Size: 16.4 MB (16397921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1152674072f2d04637796358e661c8ff5f1b2f4376325f21d96d08b33a2143da`  
		Last Modified: Fri, 27 Feb 2026 21:32:59 GMT  
		Size: 4.5 MB (4517792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02a2b2b93397f780d2f9417c7c02cf67bf079528cc324dc6ea6dd15633b84af`  
		Last Modified: Fri, 27 Feb 2026 21:32:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90588a91601be03089d7d2deec9af8c5e2d1bec57e4243b8e2dcec8fa2b7be68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda5471f9a0cbc97a89b574589e8a095fd4651cf28d8c8ee4afedb9ab689e64c`

```dockerfile
```

-	Layers:
	-	`sha256:79e41e30629b1a53bb42e5b42ae09e34dbe1b9040213b3e0e9843dba487e3b99`  
		Last Modified: Fri, 27 Feb 2026 21:32:58 GMT  
		Size: 2.4 MB (2354881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7653ab4440d9a2d7bb53211e67357e55fb87aca2e59cd1eca4e32b6f7dd81a0f`  
		Last Modified: Fri, 27 Feb 2026 21:32:56 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:66012a7032a884067dc77dc394c3e5e92db505b967309e367f77812f53f44d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186466968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1dd640c3d4c6abb0803adc17fe2ed1611b3c40e9be03da4df1db344704bb39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:17:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:17:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:17:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:17:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:17:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:17:05 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:17:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:17:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:17:51 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:17:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:17:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:17:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:17:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f289f55a9025a1eb0402e10e630cc784a43d5e695e72ee4f0e0d7b8e5189d`  
		Last Modified: Tue, 24 Feb 2026 23:18:26 GMT  
		Size: 135.6 MB (135627060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ca1db7860155de2cbc71f444f48ff4158751e18b205c617495ea66ed5814e3`  
		Last Modified: Tue, 24 Feb 2026 23:18:23 GMT  
		Size: 16.5 MB (16483583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81969b0182d8b65932ca169bdca5e08131393f92591dd9c4a42434bbab6ea454`  
		Last Modified: Tue, 24 Feb 2026 23:18:23 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a71fd4d46ea3cb27088a901f36fc167d3c280386a11afbeba8465ffdd91afb`  
		Last Modified: Tue, 24 Feb 2026 23:18:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f9285c97ec6fbe12bab76eb340e816f11bccecd0cf8934ebd426e219f6eca70c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd09885a33d96b1ad4ebad41dbf25b46fbc4d0e3aec9bc3ac29d0fa04cf2595`

```dockerfile
```

-	Layers:
	-	`sha256:783f9c985a3357c383cc6880a04c3f1c0aa28249110edb2a4fee5249c6c6635a`  
		Last Modified: Tue, 24 Feb 2026 23:18:23 GMT  
		Size: 2.4 MB (2361179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8235ea408ac4f1889d0187ed58dc5c1354bda844c7818259f57442b6c3c7c1a`  
		Last Modified: Tue, 24 Feb 2026 23:18:23 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
