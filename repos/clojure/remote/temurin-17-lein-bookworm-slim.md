## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:917a4d61cf50e91e073251a788c17392af42f221facd9bb018aa98237899ab0d
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

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3304d1c2e034398bf5147457cc067c80a49ceeae47f443c3ccc48cdefe7043bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196717918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e117deb9cbd553a66aec2a95812a590af3a51d40da31d1bf5fd005e181bb3d16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:34:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:42 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:42 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:51 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:51 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16c629b98060f1863731b3c6088b9f0d2e0f17f892b39dbf067ca09116e669`  
		Last Modified: Tue, 16 Jun 2026 23:36:11 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1be9ede64e821f85426eaaad3ea1273430d5af8a278457dcfb601d4cbf9fbc`  
		Last Modified: Tue, 16 Jun 2026 23:36:10 GMT  
		Size: 18.1 MB (18059188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764adcaf154d744fcf1e7f60cf52d2077174cfb14d05e10bdcae027811c7f138`  
		Last Modified: Tue, 16 Jun 2026 23:36:09 GMT  
		Size: 4.5 MB (4515224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc0e0095096eaa0f7095fcb0e8437842813398190fb3a68ea33f0cb0f4d4a6b`  
		Last Modified: Tue, 16 Jun 2026 23:36:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:abbc1581f4f87f87a3c0116584e3af1258ea6fea4fbe977e26680cf7e13b5032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ee98ccb1e75296a3ba31f1a5d7a4bd77b21aad1df0d84f4cfbfadc3a54e307`

```dockerfile
```

-	Layers:
	-	`sha256:a3a5b39fa34dc18ef815627450de3c1052a88c2ed32b5ecb978b3cfde60dfba5`  
		Last Modified: Tue, 16 Jun 2026 23:36:09 GMT  
		Size: 2.7 MB (2732337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e7994449be3bf67d90bf8244372a778406fa5e36c9fe8f9e287b4b8fecb0543`  
		Last Modified: Tue, 16 Jun 2026 23:36:09 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc775cf25d6b1dbbde22cafda5a9068476763c9ea73bfd4553cd3fc939c3139a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195256528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedc3a3634bf2950505296f79bc11006e284a93016dad03890b729ba51443d01`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:34:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:27 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:27 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:34 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:34 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9090a7e8ccc0dff80117025cdae6e2ebdb149728f45adafbf341d5381348d6`  
		Last Modified: Tue, 16 Jun 2026 23:35:56 GMT  
		Size: 144.7 MB (144724405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b558a86d31aceac021659732535a3e58695d8aee54946e0400ff702d26643c`  
		Last Modified: Tue, 16 Jun 2026 23:35:53 GMT  
		Size: 17.9 MB (17894165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c028d45cc100d45531945526645326322ee7e9e06c1ace967f3ede3edd5a5d`  
		Last Modified: Tue, 16 Jun 2026 23:35:53 GMT  
		Size: 4.5 MB (4515221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb40d3db600db7ff36b02f5bbd68924ab4e29a173bf590916fb656ebd1e5726`  
		Last Modified: Tue, 16 Jun 2026 23:35:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c14316b5c57b183def10987cc74c2c34631ba7cdd69a6367a6bcc50756e1337e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2628ac64d62fca52ab28964ebd48a87de45862d6b4a05b4a165f5fa8bf67159b`

```dockerfile
```

-	Layers:
	-	`sha256:9d453e53f0488cf8efa6ff90b84a8927e19254a21c0bd670ebd31074f8a3efc3`  
		Last Modified: Tue, 16 Jun 2026 23:35:52 GMT  
		Size: 2.7 MB (2731952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bfb209468626cdee1fbcecddaee1521d4b471da17d55de21d900c64e3af9551`  
		Last Modified: Tue, 16 Jun 2026 23:35:52 GMT  
		Size: 17.9 KB (17894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:104f2921e134941c4983842895d35a6148fcc9c48d1d1ec4f3f285b8257b6747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200627317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953259df767e7119eaab12113a40511fefe8fe02f046f0a847a1c7b73d0d2a4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:44:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:44:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:44:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:44:51 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:44:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:44:51 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:47:25 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:47:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:47:25 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:47:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:47:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:47:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:47:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f05ba64318496d6a3ae538f5f13df3b1a61470e5478691742379b371d284481`  
		Last Modified: Tue, 16 Jun 2026 23:48:02 GMT  
		Size: 145.8 MB (145766120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c19c6aacb702b0435bec709dfd92b2e263c04a6cbe7d75270beeb3ea9dbe7e`  
		Last Modified: Tue, 16 Jun 2026 23:47:59 GMT  
		Size: 18.3 MB (18263598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba90d69313b4e9422fffc29f9c1e925bd36773879cb9f69063e006330032ade`  
		Last Modified: Tue, 16 Jun 2026 23:47:58 GMT  
		Size: 4.5 MB (4515228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c8a0439b5430fbbb2799b9adb5c0f2d781543601e84a2d15682b55ba96f4a0`  
		Last Modified: Tue, 16 Jun 2026 23:47:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6bb23f5b45b94c9cb9a5bb55e68544ba3921ad825922366b3698b27d816b8bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0af004c108641ecc52add681c6e13fb92c273ec7a35cd86fa2567f712c6ca64`

```dockerfile
```

-	Layers:
	-	`sha256:db20a1c6803827db7e47772d468856dce8ebba4c135cbae169a9d310eef34772`  
		Last Modified: Tue, 16 Jun 2026 23:47:58 GMT  
		Size: 2.7 MB (2734170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5daafdcebf0ec6a95ff4eb681600d79d4310684ed23799e5cadec91bad62040`  
		Last Modified: Tue, 16 Jun 2026 23:47:58 GMT  
		Size: 17.8 KB (17817 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:be9b839d087347b360ee1b94fe8c20de412da94e422713371cb516058b542105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (185044359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f63b4ba67bc08f1076d6b89e1625ebb7ed558029cc2561f2adb104033e9569`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:33:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:58 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:58 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:01 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:01 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becefd1450c68498f50f057ef82533009b9d1f4f9319b0a1d01244b208c27792`  
		Last Modified: Tue, 16 Jun 2026 23:35:30 GMT  
		Size: 135.9 MB (135910409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44215ed223a4f893b823176a2740a043ebe5698098d1916792370086447299b7`  
		Last Modified: Tue, 16 Jun 2026 23:35:28 GMT  
		Size: 17.7 MB (17724815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0087ac664eaa6f94757efcc5c5b5be050a6c479c559117d2032a397b13cd5475`  
		Last Modified: Tue, 16 Jun 2026 23:35:27 GMT  
		Size: 4.5 MB (4515196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f831f055d1733f6f5d063d0bf5c45022bc677cb41c94a66efe4cde2edd9f1f9`  
		Last Modified: Tue, 16 Jun 2026 23:35:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:694b4cd6d29fccbf38f6e9da80798c7ad022cc3a85eb7c9ec015ddd84dea302f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2741924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0348dd2037499113643a8e1fb566b72105a1981a6b4bbb26e1d080ea815f99a9`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1efd39a399ab62b850a7842aa68bf509ca83242be69c5a5421a7d080e675e`  
		Last Modified: Tue, 16 Jun 2026 23:35:27 GMT  
		Size: 2.7 MB (2724151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9810cada35123955b434cfd3e7d52f087345234180861994d18535069eedcfec`  
		Last Modified: Tue, 16 Jun 2026 23:35:27 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json
