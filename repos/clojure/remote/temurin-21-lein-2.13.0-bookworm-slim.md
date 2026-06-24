## `clojure:temurin-21-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:99c5bd69f614fadb381ce182b668955b0042db0474389236113c3f4903d8355c
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

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:471e2b867b83ecb67c5128351012a8c6e7c63989e66b81206d7b691eb578dfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208979200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d6e9770e808f2d75fe26ab6575dd9d3b14fea807cc282c9eeb1169cc394977`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:18:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:18:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:18:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:18:49 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:18:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:18:49 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:19:58 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:19:58 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:19:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:19:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:19:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:19:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ffe70c528142bc97699f590bc407d031b4c542c647cf6d40dcb56b243ff8b3`  
		Last Modified: Wed, 24 Jun 2026 02:20:20 GMT  
		Size: 158.2 MB (158166945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09f30f858803f8742a9a1d155d981b467cc08d23b21872336d9ca95d44d60cf`  
		Last Modified: Wed, 24 Jun 2026 02:20:18 GMT  
		Size: 18.1 MB (18059009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0a93926dd924d2b51c2c1306ee47d3f9598c206e3f9d8055d4b45049fb675a`  
		Last Modified: Wed, 24 Jun 2026 02:20:17 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10245d8aba719957cc01013041dc03b932f83c33676c90eedde3a6430dc55dce`  
		Last Modified: Wed, 24 Jun 2026 02:20:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05a8c3dbe8e8c9ec79e8f99b8dffb43337f83bd9216df9387f26a607c2fee8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080765e1a2eb6305bcf1aa7661097ea1bf45fa8c0d52fe1b8058d32ee05d102e`

```dockerfile
```

-	Layers:
	-	`sha256:73a9ada028898d2ca033fbe37831e7ea772cf467c7fb8782e40271e018c75a43`  
		Last Modified: Wed, 24 Jun 2026 02:20:17 GMT  
		Size: 2.7 MB (2734189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbebed9235c0ed98a3beb65adda85cb8b4121b14d18cfd7d9af755f129701b68`  
		Last Modified: Wed, 24 Jun 2026 02:20:17 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b60297358ed12c9d7ba2e7e303abe2cbbf62430ba77ebc4700da1c614e69a5bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206993717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578352116717e9ff169c4efed35293a016f7df9981f5106555b1c826c5312bd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:25:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:42 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:25:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:25:42 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:53 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:26:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:26:53 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:26:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:26:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd314a99e7a8e6d5819649eebd2a632680c8edd400536d54ec30083b55bc414`  
		Last Modified: Wed, 24 Jun 2026 02:27:16 GMT  
		Size: 156.5 MB (156461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca4823486e35542890dfb1ebc98407abeeaeda86d51b0b29e13d72c1d82eec`  
		Last Modified: Wed, 24 Jun 2026 02:27:13 GMT  
		Size: 17.9 MB (17894445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42b7487b3e93898196bd25f93564eabf6d370a50da9f15366c44e81a5c3fa1f`  
		Last Modified: Wed, 24 Jun 2026 02:27:13 GMT  
		Size: 4.5 MB (4515174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09583ef7917574fdc2804b201c341a6ee709779af7c7553a55b55c44fdfee8cb`  
		Last Modified: Wed, 24 Jun 2026 02:27:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3a45bf9a4991e29d3e387a512bf89faa55e3dcfa6ae9b7c7a35d14d1daf6bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5d76a61fab001d7ea76a91d17d84627b7c89d0f444b1006f51f0b1720dec4c`

```dockerfile
```

-	Layers:
	-	`sha256:da8fd513b4b7edebd72ecfb634803f51e3c69ffca38a3bb5c05091b110b3e944`  
		Last Modified: Wed, 24 Jun 2026 02:27:13 GMT  
		Size: 2.7 MB (2733804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe2c633cd4c456e725ed1423f3e872822f8f23cffdfece5ef5a0e602eb19676`  
		Last Modified: Wed, 24 Jun 2026 02:27:12 GMT  
		Size: 17.9 KB (17894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cc40384948213e5add04f7c8814fccc529ef85e33a9af945d3932103657d5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213204365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d914bdb4526f5f00456c941a3c9981a52aa4bf7eeae19254e32b7e2d3e17a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:54:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:54:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:54:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:54:22 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:54:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:54:22 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:56:39 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:56:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:56:39 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:56:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:56:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:56:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:56:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e41ba91bd198088eadb03a3c25545d904cf2490691f50cad346a585a8741f3`  
		Last Modified: Tue, 16 Jun 2026 23:57:21 GMT  
		Size: 158.3 MB (158343240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22cda46999dab13e1a86484f55ebe6af329cb34c9d7b8669ecf478b6c76d5c6`  
		Last Modified: Tue, 16 Jun 2026 23:57:18 GMT  
		Size: 18.3 MB (18263539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb112f8f8bbceda17d6125b9f026b97eaf83ad53233c90c09661e640ddb2db`  
		Last Modified: Tue, 16 Jun 2026 23:57:17 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7f388087fef03a3df8f2a52d1ed5ead2ac342aa1350e11bd0ec4a9cac182a`  
		Last Modified: Tue, 16 Jun 2026 23:57:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7a2744f9559426a65c2364db1b0fd99b3b315071392b0a8faca92200ae6238c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb31b88820f36d4758439049987b10516e2609cc59a8917b8c0b5f168be96106`

```dockerfile
```

-	Layers:
	-	`sha256:d4c74d7bfe145ee33a6b3e6f38b00c02a3ba4bf5720b02aab39db23462c39993`  
		Last Modified: Fri, 19 Jun 2026 02:49:16 GMT  
		Size: 2.7 MB (2736022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:757a99733dc215ae7a80f9eeb236bd31c576c9ab2ef37e54051923472412b3b0`  
		Last Modified: Fri, 19 Jun 2026 02:49:15 GMT  
		Size: 17.8 KB (17817 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:267c9c509de649e961aa49471644c25ac614a8751d728772e20728d20930173a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196522412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484d9a1995e3fcc1595cd44a830a572b2680b353d45cbba7cf12d46a2b4ed63c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:14:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:14:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:14:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:14:43 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:14:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:14:43 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:15:43 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:15:43 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:15:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:15:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:15:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:15:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5826e9d8424a8f27820a67c0c7ea6c7db06d965fa6dbb950d7b53496a99d834`  
		Last Modified: Wed, 24 Jun 2026 04:16:13 GMT  
		Size: 147.4 MB (147388430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88324342bc202dba8de270bf82986504a23e5bc09eb012f37596c6900424883f`  
		Last Modified: Wed, 24 Jun 2026 04:16:09 GMT  
		Size: 17.7 MB (17724787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2cc5563f4c58cdaa854dd687e078c1c4388367591882fb544d88e766203e83`  
		Last Modified: Wed, 24 Jun 2026 04:16:08 GMT  
		Size: 4.5 MB (4515181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21d65e32e71dcf3329c271795c5f6ebe72507a6fae1dbcb5d0ccd54169c22f8`  
		Last Modified: Wed, 24 Jun 2026 04:16:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03df423f49d6557ecdf500f64790a3f4e09478bf5b894aeb5bf9c1ea7fd8854f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2743776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a4ee11051beec01a1c1a2f6b13d40b7c9f5ff2bc0a521543fc943ae7b82184`

```dockerfile
```

-	Layers:
	-	`sha256:1a9758c3857f25090207f551272d5d3b4668442863bdc6e2a161f4a0048b4a68`  
		Last Modified: Wed, 24 Jun 2026 04:16:08 GMT  
		Size: 2.7 MB (2726003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e702904a682fefa52186de4ae950b6b17012b602f3b189cdf39c155b822af0`  
		Last Modified: Wed, 24 Jun 2026 04:16:08 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json
