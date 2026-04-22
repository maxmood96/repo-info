## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:0be4cc04665a7db1d6317aa63bca1a24d740f9d422122205f6cf6fddf80ef723
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:631100bb54187dd8163c284c11564b2f1476a1c0d5f764232b5687fb57b451ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220716957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d08da936b6075d7b8b70f7253e5abdb107906a2ea14793eba7cb8024d8b47c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:02:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:24 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:24 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:39 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:40 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39fb37449e696f5b6785eb959876bb7b56e795d6b22296a84cffff34e2e14c2`  
		Last Modified: Wed, 15 Apr 2026 22:03:01 GMT  
		Size: 145.8 MB (145806793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69ea13037d2702c1e177576abfa7f4a4eb97a6502422cf0983b7094e596f70`  
		Last Modified: Wed, 15 Apr 2026 22:02:57 GMT  
		Size: 16.6 MB (16629645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b23ff2a5ae64b2b9e5231edd2892406a660dd8f2011c5624560ee4c15283fc`  
		Last Modified: Wed, 15 Apr 2026 22:02:57 GMT  
		Size: 4.5 MB (4517694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3c60f9b65380efcc6ebb3ebfd33b450f1650984e80b44ca37dc4c84705f9d812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a5050bc8437617df1b2b669d7eaed11e8c07e388f3f395572ff8ca55628b05`

```dockerfile
```

-	Layers:
	-	`sha256:7e0fb3a973d837d95b2e5cd95d01308bae3e3e3574cafd0f5f43bdea18458ae0`  
		Last Modified: Wed, 15 Apr 2026 22:02:56 GMT  
		Size: 4.5 MB (4506003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa78201d7cb314b8e5db249fe3d6941103ece00efe099300fa221bbdf591fc7`  
		Last Modified: Wed, 15 Apr 2026 22:02:56 GMT  
		Size: 16.4 KB (16381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6ef52a7f88813086128241b15426e869ac2507bd8f88303a5f3be2817520ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215888128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a5cf7a6ffe8096956954d82375d238bd955cd73c58a3cb020acaa98808ec8e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:28 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:20:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:28 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:20:42 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183365b28572bda7df329b76ef6388c23ed6c0b2500e11b32f3bd486be70327a`  
		Last Modified: Wed, 22 Apr 2026 02:21:08 GMT  
		Size: 142.5 MB (142500831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdfd663d8d0b70c8bbd1bf33e2770029783bdd38804cf79153354f394d0a836`  
		Last Modified: Wed, 22 Apr 2026 02:21:05 GMT  
		Size: 16.6 MB (16616515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85d9e58e8596aab346dda2526b221b816cff9ae8308ca19912438b948fd59a0`  
		Last Modified: Wed, 22 Apr 2026 02:21:04 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:afac90cd84a668fa7fcaf6529b93d34b11bcb242885fa98a2020a5ed1be6ff29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01545f13ee2ff1b160a82b1e662cb2758315895bef3c65b26432b88d17776d92`

```dockerfile
```

-	Layers:
	-	`sha256:29471b814f04301a08d1fe0fd448b03c5558879009a3d262e0b888bf907b7be0`  
		Last Modified: Wed, 22 Apr 2026 02:21:04 GMT  
		Size: 4.5 MB (4505595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f6993e51a3470b4f96240027a08b935a136832d7418d8f2350cd99dae2ca10f`  
		Last Modified: Wed, 22 Apr 2026 02:21:04 GMT  
		Size: 16.5 KB (16501 bytes)  
		MIME: application/vnd.in-toto+json
