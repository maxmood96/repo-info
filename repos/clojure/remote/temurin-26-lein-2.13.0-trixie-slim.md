## `clojure:temurin-26-lein-2.13.0-trixie-slim`

```console
$ docker pull clojure@sha256:8fff01f3acb37e9e963fe0b98b8ab079ea7b3a225fa483fa925c769107454464
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
$ docker pull clojure@sha256:f58c679db6708d2ba7137dd8aed777b83cea7d0614fbb6474305f5c8b3ce815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145568730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab373ff9d1f3d91d59ae12a18363e0a5067f58cdf3048ecbabd78652cee1073`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:22:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:37 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:37 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:49 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:49 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f5b6cc0fcfc79c342d1936b630c95d9a3b50c050f5c74ed4fb06fd667189b2`  
		Last Modified: Wed, 24 Jun 2026 02:24:10 GMT  
		Size: 94.5 MB (94524331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551387aa0b06f7a118dac0568731d4c83132d1c21aacd3341737a93da2b04cc`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 16.7 MB (16743348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1036308514c59733e7f1bb01c9c2d5ad2ef4709dae7721c6eb33ae6b5807086`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 4.5 MB (4515202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07293f2fe21e4be5e0b12c82c97c326a8ecc57d19ac86b4da9070f97b5fdc8f6`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4a7bf0cbc4dde2d55cc57dc5caede2094f1b04053b948910cdb72ef2264be45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608bed0d9ed2fb74f947ced19be002a5338662f963526f85420f85446e48a7ce`

```dockerfile
```

-	Layers:
	-	`sha256:b3be1d069e91cafd91097fb892e0b80d87235395c86e119c9dbc5bae5ac5c6ca`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 2.3 MB (2331972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a717e18e029002425c16c9dafb9b316515cc0500aa7d0475fbefcf17172fb8`  
		Last Modified: Wed, 24 Jun 2026 02:24:07 GMT  
		Size: 17.7 KB (17746 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b702b082a438fdcd677a4a5da9c53cf1715d756edcddc65338a822ccc2a625c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144880192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a3bae3ae786a5ea2d3e0f1514614030e02f35fd5cb1a47ef59cccfae0cf5c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:29:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:27 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:29:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:29:27 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:45 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:30:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:30:45 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:30:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:30:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c84670bb579c5eb438cc79693e1bcde0d6222ef28699357b17a2857a057ff28`  
		Last Modified: Wed, 24 Jun 2026 02:31:07 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14174148a2a8da1dc9e43e44b61142760add7e8faadea4c55c4737502973584a`  
		Last Modified: Wed, 24 Jun 2026 02:31:05 GMT  
		Size: 16.7 MB (16711670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c616b514279747fd5b6c089b11a88ee5ccf17331d50f7e856875d76a505173f`  
		Last Modified: Wed, 24 Jun 2026 02:31:04 GMT  
		Size: 4.5 MB (4515208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e11a0dca487abf69ea985e9a3d40b875b427692a7da901243f0b15c2892b27`  
		Last Modified: Wed, 24 Jun 2026 02:31:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:117cb4ec7015513fc98e16245c98915377ab094adff09c571037f911a681af8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce089fd19bf5d666b6903e13547d749b4bb7715f17a31a86da0c09f9083140f`

```dockerfile
```

-	Layers:
	-	`sha256:4c7310ad59c5a500aaead57d42e33c0af7a88c5f4ba77f37f9345e05e1803780`  
		Last Modified: Wed, 24 Jun 2026 02:31:04 GMT  
		Size: 2.3 MB (2331579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e7df9480391639d4c139f7a210cd4e7fcd8e51cd5f48224c6e34380b68c2d9`  
		Last Modified: Wed, 24 Jun 2026 02:31:04 GMT  
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
