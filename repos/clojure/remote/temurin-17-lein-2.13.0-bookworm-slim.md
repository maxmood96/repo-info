## `clojure:temurin-17-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:32eeef18e37962608b33c43816c741e311f9d8a3d40fad76a0b213502077eacb
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

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:23e09f2796720db3f464c01e4bd96464f073929fd6ce855127c27ee68b6316bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196717405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab2df41cabb6195e8bd60b22eb6c83789fd8c2a503efde88e6f61822abcc417`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:48 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:48 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:58 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:17:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:17:58 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb9c32641b215bd65149564c129342e3d4eb5f64a3511aac23e9e5291bb8e5b`  
		Last Modified: Fri, 19 Jun 2026 02:18:20 GMT  
		Size: 145.9 MB (145905426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c956e56614d4fb30289f1cdd9068cfb97d92fa3b1be2e1286265187ab1dc796a`  
		Last Modified: Fri, 19 Jun 2026 02:18:17 GMT  
		Size: 18.1 MB (18058711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894222a62b11dd4cf55e59f420833fe975d7410004b08949018f7ba1b08dfb5b`  
		Last Modified: Fri, 19 Jun 2026 02:18:16 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a8f7d08e398438c7d3bf4a46cbc28bd418aaa524ffba68887d414c9d73e126`  
		Last Modified: Fri, 19 Jun 2026 02:18:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eca4c61a9524ed10a8a0b2e01269d558773bd6adc40285dc87093dbf57756e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea41763dabd0d643e46c5c47f3faea1e8d2a814d17119fa670cced6ba8cef633`

```dockerfile
```

-	Layers:
	-	`sha256:b203b1eb0aafc8bf6439b6ae0bcd4c5159e3fd8ee0611ffbffd70512f7c8e6b4`  
		Last Modified: Fri, 19 Jun 2026 02:18:16 GMT  
		Size: 2.7 MB (2732337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a486f18d19ed36a3263554f3e7093abaf296afc115816cb2ceeb8d57381d069e`  
		Last Modified: Fri, 19 Jun 2026 02:18:16 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b20fb6d65fc7a4695ceee041664e1a2de2e215d4fc9430f82546ad50e30b08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195256405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110a5587a1157ddc00e47aed37bcc1416958fa4e46b9f2f37543000090498abf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:17:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:08 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:17:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:17:08 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:14 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:14 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5fb09eeba2aba8e38ba8222e169a3dc2c52a0f1df9d554f9afb9e192c69c11`  
		Last Modified: Fri, 19 Jun 2026 02:18:35 GMT  
		Size: 144.7 MB (144724342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9043014f78151a83024634e0faa4c014cf8063ff96046ca7013ac14b1c6e9e`  
		Last Modified: Fri, 19 Jun 2026 02:18:32 GMT  
		Size: 17.9 MB (17894126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3848bffe6555ba2113b71b67880d3b6e86f756b734e45fb18bffa951b1bf742`  
		Last Modified: Fri, 19 Jun 2026 02:18:32 GMT  
		Size: 4.5 MB (4515201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442e606049fea15ee74655f1d42c351aca46dbb350da3caa1718091eba3350b6`  
		Last Modified: Fri, 19 Jun 2026 02:18:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d16e6438486ef3bc417e5778ba820b7493c030e8665aa0e581197e4006faf5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144629a9cfa3a9eef77661191bf8077ca7abf43563450509b5dce155bc5af068`

```dockerfile
```

-	Layers:
	-	`sha256:26d92574c075ca5af82d6f862b62bde1c01348b3311aadd928eb6c6fd210550c`  
		Last Modified: Fri, 19 Jun 2026 02:18:31 GMT  
		Size: 2.7 MB (2731952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070ff64d544ab6faf9d7b22c5ae1336da8daf6e29431c5236a83923b1f76074b`  
		Last Modified: Fri, 19 Jun 2026 02:18:31 GMT  
		Size: 17.9 KB (17894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:93a727013f1fd2704f8b6b6a6def79f27cbc8e499d486544a370bdd241748eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200628124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5c3ef3d3d1710b2472a47813f5aedb8430980ceffa30fc1b299c4f44084de0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:36:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:36:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:36:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:36:44 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:36:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:36:44 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:39:43 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:39:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:39:43 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:39:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:39:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:39:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:39:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a8b1fe08cbca6cfbf84dcf1035227586f8c0a013a520d08ca8f1bb6f1baa7`  
		Last Modified: Fri, 19 Jun 2026 02:40:33 GMT  
		Size: 145.8 MB (145766212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b9429faf06a6a931fcef324548560e9d32258e57b641ee3dbb734991114222`  
		Last Modified: Fri, 19 Jun 2026 02:40:30 GMT  
		Size: 18.3 MB (18264317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d3ff347e392f913353f35894537b62ca405c4cee7b9a8b913d564c9ff68e65`  
		Last Modified: Fri, 19 Jun 2026 02:40:29 GMT  
		Size: 4.5 MB (4515224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137905a61e4f8bcfce485cff77745059e0d5b7ca2614d760c9d7b63109355888`  
		Last Modified: Fri, 19 Jun 2026 02:40:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c3aa451abe9502b11d992728d892494dc6e384e8753dc519393f5d94b265d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fa7b593547aa559e15e1de8a5b11eec97250e72a921e0c27448f325e91cc99`

```dockerfile
```

-	Layers:
	-	`sha256:fec91cab972426c6d095c5e54ff99efce334cdfbd91a1c9a4966d447164b00e9`  
		Last Modified: Fri, 19 Jun 2026 02:40:29 GMT  
		Size: 2.7 MB (2734170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1ee7abccd29301ed079d7c2c1387605ac5cbba877f9d0be673f6779c199541`  
		Last Modified: Fri, 19 Jun 2026 02:40:29 GMT  
		Size: 17.8 KB (17817 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c292c355fac241b3757881fe77ae2ebfc6782d471def6e2ba3b3c3629ce73246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185044183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02ffda4154db64e0869acd7948684d0ae557ae5d1e5a596e2f67c2602c9d6a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:40 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:40 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:37 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:17:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:17:37 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:17:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:17:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12de02280ae8885a4001fbd484dbfc1d6554fb904cc661889a6e6ecda0108b20`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca2bcd94048a86c6e0e0c7ece80a89ff5d7f968530f75ef3a2e3e78f4297e5a`  
		Last Modified: Fri, 19 Jun 2026 02:18:01 GMT  
		Size: 17.7 MB (17724608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26c701fadb65fc96941cc6b306bfb5ddda9340e3a7e5de08c2a208bb8e8aef9`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fb507f01a3cf7ade72ac7b4af46d7ec2a3830e45b177f8326448bccafc00b0`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2de1aad371661a6f870b0a0a17c197d664046a925330f9b2d2c8cb3b67ef0978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2741924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1949e1ca33eb9564eff5671d555d79e2b15fcd217f9db8a92a9dc403c7ad82ab`

```dockerfile
```

-	Layers:
	-	`sha256:b672d88b15d83ee63f4cd77ed81658ec243517122778bf6b3f890c18ba90b32b`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 2.7 MB (2724151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1637a6d31fb8f391e8021968174cfdf4889bc381f8d644780cc324335a785eed`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json
