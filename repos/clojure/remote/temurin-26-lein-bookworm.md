## `clojure:temurin-26-lein-bookworm`

```console
$ docker pull clojure@sha256:2d4886644c29fd038a47fd388634e5e3bc2281df6599234a9a4434c4bac2032c
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

### `clojure:temurin-26-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1dad8ba433db0322544b5ab5ecdb123e391e998707abef6e9842f43d9cd8c75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167650169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29b17f153786982a24f9bc4dcb9f0ce3d48c5fa34e44f245026c22b76865b74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:01 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:01 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:12 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:12 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530ea061ba9314c4d2319a7d81a1a851fc0aacbe4e429005dbba736a5b8e8c4f`  
		Last Modified: Fri, 19 Jun 2026 02:22:34 GMT  
		Size: 94.5 MB (94524360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbce4cecc2c9c8bc8f0fa3ebe0e182f59b6c7d4d09ae47ef39075544f866c97`  
		Last Modified: Fri, 19 Jun 2026 02:22:31 GMT  
		Size: 20.1 MB (20108155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba73cfd9a067a86a4237e827fccda02f2b853d2de40b0386813bae49f1719abd`  
		Last Modified: Fri, 19 Jun 2026 02:22:30 GMT  
		Size: 4.5 MB (4515182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a391f703d379ac81fc2306885363d6449ccedccc9c79cfd5d52173d455559e8`  
		Last Modified: Fri, 19 Jun 2026 02:22:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bbf5febb5608569ea6250d0c3771bf9f295fd70aa3404c8eac5582ebd8813226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2fa931a51a93d06512c68deb5063c2b2f535d60dd6db9fc181a96a5a67de75`

```dockerfile
```

-	Layers:
	-	`sha256:1821398b5bdd1481be590176fd8eeb241c63c15f6b80c8354f3f75afc1da6e7d`  
		Last Modified: Fri, 19 Jun 2026 02:22:30 GMT  
		Size: 4.2 MB (4249559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d920df33627a8fce2a7714cea244fe2a735d0e289c5de869d297b2800f9968`  
		Last Modified: Fri, 19 Jun 2026 02:22:30 GMT  
		Size: 18.4 KB (18381 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:01e1e9de5d192f1972d57392ec621c4b4433798fd90429ea044a85149fe391e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.3 MB (166349245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ec817314cac71667595f2c77fa4797992e6b75f5092c099ec55b71d2cff7c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:27 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:27 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:38 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:38 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88605f48a9e112db5a4715192f87a586d78e792189231ba33666bd2fa0d117a4`  
		Last Modified: Fri, 19 Jun 2026 02:22:59 GMT  
		Size: 93.5 MB (93504337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c91023ca296e3f1b877b5c24802a83910d9a3579508b499ab06835735060f49`  
		Last Modified: Fri, 19 Jun 2026 02:22:57 GMT  
		Size: 19.9 MB (19940293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e56f06a4a5790690bb324fdb0744dc3b53b8584655cee0508fb1268b08c0f37`  
		Last Modified: Fri, 19 Jun 2026 02:22:57 GMT  
		Size: 4.5 MB (4515170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290d463c74db435cca96bad9853d0af77d4e185517d81279547ae9c60efe7fa7`  
		Last Modified: Fri, 19 Jun 2026 02:22:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e13d408b5b82ba9a473bb7859a7509d0cc7c66425740db60d6da89267e6a76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4267720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3762a828e54b8d06bdf42f3dc940b5e1bdc457043aa958fed665377d4d6e04`

```dockerfile
```

-	Layers:
	-	`sha256:8a82d053e7e57eee25dc8d93f467e6dfc0c470b446a623e703248bb0b768102d`  
		Last Modified: Fri, 19 Jun 2026 02:22:57 GMT  
		Size: 4.2 MB (4249195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6472c4bf7a52ec3fb4d9a892612966267a2946056547799f96045b4d4d48256`  
		Last Modified: Fri, 19 Jun 2026 02:22:56 GMT  
		Size: 18.5 KB (18525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f425df151a5487c4e7e275fe3ccb766e8953adc5bd37e02b8fb42a3195397136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171096405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab40800dbcc4110b9702abd3947ce9d6bcccee5261793d8f5d46d04c5f07b15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:07:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:07:21 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:07:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:07:21 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:10:01 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:10:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:10:01 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:10:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:10:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:10:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:10:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4759a87d2ab24b2fac4a2500d8d0888984823a78af74fea7debdc9f59a4aa41`  
		Last Modified: Wed, 17 Jun 2026 00:10:39 GMT  
		Size: 93.9 MB (93902050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438cc53d9667f2fae2cf6b81e25d13181a80615b69a51ecb6af55b0ce07dbfc4`  
		Last Modified: Wed, 17 Jun 2026 00:10:37 GMT  
		Size: 20.3 MB (20332041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724f86330d8c7e704aa8121678a6898fba98afa1958fdf22addd0c9fc1b01869`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4d010da56d491c545e90064f0b0222259c84c59bcb739d6bb5e16079fabf8b`  
		Last Modified: Wed, 17 Jun 2026 00:10:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2ae5a09d535af18f63527a2bbb7e56a736dc0060fb1c218647a7e20e4f3da06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4253805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2187a0793c003965ce0bed1ac56564a8ebb39b46c611989f229e0e85086f3d9f`

```dockerfile
```

-	Layers:
	-	`sha256:44d6f25d070f9b0e0e0e7186232d68987e89e58d0392edc98719e635675138cb`  
		Last Modified: Fri, 19 Jun 2026 02:58:39 GMT  
		Size: 4.2 MB (4235368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a498a1cfb1ed15102f9bbfe73d4e939d7229777f04a5adfb76dde81b30a828dd`  
		Last Modified: Fri, 19 Jun 2026 02:58:39 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:eb692e872b14f7a42f7664e40c37bb558c4fe80d55a29e1bf334df1c4d6728bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161984418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1abd3cbc255d895e8493c4a2e27c4fc5403078a9fd250fae8b099f5efa470a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:22:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:54 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:22:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:22:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:23:59 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:23:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:23:59 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:24:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:24:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:24:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:24:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93dffac2f0aa26f15bbfc00b26f8e00f41d28e225af70af77c70295cf7b0a6c`  
		Last Modified: Fri, 19 Jun 2026 02:24:28 GMT  
		Size: 90.5 MB (90536936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b2ba4cbbb6a84ff9134b153722a1d1cdb79ff03db443f015b0ff4a087dee98`  
		Last Modified: Fri, 19 Jun 2026 02:24:26 GMT  
		Size: 19.8 MB (19770341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf36d5b55df0ad38c1a8ac0fc544db96c4b3b52fd843aa16f758e1b62e143b07`  
		Last Modified: Fri, 19 Jun 2026 02:24:25 GMT  
		Size: 4.5 MB (4515212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa226d21a8c685abca41d8e6535188edd0e44c1827dc1e1f208fc637fad2748c`  
		Last Modified: Fri, 19 Jun 2026 02:24:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:641760ae5648d3600ac42e9d1fa9e5272b3173548b3d543ea76a1934ec563b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffef27a05901899601f498eae7f84be15fdef005c0cafc7d7e0f60153cba9500`

```dockerfile
```

-	Layers:
	-	`sha256:c6cb7c2fece12f8f790fe4b597da5d678bfb47e7f4100be4a459fa714d897a79`  
		Last Modified: Fri, 19 Jun 2026 02:24:25 GMT  
		Size: 4.2 MB (4226559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a082585c1b2c28d5978b3e29326b5da8c0bfe276181867110fc101e2ed706cf5`  
		Last Modified: Fri, 19 Jun 2026 02:24:25 GMT  
		Size: 18.4 KB (18381 bytes)  
		MIME: application/vnd.in-toto+json
