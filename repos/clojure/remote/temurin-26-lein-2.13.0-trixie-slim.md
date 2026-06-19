## `clojure:temurin-26-lein-2.13.0-trixie-slim`

```console
$ docker pull clojure@sha256:3ee361fd1fa30d3ddb13f6bb3952cd2d587816fe58fd9da9e1c84416af162e18
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

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c313345747419c221ad68ecc999edba0e4e2fa5b4a990e5ef041cdf035bc534e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145568671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8d335d0e2e0f818f9a1e4f0ed0d0969620fc292b49f3b53897dc80a9da56ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:42 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:42 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:50 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:50 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dd40342dfbc320834a0796d624afea859146fa4ffe66f0c26d8222edf35829`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 94.5 MB (94524351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b45059e48d062b240a6cc4399ae3ac67bdc99fe748b0896a63db551a9c76760`  
		Last Modified: Fri, 19 Jun 2026 02:23:08 GMT  
		Size: 16.7 MB (16743305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22d2eb6ed5424aaffc3b6b276860dbb333732b82d329ca7ebee937d54290d52`  
		Last Modified: Fri, 19 Jun 2026 02:23:08 GMT  
		Size: 4.5 MB (4515170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb4e8005b200db54bf7b60b986ba9f7a54ace46b45ea2c18c2ce7374ad801e4`  
		Last Modified: Fri, 19 Jun 2026 02:23:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:37fdb49690941f84b39a0260b388adb7c8eacbfeda018de4b69f63d976b0569a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2416db9cde9708536b459c87789883a02ccd753b4222614d143a0b1f90caaf80`

```dockerfile
```

-	Layers:
	-	`sha256:9c96e8d5748ac5c3b6d379af17b072791ea1d2d194d0cc95c8e19b49683e2070`  
		Last Modified: Fri, 19 Jun 2026 02:23:07 GMT  
		Size: 2.3 MB (2331972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7fb728c92a18711c61d5932792f6888e5e3a5b67fb1325132fc7528a80a7b83`  
		Last Modified: Fri, 19 Jun 2026 02:23:07 GMT  
		Size: 17.7 KB (17746 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21a384bafc80ac871bde4be0ff3e3c31277146b7e1b115f06b904c838c10e64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144880239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023bd044dcdf94e28799a443c221cbe904f41de20577c8ed5b54e92bd2a4c1e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:45 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:45 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:23:01 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:23:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:23:01 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:23:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:23:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:23:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:23:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbecfb1b112c56f04bcb4f86e7427c8f61740d8298dc7a1e35a95ee4fef2033`  
		Last Modified: Fri, 19 Jun 2026 02:23:21 GMT  
		Size: 93.5 MB (93504322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2fd96147fdfd03c9d85ff78dd52fe4c093c9279ca106b8dabc194dd41628bd`  
		Last Modified: Fri, 19 Jun 2026 02:23:19 GMT  
		Size: 16.7 MB (16711742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761999b37c78c43631d2b65cb6cdc3a0ce95da35790c13318df3c568b2b2331`  
		Last Modified: Fri, 19 Jun 2026 02:23:19 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8338dc979a026f5f703366fe3561048ed699ace44b5f03c4c764924ce6bf948`  
		Last Modified: Fri, 19 Jun 2026 02:23:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:10551aa57d278810de1d471540c11ffefc9855e5eaf0d5586dedf7591ce68400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa5acf94499eba9f4ba7cedd568c9764a196e23ed7bc373c8765f939e49f0a`

```dockerfile
```

-	Layers:
	-	`sha256:24645affcfe3e45269a6c6ff973325eee941fff91d9ba824eae542493a4800d3`  
		Last Modified: Fri, 19 Jun 2026 02:23:19 GMT  
		Size: 2.3 MB (2331579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c01a5f48effc6188e0e378d5df633f884e310871ab83e3af31eae71aa33dce8e`  
		Last Modified: Fri, 19 Jun 2026 02:23:19 GMT  
		Size: 17.9 KB (17867 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a16c90dec3428859d2697aa9859086278b8cf39ba05b970de230eaf6169438da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148806305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b414b0addaedfe430397f1a8364ec695701019d91ffd06255e65911a4222596`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:16:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:16:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:16:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:16:36 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:16:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:16:37 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:19:15 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:19:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:19:15 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:19:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:19:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:19:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:19:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39924b9a0b3b71c629e701ebc624d301c203a2ae6fb0c2d988f2e31cf6d3001a`  
		Last Modified: Wed, 17 Jun 2026 00:19:51 GMT  
		Size: 93.9 MB (93902069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f128f29649e2d9d5a0b8fd348e65e3a537e206ecbb495a975b39c807dbf1d2b1`  
		Last Modified: Wed, 17 Jun 2026 00:19:49 GMT  
		Size: 16.8 MB (16782275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7a96b5d7f65d8baa2396d9d70b7f3ab51bf12d51e7ad51ac8501766b4ebfb3`  
		Last Modified: Wed, 17 Jun 2026 00:19:48 GMT  
		Size: 4.5 MB (4515190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb3ec8f2301744e4f40a3bbee7efb2ff7885e30aefefa4ee815991ab6dc8dd`  
		Last Modified: Wed, 17 Jun 2026 00:19:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e6597a023415ef0552ab0a02972cb48f28ec996adeee7e1580a84c82ee11dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee806c5890da0d1b1b3fa70139b4a7ceb3c662d14e7c33ddaaa9d1f664d2ee7`

```dockerfile
```

-	Layers:
	-	`sha256:b3d40a3d8d0ab766c27c5eb22fb65275d872e4e4fb797d198564d483984c2a10`  
		Last Modified: Fri, 19 Jun 2026 02:59:20 GMT  
		Size: 2.3 MB (2316888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7171431d86acc089c37b552fbabc0a7d7cea2331991d2ffa88c430260669be0f`  
		Last Modified: Fri, 19 Jun 2026 02:59:21 GMT  
		Size: 17.8 KB (17790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1670a84b79e49b722adf0d3f3fa52f7a5c8a957de79a8f7a4182c427b88653e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141684196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ffd3848b5ff373057e7368b2a73221c170192e96762a80020bd51280970b4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:43:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:43:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:43:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:43:20 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:43:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:43:20 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:44:26 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:44:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:44:26 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:44:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:44:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:44:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:44:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6666b2e16ace3caa508abcb5ec79bee75e0958f8ba96201027e58a0fba671529`  
		Last Modified: Tue, 16 Jun 2026 23:44:52 GMT  
		Size: 90.5 MB (90536964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72373f9bea54f125c54e421b531ec98571436247c37a4bd7edb1d9c269a62b5`  
		Last Modified: Tue, 16 Jun 2026 23:44:51 GMT  
		Size: 16.8 MB (16780284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b482f0a5e2889cb3d9b2c88dd6be0ce04035b5797850b6b4109febd2c3bbcd5`  
		Last Modified: Tue, 16 Jun 2026 23:44:50 GMT  
		Size: 4.5 MB (4515164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b767a37d3ea883572dedbab3bdfe407589e360e5573ea9daccd4a3f80c035047`  
		Last Modified: Tue, 16 Jun 2026 23:44:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72986c6ba60d61e68f9a35fee853d2f4de557bfa37726222386174db1a6187ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13343772efb3c43d5783b09f71306ffe36fb22543336a0fe85dbadf9081e63a1`

```dockerfile
```

-	Layers:
	-	`sha256:4c709a0c8108c0e71fc7276c009826fa6bbac2c41d7eabe8114572f021e1103d`  
		Last Modified: Fri, 19 Jun 2026 02:23:53 GMT  
		Size: 2.3 MB (2313585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cd68aec50853c2914a3ec7ce75b6f5e2adb98f35b9388fcef593f3e2994874`  
		Last Modified: Fri, 19 Jun 2026 02:23:53 GMT  
		Size: 17.7 KB (17746 bytes)  
		MIME: application/vnd.in-toto+json
