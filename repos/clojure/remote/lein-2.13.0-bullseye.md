## `clojure:lein-2.13.0-bullseye`

```console
$ docker pull clojure@sha256:1a57d86500d1f8d496e01daf4cbdd0efc77ea02efd6cf3e09dc53c0e5e86aaba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.13.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3a54d488215b0350f1a62bb63adc5197ffcd818cf2382ab89b78cc83dcce166b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167791064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9820e1b32992ecb7e25fcb17e2ca034e84a91807a1ee2add645e93a3ca5ea71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:19:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:56 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:19:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:19:56 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:01 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:01 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730dbfec754f21b9d53d90eae0d5d71de648ee186a89cfb785e22fae830a12b2`  
		Last Modified: Fri, 19 Jun 2026 02:21:22 GMT  
		Size: 92.6 MB (92574570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637206cd3389fc0758b0c85d611cdc792f1939603cdb92bc7ef2d2ae90127b88`  
		Last Modified: Fri, 19 Jun 2026 02:21:20 GMT  
		Size: 16.9 MB (16929114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2eebf0ae29cd2cb5d8d1411cd5727f8a445fc3b32a02d2815c591382aba09d`  
		Last Modified: Fri, 19 Jun 2026 02:21:19 GMT  
		Size: 4.5 MB (4515182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307c2017f766dbe8b2458e478bfb06d6e1758d6b0a2edb828500e7b3388eab05`  
		Last Modified: Fri, 19 Jun 2026 02:21:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1f0b08bcb2f6a9f7c463487fc33804965b02d9cb8f8eebb3f127fbf3c9f568d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4489060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0878b631f508917bf8f7796964cc5a4232978efa649fb2f2049b409ca13adcb0`

```dockerfile
```

-	Layers:
	-	`sha256:50c0c34aa6d1f183e138e633a9b8e3e16e3dcd472b95f2e4b9e4c4ca49fea080`  
		Last Modified: Fri, 19 Jun 2026 02:21:19 GMT  
		Size: 4.5 MB (4470687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee4b28e8ed2e9eb85d37111564f0dd2494a35c82511dc82a56f4ad16aa3c389d`  
		Last Modified: Fri, 19 Jun 2026 02:21:19 GMT  
		Size: 18.4 KB (18373 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3eadcfd740e3a98b2518c79b5a34a12d5a5f1de9306b8d752e75ae45e44f362f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165239882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e3bcbe47ebd0480552b549daf85ebd7f7b112c2da36a8f74263e722659cfaf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:20:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:00 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:20:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:20:00 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:43 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:43 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffbc1e149ff8545053c116483fb51f8541168bc27096511b6766ebdc268a6dc`  
		Last Modified: Fri, 19 Jun 2026 02:22:04 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2a3dc3bafdf39ddb839c06f75c333f737f7399939f2b60a499176505271cf5`  
		Last Modified: Fri, 19 Jun 2026 02:22:02 GMT  
		Size: 16.9 MB (16917885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bfdc7b1a7d1dfa38a1927143447f43da1b4f6a06341c91dbf0a8095c5e0ab2`  
		Last Modified: Fri, 19 Jun 2026 02:22:02 GMT  
		Size: 4.5 MB (4515203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a433acb3ca0855b6248aa482942bfc0d98c7d5d47fc59c9ace10eb2761baf514`  
		Last Modified: Fri, 19 Jun 2026 02:22:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7d8ba460e7fea559f25f19f043681e278c397a6d2c86e68bfbe4433896f787cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a87ec1ec17fb9a08eab9c6aa83e6e03edf021b8903d6368a546367415615c7`

```dockerfile
```

-	Layers:
	-	`sha256:9e03a97dfd98aff183d07507e45f19223bcda32ee414bc0e8f6dfeaf861fccf3`  
		Last Modified: Fri, 19 Jun 2026 02:22:01 GMT  
		Size: 4.5 MB (4469682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85fccb398b620bd89bd0da8a11551c644b9b6afa4e620d15c080fc6c6f78e47`  
		Last Modified: Fri, 19 Jun 2026 02:22:01 GMT  
		Size: 18.5 KB (18518 bytes)  
		MIME: application/vnd.in-toto+json
