## `clojure:temurin-25-lein-bullseye`

```console
$ docker pull clojure@sha256:6643be3637ce3a1428bd0537224c8be96b2aca65b38cd8dfaff4fd5435f634f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:93c3519c6afd1aa0a002fa626de26d4dd7c7d251dfb2b93b2b8da73b053e7b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167790945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1501b5c63c0ff2edcd4ee30283b33470f08c734da0817c83f3bba37d5c5b4fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:37:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:37:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:37:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:37:15 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:15 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:24 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:24 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628e4433fb4d3c64804f65823bbac9aa638443ef7cfdd7521dc6bb0d984e25e7`  
		Last Modified: Tue, 16 Jun 2026 23:38:45 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe44aaef61215042176cb9ae7b65c49692f2f51ad067c3b04c4c32583030b96`  
		Last Modified: Tue, 16 Jun 2026 23:38:43 GMT  
		Size: 16.9 MB (16928953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b66cbd8de465f679a4b876574bf1b9bcf8cc838194d438d28d89ca5c786393`  
		Last Modified: Tue, 16 Jun 2026 23:38:43 GMT  
		Size: 4.5 MB (4515207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6735542513234014da91cc199773d31abe229d534971323ac3480596f70378`  
		Last Modified: Tue, 16 Jun 2026 23:38:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fb7f5e7411dcea686b655c55f065b9beec7b470a2332d4bf4a2fc131e4b96749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4489060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3936632559bd4fe843638b00492d5354baa3767d45abe6fa8e5bbfc40370a9`

```dockerfile
```

-	Layers:
	-	`sha256:62a827ba6b5ae54fede4bc4e392247e1a17a7b474c1066286102ef759570e486`  
		Last Modified: Tue, 16 Jun 2026 23:38:43 GMT  
		Size: 4.5 MB (4470687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad81bdb8cd9360d3fcd4d9267e92788b7249f59b7abb6d544f0826719ff3e7da`  
		Last Modified: Tue, 16 Jun 2026 23:38:42 GMT  
		Size: 18.4 KB (18373 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc51773ba7ea3215cbd44f3965cca1f43cffcd5fd4a4fe68ac38ed087b53b363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165239825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e003d07224979beff724bcc115a0af9343f529db471ae63db0bb6d71be2d1ebb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:36:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:53 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:53 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:02 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:02 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366947bc85ba2bc0c491940764363726a26c175323849c8baa2eed6d237b2495`  
		Last Modified: Tue, 16 Jun 2026 23:38:19 GMT  
		Size: 91.5 MB (91542296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe100fc00cc7335d0758dddb53938d791ada4e9fda81375595d627b5e10f77a`  
		Last Modified: Tue, 16 Jun 2026 23:38:21 GMT  
		Size: 16.9 MB (16917786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa6d2fd5410d6e0b660b126e2945808e9890dac59afe10df71d7f4043591a8d`  
		Last Modified: Tue, 16 Jun 2026 23:38:21 GMT  
		Size: 4.5 MB (4515199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f978eda652a6caf7c9e14c61cf55623e39d3187a0b862715ec617446f7cd465c`  
		Last Modified: Tue, 16 Jun 2026 23:38:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:59a42b83bb18e26ba5ebf2754e0fb0c23e879c20dc2b4fa42795e9eaa0715fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eff8ebc3c955920177ab2fa4f11cf32136759aded695713eb6fc9c02f78873`

```dockerfile
```

-	Layers:
	-	`sha256:2eb508f0e1f122a5718a931c268230e162b0ba49e44e690e0b03656b79a92e38`  
		Last Modified: Tue, 16 Jun 2026 23:38:21 GMT  
		Size: 4.5 MB (4469682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a5482dfa39277324d2251b7e6986cf4b551757d9461ad115b1dc823fcabf483`  
		Last Modified: Tue, 16 Jun 2026 23:38:21 GMT  
		Size: 18.5 KB (18518 bytes)  
		MIME: application/vnd.in-toto+json
