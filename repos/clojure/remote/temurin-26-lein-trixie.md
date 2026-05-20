## `clojure:temurin-26-lein-trixie`

```console
$ docker pull clojure@sha256:bf96437219afc7cba40d59275513028b318a9876495d729630200147e18d5755
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

### `clojure:temurin-26-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d0dae666dbe7d7dfee1fd5c023ee8c593095157db0d8755bd567e1763c6ee5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166942631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ca00a479789e3e391b81f051ed0881abdf980d6eb36abd864185b666006c46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:01:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:56 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:01:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:01:56 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:02:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:02:11 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:02:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:02:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca65b93dc4c329330669e49a050345db4dbf652cf5cd9083c8cd28b4a049ea1`  
		Last Modified: Wed, 20 May 2026 00:02:30 GMT  
		Size: 94.5 MB (94524363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc46ee28c7316c03156ecc45893d54b42500ac956f05fefeb23ad43a13cf847`  
		Last Modified: Wed, 20 May 2026 00:02:29 GMT  
		Size: 18.6 MB (18589480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9d920410e10399681442de8a4da84256ee8d4c507b228047fdb92c29f15d23`  
		Last Modified: Wed, 20 May 2026 00:02:28 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ac034de9e339c6c5377fbc1959f15e46b3bc972760a279d39eee294842331c`  
		Last Modified: Wed, 20 May 2026 00:02:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:81aedf6dee094d67359b9476b55669a5ae341833dfa4b6d4e30a800fe47e6346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e3f63470609c92f4bc20d912f10c679955f8c6576b07095d8086ac1176c13f`

```dockerfile
```

-	Layers:
	-	`sha256:379da8e44a48a8e54a5822ac947a46af3c56ea22c400bbfd6c3bc9e303c29ca0`  
		Last Modified: Wed, 20 May 2026 00:02:28 GMT  
		Size: 3.8 MB (3781087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad4728d0f53be39b8ecf9b2d7f1dc45426e429fd769c436f2c22d9ff2df366a7`  
		Last Modified: Wed, 20 May 2026 00:02:28 GMT  
		Size: 18.5 KB (18499 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6a123774f68b99841a5430705dec0adb3c9f17af18e0a35f9a93fbdbc73048d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166242345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbab26b8d9dff78518d72b6dde0f9296a94d778a551c8e8e336f4a0681bb9827`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:08:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:54 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:08:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:08:54 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:09:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:09:11 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:09:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:09:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8ec400465f379d2c527e44898ae7ffeaa48020b7270764c9a94f685e0bd091`  
		Last Modified: Wed, 20 May 2026 00:09:33 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c943d80f298268498cf265f58f1cae96e70f4aec54708c2eeb750605f181d198`  
		Last Modified: Wed, 20 May 2026 00:09:31 GMT  
		Size: 18.5 MB (18547597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada0c180af7929fdb8b65d8bf7c052a6aeebfbda883429cc54a06cd2cfbf8221`  
		Last Modified: Wed, 20 May 2026 00:09:31 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ff40d23472864c1b4af6a437f84c8ddf1650e2f99619f6d26c0610cd28c8d9`  
		Last Modified: Wed, 20 May 2026 00:09:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:126757597ec515146302c92faf13ed79b9ec6a464901360f3631dd96fac2a21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf161ae624e278ec77499ab7621df7f938397f59df36824dfcadf12bd1b75099`

```dockerfile
```

-	Layers:
	-	`sha256:508ffb7761b4a956434b5e148fb7adee8b8080258496883507829103f796d1fd`  
		Last Modified: Wed, 20 May 2026 00:09:31 GMT  
		Size: 3.8 MB (3781324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f630b024cf2e934194505475057185e0c2e64f5e5b28936d72e520af8362e183`  
		Last Modified: Wed, 20 May 2026 00:09:30 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; ppc64le

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

### `clojure:temurin-26-lein-trixie` - unknown; unknown

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

### `clojure:temurin-26-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1499060d448d29e4797364c9b4bbec80163db153b52f31735ae5fe74eb1ef66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163065516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0614ecc27d09802e9fc1f2df81abed3e2380f718baec73fcc6205295641644c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:49:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:49:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:49:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:49:20 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:49:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:49:20 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:49:34 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:49:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:49:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:49:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:49:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e78591af633be5c5c5ae98e96de9d0de46d4de5e2027e52bc4a9b36a4f651b`  
		Last Modified: Wed, 20 May 2026 01:50:02 GMT  
		Size: 90.5 MB (90536967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b102f8d9b85e710cbcf5a56478e5d8d3b20d659c4e70e1b273ca291473cca5`  
		Last Modified: Wed, 20 May 2026 01:50:01 GMT  
		Size: 18.6 MB (18630629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960e798d2a75c9a5927b4731dea44019b5e78134f622da61f067f6d7ce8ae196`  
		Last Modified: Wed, 20 May 2026 01:50:00 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bdf2ace86be43d7458ca55de37d23113d0a23233665306ecc9e6708433459d`  
		Last Modified: Wed, 20 May 2026 01:50:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7845372c163b8ff4e93dc21f2b3cfdf225012e577914ed65ef90194821881aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3781199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e059fcb220c9fd6649b4eb9c49809b4b6d5b0652a0334915ae88eac8624fdc8b`

```dockerfile
```

-	Layers:
	-	`sha256:fbc21907f09625d2acc50891c405000733dc2678793ba12fcbbda2ebf22160e0`  
		Last Modified: Wed, 20 May 2026 01:50:00 GMT  
		Size: 3.8 MB (3762700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a447c0664a84b7d448d5b5c412c586e52bd55bb3e66dfa0775acfcbebf6cb6c`  
		Last Modified: Wed, 20 May 2026 01:50:00 GMT  
		Size: 18.5 KB (18499 bytes)  
		MIME: application/vnd.in-toto+json
