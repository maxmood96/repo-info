## `clojure:temurin-11-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:d4e3f107b775af7ed31e51bf0ee8957384f1dd02185d4c0abe177f18e9b8bb02
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

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a85f6392c2c26c4ee8543a069fecc6999f5ec175129a35579d3172d5095894ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196698454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d55aeab97a24eab6ddfbb477b103dd79ccc13a9d98e74a3cb44ea7c6b418ef`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:15:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:15:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:15:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:15:16 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:15:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:15:16 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:16:24 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:16:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:16:24 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:16:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:16:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9b3b28a16693c7f2e6054b689271a69c87de6b1489ab9032cc2d76ef2cb538`  
		Last Modified: Wed, 24 Jun 2026 02:16:47 GMT  
		Size: 145.9 MB (145886165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845423d49d92d8808a4cded13f83332e4a71e3846024622bc220729499f5dd0a`  
		Last Modified: Wed, 24 Jun 2026 02:16:44 GMT  
		Size: 18.1 MB (18059397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc2eb39cd50ad3de4c717278331e13823cf0d7bb3c1b35377bf0fb43073dff4`  
		Last Modified: Wed, 24 Jun 2026 02:16:43 GMT  
		Size: 4.5 MB (4515221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0366507552596942614d761764ad4cb35b6027bb142381a3e71a75d9bde0699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea6ee3e3c61650d6195f6c772bff1bb00d9182f6e19e3edcef21f1c5b3f2831`

```dockerfile
```

-	Layers:
	-	`sha256:9276844b550bee78ec92509ae9fba0c1057888dcb2ca669a55928c3a610b8f82`  
		Last Modified: Wed, 24 Jun 2026 02:16:43 GMT  
		Size: 2.8 MB (2751853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bac0f09fa65247391a7d4e42c7bc4cc10973d18c541f282e9ee8ede5d4e166`  
		Last Modified: Wed, 24 Jun 2026 02:16:42 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5e00359e91804423d4a8e7e500cef291e5fa7ee20a6a94ac11654432a1a25427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193114066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6227dbe7f1c7c177205465fb6ca5bb43f53fcb2b18abcff9b5cc920a6fe727d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:21:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:50 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:21:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:21:50 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:59 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:22:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:22:59 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:00 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea44b0147688fa230ee17bcc5f2a5c23a703bbbeacfbeedcdcbbb3932e2fe23`  
		Last Modified: Wed, 24 Jun 2026 02:23:21 GMT  
		Size: 142.6 MB (142582159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b2fed1c572fd3e105a320c176dc57ae54620b7ea2d10d99bc36eca065a1240`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 17.9 MB (17894284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c3446af466561ee0d48b6ef26b28f9ea997ff0d32a85d68d56827ac671acd3`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 4.5 MB (4515173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f89ce0864f8672b5b80ad4a17cfda218dac1ac7096b4b8004818733483c63bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc04298f8d7411e5b54afe2c62dd50dd3397ac3fe3d3e4502189cd8750a7bfe`

```dockerfile
```

-	Layers:
	-	`sha256:23f1cbfc900e0cabc2b126e4e663d18ee5e02a94529521b13aa19df94ed9f7c5`  
		Last Modified: Wed, 24 Jun 2026 02:23:17 GMT  
		Size: 2.8 MB (2752086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f5ae5fe7b19bc0726e727da420952ac42bc30782da3dd1c1c83b3691bc239a`  
		Last Modified: Wed, 24 Jun 2026 02:23:16 GMT  
		Size: 15.9 KB (15899 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e29922b099f223ea6680f6679244f4044057134243b9fb9b95e1c42802052a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187971311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea9aa7f24ff1292c4da23297b77ff14b74a9095d3ce13529965f3f60b58ded6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:24:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:24:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:24:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:24:59 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:24:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:24:59 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:28:03 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:28:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:28:03 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:28:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:28:07 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09682529f6dcf184fbf2932f1bc6307869164c5cfcc088948da539898ec50cb2`  
		Last Modified: Fri, 19 Jun 2026 02:28:55 GMT  
		Size: 133.1 MB (133110739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef88aa7bcd9b7d613c9b42a86f03c8f380d202a7691a98be094bb485c20f4271`  
		Last Modified: Fri, 19 Jun 2026 02:28:52 GMT  
		Size: 18.3 MB (18263380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4833932f2cd8f6d284f48051b7844168ad645c6b001e847151ec4f9823bcfb`  
		Last Modified: Fri, 19 Jun 2026 02:28:52 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d7f9dda8e0d3e9722e9133423940e23d5faf124874b25ec96249fc391f77862c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2768893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217ea2e0075d65ec1856d21f5f8f6bf6703c0e3b736c9a38529318b04cd36538`

```dockerfile
```

-	Layers:
	-	`sha256:6c13b9e39a7a1b619750a6c7c3318f664397a7104976018d9a2a188b2bc13d6d`  
		Last Modified: Fri, 19 Jun 2026 02:28:51 GMT  
		Size: 2.8 MB (2753071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3628c3b3fa290c45879811060fbddb66485807f6f4a33b114c6bb6299c9d2473`  
		Last Modified: Fri, 19 Jun 2026 02:28:51 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4aa349d262dabc4679d7374360fa3aa5265f350ce9f5560ae238003f86834927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175786015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f68caea4ccc5b607d3c10a71e9769d2119116d8354c11d0e7d9a9f68c69c15c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:54 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:07:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:07:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:09:01 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:09:01 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:09:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:09:03 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894f0ce15fa11bb3c6ca37e7d0ec532b71cf5687d8bdbe22e95582d18a8c14f2`  
		Last Modified: Wed, 24 Jun 2026 04:09:28 GMT  
		Size: 126.7 MB (126652580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda1a856d12e231d47366145fbd4299200fdf596050406e5418aa076a2b0b34b`  
		Last Modified: Wed, 24 Jun 2026 04:09:26 GMT  
		Size: 17.7 MB (17724586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9943e39d216bea180f786363e05e8e68686c67ac186b8a656a1257749de83cc8`  
		Last Modified: Wed, 24 Jun 2026 04:09:25 GMT  
		Size: 4.5 MB (4515232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e478b28f33cc3eb9162527902d9319a5edf33e6d2ebff06920489a384cee7109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2759449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b83b0a99c28153786fcd5d4afc97c32b5211eae3e62fcf09196f6af596a7f9a`

```dockerfile
```

-	Layers:
	-	`sha256:26d16b8b9b029b137d7fd5dc38ccdd518ae047bfd8f4084771affa7ad380cd45`  
		Last Modified: Wed, 24 Jun 2026 04:09:26 GMT  
		Size: 2.7 MB (2743671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb7473198844d9a0e2951a6b114bf3c289594dc3c13ab9a5dd80f1b520e2bc4`  
		Last Modified: Wed, 24 Jun 2026 04:09:25 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
