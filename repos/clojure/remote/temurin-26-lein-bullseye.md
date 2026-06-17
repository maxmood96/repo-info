## `clojure:temurin-26-lein-bullseye`

```console
$ docker pull clojure@sha256:032a55b348fa101df2e0a73b07f8c15665c467091aba8dbfd9fe80f564e0e72e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:de6ade6ba23e1c350523fc93ff9946b923ca02d6674bd2f626061827f48ce527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169740964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a56c48091fd98ba6bb483ea75e78ca288d5ea722920d055841bf7c74c81594e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:38:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:23 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:23 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:33 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:33 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1e637039746bb5db493612ae97efaf39db1cff094e778e3bd80b4e13cc5cb`  
		Last Modified: Tue, 16 Jun 2026 23:39:54 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245b40b0e5cc68018a35bc83dc4ceebfba4de560be2fc492154f6d71bc60655d`  
		Last Modified: Tue, 16 Jun 2026 23:39:52 GMT  
		Size: 16.9 MB (16929244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118efc9272295d886f4bca015c7c8b5b05800c6733092fdde64e10c05f0a8570`  
		Last Modified: Tue, 16 Jun 2026 23:39:52 GMT  
		Size: 4.5 MB (4515177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebec1bae3de07e44c3a57e61d01a4f2ff640c21dd245a6e8070ea294a54f097e`  
		Last Modified: Tue, 16 Jun 2026 23:39:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0921c7797df7b1e7e4a4dda6b6a6b6905b4870ffebc75e556d33963990160ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4485273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68262c6262f63822a75744b0e32e00f76f5d5a708c7a447c0c12fc86f22cdcf2`

```dockerfile
```

-	Layers:
	-	`sha256:36971303c8750c261867ff90ee58c7e927148f548b40e6336b9dac7efccbae8e`  
		Last Modified: Tue, 16 Jun 2026 23:39:52 GMT  
		Size: 4.5 MB (4467542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249a386a4481b3c766ab61e61f1567b8cd64cd3d863e0846605193ea29bf9e0e`  
		Last Modified: Tue, 16 Jun 2026 23:39:52 GMT  
		Size: 17.7 KB (17731 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bee03bbe47af9f01ab0044598420aed87d515d8d5deb43373d849ff6aa19c71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167201979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e411867b31c6c1510ea6ce59a2f8e7f6fbc374c880cba56809cee771af8a8ab8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:38:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:20 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:21 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:31 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:31 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdcc481a3f6d1a036affc4c963e8ebf207e452eb166a9369d8cc0bd2ba48a67`  
		Last Modified: Tue, 16 Jun 2026 23:39:52 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c425a4e19a663b5fb61d6b6a823abbad0159f290bc3a388cb5b63d0930492722`  
		Last Modified: Tue, 16 Jun 2026 23:39:50 GMT  
		Size: 16.9 MB (16917926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1909fae45c30b72374862c939c9355a566340f397b0bc32b1e2299f71455a4`  
		Last Modified: Tue, 16 Jun 2026 23:39:49 GMT  
		Size: 4.5 MB (4515175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1324cbed6958045d2e7ae701d7812388bfe98c47367af4c3193575e8eeebe1d`  
		Last Modified: Tue, 16 Jun 2026 23:39:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3a0f91e7b01c72facf351f80ee15be3511b13ee683c410231f9b08e2eaeb5ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4484365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30be6262ee6d8f4e9869a91aa1ff1bf1c5367fcb63cf4e6defa2242a296a997d`

```dockerfile
```

-	Layers:
	-	`sha256:5cb317a614e3b01d70bb1ebd3d35a81a47796dcaada8388ab6d013b73e0adb2e`  
		Last Modified: Tue, 16 Jun 2026 23:39:49 GMT  
		Size: 4.5 MB (4466513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11540e1163d972989126aa67b5879d47ec205895ae9877d66b1c3ff28153de22`  
		Last Modified: Tue, 16 Jun 2026 23:39:49 GMT  
		Size: 17.9 KB (17852 bytes)  
		MIME: application/vnd.in-toto+json
