## `clojure:temurin-25-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:e5a594b45c63357763f1c02c698c88a8cf3a77ee1177b0ed3e3d1a10c1ce88f7
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

### `clojure:temurin-25-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:26387dd49adc9f28c2166028e39418cf226e24ac0d4dc6564d0f0a7f6a6ec8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165287314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818d0146cc737977ad7aaa4e49a910a3c9b934a2c4dc369ce4bd359d380c788d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:20:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:11 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:20:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:20:11 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:22 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:22 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762dda30aa9cf76546a178edf37e9aba848ac509a22fd4f31639f63f01b50df4`  
		Last Modified: Fri, 19 Jun 2026 02:21:38 GMT  
		Size: 92.6 MB (92574569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc7c560a7962e037e30447d5e834541b22d1be4d8f9afa90247613947ee0173`  
		Last Modified: Fri, 19 Jun 2026 02:21:40 GMT  
		Size: 18.9 MB (18879988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a421172ffd933d172c4d44ffe3f84585726bad11fa4dc91bcbe13b2fa7ad9f`  
		Last Modified: Fri, 19 Jun 2026 02:21:39 GMT  
		Size: 4.5 MB (4515206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afd9398759c022765c075ff37774db0284658f728321c04c10cdec15d466c92`  
		Last Modified: Fri, 19 Jun 2026 02:21:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5edf984783910a0959835c6d9aff14716ec7d2c103b6d30b1ac414ed8796fabf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fe51fac0105fe0935a9192cce58d2d92676a7ef007dac54c6663773e1493d4`

```dockerfile
```

-	Layers:
	-	`sha256:1f34d7af9882ae41b2c15ab3ea3723b0d9ebfd31b36031b9eb8955d191305549`  
		Last Modified: Fri, 19 Jun 2026 02:21:39 GMT  
		Size: 3.8 MB (3785848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b3ba232bfff5a9542488fbefc86483c80ddeb1f7084328ed653f7e949e17c3`  
		Last Modified: Fri, 19 Jun 2026 02:21:39 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f19a182f24647230939b8293a57be1cbcac328fa5150369d2b6deedcd56f383e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164575669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9ff27c236b0c18c3797462b7765114a54214a897e98afb800b94245ab5fd82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:20:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:14 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:20:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:20:14 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:32 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:32 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a74dd7b3754869b23a30dddd1ced16fabdecf4752ca4374b07f5bead73120b`  
		Last Modified: Fri, 19 Jun 2026 02:21:53 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b70b5adc6bd7b886b1a7f8906d2bab493243da01d76d889207468ca001b1b1`  
		Last Modified: Fri, 19 Jun 2026 02:21:52 GMT  
		Size: 18.8 MB (18839625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf36185e1097505a231f3b337f21aa27a5f3d922bd6a75d6c9c7f0ef31f2e3bc`  
		Last Modified: Fri, 19 Jun 2026 02:21:51 GMT  
		Size: 4.5 MB (4515195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1816b6345dd4bc608862eb5876896a0a47e70025036a768788c28f55a623da66`  
		Last Modified: Fri, 19 Jun 2026 02:21:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8329c68f8f371450416bd3640c6bc0a795ca029e6bec23749468fcee74da73be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93bd6f7f2f35df8f2731e0b6050df425cfdc2346340455753207c83f8b3606b`

```dockerfile
```

-	Layers:
	-	`sha256:a5ca7800ce2ac95a3b19828698bcc64a405257bdfd1028dc88047e4556eb75e3`  
		Last Modified: Fri, 19 Jun 2026 02:21:51 GMT  
		Size: 3.8 MB (3786109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232be758143bdb89f0031dfb00b488b3613af79eb593a8e25fc5678ce2223480`  
		Last Modified: Fri, 19 Jun 2026 02:21:51 GMT  
		Size: 18.5 KB (18490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4981c8e6c5275a05f69d3da84fdbc0a73e7136160c7838d4d97bd8b32bcc66fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168504056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc7af32c2b409e0c04012fcac01cd73d7684dd9608423c672b5d84e756015a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:11:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:11:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:11:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:11:00 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:11:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:11:00 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:13:43 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:13:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:13:43 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:13:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:13:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:13:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:13:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6e91230e9fcb06c48eef2eae63696efc222edfdf9387e828c0e8a79c0a8c9`  
		Last Modified: Wed, 17 Jun 2026 00:14:23 GMT  
		Size: 91.9 MB (91914030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545271dc17cd609e72c45c99cc2b4c230217501733bc396ea85bb6cff9be56e8`  
		Last Modified: Wed, 17 Jun 2026 00:14:21 GMT  
		Size: 18.9 MB (18936466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c816ddc4d5518aa88e3295640163da90bcf82a13d4b932d4a76c10753cb825`  
		Last Modified: Wed, 17 Jun 2026 00:14:20 GMT  
		Size: 4.5 MB (4515191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de2f92949336d91b0ec75fa618b27498fcb6a8e3610fabf898d448df7b34d2`  
		Last Modified: Wed, 17 Jun 2026 00:14:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d2f6b9359c27ca137462b3b4b2208b3d4a5606201e3af3b09f261fa0b3c4629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3788573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959de4091a6cd882da19bef09042035a175aec6475b471725ee9c7349e51aeaa`

```dockerfile
```

-	Layers:
	-	`sha256:b29526bec01305e8fbf25ffc9ec7b76d215f3c56384f7fed330cb99fdc8ec023`  
		Last Modified: Fri, 19 Jun 2026 02:54:49 GMT  
		Size: 3.8 MB (3770172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d9e689dcfed501c47c21abe3dac107a5e9c1a58103e81f53b88de49963bd70`  
		Last Modified: Fri, 19 Jun 2026 02:54:48 GMT  
		Size: 18.4 KB (18401 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8d43703a222e075f821e7152e64d96a884d99a0c5531667aa3d8d6ce2e995c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161244298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818ce55cbe9f34b4010ac65785166e6a6747d2219c27a5512a7dad8a36403ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:14 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:14 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:20 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:20 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61adec2576be28516842462114579539904738dc16abf2591b21445e78b04e67`  
		Last Modified: Fri, 19 Jun 2026 02:22:47 GMT  
		Size: 88.4 MB (88420353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9873fa465d3bec1aa8b3d55c02291bbfb10221cbe07b981c9af8ca839115a3`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 18.9 MB (18922406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e440901d2089b07683b29baecc9902bc52c5f9df173bf32e7aad54e18440dc`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ad4ce9151d8942e20063529fe7a312e7d514686da05d72d567b14a80e251f9`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40541c44f656bb03ca44b9dd0b152a55f46d9b8e0e0c3a4b50d313cf4bb51ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3929695e1020b4b52b312873badfd9f6a66807549391c2b6e9e2902b37d00e`

```dockerfile
```

-	Layers:
	-	`sha256:8b33bf85b203a59e6f4cf3dbcd7abadda372ef84b39851f34fa8bd528deba340`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 3.8 MB (3766837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94a231ec87af8b55771a69878f7e2b218b5aeb4f44f3df35118ad9ca4adf735`  
		Last Modified: Fri, 19 Jun 2026 02:22:45 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json
