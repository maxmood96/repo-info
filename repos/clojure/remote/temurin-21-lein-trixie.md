## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:cce78b9e7ea0a103e794ffa4e74831ec3b4b04b17d5b0e0aa5b4e8c6a9d68bc6
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

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:01f7055d1bac83ba63abefaebeb7d9b392470e57eddf9b0522983823f78f8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230879842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafaff6818102960323411eef0ae087d46cd2c8a368985cdbad4de64b7022241`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:36 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:36 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:45 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:45 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ffcb1f06b7d559d9476421e8a86722c9124bab3c74bb17358828c88b45f866`  
		Last Modified: Fri, 19 Jun 2026 02:20:10 GMT  
		Size: 158.2 MB (158166925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5ac9145dab7ce75f7ab9d0b69ec7abc7bd0a87c9bc85b3525e2c6b92ed8a04`  
		Last Modified: Fri, 19 Jun 2026 02:20:05 GMT  
		Size: 18.9 MB (18880174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1950184eb99670da1f04abf5c500b064441a37e74508c08fe448a21c6de09e8e`  
		Last Modified: Fri, 19 Jun 2026 02:20:05 GMT  
		Size: 4.5 MB (4515193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5181a3f6dc4c2a93abe8439dfbd7664c291b04753172a22a0b88ab6f3b225a21`  
		Last Modified: Fri, 19 Jun 2026 02:20:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b7e265f37924b3b586cce25e910bdddd836b56506af744d86df10969674fecbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e14e309532b914b00f885445bfbface9073f96616605d6d553a0ae7cf799d3`

```dockerfile
```

-	Layers:
	-	`sha256:b70429fdb3c3bdb2ae526db537f061bf3bc87d02d697316fd78cb8a91dc6a244`  
		Last Modified: Fri, 19 Jun 2026 02:20:05 GMT  
		Size: 3.8 MB (3819672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f73719f389410385c7bc8baef9feeff3ccbaa6e1a881ef2609ac7582e32f58`  
		Last Modified: Fri, 19 Jun 2026 02:20:04 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b09fd5f8248a0ea697810248136464fbdaf562b3a2dfc4839f0456e7e631605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229494719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3727597deb5b8dcb0edb269314a905c46201d7b43ae319c5e501b7af117f8af6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:18:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:50 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:50 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:05 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:20:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:20:05 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:20:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:20:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86abf5a978f1933a6792a4d8263aaef8f172a011b54575e720d23720fe4a6ca2`  
		Last Modified: Fri, 19 Jun 2026 02:20:29 GMT  
		Size: 156.5 MB (156461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010a0a7105e1b4d491f0e47ca0d83eed71e980e5a40324ecf84ba2a4e3f68846`  
		Last Modified: Fri, 19 Jun 2026 02:20:26 GMT  
		Size: 18.8 MB (18839648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a5a2fd271a41173f21895a17a0f491d302be1a584e9839233d2f1f7bb3c124`  
		Last Modified: Fri, 19 Jun 2026 02:20:25 GMT  
		Size: 4.5 MB (4515221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5472090b73674643cf441d8917e2f8118ef44663aaa2666a0eaed546e86c8f6`  
		Last Modified: Fri, 19 Jun 2026 02:20:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:95c5d3f61d9c8c3ef4142291f70ff005075e6a16502fbf13aaf65618f696c5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51e4d6dc4127b3d4ebca013ffdc2a6554ea1a6ab60e5371dd86dd9886326a08`

```dockerfile
```

-	Layers:
	-	`sha256:888d7d3188927e627d354866babae70fa31f7c580ac84def2e35a7eca354ecbe`  
		Last Modified: Fri, 19 Jun 2026 02:20:25 GMT  
		Size: 3.8 MB (3819912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a584d6abd6451fa2d0db05e1db7e47705c1277aa5c95900475c871301997889c`  
		Last Modified: Fri, 19 Jun 2026 02:20:25 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ab14769b431f16a0a6ab95c589476021c80d4faac7f736afa5ce7adea03bfddf
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

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b593370ee92e6fe86a5c22afad7ae1274a04fe267489be3516d189ff163800fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5df3c4988872ad6ff719a593b52111e55a9a2f9ffa31b9787caa80dd33388ff`

```dockerfile
```

-	Layers:
	-	`sha256:19326b132076c95083fd5e71612040f62f8aaa1191fdee9bf1e8b43bc33f27ba`  
		Last Modified: Fri, 19 Jun 2026 02:49:51 GMT  
		Size: 3.8 MB (3820672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd7c040213623a901057c08ae52d8ecf74bc60ed625ab0019d81d797c622efb`  
		Last Modified: Fri, 19 Jun 2026 02:49:51 GMT  
		Size: 17.8 KB (17762 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e6b7a66657eea5881e8116c55eb2ae638eb3d93c6662b336a63fc26c15f101ee
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

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6ca5b81a2e8cefb2a54d291a661174f0c2f48fa378c94a99109a652b4b83179f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c79ba919607906847ddf9ffb353028b4a9991d6a4740a447549fdaf63717081`

```dockerfile
```

-	Layers:
	-	`sha256:7da08f9f8c9d8c83c2e95d12a784ff563f810af428c56c704eabc4c1de1d54a1`  
		Last Modified: Fri, 19 Jun 2026 02:20:00 GMT  
		Size: 3.8 MB (3816099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e64c03082668cb74832df27a5678250a93334fd617e338854e6976a8dd074e4`  
		Last Modified: Fri, 19 Jun 2026 02:19:59 GMT  
		Size: 17.7 KB (17718 bytes)  
		MIME: application/vnd.in-toto+json
