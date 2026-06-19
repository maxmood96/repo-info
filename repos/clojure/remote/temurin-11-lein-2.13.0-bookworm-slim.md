## `clojure:temurin-11-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:088003e92f1b0657b49df33e7b0946974a611404f1662c0d6c133b458932878a
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
$ docker pull clojure@sha256:aca0f7a4ad5024117e270d998f35ac0a92cc75657d9a3bd369d2afff6047affe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196698097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6f53f85df0e5539871a981b43cfa97b9c5093c288484fa0351207e7ce2f60b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:15:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:18 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:18 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:24 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:24 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d484ffbb46bde9cdb8195c3fcf77a04719b57173d3c760f2774d806ef65c49`  
		Last Modified: Fri, 19 Jun 2026 02:16:43 GMT  
		Size: 145.9 MB (145886162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ca38fc2362682305d2db3a3027fcd6d6b6988b191852dcbf6bdfa472bfe100`  
		Last Modified: Fri, 19 Jun 2026 02:16:40 GMT  
		Size: 18.1 MB (18059072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7df20e7ebf697f100f1d80a4baf544b65402f378b24524b1b69446222f4e594`  
		Last Modified: Fri, 19 Jun 2026 02:16:40 GMT  
		Size: 4.5 MB (4515207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e98fa02cb0d8b6fd90d335ff2745217abdefc7ba99fbc45094ec6b97c1801ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f73fe503aa20372e85568272a7b859a243e935857f362cbd91bea486f407509`

```dockerfile
```

-	Layers:
	-	`sha256:e4a91b385b56570fd2cbdc8e9eaad1421d237529831fb14fac618f947da406b0`  
		Last Modified: Fri, 19 Jun 2026 02:16:40 GMT  
		Size: 2.8 MB (2751853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:054a0ddfea930d0d96fd5f56c9e12ea1cab70cd5c02515fc14ad78399bb0f7d0`  
		Last Modified: Fri, 19 Jun 2026 02:16:39 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51434ba71dc7e21ff205b536e8e21f2463c76206c1f67a600455120beb25dc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193113974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8ba479cc473a75fe7fc6d576aed1d263b4c4917944958639c9c6ddf7edd84`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:15:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:29 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:29 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:35 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:35 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29804fdcd30c726773071254e1b33c4a90fb37b585d923bb27e715e481dfb3f`  
		Last Modified: Fri, 19 Jun 2026 02:16:56 GMT  
		Size: 142.6 MB (142582165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03ecb3c40ef61f2fc85ed928c233bca4e54e6c35b0384b2f89ee90036dfdda0`  
		Last Modified: Fri, 19 Jun 2026 02:16:53 GMT  
		Size: 17.9 MB (17894287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e15a327f05f21520e2e6ad44f1b61d9a35f6796d5d7c9485caddd0f5fae465`  
		Last Modified: Fri, 19 Jun 2026 02:16:53 GMT  
		Size: 4.5 MB (4515183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:23d0b7db353781bcf9255618ce7cf14f0a3a0131256252b311fd307b2f172fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c5093b9a2da3b4a3c8eec4c9c0c15efc3ca0f1388d886fa5684d365f2c851`

```dockerfile
```

-	Layers:
	-	`sha256:5141b46e2cf82310469f3e919663797ff2ab7b78bc6978713d5dcd8a854d4cab`  
		Last Modified: Fri, 19 Jun 2026 02:16:52 GMT  
		Size: 2.8 MB (2752086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4065427c8fc599c6c91adaf0844419b872196e0050237237d08f4cd33984c493`  
		Last Modified: Fri, 19 Jun 2026 02:16:52 GMT  
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
$ docker pull clojure@sha256:2e51b0cc4a9fab45f1212e9b225fc5711488b5fd0f673d6fee6a424cfe891c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175785970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3268dc384138ca1e5b4b8821efd989bf8a56820c912f9a888cd335848a3bceda`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:53 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:13:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:13:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:02 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:15:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:15:02 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:15:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:15:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61d6cbda07a1a85b6a53b221f86a3eebbfb9b38c4eb3192694a80b88b525000`  
		Last Modified: Fri, 19 Jun 2026 02:15:29 GMT  
		Size: 126.7 MB (126652584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad891aae5f9dd6e7f866e622baae14cbc4756877e319f723a197c4a600903f30`  
		Last Modified: Fri, 19 Jun 2026 02:15:27 GMT  
		Size: 17.7 MB (17724634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b595cc15c4d3c721b00ae5c7d47be1820477751eecc9c53d3eb9f1a299b44b8b`  
		Last Modified: Fri, 19 Jun 2026 02:15:27 GMT  
		Size: 4.5 MB (4515212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4a42fe7dcd037c82178d0761c99ad099067594115a8cb8a65c73d30c054aef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2759449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507a5b1b2940d521340501283ccd08a4d9b95adc632f587e8f17e374b32be806`

```dockerfile
```

-	Layers:
	-	`sha256:7127ad954addf5cd8b5e938f6331caca917e5a32d5781705f736354f0982ae8f`  
		Last Modified: Fri, 19 Jun 2026 02:15:27 GMT  
		Size: 2.7 MB (2743671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c4d0afdc7ac67eae203bbdb3e165eee9c61934331387355fad45b9f81dd265`  
		Last Modified: Fri, 19 Jun 2026 02:15:26 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
