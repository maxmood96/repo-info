## `clojure:temurin-21-lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:f729710d25df64f3135fa195cd16a9667148d940d502fa988910a18b6277b04e
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

### `clojure:temurin-21-lein-2.13.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c654c85577a986bcab428117eef1fe94ec66c689ef60842988c9e170b2b6b4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231292442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d89756752758bb14ed84ece3a283943b05f3b8fe91fc070e263119333b96f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:35:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:35:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:35:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:35:29 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:35:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:35:29 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:36:38 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:36:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:36:38 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:36:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:36:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:36:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:36:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841d6c549cb0fa3524afa27cc9b66bbbf9be6f7676889e444208dd0ef22aa014`  
		Last Modified: Tue, 16 Jun 2026 23:37:01 GMT  
		Size: 158.2 MB (158166942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16246750f57220de36b0ce03e2df00c972d5cb18e661b352619dcddb389fcafd`  
		Last Modified: Tue, 16 Jun 2026 23:36:58 GMT  
		Size: 20.1 MB (20107816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa1b89f036c3606685bc3110b6d2cc9fdd3463cf9841470f0c240b3e1f15ac`  
		Last Modified: Tue, 16 Jun 2026 23:36:57 GMT  
		Size: 4.5 MB (4515213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c8dc2160e8f0a09ec3dfd184db7ead41c407899be7b3730dcd7018b92fdb61`  
		Last Modified: Tue, 16 Jun 2026 23:36:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:70b52049a69fefc6f5aee60083a065c5c408f6138617dbc98776e81c829497b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b8d1d59282af636cd8ede76be0e3c4f6b2bd53811bb2da999a5a151a67cfdf`

```dockerfile
```

-	Layers:
	-	`sha256:d765db9ff4c7ddfdda816f078372cceebbdf840a036567ac45e03809c232f30e`  
		Last Modified: Tue, 16 Jun 2026 23:36:58 GMT  
		Size: 4.3 MB (4286520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c047f7adcf8a60d33dbc8b7835f91056c6a9924dff6a88e0836a01ef0ea3bb98`  
		Last Modified: Tue, 16 Jun 2026 23:36:57 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c06588627ed4ac5bfcb1a644e50866bf8aeb7be4d8510e6f325aff9c8ab011d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229306223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34e8f57814a69867b2436ebdb31c0c716ed36d73a0394565f3f69cade3a43b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:35:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:35:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:35:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:35:09 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:35:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:35:09 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:36:16 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:36:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:36:16 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:36:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:36:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:36:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:36:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58ff78706ed9c2ce0aeedc0a126e3c079b33cb50e0cef4a4662929ee5ecc58`  
		Last Modified: Tue, 16 Jun 2026 23:36:39 GMT  
		Size: 156.5 MB (156461329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fe004de669f42d77659baef66982db73058e65acdcfff66f59c772080be270`  
		Last Modified: Tue, 16 Jun 2026 23:36:36 GMT  
		Size: 19.9 MB (19940269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4c84c015b8a38803df7efb4453cb4a6ea74ad080a411826a5d6e69dc8dc2e`  
		Last Modified: Tue, 16 Jun 2026 23:36:36 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a773bf26785c1534ad268c3e7dde5b5b6d432c78d54a13793f15edbb81d1d8`  
		Last Modified: Tue, 16 Jun 2026 23:36:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:771000d36b3e12b1e21c1f45cfd271cefc0b4bbaf5f540c9a8ac03d1957959b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be88dab207671fc9eeb7dc40feec255539f078593aafad29f12cb88f65cbca27`

```dockerfile
```

-	Layers:
	-	`sha256:aa33b155c79d961c7e9940c62fc8680254679fd997f1e3d5145407d2cc570cda`  
		Last Modified: Tue, 16 Jun 2026 23:36:35 GMT  
		Size: 4.3 MB (4286159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748235ca9790f6ffc7eb7373dce1d880d8a5368ed9ddcf57ed48b1dd88332778`  
		Last Modified: Tue, 16 Jun 2026 23:36:35 GMT  
		Size: 18.5 KB (18532 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:43efeed3decb6e91b2e508cb1c96668878a0d118d54404d42566ea53a5d0c55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235537443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532a20bf16f3dc91f7cb36e806e341f1035f13b5777c975b8952f36601e94a43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:52:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:52:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:52:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:52:36 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:52:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:52:36 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:55:04 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:55:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:55:04 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:55:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:55:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:55:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:55:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2baefaed51aa669676a6ca72a1976a52e2ef31d6ede3f6e16283490f461501`  
		Last Modified: Tue, 16 Jun 2026 23:55:52 GMT  
		Size: 158.3 MB (158343250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e1762dab3b12110445d517436d5dd79afd8d83f1d1a439e96a794c216f36ff`  
		Last Modified: Tue, 16 Jun 2026 23:55:48 GMT  
		Size: 20.3 MB (20331915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894766e1b2773f8625e4a21b64cf66378dd5fda0b734343805be2d1573d85c94`  
		Last Modified: Tue, 16 Jun 2026 23:55:48 GMT  
		Size: 4.5 MB (4515177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffc8cbac292e1f94413f98d281d038f1fa8f7bc61f127f95c1f3d872e62801c`  
		Last Modified: Tue, 16 Jun 2026 23:55:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f749ba3020a9dc076d27021f6afea3a8e41f643615d9853a5d5f7c581b88c477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddd1c14c94edfc3550e61333a24149db6c6ad121c17e3669a7f7204daf7b870`

```dockerfile
```

-	Layers:
	-	`sha256:42e37de35e022e2ab98d307f95455b66e75ea5d6c0e44e2ed3e33ce0c1f6b951`  
		Last Modified: Tue, 16 Jun 2026 23:55:48 GMT  
		Size: 4.3 MB (4288393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff12c684b18ea7c44ae10971f9db9bc6884984d68147d67f088808a5dda93e99`  
		Last Modified: Tue, 16 Jun 2026 23:55:47 GMT  
		Size: 18.4 KB (18444 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0d8dfbc03dacbd71d6be3c4c5a7be8d1bda69a5d34e53c961e3d8354e72ac91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218836061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bafd72370004ee35f77ef85f4cd2bd5d99e011e7d4306dad554a4cdfc633305`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:10 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:10 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:11 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:11 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f3439d92caf07670440a960bb879707c16dc5e881fbc688c4e1a643175e72b`  
		Last Modified: Tue, 16 Jun 2026 23:37:41 GMT  
		Size: 147.4 MB (147388366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448b2f1929830044715136d8917d3cf5e3b43adeebc3f4d6a7faed46f42782db`  
		Last Modified: Tue, 16 Jun 2026 23:37:39 GMT  
		Size: 19.8 MB (19770559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4fb1919e8e25d0a10f1912fe111f152ec981ab09fb0adba162eae09b90b5a6`  
		Last Modified: Tue, 16 Jun 2026 23:37:38 GMT  
		Size: 4.5 MB (4515205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf6f584c7a4c4035174f1b27e3dedb0c93a167ae544088b733b2bc1e6be08e1`  
		Last Modified: Tue, 16 Jun 2026 23:37:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:eb1c54268b9587d40c5cc7613d7af31a99bb0297160862da20ac600d6042abb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53efa43612e487255e197c3be0d12782cef724b58e58edbc13fcdd4841f9b83e`

```dockerfile
```

-	Layers:
	-	`sha256:3d8534d09f58c517b1b17498c24222b67cb822b65f0eb708d4ba0a48af7f4424`  
		Last Modified: Tue, 16 Jun 2026 23:37:38 GMT  
		Size: 4.3 MB (4278334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a941a0e487cab99c83d5c06a6f661c604084677fcf32e3602a0600f0499fc3b`  
		Last Modified: Tue, 16 Jun 2026 23:37:38 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json
