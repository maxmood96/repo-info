## `clojure:temurin-17-lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:eff9fd2d6840fb0417a76abb0e15e2f668fd2441b211afece4a1e958a5f02858
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

### `clojure:temurin-17-lein-2.13.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5836d824a1af4113e13921863bf9ca9c830991b6915950dd8eadeece25a3bdcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (219030676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d3ab337c8cebb76a9787e005c0172334f762fd9a33e12b9c3ca672c83b8c2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:34:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:34:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:34:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:34:39 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:34:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:34:39 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:35:43 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:35:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:35:43 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:35:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:35:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:35:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:35:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00c5ef52a6e009decdcd7ed1c3294cad1c1fc1e5139ab93e8bd7ded08aea9e4`  
		Last Modified: Tue, 16 Jun 2026 23:36:04 GMT  
		Size: 145.9 MB (145905476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de373b82439d0f2da4dfe4474ae0846e95e9ca05eb5d966644645960c868773e`  
		Last Modified: Tue, 16 Jun 2026 23:36:01 GMT  
		Size: 20.1 MB (20107513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b731828b1018d081e84d618b17e1a4e6982882c90342ed49727b9ce22e99ca`  
		Last Modified: Tue, 16 Jun 2026 23:36:00 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712f096fc235873db7aa1e372553ad68d770b0df73c3e88c417bd94df34d009b`  
		Last Modified: Tue, 16 Jun 2026 23:36:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a109b24c5e6c24736e550fce8d6dd5984db765b866263dba6631e88c1d4faa24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4301756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107ea5070e30c6d4bd707712c479d401fe2887a20d2c3118e17e6d46c0c95ee8`

```dockerfile
```

-	Layers:
	-	`sha256:f0c6c4983308872cc7588f0bf974682db1d25bd8f91f42db9e7b8596cd8f01a7`  
		Last Modified: Tue, 16 Jun 2026 23:36:00 GMT  
		Size: 4.3 MB (4284018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8f44bd4ba6a267531022aabf42cb9536bd9dcd5c076b3d81e1e6b1e67e737a`  
		Last Modified: Tue, 16 Jun 2026 23:36:00 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6c7bd8637c82d16db9fdefbc9824fef64efaf4f94a84ed53230687ac9e8e65be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217569293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554f4128a81f9c663583e6e8cd31cbfe75153c44baf5830806c31da0b2bd792b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:33:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:23 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:23 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:33 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:33 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:34:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:34:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5b53db6534fa9f3064cafaf7272eafac29c458893f37bb6c50bcfdec601a6`  
		Last Modified: Tue, 16 Jun 2026 23:34:56 GMT  
		Size: 144.7 MB (144724405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cb8b1c4f44413ad0bc895969f7586792dd90f75666be5153e69a8a6114f0e9`  
		Last Modified: Tue, 16 Jun 2026 23:34:53 GMT  
		Size: 19.9 MB (19940252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b52c2626b5cb116725f4bdfeaf74e86b36402b7eea1875b7a50576a8d7ffc81`  
		Last Modified: Tue, 16 Jun 2026 23:34:52 GMT  
		Size: 4.5 MB (4515190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df1643e5297c61e5663d67ec1035bf960d29b5c826da413d153df293644df34`  
		Last Modified: Tue, 16 Jun 2026 23:34:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a7cb6ebdbace5210d292d789c6942f7e736720bdea32a30d3bbfbe395024efe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4301491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cc9eb7991f7ea9e74f47dd8f09518e15b20c94752b64995c094ab2fb9bbef0`

```dockerfile
```

-	Layers:
	-	`sha256:f6871bdbde7d8f539b291c8fcd128b1635561c1b31be9e068160c3d08650d865`  
		Last Modified: Tue, 16 Jun 2026 23:34:52 GMT  
		Size: 4.3 MB (4283633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a4a234104a7676357d90979da9ba74971e682bcc2b7e0f1fa7605634787184c`  
		Last Modified: Tue, 16 Jun 2026 23:34:52 GMT  
		Size: 17.9 KB (17858 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5f29d2af1031ce5902875ab5d09e9f75373a2dacdaf569c63c160031b5a4bd3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222960332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a6f6fe426a4546a54b15ceedab7a2e66dcbcba847d2ab91f956ec4c6329f04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:42:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:42:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:42:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:42:34 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:42:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:42:35 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:45:15 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:45:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:45:15 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:45:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:45:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:45:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:45:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee41a41cba622618de5e159b9d46260bbca19ab81b8ec8ccc79b6e695719319`  
		Last Modified: Tue, 16 Jun 2026 23:45:54 GMT  
		Size: 145.8 MB (145766120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071a13b50e316b12f99dbd524d5e7618bc1a3c05a87797b7c1ab2d2bbee07271`  
		Last Modified: Tue, 16 Jun 2026 23:45:51 GMT  
		Size: 20.3 MB (20331906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7638a69aecdebf06093fbfc436bba11abc80562bfedd5303de9c4ff8f0d83`  
		Last Modified: Tue, 16 Jun 2026 23:45:51 GMT  
		Size: 4.5 MB (4515206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75df5d6e529dc42485888d8a638da4c1a4d15204dc416ada86386848e8324153`  
		Last Modified: Tue, 16 Jun 2026 23:45:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d36cf03101563d9dc8090629a7736b2706cd87f98dc4a207490bc743636f6eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20d6f8cb1c8948956cefc40122b03a14c4b6a72eb1a3cb11dfd923672183990`

```dockerfile
```

-	Layers:
	-	`sha256:b6d5562ccbb052b0711a371e08fc4881cb8fce9e538e8014e8af919fbcb5007a`  
		Last Modified: Tue, 16 Jun 2026 23:45:50 GMT  
		Size: 4.3 MB (4285879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3839240d86c7aebf30d6e447b3a1e55b5b71e37abbd3e42d2f6746d1fdf8da`  
		Last Modified: Tue, 16 Jun 2026 23:45:50 GMT  
		Size: 17.8 KB (17781 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:937fdb8c55202ec2fceae7095413fef8def19e990e085dc0aa9526b1a6ba7df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207357832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a6a50e53db42b55c13eb5f0aa45c44690a44d4399c3dc7c1d7adfc2b68ed35`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:32:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:42 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:42 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:33:44 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:33:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:33:44 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:33:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:33:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:33:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:33:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcbf5fa17a544f4f185bb30cf7f6677ef4e378cffc846e5e2320472cbd66d24`  
		Last Modified: Tue, 16 Jun 2026 23:34:13 GMT  
		Size: 135.9 MB (135910448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51edc1d5e3d183a29a838792e71f275e1595c9acb75cdecb6db4de71bb3b81f`  
		Last Modified: Tue, 16 Jun 2026 23:34:10 GMT  
		Size: 19.8 MB (19770237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d18292c30e4de27793194a7dfe05a6c38fedae4e7e39bd079660e0cf9428c7`  
		Last Modified: Tue, 16 Jun 2026 23:34:10 GMT  
		Size: 4.5 MB (4515217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed10bff52472e3e037c12a7086252c565291abc4f697c22ebaa35f67598ce74e`  
		Last Modified: Tue, 16 Jun 2026 23:34:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1d01683b6030bed9cd0d83d83a6be0b0657396aa44a80c76fa0fe0089840cba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4293570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a57b838bb79dbc4a3a29daa34b16d0cdcc9c410c53c9b1db8036b1cb02626a`

```dockerfile
```

-	Layers:
	-	`sha256:6ace68367e87558797d10ac99760a77c63fec4737b2d40e3694934bc692957f3`  
		Last Modified: Tue, 16 Jun 2026 23:34:10 GMT  
		Size: 4.3 MB (4275832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16418463dd586adc7b50436935195a3bae678547422b6868d3072f763f33733`  
		Last Modified: Tue, 16 Jun 2026 23:34:10 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json
