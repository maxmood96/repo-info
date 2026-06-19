## `clojure:temurin-26-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:843559aa97d798227be008dc4fb4ba8ffa41baab52c0268ba1fecd6e4f52aa6a
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

### `clojure:temurin-26-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:82bbde45c2c5c457b543e7794a02552fc136873f6ee5ccf13f26452971d0bdde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167237589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d80d8042de72374b9ac485c611fd808179a27eed737be819c0c2934af9cb6a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:35 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:35 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:44 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:44 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ffe03213049c233dccee5d0a9fd1bfd39b2c4423c3c79c883f6a1ba48de265`  
		Last Modified: Fri, 19 Jun 2026 02:23:04 GMT  
		Size: 94.5 MB (94524351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b4d0977309b96fdcb95a79dc81e67d7b8b8de3e9f04305d4da642aa962adf3`  
		Last Modified: Fri, 19 Jun 2026 02:23:02 GMT  
		Size: 18.9 MB (18880498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef5d9c04aa2f6ae2cbab8a2c8afda3f78bd201e6091ef4767c2b7c59ca6ad91`  
		Last Modified: Fri, 19 Jun 2026 02:23:02 GMT  
		Size: 4.5 MB (4515190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806c875d9f68bf79e8b80dee95e2423f2ab2ee222a14d41217d0fd67b51e8351`  
		Last Modified: Fri, 19 Jun 2026 02:23:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:66a0f5955ef14993ea4ce65f38ae656d38e8d41f1111bae47cce8b34baf7c9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76373fa1d23caea367b988007519cde175ce3977ab09030d3b55315bd74e1ba4`

```dockerfile
```

-	Layers:
	-	`sha256:3d0d94e6cacef94986cdbfd8392fb165741f7b2c30b6eaf63169c1af664e067f`  
		Last Modified: Fri, 19 Jun 2026 02:23:02 GMT  
		Size: 3.8 MB (3782711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34f397ec13eacb73492f5f6552fcbc1465ecc3473d0854c06d1e3bce9249156`  
		Last Modified: Fri, 19 Jun 2026 02:23:01 GMT  
		Size: 17.7 KB (17710 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:83b029a4f944c645a6ed47e2ab75dc4d9e71fd3cd9272e4cf2f026bb5f7f8452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166537743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054bf88bf282238a2ad6bc9312713dae8ed1e013ddd9268abef3e500004b2979`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:45 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:45 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:23:02 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:23:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:23:02 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:23:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:23:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:23:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:23:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbecfb1b112c56f04bcb4f86e7427c8f61740d8298dc7a1e35a95ee4fef2033`  
		Last Modified: Fri, 19 Jun 2026 02:23:21 GMT  
		Size: 93.5 MB (93504322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b88456bf80ffebc412e6d4960761b96aca61c4d05ce1a89cf046ccea75c2da`  
		Last Modified: Fri, 19 Jun 2026 02:23:20 GMT  
		Size: 18.8 MB (18839653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3bdf38b8bb7df06d333706671701fc6579cb76be26e08114375b58d5ed91ee`  
		Last Modified: Fri, 19 Jun 2026 02:23:20 GMT  
		Size: 4.5 MB (4515168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8338dc979a026f5f703366fe3561048ed699ace44b5f03c4c764924ce6bf948`  
		Last Modified: Fri, 19 Jun 2026 02:23:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:24d2cfbcb1399b7662339868f766a1c0871d23d40b28e4ef4c041cc2dd2fca5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0114b444702a7685bda94dcad0e4c9742fb618205a6cd6b09e6efb7693fdc9a`

```dockerfile
```

-	Layers:
	-	`sha256:ec62569f783333f033169bda919a4a48409b1effbb7a59210f46f0b568551eb2`  
		Last Modified: Fri, 19 Jun 2026 02:23:20 GMT  
		Size: 3.8 MB (3782948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456ef33c5274763ee1d06cc8c5a6ab9fbe76d4b86fadf8b6e5122d579e3a69ae`  
		Last Modified: Fri, 19 Jun 2026 02:23:19 GMT  
		Size: 17.8 KB (17832 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a2829be1e7fdd335db1fca9ad192b56dbe2ff9bfd115774f6a6610e2711837a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170492207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e234cdc7623c1bd4ae74205325c115fbdaed8085d21f4205ec5bb3d0260a93fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:14:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:14:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:14:41 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:14:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:14:42 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:17:40 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:17:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:17:40 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:17:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:17:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:17:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:17:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328775c3b052bb498a48836eab308724b02180a01e1a5397b2235df60a8765bf`  
		Last Modified: Wed, 17 Jun 2026 00:18:19 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c0856248fb467b82985129297c21544fb2328e6f1fb68d6913e6e87ca96b7c`  
		Last Modified: Wed, 17 Jun 2026 00:18:17 GMT  
		Size: 18.9 MB (18936572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064532ee2c899459b97ebc1eb2b2b07fc800dcc2b2ce9e37a19f17ef71edc802`  
		Last Modified: Wed, 17 Jun 2026 00:18:16 GMT  
		Size: 4.5 MB (4515185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c2f5619a2374ba7c1d16953d8042d97597f1b93902129f3555e8ebb80ad576`  
		Last Modified: Wed, 17 Jun 2026 00:18:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1a2caedad55b51d49138e7d741ff6df37e9343b5b5a261714c05766fd7711862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7d209ad7d503bba88db04edc0ab83b7bdc346b86a7e957b51c6a914c6308e8`

```dockerfile
```

-	Layers:
	-	`sha256:bd2b7838da7143212cb8c4e0aaf37e6636156970d2a77132a460446719833bf7`  
		Last Modified: Fri, 19 Jun 2026 02:59:21 GMT  
		Size: 3.8 MB (3767647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5510daff7e8c3f7e426a67c2ab48deb83a7390cc453d831e91b29b078fe56ef8`  
		Last Modified: Fri, 19 Jun 2026 02:59:21 GMT  
		Size: 17.8 KB (17755 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:098c901429176bf0a0454f4cf14c7d65e87500ae44603846f648dc3c1d825a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163360901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f232aee87967f8585e380750be7bbb020cddfa4da74b9c38e8203ad78d4e33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:23:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:23:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:23:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:23:18 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:23:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:23:18 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:24:27 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:24:27 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:24:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:24:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:24:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:24:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e115ed65869a2302b68254f8c52d0c2feb86c4b1d7188f0b2f1d3602dd4ffc27`  
		Last Modified: Fri, 19 Jun 2026 02:24:55 GMT  
		Size: 90.5 MB (90536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8ac7a218a1ee31e69904158cbeb24c7c65ec011682530577cade5566c17f41`  
		Last Modified: Fri, 19 Jun 2026 02:24:53 GMT  
		Size: 18.9 MB (18922457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45b33541446e777633ba30a4c7a3b3cac925bb73a80cd475a6fdc5559706e00`  
		Last Modified: Fri, 19 Jun 2026 02:24:53 GMT  
		Size: 4.5 MB (4515184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdc4799e639138692c2aeca9d0434918e8168f653ef5969f6f3557b83448a46`  
		Last Modified: Fri, 19 Jun 2026 02:24:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9585ababed35a7f8420ba50bd6b727cbbde3f935e06ea6599a5ffb0eec7234d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0626c31ebb7d6064e27324c53b3b2caee0a7191a4e374fe69c25281c34df384f`

```dockerfile
```

-	Layers:
	-	`sha256:f3cb82af5031699448cdfe94f441616406a6f94c82175824ab7a43f4d940a448`  
		Last Modified: Fri, 19 Jun 2026 02:24:53 GMT  
		Size: 3.8 MB (3764324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320bc14d36aafdc7c80fb50727767b40cc18d7fa482e6fddaa7637ac036887b2`  
		Last Modified: Fri, 19 Jun 2026 02:24:53 GMT  
		Size: 17.7 KB (17710 bytes)  
		MIME: application/vnd.in-toto+json
