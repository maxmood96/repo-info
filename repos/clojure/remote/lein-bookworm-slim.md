## `clojure:lein-bookworm-slim`

```console
$ docker pull clojure@sha256:3531acd6ea5f13238377a35d6b7ed105b665ff2399a136ec30f2d753cff6111b
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

### `clojure:lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d6985dcce977998b76f534c976871eea4b7d76d15867cc2ad62e1aeedd8c3c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143387669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579495097b748ec733b75d12710fe2386b7cbdf04771fd477fecf73bb57c81e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:56 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:56 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:05 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:05 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3e8ca1600ac8928daf08c751b49624e8ef327da5aca76b12b4e80bc28459d5`  
		Last Modified: Tue, 16 Jun 2026 23:38:26 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f7f64271e31ac343ad68022f9d52940832c8e835a07532d7183cb14f8d76f8`  
		Last Modified: Tue, 16 Jun 2026 23:38:24 GMT  
		Size: 18.1 MB (18059856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df606c6550afd92a8bf678291f81b59cc60cd9775b5c0e5937acce24e1db910`  
		Last Modified: Tue, 16 Jun 2026 23:38:23 GMT  
		Size: 4.5 MB (4515195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e68522faf33bef360e2fb57121363e906ff8e2aa82d073d5e3d26c16cfe6483`  
		Last Modified: Tue, 16 Jun 2026 23:38:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:711cc277869272c0fa7218138085d37599a40e7d15f53ab79899593d7c93c87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1098125e1b8b3fdbb2bea5b644b31bf5805f46f6a10e974bdfbc61ef37c7f29`

```dockerfile
```

-	Layers:
	-	`sha256:a1b7689eda8b2cdbe3d1984f2f41881bb77e40cf526e51acfa6b2be4394c4610`  
		Last Modified: Tue, 16 Jun 2026 23:38:23 GMT  
		Size: 2.7 MB (2700393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b79be22a96d980fbd4da8e03970f4314ea317aaa8e3df09007fb141cd5a6c26`  
		Last Modified: Tue, 16 Jun 2026 23:38:23 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c86221e83f2d38e622902e5ae9afbd5358eb9253994688e7e767944164c30f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142074493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a878b42144befc6bf987a4508241bc9a1b66ad0ff2a472a8a52c9db4f3ace96b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:52 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:52 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:59 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:59 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366947bc85ba2bc0c491940764363726a26c175323849c8baa2eed6d237b2495`  
		Last Modified: Tue, 16 Jun 2026 23:38:19 GMT  
		Size: 91.5 MB (91542296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97624e3c43a7cb02a613fc63a2fc0d72e319b4a4ed041dd9bc7c2feb56fe374`  
		Last Modified: Tue, 16 Jun 2026 23:38:17 GMT  
		Size: 17.9 MB (17894269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4700d2166b6643b0552d7715711f820ce50aeac53ba52effb58301f3629873`  
		Last Modified: Tue, 16 Jun 2026 23:38:17 GMT  
		Size: 4.5 MB (4515192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba3b59d187c6906f90983577d8d6890b63e9a37fad5d1fe65aa156382df0f24`  
		Last Modified: Tue, 16 Jun 2026 23:38:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ebbab4c7b01b6b0e06e8c9b9a3b2662ecbaef8f40a109e995905c068a6e4734c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bf9519ed23a06403074f39dcaf7a883df594358ea013f658d066649856a0d6`

```dockerfile
```

-	Layers:
	-	`sha256:e07294d58cd6f4bdf043d30b479a8cb8f31112ecb60459f4923746f350ceb3bb`  
		Last Modified: Tue, 16 Jun 2026 23:38:16 GMT  
		Size: 2.7 MB (2700029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b458a63a39939cecbf6dc5578566c32d819562396f98957893a0fb4ea8ec28`  
		Last Modified: Tue, 16 Jun 2026 23:38:16 GMT  
		Size: 18.6 KB (18573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4e72e21040f740ad405454610c44a9a94302f4e703e1d43dc50fa1fd35d0b215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146775616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c5150f7938eb18bb743ed0044513960e4ab0f3e4416fa724f55698a16e13aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:03:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:03:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:03:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:03:19 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:03:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:03:20 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:05:41 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:05:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:05:41 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:05:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:05:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:05:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:05:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ceb0eb5280b5d711b09e7b6fc60f0539124c87d3b78261261a7696dc0d1b48`  
		Last Modified: Wed, 17 Jun 2026 00:06:20 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288824b737e140672c5359ac26cdf40f7402af84806ca2f2ca85693c1a65540d`  
		Last Modified: Wed, 17 Jun 2026 00:06:18 GMT  
		Size: 18.3 MB (18263976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d8b18ccb620978340ca0e9523359cdcd9b22288db9e8520225def4084cfb72`  
		Last Modified: Wed, 17 Jun 2026 00:06:18 GMT  
		Size: 4.5 MB (4515231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c1d33dd77c9c8b63e94da87f5cf3fad3f10c885655fc1a1dbfa1a05ae9eda7`  
		Last Modified: Wed, 17 Jun 2026 00:06:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:76c4bc6e710dd0680b57da437d35cf85e47300ad71a03d4ec5226621cac7c989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2704034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd89b6e5aa34335c8dbec51258f4ab81fd37b1ee159971eff5138831de5ac6f`

```dockerfile
```

-	Layers:
	-	`sha256:d2fbd97198e1a4cbcbd08b84e18a99878932b054148e64dc168c0222788ae0f5`  
		Last Modified: Wed, 17 Jun 2026 00:06:17 GMT  
		Size: 2.7 MB (2685550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbcc0445ee6d66b93382d1804081c1063ce3d33cb7c983d7b14f360de05dc9d`  
		Last Modified: Wed, 17 Jun 2026 00:06:17 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:47c8263fad1490ee21b77af8bc00eeec8f6c6d7e177e74097ba23c6053d6325a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f510cc9a01a262329ceb1cea06fcc03cc00af3955d109872f8b35a0e4d31a203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:39:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:39:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:39:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:39:29 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:39:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:39:29 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:40:31 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:40:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:40:31 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:40:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:40:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:40:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:40:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff3de415fa78938620383fc0bde8a9b11d2013998e032ef0dbe1f7aced550ef`  
		Last Modified: Tue, 16 Jun 2026 23:40:57 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db31d6184e94a73dfdc19d54c7477e86ba9544c3aa872a9fe277cb4e57301bc5`  
		Last Modified: Tue, 16 Jun 2026 23:40:56 GMT  
		Size: 17.7 MB (17724890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc54dc80ad94c7d4dd82a86a9e8bc90f64309a8d9902871c207f12752fffe5`  
		Last Modified: Tue, 16 Jun 2026 23:40:55 GMT  
		Size: 4.5 MB (4515209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a430ccf529c0b304995632980e226a216ce4b1e417bbe3608b432ec65290d6`  
		Last Modified: Tue, 16 Jun 2026 23:40:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9783971186a3666cb0aca99defb6711cb8e2b56220d2b4e28b28fce944337f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280095288afb2b183bda70bc8878cfb7e422ad78119839b4ef40eb8099c6522b`

```dockerfile
```

-	Layers:
	-	`sha256:3ece7b6b861ecc4c22c451f54d730888c07b88d950494a94d2f1b66ce5a17688`  
		Last Modified: Tue, 16 Jun 2026 23:40:55 GMT  
		Size: 2.7 MB (2676769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:770a2f4efa9eb174cfa93851428a86a1598aef165bfb759e9a07744878a16622`  
		Last Modified: Tue, 16 Jun 2026 23:40:55 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json
