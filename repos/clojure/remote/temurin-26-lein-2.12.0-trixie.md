## `clojure:temurin-26-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:75f2f37c7cfe35ca23d6e597c76cc4c0eb5aec7b916b8e97c67793290cdd3b3e
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

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3ca1bae3936b50e8b28064fcb6c1e24b112e7bb97cd288f6402a2ac35566bbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166930419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70136902dd0755ca09d22b58063df4c1440f5a3f98800b814d210b4e7c25d546`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:36:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:41 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:36:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:36:41 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:56 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad5e51dea3dfcca0f34e53661fda97f440747b586674c210ea5fa943e8472cf`  
		Last Modified: Fri, 15 May 2026 20:37:17 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026331ebb4fc209dcd6b2b2f476d27440ccc13b44c332c4cbd9cb682a23e1ade`  
		Last Modified: Fri, 15 May 2026 20:37:15 GMT  
		Size: 18.6 MB (18585596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f695bdf061a53f43aa2b6eb5b9e35b725002e4d0add376ace65d6748b06eae0b`  
		Last Modified: Fri, 15 May 2026 20:37:14 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d5490c28f3c3da7f08fb1fcd37eb3302bb83f12419cdc4de6f7b8b3e7b95f`  
		Last Modified: Fri, 15 May 2026 20:37:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:449c4344619e83212a998c6c41a5066dc9bee3be6f4855c2ed1b2e258b629e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0963c584f2c75aa9f366a04be27cd81468e680e60ddbaca0cff5518c0430658`

```dockerfile
```

-	Layers:
	-	`sha256:295d3dcc353a3cc4896c6cc6adea00919c53a06ceef741fb2f1402c0b2fb420b`  
		Last Modified: Fri, 15 May 2026 20:37:15 GMT  
		Size: 3.8 MB (3781045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4706d25581530af54bbebb04f35e89e98562a7358a39735a969d52ff0d8c026f`  
		Last Modified: Fri, 15 May 2026 20:37:14 GMT  
		Size: 18.5 KB (18499 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6425f2c4440257ef999c211144972380bf8d74c5b51b5d01154c1ae5a4422fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166237616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318091a4120706991b568c6ce6b8564268c33a5fa6dab590c7b44da82f10deb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:36:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:30 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:36:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:36:30 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:46 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae722db48b7644997ebf4e397c15e3147b3970965310907cce1708a06d31b28`  
		Last Modified: Fri, 15 May 2026 20:37:07 GMT  
		Size: 93.5 MB (93504390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e66961e9fffa850aaab056c8b6a99a6c1ea0e84269b596e810deec9582422c`  
		Last Modified: Fri, 15 May 2026 20:37:06 GMT  
		Size: 18.5 MB (18545603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd604f1f1b3d77b3d22f96de11584533b59918fc5178b0912a1eb5c6f7c99e3`  
		Last Modified: Fri, 15 May 2026 20:37:05 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d85d2567188263ba1ddc5f651116121d19a6d436603c14013d2d1a373b504e`  
		Last Modified: Fri, 15 May 2026 20:37:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dffd994fd016e1e9f8c0bbced9cca633b7040968e5675aa33c08d330b53e80f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb391b3f0efac3ade81631d5f90ed7ee8618a575dfcb1bd654a188933e559b60`

```dockerfile
```

-	Layers:
	-	`sha256:1472a107bb9a922bdf3950499de86acfdb0b0429b87a133640374854b8785eff`  
		Last Modified: Fri, 15 May 2026 20:37:06 GMT  
		Size: 3.8 MB (3781919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4768fa6596ffc88f9e46952576b2772245b3e21afa38cc59860373f4980c10a`  
		Last Modified: Fri, 15 May 2026 20:37:05 GMT  
		Size: 18.6 KB (18619 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e7361fd6f7c2f9752efeda19c353e8a79c3dae6c5a21d98c74c612fa5f7ba8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170184575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2fd09184f25d7e1ba1bb138b5584521113698b65c7c61cc2822af868c18efd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:47:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:47:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:47:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:47:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:47:27 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:48:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:48:03 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:48:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:48:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:48:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:48:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ae203a513e0c8b74c981e5684b8f31f4776f60d5e19fb39186eaa7bfba6fe`  
		Last Modified: Fri, 15 May 2026 21:48:46 GMT  
		Size: 93.9 MB (93902122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eb9f1fdab41e85cad5cb583eacb6d5482a1e1000512f8fffe118147999ccd7`  
		Last Modified: Fri, 15 May 2026 21:48:44 GMT  
		Size: 18.6 MB (18641109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cb302133a9346d38616e5faaa62c6ca27745d4d777390bfff2889c4e725c75`  
		Last Modified: Fri, 15 May 2026 21:48:43 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7671545ca07302b4d7b081eefa17757ff383301ed0d40571a3a845ae51dd3e1`  
		Last Modified: Fri, 15 May 2026 21:48:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6734950197ad4e5d055cd723c89535a145b16292798103239e9bcf95a50223f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac033ac77c2e572029ca256598ce659c83410d02d92df9afcc5f6eb67d5a994`

```dockerfile
```

-	Layers:
	-	`sha256:27acd6aeb4c2cd9dceff4a1d443fcd61ba1e04c5e6acde4c56c5f7f8f5d40b25`  
		Last Modified: Fri, 15 May 2026 21:48:43 GMT  
		Size: 3.8 MB (3765981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88a79aae3165e9abda23ed71298f524dea1e1f9ec07ef0a66ccccd9796d3130`  
		Last Modified: Fri, 15 May 2026 21:48:43 GMT  
		Size: 18.5 KB (18543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e420e2ae0f53094229206251a5fa41b76290fdd70693efe7da13f2d4425380a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163054387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619334dcf70b031dab6a0599858f68c9b03379f75b68a6831b143576d8b0db49`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:29:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:29:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:29:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:29:24 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 21:29:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 21:29:24 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:30:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 21:30:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 21:30:15 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 21:30:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 21:30:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:30:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:30:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b45323254ce3bd87b7d048e00f69b36859e12f3173f4f96cdebb3ea0b71fbc`  
		Last Modified: Fri, 15 May 2026 21:31:00 GMT  
		Size: 90.5 MB (90536948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6a047cc97bb63d42d2e75633b37d6f980702072d9ee6bb155844a00d044edd`  
		Last Modified: Fri, 15 May 2026 21:30:54 GMT  
		Size: 18.6 MB (18626958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48fdc7e0d06005c7db784f0ebd6d4a756d4eaeca0d63ce1c2e7835f1f06de88`  
		Last Modified: Fri, 15 May 2026 21:30:53 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f327ecd6e5ea1ddfb45b9bd393b01723bc3091adfc8cb70284278649f56234e`  
		Last Modified: Fri, 15 May 2026 21:30:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d768bdcf7ef5864d2a316af66171e0e6894a8d4076e57364780f9263bf998ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e83abafb8e0893a2458bcb363e9db4e05a83bb42daf1acdf0fa1cf2ac5450`

```dockerfile
```

-	Layers:
	-	`sha256:8a348da58e70db92aa9ac9d9e3b03c47d184e67cb1b02da2f8f6869f942a5561`  
		Last Modified: Fri, 15 May 2026 21:30:53 GMT  
		Size: 3.8 MB (3762658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f6b7bd39a65e3fb4d52ab20c930b749cf72903675204289ceac91927e3876d`  
		Last Modified: Fri, 15 May 2026 21:30:52 GMT  
		Size: 18.5 KB (18499 bytes)  
		MIME: application/vnd.in-toto+json
