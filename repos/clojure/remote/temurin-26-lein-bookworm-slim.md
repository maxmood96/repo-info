## `clojure:temurin-26-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:de3b8bfe380ea49c11b58cae9d16590194339f973a483790e44bbe17e4e19dd0
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

### `clojure:temurin-26-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:09d4134c86d241659ac5abccbba9f0be9d2b8149783053e1bfdba690ba6b9a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145336833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf635440b0030e94e36c9c497f5a6eef123868e6f90fb3b5858f37993dce6d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:38:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:16 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:16 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:26 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:26 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2c74f7d25c7699f8c62c536f552804d49fe76b5d6efb21dfc56f1612635775`  
		Last Modified: Tue, 16 Jun 2026 23:39:47 GMT  
		Size: 94.5 MB (94524345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0f7abeb6656ba92e2f8dd2a5b31f30ec10173fd91c86b7d9e8146094908e7c`  
		Last Modified: Tue, 16 Jun 2026 23:39:45 GMT  
		Size: 18.1 MB (18059204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03315fa756e684c042e3020b4ff59009520e0ab8ecf820073e085190ad56162`  
		Last Modified: Tue, 16 Jun 2026 23:39:44 GMT  
		Size: 4.5 MB (4515231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6290e107b914e33d8fd1e09c6a1456755e477848ce1dc7b92de822082c559d59`  
		Last Modified: Tue, 16 Jun 2026 23:39:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14a836b73b76447c1fb17273db1035193d5e962edbc7472795ae7f6fe4ceebc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fddd943b9f6c9e6476321c4e89124c2fd2d287fd7fe275a42d803d5dfbbbe94`

```dockerfile
```

-	Layers:
	-	`sha256:5c50130e6cb39ace22792bc85e4bd5b49f789fa0004f9ea6c52b9fb795c3f533`  
		Last Modified: Tue, 16 Jun 2026 23:39:44 GMT  
		Size: 2.7 MB (2697228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798f9828a5213ccfa9e0cb88f0550d3b838aa94be836de19901607cf513c05f2`  
		Last Modified: Tue, 16 Jun 2026 23:39:44 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f60b512cd6200c6c282ab902494f5ea9c249dc6c69928071239d3933dcc9726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144036714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba345a1ac25cca33e6391d1e31d13402fbd355ffcfbbc013b9e9a8b2eb9f175`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:38:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:07 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:07 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:16 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:16 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9240bcb17636e8253590a4d7e76d9f2b95e2e1f5b245058d1d635b45a74c48`  
		Last Modified: Tue, 16 Jun 2026 23:39:36 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c5d48213b77c7155f635a5788b5a5c26ec7729bb70e238416fa7a6c505ad69`  
		Last Modified: Tue, 16 Jun 2026 23:39:35 GMT  
		Size: 17.9 MB (17894429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e929a9f1616264a93e50e83039571dd4988c5d65c173cf20bb0a59ae24a0ae93`  
		Last Modified: Tue, 16 Jun 2026 23:39:34 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2904166998ced429b6ffa857b89c5a541b289961291a5c2815f6a8444fbac0f`  
		Last Modified: Tue, 16 Jun 2026 23:39:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b696e7a88959aa563e47fd1c4c51d8a0b599378d5bcb160f338ccd10a3d3841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d33a286899c37eac150e103f236da428d48444273821b65b2a09c0d53c1c6f`

```dockerfile
```

-	Layers:
	-	`sha256:a68cdf02cc571a42993ccc8553711f60d230cc48f476606ca9a226e6cf135be6`  
		Last Modified: Tue, 16 Jun 2026 23:39:34 GMT  
		Size: 2.7 MB (2696840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0432fd17fbc0e805fa9503f8b4bd1082b6b84148c9292bd0c5ba541fff9421`  
		Last Modified: Tue, 16 Jun 2026 23:39:34 GMT  
		Size: 17.9 KB (17887 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:01465d9dc29b199b004c857d2c86e7c917858b4df8f0327e7457f2a4680ea6bf
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

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3e925dcd468787730884c1ce5cd8060da93bcacddb43917dabd306d5dfdb74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2700807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ab068a2a93a54cd8ad2899a5fa7cdd5363f1906b9683003ee0cc68b72a7642`

```dockerfile
```

-	Layers:
	-	`sha256:9026a8f5d5546a88a9083309adda79035a83757b0940b2a4b51110d778d2cd0b`  
		Last Modified: Wed, 17 Jun 2026 00:13:17 GMT  
		Size: 2.7 MB (2682997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4027800fd6be96dd9c53f1e5e9ca46857e2fffc78903f004921ad5be0e61bda5`  
		Last Modified: Wed, 17 Jun 2026 00:13:16 GMT  
		Size: 17.8 KB (17810 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:abc3a8f0f72d37dbf2e756837a52b2ca4a0a102515856ba9fac327821e95fb5b
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

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43858eb30224a76e47090f78561ff20e620ed0202b67e9982f1b02e5bc6f19b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a28d184f48ae455c2682c07c6297da491a2c5b228783a8c4e976418b669bdf`

```dockerfile
```

-	Layers:
	-	`sha256:8ce4dbcb609b72186a1ad49215defa6e477b7709f5f9a071128c548f6963c5db`  
		Last Modified: Tue, 16 Jun 2026 23:43:07 GMT  
		Size: 2.7 MB (2674228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe63f3b3b04c62ddcfb10fa1eb277668126c3c37d86305c29f2662c3d124bedd`  
		Last Modified: Tue, 16 Jun 2026 23:43:07 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json
