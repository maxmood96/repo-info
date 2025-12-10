## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:e98c85cce0c13c732c52033731a6b4a93ef8b69c806adc51f6396766ba79f279
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
$ docker pull clojure@sha256:3b63cc5758db7735bf99942945d8ffad1203ed0f75e170353bae5be77238a653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217649739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fae6b0ecae42874395afce5a502cf95f91e67b2f1749dac1b85c6ccfc4af1d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:52:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:52:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:52:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:52:13 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:52:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:52:13 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:52:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:52:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:52:28 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:52:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:52:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:52:30 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:52:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4936ec2e0a93fc1898676c67efe80799140135c0e77d8f4e33887da6601260`  
		Last Modified: Mon, 08 Dec 2025 23:53:17 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb205c23017606d6eed487a45e836b9369b0e6666c1c00fc01f839cf2566cef5`  
		Last Modified: Mon, 08 Dec 2025 23:52:59 GMT  
		Size: 19.8 MB (19802914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7659c0d89dfa7fe57b9b07f8a5e3bbc0d454d5020fc461144026a31e5bd05f`  
		Last Modified: Mon, 08 Dec 2025 23:52:57 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866d69fb53200797337591d897e10fae9a6540c3ac360eab63fbdd854a31d3fc`  
		Last Modified: Mon, 08 Dec 2025 23:52:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f4839441fb3cba073e71729541987e69737ba0536b97b6647fca1e7ad75b0b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6191959eb4d4f7d43a787cfb8e656228e4ced0e82cc4a20226b47c313099ab78`

```dockerfile
```

-	Layers:
	-	`sha256:b422412225a3437fe70bb284ed42bd87f3c5c18d6c5411a5be6de3f5394f8239`  
		Last Modified: Tue, 09 Dec 2025 04:39:41 GMT  
		Size: 4.3 MB (4279836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad249da01bb4c9d88be66bf629e5c8577e5b86af3c5f0a8d7a748b66b85f8eb`  
		Last Modified: Tue, 09 Dec 2025 04:39:42 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bcfd1724e8df2506a7b68ef2ea14d53e691e9352763b0c81ac229e7fa7cef39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216189325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca4329027ff61bb463186807cc12a1ff0500cb4c5f5cb6554bbf84e9a7a2b43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:00:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:00:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:00:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:00:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:00:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:00:59 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:43:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:43:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:43:10 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:43:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:43:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:43:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:43:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1c1de6f000339346820df8180799beda05986da7e242490c4245da149ce361`  
		Last Modified: Tue, 09 Dec 2025 00:03:21 GMT  
		Size: 143.7 MB (143679912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64503905e04989df9bc0c5599d27b9d846c3e0341b76eab65e9e0999260020cb`  
		Last Modified: Tue, 09 Dec 2025 00:43:39 GMT  
		Size: 19.6 MB (19632166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e692c959a73488b1322608f8bd92daa70215f475909e47275f7a904a9ee9d38`  
		Last Modified: Tue, 09 Dec 2025 00:43:38 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685deed21b288ef9b4bcaa398cb3881fb2c13918cd9b2fc69af2b722444a1e8a`  
		Last Modified: Tue, 09 Dec 2025 00:43:37 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f0a9456c24e2090f1abce915bedf3b8205034b8518ddcc06ad28089c634cf2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611918845974e579939f21933a12e7aa74cd1d92324286effd2653779d7d29e9`

```dockerfile
```

-	Layers:
	-	`sha256:526a97fb92d5fd91c24737112da735166b4de05e1102d11dac6e31c648891887`  
		Last Modified: Tue, 09 Dec 2025 04:39:48 GMT  
		Size: 4.3 MB (4279451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a9567c70700dec3a2428ed95780870a718a857d8ac2e0b28bdfd76c7c7c45f`  
		Last Modified: Tue, 09 Dec 2025 04:39:49 GMT  
		Size: 17.7 KB (17688 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:fb5f6009c96485c27118608f355a5853fa8463734a9c68b4b034e43726ab8766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221392057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daa2d8e2c60a17a9b5cc5f5892e5bc4905d3604b533bab3892f5c26ee01e862`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:42:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:42:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:42:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:42:09 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 22:42:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 22:42:10 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:42:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 22:42:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 22:42:46 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 22:42:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 22:42:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:42:50 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:42:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35000cb1964cf20b1dfaf0b01681b83417814d0489bb0ac766df92e26616c6ab`  
		Last Modified: Mon, 08 Dec 2025 22:46:18 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af16074a1bdfff434f80fa5ac333e2e1ab89e2de53100eb427885bcb9274cda`  
		Last Modified: Mon, 08 Dec 2025 22:43:40 GMT  
		Size: 20.0 MB (20021647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6f5e59a34fae5901d1238ee96d04789217a8abc9239a299b1f14ebd4e92e31`  
		Last Modified: Mon, 08 Dec 2025 22:43:39 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e709223ae160b3ddcece5e0dc387d249846f2d3fb7f88987f23e579d9afeb0`  
		Last Modified: Mon, 08 Dec 2025 22:43:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a86278a1887415fa76cbe78027bb88f36965a5854a1ca164a4c901d59a538a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1441b00b621e29090a02a454824025ee696c9e00ed88cfe0d69e157b9b8982`

```dockerfile
```

-	Layers:
	-	`sha256:df7ba260129fbba9f537cc170be8b363213bba8c950c3dcf0cbc849f20b72617`  
		Last Modified: Tue, 09 Dec 2025 01:36:39 GMT  
		Size: 4.3 MB (4281695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b81b0d80f9f5c6ee5ed48a8f179ecee71bd9dd4a02a046192066e674eb02d4d`  
		Last Modified: Tue, 09 Dec 2025 01:36:50 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a5e7df693f517aaa0695c1a3456f42ec6c94b8a63b2aa0591655c716d999ec17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205975693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2b3d55959c31617ebbe9b4ec13325d0b98399fd33ad3a224916d0d4bea5a9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:28:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:28:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:28:22 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:28:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:28:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:28:33 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:28:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:28:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:28:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:28:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068f08d66ab2276a2c9ca78524faf8035ccd0094d15e25fe24702ef0fe52c031`  
		Last Modified: Tue, 09 Dec 2025 01:29:16 GMT  
		Size: 134.9 MB (134859062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4791cd6e8dc1625d8372ea621a38f9fe780a8263782f480063c6dfb3ca3dc04d`  
		Last Modified: Tue, 09 Dec 2025 01:29:10 GMT  
		Size: 19.5 MB (19460777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11399ee4992d84165c4dd3bb97fc731deb9f72bd6584b27bf4bdae17907fcbdb`  
		Last Modified: Tue, 09 Dec 2025 01:29:08 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661f08cb25e9d60c679154c54cba27e957f48a5300055604f98b05af56c88860`  
		Last Modified: Tue, 09 Dec 2025 01:29:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7b360d33e48252450c5756d162eeb630296eeba10864142fa53ebabdad029600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b94c1e194af3400212748840694511857aef2d2ce411db7ab94436ceaced14`

```dockerfile
```

-	Layers:
	-	`sha256:43f2abb5d217660e70cee8a59d28b13ecdb98599867952c6a36862edfc606f1d`  
		Last Modified: Tue, 09 Dec 2025 04:39:56 GMT  
		Size: 4.3 MB (4271650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846fbdcfd36414ef9f58a593bce53e358c0e884c67c02e5dff2787e34e5b53fc`  
		Last Modified: Tue, 09 Dec 2025 04:39:57 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
