## `clojure:temurin-26-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:10f11e85eecdf47696c85a9056108848083229692005df6411b8dd98f0512911
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

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b84532a65c5672b34e6cc6a2c21563104c19402b2fb6bab35599fe3117f9ce8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145337351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c75b8d794a1b0ac5734c7eb71fb3cd64ecac9585c53dcae1618da87c7930305`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:03 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:03 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:09 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:09 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039b61e4ee37d0a66deb585164ec6724e2ea3d3e1a579b30027a071cda37689f`  
		Last Modified: Fri, 19 Jun 2026 02:22:30 GMT  
		Size: 94.5 MB (94524360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b818a541b676e24f4e26d65e48a8d457cef696fca95cfd3d25bea78dd7d25644`  
		Last Modified: Fri, 19 Jun 2026 02:22:28 GMT  
		Size: 18.1 MB (18059751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9610d42c0a6862476d875bface1c3ba20742c38279bb3ae0aeef3563703822c`  
		Last Modified: Fri, 19 Jun 2026 02:22:27 GMT  
		Size: 4.5 MB (4515186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091b38cc0a42b1e81e2e409cef466741cfdb8794a5d79129f89d48c76b210d7f`  
		Last Modified: Fri, 19 Jun 2026 02:22:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c25669dfb747a4a3bd3f98001d7529917dc5596595e0b23885d056e5898e1d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba651c1fc8e67860e01c4cee72d3f0499d0aa5f44de3e7d3c93ea90f01171e8`

```dockerfile
```

-	Layers:
	-	`sha256:2fd6c1ade987eaa24cb43dcb8463a9bbdd0649cfadbaff0d997e3bdac11e71ca`  
		Last Modified: Fri, 19 Jun 2026 02:22:27 GMT  
		Size: 2.7 MB (2697228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3efc4fb033977530a63cbdbc197fa14061ab63261f606750a6ac48450e5241`  
		Last Modified: Fri, 19 Jun 2026 02:22:27 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:488bff9f8e1666bb8f5a603fcd89638d7a10e5a860d64b4757c13c71616b0b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144036255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afeaec7b9209eddf569be89d94e2691d507c2707e75919c37f517e4ac600038`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:25 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:25 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:32 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:32 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82890eb27eae5c93f1964e8df2682d33e1a6d09a557c0f6df401f57f05853a4`  
		Last Modified: Fri, 19 Jun 2026 02:22:53 GMT  
		Size: 93.5 MB (93504322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a5be52b6fcb73599603bfd55a7dd0f351e4858688d1c6290697dfe3418d9be`  
		Last Modified: Fri, 19 Jun 2026 02:22:50 GMT  
		Size: 17.9 MB (17894015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea5712c9dba3a846251db14c4358878036288fe7e0d368fbdfbdde4af37627`  
		Last Modified: Fri, 19 Jun 2026 02:22:50 GMT  
		Size: 4.5 MB (4515181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96ae8ccde7c96810283854e462c035a1f44ee836cf2665b081b546096ec3b61`  
		Last Modified: Fri, 19 Jun 2026 02:22:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:250fcdee4ba2c3bac32cfe96c280f66bebc82171326998474c214edecc03f04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb869d7e8f1c9a3dbe213b8ee4ac9ce3e3ba52594a4c0242ef8995e6a18d9bd`

```dockerfile
```

-	Layers:
	-	`sha256:7c1128a6d174f8507fdde0693d296861f27a438e6246d518917b9dc71cd5d6e5`  
		Last Modified: Fri, 19 Jun 2026 02:22:50 GMT  
		Size: 2.7 MB (2696840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1a91679cbf4cb81cedacd0d3b0f6a8533857e58fcd4a13bbfb46c33fa5ae9e`  
		Last Modified: Fri, 19 Jun 2026 02:22:49 GMT  
		Size: 17.9 KB (17887 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c309e748d6a28784a55a8e95b4b7cd0f06b339fcc502bc8fb569977eae872838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148762978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ec0f64b9479cfe505f8820410b55ef202feeb9f438a5db254c7aa1be625e11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:10:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:10:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:10:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:10:18 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:10:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:10:18 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:12:42 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:12:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:12:42 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:12:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:12:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:12:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:12:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f29b00e9bc0b9af92e1b64e13edf9ecde1571af48c5d8d0fce068fb62ea3514`  
		Last Modified: Wed, 17 Jun 2026 00:13:19 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33648ce62c2e7cdbec7791b4a5963531c6c9da3b53bd57ffd24ff658ad445438`  
		Last Modified: Wed, 17 Jun 2026 00:13:17 GMT  
		Size: 18.3 MB (18263305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6745d66e8d3356f540699a80478b7c520e561c7dfb1d2688ebf23ca2fd13751`  
		Last Modified: Wed, 17 Jun 2026 00:13:17 GMT  
		Size: 4.5 MB (4515220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a7582c65a86f0c61d178db1cf4278471b35085c8a5a6f795025d4a420910df`  
		Last Modified: Wed, 17 Jun 2026 00:13:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:083f7c9c337e541cece8a1254513006c618617b2fbd47e54a8a05666f2fe62fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdc3de8df0d15057ac261ec3775f3fe654c0d6b12e1d1ce05a8ae3b3a7c3055`

```dockerfile
```

-	Layers:
	-	`sha256:a758da015a4fe5dab05f606a226a79773e595c12b92833ba972b76cf15fad680`  
		Last Modified: Fri, 19 Jun 2026 02:58:37 GMT  
		Size: 2.7 MB (2682997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16c0f16a8542596fe98abc9a6bc33711f03df8cfa4d636236356e1bfefb779cc`  
		Last Modified: Fri, 19 Jun 2026 02:58:37 GMT  
		Size: 17.8 KB (17810 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6d08a18e70f5c377d67250f3a83e29359a5b558fd618f55fd48cbc8b283de6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139670839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0984050092453bc3ed36f851d1c4c2011dcb1f8e4aad2ce22b0cce0b13edad2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:41:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:38 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:41:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:41:38 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:42:42 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:42:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:42:42 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:42:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:42:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:42:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:42:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf175e00b02ff27e4e23a84cea45ce5d6e96921b94bae771e56baf106f5ca05d`  
		Last Modified: Tue, 16 Jun 2026 23:43:12 GMT  
		Size: 90.5 MB (90536986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b18fc53195ca16c8f512abd533e71c7fd83ab03cdcd4d8cbf724fd5f3f1ade`  
		Last Modified: Tue, 16 Jun 2026 23:43:07 GMT  
		Size: 17.7 MB (17724750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b28712dee199a5f23dff199f0923337ed9249b115fae54416674a78cedb4ca`  
		Last Modified: Tue, 16 Jun 2026 23:43:07 GMT  
		Size: 4.5 MB (4515165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed2bd0fe82b37d4c48add1576ea3211b6fb9bb136eab35c1e5e295607f993b3`  
		Last Modified: Tue, 16 Jun 2026 23:43:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d2a745675f6384e5f82d9fea990e8ec0f93bd204a0319448970787dbb39ce651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f878ef018647c2e0b01679be5b181fa5517af881d3525a5c238d79ed354632`

```dockerfile
```

-	Layers:
	-	`sha256:01c2735d9bbc6361fc090c9d00d64a4586ad063e0e42afdda67476e2e8dd6bd0`  
		Last Modified: Fri, 19 Jun 2026 02:23:22 GMT  
		Size: 2.7 MB (2674228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7da8befa0f2a26352d3fdb8ccd8e38dfbb81562384f2ae1cb947a7cebf39072`  
		Last Modified: Fri, 19 Jun 2026 02:23:22 GMT  
		Size: 17.8 KB (17765 bytes)  
		MIME: application/vnd.in-toto+json
