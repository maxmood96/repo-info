## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:0ae81e2f76a1866265e08792f74befab1407f1ed143968e48150559e304480b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e392bb018f0b8f2522d20f1097ec22fa46953cce099f23db31e5e691de45457b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233384198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e06b532f31965f2012aa56aef348cb8ded3a54723e695299dd118f37b7983e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:19:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:19:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:00 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:19:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:19:00 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:09 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:20:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:20:09 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:20:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:20:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc35a7a16fc49f4b1b793f3fd36f9ee0634c90da556a07083c3df2d74c81d27`  
		Last Modified: Wed, 24 Jun 2026 02:20:35 GMT  
		Size: 158.2 MB (158166915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ae1a4807939c419fd234c20b69dc0c4098676c5e605036af3152b493509a97`  
		Last Modified: Wed, 24 Jun 2026 02:20:31 GMT  
		Size: 16.9 MB (16928652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099cc04c18fef803d254dc265bffe66fa2212a476747ee1b316aed885cb8365e`  
		Last Modified: Wed, 24 Jun 2026 02:20:31 GMT  
		Size: 4.5 MB (4515194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa032fada7b342254063326e51c12b0c36d4cac90bb5437949a9a2013b0c775e`  
		Last Modified: Wed, 24 Jun 2026 02:20:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:04751719bd4ae61db0f50744392158ae3566bfd85244dd2e3cb7ce3739c2ea87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5c7b46c3a9f176559d79ef654956a3e517e90083984d82f5c4f44e8e913885`

```dockerfile
```

-	Layers:
	-	`sha256:138ca6a965c263ecb358243fd7e0fbb7bbb80e82c9cdc6851ecceba1bd6672df`  
		Last Modified: Wed, 24 Jun 2026 02:20:30 GMT  
		Size: 4.5 MB (4502879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b1d3f73c99d5eb59f1837d18ded3f6b077257ee9fc2ebfccbf083f3f116132`  
		Last Modified: Wed, 24 Jun 2026 02:20:30 GMT  
		Size: 17.7 KB (17738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b8b4a712fc9c34a08e3dc7c56c5b94d447f382253f6931c38b3e463ea53fc68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230151764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2682738eef44f82b70414151812b0e39803fe62089f3d7b81ac449076a564bc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:25:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:47 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:25:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:25:47 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:54 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:26:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:26:54 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:26:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:26:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1eef0811dfe32f17698e9de375d5d62959769e95c6c5d929faeca181ba369`  
		Last Modified: Wed, 24 Jun 2026 02:27:19 GMT  
		Size: 156.5 MB (156461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d8acd75a2982f17bce7ee1b12180aecc1542af28749b10ba07339d85bd2584`  
		Last Modified: Wed, 24 Jun 2026 02:27:16 GMT  
		Size: 16.9 MB (16917648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ab589b46c9d013c12accdfedcf0afd994c212a3ed19a454002b8251e6dfa86`  
		Last Modified: Wed, 24 Jun 2026 02:27:15 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ad4c7e64d740f31f546686ea9e47132a733520a51ddc35ff8c495aa4573bb5`  
		Last Modified: Wed, 24 Jun 2026 02:27:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e28dac39a7f4df072cce9bb84fc943356846f7aa2a7122d93bfc576b5ee9f83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4519712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14d05f0c3dbb78fc8a082829eb28439b963c3eb32e6da3012cbdc007575f4e0`

```dockerfile
```

-	Layers:
	-	`sha256:49ceca6a78a14420561cc10eb0a70b464eae4c0fcc8f3bc60a28237dcde9c2a7`  
		Last Modified: Wed, 24 Jun 2026 02:27:15 GMT  
		Size: 4.5 MB (4501853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70f64f7407f5991782c143a4ae58a3e593442d1fdddbe9b38148d8d5c1708bf5`  
		Last Modified: Wed, 24 Jun 2026 02:27:15 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.in-toto+json
