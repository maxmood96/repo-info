## `clojure:temurin-26-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:c262dc6516e7a400521055ec5f20c40e7f2e129fb9cc7254254e8e21f9955aff
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

### `clojure:temurin-26-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:56b8be90c4a48295f23f9b31648059160d89dda08e7e8ae8b4c1407e68cffe9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144969751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2df2bc7f514645b289c2ba74d509d2ec2d716e6109dfb4dc51d1a60d87f142f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:19:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:12 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdca31400182160893849da5f98ca5a2b7b2aa66f9f207a9835680bec2e48d2`  
		Last Modified: Fri, 08 May 2026 20:20:33 GMT  
		Size: 94.5 MB (94455690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efde03e5389d8b897970db4224693105783a8547ad8376dbc9b835fdf48660b`  
		Last Modified: Fri, 08 May 2026 20:20:31 GMT  
		Size: 17.8 MB (17759607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a744a2b2f31c574d88d9c8c92526fc89f0a77da39d6498d115f3cf1daea38bec`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22c72666a4dae24cf9d90282c836b5258855bedf95aea610a100cdea05bd2c5`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddee3fbcd780dbf193a6c7e4ca1b6e3d4ae04a9391203ff43c4506a8729bf047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a93c5fb74e65cd0bc350cc5b3b26df5ac01a85e7b26215931d435e9e37150d`

```dockerfile
```

-	Layers:
	-	`sha256:c5e790896748760d4024352fa3ca028d422ecceace2befc865480d59d900efe2`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 2.7 MB (2695554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e8a65a4f3bb1e463bc81a3c9f5d98e6f7d9414e1b1dc0e4abfec590ed943c86`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d5072e7a8a809bfe7c4ec81b0c76a447373aee921d9e86d7fbdf5c7e33b0c3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143622556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea219d17398febedb5204aeb1f77b70eabc5554faa0457724b38c0f1354d9d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:24:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:13 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:24:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:24:13 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:24:27 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:24:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:24:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa77059db8b13ea59cf0d8bd2dded1f226a229812a79a8f7250a0252100c5ce`  
		Last Modified: Fri, 08 May 2026 20:24:52 GMT  
		Size: 93.4 MB (93395168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7baf3c91e756cf4a16b581f13c48030c0beb7d5bc2530ed18f90edf338d26a2`  
		Last Modified: Fri, 08 May 2026 20:24:47 GMT  
		Size: 17.6 MB (17593045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf7aeef5a51ad8c6000027b0301d9e97b67cd4036dac465bb9f3dd9e800d0d4`  
		Last Modified: Fri, 08 May 2026 20:24:46 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0176f9b59306e6e6fd09907e512751d770bc1d1b1ebb97841910ad211f4641a6`  
		Last Modified: Fri, 08 May 2026 20:24:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de958ac20c87a20ce25228c7dce24e74fdd33670024c12810d89625b034e93bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56352f8217538ef872f3201af720ad3b3abb620039c73720e34c8ebc12c4105d`

```dockerfile
```

-	Layers:
	-	`sha256:00d204ae76449c6f7e9fd8826d8b4df662c9e4a5ba8b14295c5c79f2347c5c81`  
		Last Modified: Fri, 08 May 2026 20:24:46 GMT  
		Size: 2.7 MB (2695166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a28391602cc5108afce072341c5dd57c1e34201d50f334238c00bf02281f455`  
		Last Modified: Fri, 08 May 2026 20:24:46 GMT  
		Size: 18.5 KB (18517 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:41812fdbeb0cb18aeaec8fc0da10ac2be5f8554a9a1b9880dad956c590e0cf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148339446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec588f0dd4538bb2ee7a810e7487032da1a017cf00801a28c52382f78987b1cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:51:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:51:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:51:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:51:10 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 08:51:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 08:51:10 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:51:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 08:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 08:51:40 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 08:51:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 08:51:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:51:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:51:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30eb4eb9b2f7105e84346a7caa4be9f9fac688f33aad32bc25bad332349d4d4`  
		Last Modified: Wed, 22 Apr 2026 08:52:19 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0216fec632526879e7fefc2055d24b1c95258be4c260ca065844375b199036b3`  
		Last Modified: Wed, 22 Apr 2026 08:52:17 GMT  
		Size: 18.0 MB (17961379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a80ebb5e7b187dac71f7cafd7a33981cf2ba3bfd761ac436e1fdcf1578cda3`  
		Last Modified: Wed, 22 Apr 2026 08:52:16 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a5feab0635dcd3e53ee9aa1fee3412e4cb6f0ece23f3262c051c7317bc702c`  
		Last Modified: Wed, 22 Apr 2026 08:52:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f7b768e907807d103ae4fdfde75f9c6c771aba297a484202dc50b92c2f31526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ff4e1dbe4605af1c59d1c99fbfbb81796446063f5e16bd4271bd8c15f3f4e6`

```dockerfile
```

-	Layers:
	-	`sha256:d4adc9024c63f83dc79330c8e6c757cbb187ef9ad0ac63bc343778d1bfd30416`  
		Last Modified: Wed, 22 Apr 2026 08:52:16 GMT  
		Size: 2.7 MB (2681323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9ae2ea7ac798e73c71c810f68e28f80cf940a9660151d0c9c1acca6e5bbebb`  
		Last Modified: Wed, 22 Apr 2026 08:52:16 GMT  
		Size: 18.4 KB (18440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:67019daa984f0e1312d01e37c67ebe13ed955733866699de60975d47a2b6c791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139379497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9414126f9306c2942c149bd5239864187e6bca89c599a08f7b8e3273ce6143`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:20:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:20:51 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:20:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:20:51 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:21:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:21:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:21:01 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:21:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:21:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:21:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:21:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b107cb0db7a1b32111d505e036bd5a5247c7ca1efbd8c49045017953aefc87`  
		Last Modified: Fri, 08 May 2026 22:21:30 GMT  
		Size: 90.5 MB (90547730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f2b81f44971545a2bbdafb60f70b5e7c33b9b649a2da0851fba5ecff2905e9`  
		Last Modified: Fri, 08 May 2026 22:21:29 GMT  
		Size: 17.4 MB (17421990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb96083b8f444b08c128968e01905d8eb375800b22f9c3ab6e51df8735f15819`  
		Last Modified: Fri, 08 May 2026 22:21:29 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3530bbe9e44e1a557a59dd4af6eb760f20c340ce970b04e1d1e8dd5c282866ed`  
		Last Modified: Fri, 08 May 2026 22:21:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:893c6e512fb8b264b54a7d5114aca9c5cc2378d93fef3e93d82c3459b51cb3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8371a0551d2c3eb5001265b0f7fbdcc920e96ffc48414d009b4a460f095cf7`

```dockerfile
```

-	Layers:
	-	`sha256:4b402458f23047197c667824ed23aeda8468da1e99de80aeffac9009cb0eee95`  
		Last Modified: Fri, 08 May 2026 22:21:28 GMT  
		Size: 2.7 MB (2672554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:254ec6dce65b4d63b1fe77d9d92d2a328ba0ece54bb9c15cd69e288b51688876`  
		Last Modified: Fri, 08 May 2026 22:21:28 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json
