## `clojure:temurin-21-lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:79fc3a99cfec110fe28b2c00fd8b87b8926c6f6dbd256c35e5c76f5cabb17ff9
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
$ docker pull clojure@sha256:d68ec1588958dad2640ed6a0bfc25f8b8c748e0dd72c56751d10d6a38573e4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231292346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc311ac2e4f5178cacd347a209d1d6998b46beb80a580a7a8bcb933a40fe61b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:16 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:16 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:27 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:27 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d951ded53ff5c7ddfb006c9835f3757a6f6b1671a7a58939b47cd4b92ed1bf85`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 158.2 MB (158166924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f2fea01b0ce12eef715c79c43f7f6df7f61dad7e66d5a0499590694ec87fa2`  
		Last Modified: Fri, 19 Jun 2026 02:19:47 GMT  
		Size: 20.1 MB (20107762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0619937413e5ef69cec0430c3eb0c039f775964c0d5b7cdd16c3f798a2f49`  
		Last Modified: Fri, 19 Jun 2026 02:19:46 GMT  
		Size: 4.5 MB (4515189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887944c6f71103dcc95e907cf519b8d0b29e2fd695e017db86323bb51305daac`  
		Last Modified: Fri, 19 Jun 2026 02:19:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cbdeb7ab4750958c1a4e4cfbc98608af784227f9ed3136226270e6b140e319e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b219076989d5cf2fc15d0d7f2b43218255e9f4d2cdf26de908475fb51762f262`

```dockerfile
```

-	Layers:
	-	`sha256:b35cfa2403c2a9afe82433dc9155779ce2d01e93da4d3b135184a2d7d78e7e56`  
		Last Modified: Fri, 19 Jun 2026 02:19:46 GMT  
		Size: 4.3 MB (4286520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5e562a6220baca691816613c9a05bdf0322e155cead6db72997167000b4c15`  
		Last Modified: Fri, 19 Jun 2026 02:19:46 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70b48b738ee48c2da7a7883c448d19b126d897e055f2376f72b6cc7484ebc090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229305603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e263146337bc965ed687a7dd6a04d269b6f5ae57eba5b5d057ac7c2e0243add`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:18:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:21 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:21 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:30 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:30 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f28deb8c44c3e4ff92a1bbcad713bb8704d2b0e9807c731ef971152dd2292f6`  
		Last Modified: Fri, 19 Jun 2026 02:19:53 GMT  
		Size: 156.5 MB (156461269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607da8fc4cae1994706c8a053032efbda931f612e5c88a81e938a822f5376bb6`  
		Last Modified: Fri, 19 Jun 2026 02:19:50 GMT  
		Size: 19.9 MB (19939684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e7ead590c30bddf4a5af5d03626ad16f584cdfeff05af5860b56e97b95af88`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 4.5 MB (4515204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f0dfef2d45f5b9bd2824e35353ec134004307619a58e3bfa5fa1e7d68f9b7`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c72d23cb7d4a61898e4324417864eaaab6b4c555dd5bdf221f8004f7abb877f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1feb937f13abd5c5d44cb219e37efe55f5c9d53cf985bc39c17ac144e8e06f3d`

```dockerfile
```

-	Layers:
	-	`sha256:1eff2e8ae4d8943faf76e48340f44e3f6f18fbf16fd5bd1ee7e7aa169034dc8c`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 4.3 MB (4286159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5af3a00f3a96aba4b2472c495cddf1531a548c3eb05d32f76a588db08c5d04b1`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 18.5 KB (18532 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7ff50696421d593597b96a454fc6dccd6099fcc093ed307677c5c00745c9f148
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
$ docker pull clojure@sha256:4185d3a08cc9998911e36262f01d0d1ac5ac233795cbef6119c427d8f43a4994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1040e3b4f3071beae18b8907ad870acd6fcc076f3aec749b1b8848486d9e5a5`

```dockerfile
```

-	Layers:
	-	`sha256:043eacf79ed5e8f7e34b7340061677c82e05f0ab2f4b700ddf7f3d64d8e2bb06`  
		Last Modified: Fri, 19 Jun 2026 02:49:17 GMT  
		Size: 4.3 MB (4288393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b7b7c1cd6fba7447e403eed2dfec3f5b7ea20d7aa7aff9599c7913b533e4aa`  
		Last Modified: Fri, 19 Jun 2026 02:49:16 GMT  
		Size: 18.4 KB (18444 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c4cd4d42ce8479b08515f54cb8ce0ea28f5953a6296e1a097b029f7721b23f47
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
$ docker pull clojure@sha256:b22659930c75b5d0da611601ddd6ff9ccd616326d20fdbb6e331247e2b662d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1052f2dcc063aa2204566c402773e55de4da2527e3d000df312866f952576280`

```dockerfile
```

-	Layers:
	-	`sha256:b74348791b2a36cec7b13520f8d3133ef6d7467fa9e87359a04f1fabefd6a7d7`  
		Last Modified: Fri, 19 Jun 2026 02:19:29 GMT  
		Size: 4.3 MB (4278334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2b28e60579f3c762936b67ad00568481eafd1e332e21eeb26dbafda44e1d9bc`  
		Last Modified: Fri, 19 Jun 2026 02:19:29 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json
