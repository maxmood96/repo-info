## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:c0c4b193472ecd2c73dba885a865581f54b123cc7feabeea71159e93f091d326
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:47c8a49e258bf16b7d68a37a077240d0108a6b5618b99b06f63d06bc3886aaea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221102172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd773b1fb903786cd4c91f8a392be848156fa284f0ec500fcf815d55d0c2d8d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:33:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:33:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:33:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:33:04 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:33:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:33:04 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:16 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:16 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158cc4fe0244d95723aefee1700292a1d7a3fcf74a1c4f9f77f2b07c9419f777`  
		Last Modified: Tue, 16 Jun 2026 23:34:31 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e203ee3bc706844c5b2debc99f0595a40111ab894d3d7cfa0ce2f3b7bcfc5`  
		Last Modified: Tue, 16 Jun 2026 23:34:35 GMT  
		Size: 16.9 MB (16928894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11759bc3f66f5d12525031d55b3d8ea89da96d0f91d2223b76f9555c93c93438`  
		Last Modified: Tue, 16 Jun 2026 23:34:35 GMT  
		Size: 4.5 MB (4515214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3285498498040cb085fd66f4f9d7626dabf146d25623e9b4cc9ba548beeb6626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4537915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494a3c505458413bdef715f4c0cefa483a9924f7c3fefabeb2a364b0b0199eb0`

```dockerfile
```

-	Layers:
	-	`sha256:52c38b085efbf4285de17b00fdbb352ad4325cb1b0787ab97dc4479f8bc11801`  
		Last Modified: Tue, 16 Jun 2026 23:34:35 GMT  
		Size: 4.5 MB (4522167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:539a84f791fe005524a20a0c2122d4e20967d9886f25f9462257ee01b55ec6bf`  
		Last Modified: Tue, 16 Jun 2026 23:34:34 GMT  
		Size: 15.7 KB (15748 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:28721492f148f290dc76f5e049e9476ea81f433f32cf06ed67fc464ffe8d4111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216279310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce40db3d17d450712f0c0563450c5f7addc2803f64ccdc16042559afdc84fe4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:32:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:47 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:47 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:33:57 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:33:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:33:57 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:33:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:33:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f7fb0a457d1c036a1bbbec2bc2ad8aba2ad63da8f37922d777c16a460ef4`  
		Last Modified: Tue, 16 Jun 2026 23:34:19 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02df084c1d4a1a54b586a5e7bbcb2dd465e803cf0c8eab5d69472badee40220b`  
		Last Modified: Tue, 16 Jun 2026 23:34:16 GMT  
		Size: 16.9 MB (16917759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a43ef6453400df89bfe39762e0891e5871741910d34e8e9f30369fa566ad76b`  
		Last Modified: Tue, 16 Jun 2026 23:34:16 GMT  
		Size: 4.5 MB (4515177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:eafb357ecfcbc356fe8d75904fd5012c1162626269bdc5cebcb721ef66605158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4537628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0d5b938cef6b241bbfc5ec80065f3cb9e6129ba5b99c7c902165b609b44e48`

```dockerfile
```

-	Layers:
	-	`sha256:e315b5835c66ed2c524066f23bbadac839b92771c8f405341909c92947588a47`  
		Last Modified: Tue, 16 Jun 2026 23:34:16 GMT  
		Size: 4.5 MB (4521759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019988a27d76ee2d59173d9336a4c5667ebb3117a26eb10f312c4d623b1cf224`  
		Last Modified: Tue, 16 Jun 2026 23:34:15 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json
