## `clojure:lein-bookworm`

```console
$ docker pull clojure@sha256:f7e536d4004f2e6fe01d001040529450061b41d2b72d075a7847911561e5e295
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

### `clojure:lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1e0c5518fa211fefb7b5fe46e5964835d6b72e21cee78887bb8cb7bd3241a036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164847101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a326bd2229b0b5991eb2602a0d484609a36a1b2ea92be5e8949f322b3e70a95b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:05:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:05:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:05:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:05:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:05:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:05:54 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:06:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:06:09 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:06:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:06:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:06:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:06:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f30985642f0713304a8da3b3ebd3ae1ec00b7cb01a0fd28f4a7d67699cbfd0b`  
		Last Modified: Tue, 30 Dec 2025 01:06:55 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5041b8c483b71b8b780568dae62c2dbb38f2cdd306ab0cbbb7219a7d442a596d`  
		Last Modified: Tue, 30 Dec 2025 01:06:37 GMT  
		Size: 19.8 MB (19802869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7691f0b7355649e4d362c485cef0d6fb920d68a2e6e3134b8186449e79d4df7e`  
		Last Modified: Tue, 30 Dec 2025 01:06:36 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0ae83e009f96123517d9dfd08c4d40002edb9d9149f92307ff49b68cb7f280`  
		Last Modified: Tue, 30 Dec 2025 01:06:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:baa75e7eb34508784f1941a2b22a2c53886da8a2e73960414d1d3d783b097448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2742f8d70a47a667c0b3f816edf99543bd737457ccadb83f0f45d4524c828f`

```dockerfile
```

-	Layers:
	-	`sha256:5868167a83215f38975f4145c738437dc597e75dce8b4fdf7c17b83e968ef975`  
		Last Modified: Tue, 30 Dec 2025 04:35:01 GMT  
		Size: 4.2 MB (4232396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a4cbde7751f3f94cf6ed8f1fe9f7466f8aabc38a9b6e87569a8086bce3e4ce`  
		Last Modified: Tue, 30 Dec 2025 04:35:01 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f6f8032f187bd3156e55a4370b5b103667895b4174c18f9e817eb30e6dd9242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163561947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8dfc9ef95436d10ea75f87c8ba008b33f7ea7b818d5c1fe54a4f9cd5c781a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:06:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:06:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:06:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:06:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:06:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:06:55 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:07:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:07:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:07:09 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:07:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:07:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:07:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:07:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a7b835596f9b18021078e09cc54d8de573b2fc19927f6249a28ab02201dd9f`  
		Last Modified: Tue, 30 Dec 2025 01:07:46 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4a90f3837fe0bb3069dd119a00d406a3b46b76d2c253a02da007b27495f05a`  
		Last Modified: Tue, 30 Dec 2025 01:07:38 GMT  
		Size: 19.6 MB (19632145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6993c2e34340a9406b94d41445caa69e0a154cfbfbbdeae0da09f94f29e16c`  
		Last Modified: Tue, 30 Dec 2025 01:07:37 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9b250920759377c7ca85057faff5590748597f30cb30c32920d2337b67ec5c`  
		Last Modified: Tue, 30 Dec 2025 01:07:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e1df4273bbe7659f6bdc639f6cae463be2465b8c380cb3471b52c9a7af1658a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b73489283ac9c183e66f448a10f991294ee95c684a3e9570751566ab07d643`

```dockerfile
```

-	Layers:
	-	`sha256:0a44fdc5aef1f60c7dc4362f69609b23d0ff30bc2e5aa05387a5474bbaf46515`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 4.2 MB (4232080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58073b3cdb74d152252aac34e25366a594135df4891021c2d6616d226af91841`  
		Last Modified: Tue, 30 Dec 2025 04:35:06 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d7b7301ef71dbd8deba40f500d4e3d38d73881b74d633fcedfb8fa889b92de43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168477631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc32f5f19349b8dc40d158169bdd96f8e150b6be88487df33804779b6cf9dd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:34:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:34:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:34:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:34:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:34:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:34:57 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:35:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:35:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:35:34 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:35:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:45:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:45:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:45:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9547de7380c379be8e2439a1f5f5648ea7e4adf222d1cde7b039d2d494b72f2`  
		Last Modified: Tue, 30 Dec 2025 01:37:19 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbc182c554299dfbf58a08793b74bd62a59a4ba8ffa2a25d0e3a62fedcdc5b`  
		Last Modified: Tue, 30 Dec 2025 01:37:16 GMT  
		Size: 20.0 MB (20021642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb9a2063afff667832f66c1402f909accc292f43cff781ae90caef5c10568e5`  
		Last Modified: Tue, 30 Dec 2025 01:37:15 GMT  
		Size: 4.5 MB (4517775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8342360c68ec5e731e64065641eec7db689b6acd13129a4ac1b9c55962d4ab`  
		Last Modified: Tue, 30 Dec 2025 01:46:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3335beff8a4efd3aac3cf18c5beaa2c9193ec4c7d7eff8eeaeadeec92c6d595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53374a2d85c5430f6197ce0b834601dda750c74c991231a51da5070c88f99d04`

```dockerfile
```

-	Layers:
	-	`sha256:86544e0d097776377b0d194aa9900204c07d7b4dc5e770629176e317a920c969`  
		Last Modified: Tue, 30 Dec 2025 04:35:11 GMT  
		Size: 4.2 MB (4235589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17d60ca06d1bb23de3106a58fd48d13a1830b106a236f48f645a942de54c58bd`  
		Last Modified: Tue, 30 Dec 2025 04:35:11 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0ef33deac8993b2e930396bfce7c174880f4e6155e0d7fd6767a8726ec2985ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159329285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497744d19a9eb4fc88c2641b8e613740beb16f1a5a53ef1b8a5160e80267be2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:06:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:06:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:06:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:06:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:06:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:06:49 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:06:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:06:59 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:07:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:07:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:07:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:07:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59357e56c5eabe42db724069fed8dafeb8cd07f5df0a3442d2e90ddf3c2420d6`  
		Last Modified: Tue, 13 Jan 2026 03:07:43 GMT  
		Size: 88.2 MB (88210715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411d89beacc1eab403def0f739ce5bb2ffe595713cf115a57fe38ee79d77a4d2`  
		Last Modified: Tue, 13 Jan 2026 03:07:35 GMT  
		Size: 19.5 MB (19461965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91719c9bbd000ff6bb1019da1267a2fe1c4a58a951960f94787ff9ab34ea56c`  
		Last Modified: Tue, 13 Jan 2026 03:07:33 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc130f3bb21f7630d99918a73895a6ec682c26d04e3be0539b3097b348f7b0f`  
		Last Modified: Tue, 13 Jan 2026 03:07:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4484bad6ab8a69ec41b2eabe452f3137634d36640e5c05a76611506efa3e22fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd190af098446bda19c412a95e19b60b4289cdfb63d4f283cb2ea93bcde6bc9`

```dockerfile
```

-	Layers:
	-	`sha256:654598804542b9b1cabe46f708c690a1c5924bf9618d2a1ec07974c584391e38`  
		Last Modified: Tue, 13 Jan 2026 04:35:17 GMT  
		Size: 4.2 MB (4227401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7de8cd0b345390fa23d33c07a9d273c83007aea6bcfffc3ef4784f7f9abc2c`  
		Last Modified: Tue, 13 Jan 2026 04:35:18 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
