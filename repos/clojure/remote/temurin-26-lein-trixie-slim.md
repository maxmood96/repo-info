## `clojure:temurin-26-lein-trixie-slim`

```console
$ docker pull clojure@sha256:033614595b4f1baa150255421e0d522eadeab2af2634b14bb9b7ffcec6def5e4
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

### `clojure:temurin-26-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5578b7ff8de01be9938fdb167f116cb0b3214ea3aea81a4316b83ed581c891c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145568668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7270aabcf80a83e2b726ddbe8a21501c9403967e9c390f1d3cdd9e38aadd7f28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:39:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:39:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:39:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:39:01 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:39:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:39:01 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:40:11 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:40:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:40:11 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:40:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:40:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:40:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:40:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9753ff141c5821353cc72bd5e80addbfc66273ba8da8942f0292e387437e6ad0`  
		Last Modified: Tue, 16 Jun 2026 23:40:31 GMT  
		Size: 94.5 MB (94524364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba585d954be4f4758f568981dcc2d2842ef7888d7e00d45ee95ce5484c2da38`  
		Last Modified: Tue, 16 Jun 2026 23:40:29 GMT  
		Size: 16.7 MB (16743254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37f70e8c7c5db388bc946cea3b2fbd4e014aca5265183d451d99fa8cc7aa4a5`  
		Last Modified: Tue, 16 Jun 2026 23:40:28 GMT  
		Size: 4.5 MB (4515205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72e7969dcaf7912226b65905c50ced83312bf863a7bac54893a1799a927d643`  
		Last Modified: Tue, 16 Jun 2026 23:40:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58ed1602db81da3f1c88e8ca35464a262c1b54b7a81d22df03a68e562690b4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cf9d8ef44ec44cc7fd7afd492c530d776ed85a21821317e8a37fe1ca931c5a`

```dockerfile
```

-	Layers:
	-	`sha256:19c022fdb2dafdb14251c69c2fd87fd62f48d2da26bf2b94020f2725aaa7c00a`  
		Last Modified: Tue, 16 Jun 2026 23:40:28 GMT  
		Size: 2.3 MB (2331972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8359047ba4be2e43c74c22e1f3ab8a6c480106033248c671d6a0486fd9ccfc5a`  
		Last Modified: Tue, 16 Jun 2026 23:40:28 GMT  
		Size: 17.7 KB (17746 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc48ecba57be14b61b6d87a436f0b28794d8212d4db06671d063856899f1b01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144880154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7817003055b7cbb847f0789b050b978fd13e744a01c9caa971ca48dceac91589`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:54 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:54 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:40:09 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:40:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:40:09 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:40:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:40:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:40:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:40:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871b808468d045980c9f15b0f0b8730323f168869008302d01a5f506b60cc788`  
		Last Modified: Tue, 16 Jun 2026 23:40:30 GMT  
		Size: 93.5 MB (93504349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5e9a2139716ec18597c7acc8f5c86ea5485fc96d3ec1b682024f6e72ca9771`  
		Last Modified: Tue, 16 Jun 2026 23:40:28 GMT  
		Size: 16.7 MB (16711651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25bff7748132940a12f7b13f4f797a879da123da64c481a369b147e551100f3`  
		Last Modified: Tue, 16 Jun 2026 23:40:27 GMT  
		Size: 4.5 MB (4515194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebd047d1e30077cdeba8c1a189a992b8701239423383ca222eab809d78b620a`  
		Last Modified: Tue, 16 Jun 2026 23:40:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a57bce1179b078b5117119e57f9037ddd114815a55ac36a4ca1d99800b6053c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5d50d58971debca5ba937894bc021110ab7d1a3229ef659c5d191c33aeaaae`

```dockerfile
```

-	Layers:
	-	`sha256:4ec4116762ae6b2db56d287371298466f45c45d3b39426a6c5560e1a6e921f77`  
		Last Modified: Tue, 16 Jun 2026 23:40:27 GMT  
		Size: 2.3 MB (2331579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f2008ccfd6769d4c659277fa30ac117dea6ee19a8f0a4f0e2af1bbc0ce0ac21`  
		Last Modified: Tue, 16 Jun 2026 23:40:27 GMT  
		Size: 17.9 KB (17867 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1ad9baab80776f3fa3828b13df9cfc9a75ee1d12854c1e281ace99d4b6581fd6
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

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:255bb64082260a97da14be225004cce6f79dcaa1e7727a721c83d5e38e8b6d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d4e9931b35569994205f93987d86d8837743a716eb400c2165f049f9101eb7`

```dockerfile
```

-	Layers:
	-	`sha256:43149d9a9adde66fb71e2646632985e74684ec8dfaa008f485489ecd3b85d439`  
		Last Modified: Wed, 17 Jun 2026 00:19:48 GMT  
		Size: 2.3 MB (2316888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4d835d9f412eb7904efee6bc3eac9b272c8c9ecff1694e3a0f4465af4f0101`  
		Last Modified: Wed, 17 Jun 2026 00:19:48 GMT  
		Size: 17.8 KB (17790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4fc9f300625fc8bc8a349d9ac7d8ba24d818782682b4a00fd17896ca61bd50e5
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

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7415880d47ca77ad93681bd12357585e75e773f99b6bf5c789c3122c1a83d666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89ae5d31a4624c64d84b6d5e295aedf8bb634ba91ec9a64d315ecdabc535b5b`

```dockerfile
```

-	Layers:
	-	`sha256:9c125fb7bbe9ad4e6590b6c4ceea72ab811c34859b1e440035233dc2bfe2d55e`  
		Last Modified: Tue, 16 Jun 2026 23:44:50 GMT  
		Size: 2.3 MB (2313585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6713c124385a4f0f87a46323a028e02666b80e5e37fb5755fe16d2d053fb7d5`  
		Last Modified: Tue, 16 Jun 2026 23:44:50 GMT  
		Size: 17.7 KB (17746 bytes)  
		MIME: application/vnd.in-toto+json
