## `clojure:temurin-21-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:91deabe4319836bdf2ecabac8f16c0c6298e690e81494443be7625ba5e43ea5e
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

### `clojure:temurin-21-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:26aad1547a936512b3b651a394916adb3235f11e770c53bdfb54309e92795db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230880243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9d1bfef59c1f7c71f725619135a9ff2b8a28b49b75cbfec3494d057056f226`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:36:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:27 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:27 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:40 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:40 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a712539d9d0ede94ae1afac188dec8c51f22aec7f41fce248066d87c90e9441`  
		Last Modified: Tue, 16 Jun 2026 23:38:03 GMT  
		Size: 158.2 MB (158166905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7380d0315c58061f9337984db1e6559dd71ebbc9fc0d8a956d32e8d5ff2cf1`  
		Last Modified: Tue, 16 Jun 2026 23:38:00 GMT  
		Size: 18.9 MB (18880561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9133e0cc8845b9ab978181460006f6991d4d3383df504856bead8f126a1030`  
		Last Modified: Tue, 16 Jun 2026 23:38:00 GMT  
		Size: 4.5 MB (4515225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc0e3988033c14665c924e89f4acba80ab18fc79054a67b0fe3ef20ccf9f0cc`  
		Last Modified: Tue, 16 Jun 2026 23:37:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d372ac72eecb80ed8e987acb97a9e59c7a13ced282ad4ad414e777dc2a024c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546e033973470fd1732db7f089503e156b513490443b83f5b0aad612e7176fb`

```dockerfile
```

-	Layers:
	-	`sha256:a35ea70fb5d295b9e0ca1a8835ff0a78296313a3e555b83fce92421312324d92`  
		Last Modified: Tue, 16 Jun 2026 23:38:00 GMT  
		Size: 3.8 MB (3819672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588c50dc1aeec4de613541445e3acde205c640bfe3a34c9c6aeba9f844ac8d2c`  
		Last Modified: Tue, 16 Jun 2026 23:38:00 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6fc32a88d1e7777cdaa80126da89bc6bb1cd99a8104ad29c28ebe7566a6063f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229494390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0699e8f204fb006f4a58a73928c0d74efaaef01d033b48295b4ef56965d77c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:36:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:11 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:11 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:25 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:25 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cabb4cd18d63848d161346612936fa6e38cba0b726ae189acbc3dd76ae851c1`  
		Last Modified: Tue, 16 Jun 2026 23:37:47 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6bda34f0b777883617d60c0a224c2292e9673fa13222745f3bac2dc2467dd7`  
		Last Modified: Tue, 16 Jun 2026 23:37:44 GMT  
		Size: 18.8 MB (18839287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2b5db8b1f2c3018e13f42c23c944c6ce2eec4f51c9a466ac178bddd5f1115f`  
		Last Modified: Tue, 16 Jun 2026 23:37:44 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8aaa5062f903a252269427531a0943db320251f9fc05440ceebd8fdd9d9d9d`  
		Last Modified: Tue, 16 Jun 2026 23:37:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:899856ef7d6c3408f3d11ccb2c817b1e00dc0ad21a884f3fcc484b9073c07aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3b38bf96d896a3cf5953dde19f591d1bcff5f8265b85533070ca2999f5542f`

```dockerfile
```

-	Layers:
	-	`sha256:c8c20591a824ab93a01286c08027ebbf8276466bcc2f66f25f7e23412d01138c`  
		Last Modified: Tue, 16 Jun 2026 23:37:44 GMT  
		Size: 3.8 MB (3819912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd9b7b99762dcb2fb23f7d09aa1aab14270958adce794b3584916315dbec9a2`  
		Last Modified: Tue, 16 Jun 2026 23:37:43 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:17a2968a87e1f9e035fcfb8c47b5be22a351fb8c9e51bd87fc69a3821f78f617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234933346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4e4786dc0651daedb080a89ce9a7ba162087af870616b772c44004ae17d31d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:58:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:58:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:58:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:58:45 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:58:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:58:45 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:01:51 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:01:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:01:51 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:01:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:01:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:01:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:01:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb31c7f870ef8ec8aee6455f55c7a957b94017aabba051fbeec8aa80bef9255`  
		Last Modified: Wed, 17 Jun 2026 00:02:33 GMT  
		Size: 158.3 MB (158343224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7099720225c0913e06beb4b66d0993f2d24465d292ead3ccc21012c6ea6c60`  
		Last Modified: Wed, 17 Jun 2026 00:02:30 GMT  
		Size: 18.9 MB (18936575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572eb8e468a623338b828d27253938d7ebdcdafe0d2aa6fb9a99fb626d612a0e`  
		Last Modified: Wed, 17 Jun 2026 00:02:29 GMT  
		Size: 4.5 MB (4515178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feada1fc189bbd5c1b77428e5da9f33471d76dde443943c45a2c74ca8af17d6`  
		Last Modified: Wed, 17 Jun 2026 00:02:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:69881f804222854e99bb382329404c64ac08e596ee386885d708ca5d8dd24dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa939f93893e8a5a6e159f3de53f1f55cebba308bef055633cb31774cea6a48`

```dockerfile
```

-	Layers:
	-	`sha256:5c4c31cd967a5ba72f9873ec9a4000b8dad9d26c88cd08c006cb4eda0b3f3478`  
		Last Modified: Wed, 17 Jun 2026 00:02:29 GMT  
		Size: 3.8 MB (3820672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0e8e12a014e3d8e2e251127c2ffcf2c905a5a4d918e2f923f2962ef5eccac05`  
		Last Modified: Wed, 17 Jun 2026 00:02:29 GMT  
		Size: 17.8 KB (17761 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:11d3e4f42d2a7ab26016d81c5bbe221926434149fa8a2bf5bf2eabc6dc133d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220212066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57560875545191631256b8d07931c4908c364bc0345a699b7f985cf890a1309`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:00 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:00 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:09 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:09 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c55ae26073105dbb12b878ce93ae33f8d0835ba25a28114c5d1f6b6e4fbfe51`  
		Last Modified: Tue, 16 Jun 2026 23:39:40 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ed8fffe07365062638d3780860c11f8ebedb06921526b4a116d98ac067672c`  
		Last Modified: Tue, 16 Jun 2026 23:39:38 GMT  
		Size: 18.9 MB (18922194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c44b7c05292bccf0719d305d7c8dae4e67c8b1c9b17020ee85eea9905c0b1c`  
		Last Modified: Tue, 16 Jun 2026 23:39:37 GMT  
		Size: 4.5 MB (4515197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77f648c5cda2aec12fce9071454320634ece56c82da8fbc8299f19a0178c704`  
		Last Modified: Tue, 16 Jun 2026 23:39:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9777c17f3bed9abba631d923a4d810ff9c583198ca87160cdcf4a0efa57efe6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ce63a979e57cd3ab1f303c3e55f7f06173257f7aebe6268f9ee34cd86301e`

```dockerfile
```

-	Layers:
	-	`sha256:2e53dfe7db06491d38cd1c9e63560c8a0524fb57a4ac3ecc6fcab012a94bfb92`  
		Last Modified: Tue, 16 Jun 2026 23:39:37 GMT  
		Size: 3.8 MB (3816099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2074b3e95adeb45fc227ff1f6a7f0bf4b823caf75fbcaadb76cc63fa4c2dc1`  
		Last Modified: Tue, 16 Jun 2026 23:39:37 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json
