## `clojure:latest`

```console
$ docker pull clojure@sha256:1643bb11dff9344d700e26a7e0e8bb261ec585097934e8903042680872c69821
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:79f7adef31765efdf3bd4fe41229fed895e9d8b0e83198110fc21aeb30748586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239920711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eefcec1a3e37726554cd10ef7881b30f424bb71e28a7aa728f48f9d6e5ad1f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:01:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:01:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:01:52 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 28 Jan 2026 18:01:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 28 Jan 2026 18:01:52 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 28 Jan 2026 18:02:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 28 Jan 2026 18:02:07 GMT
ENV LEIN_ROOT=1
# Wed, 28 Jan 2026 18:02:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 28 Jan 2026 18:02:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:09 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:02:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:02:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaece5621d93a4ef03aa4086ee4568b87f308af699814687542232ed006fdca`  
		Last Modified: Wed, 28 Jan 2026 18:02:47 GMT  
		Size: 92.0 MB (92045322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e997ec266d11ab2fae45f43a5b3db781a2c72407cb0d766d2c845b955912465a`  
		Last Modified: Wed, 28 Jan 2026 18:02:44 GMT  
		Size: 19.8 MB (19802887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030bbea3fcdf6e88b48c917cca7ad0944e34ed211bb12aa13b26b072a2917182`  
		Last Modified: Wed, 28 Jan 2026 18:02:44 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b677713bea1f7ce4fd718ceb59bfd2ab610e33f8b9b83f06995636630f6b2621`  
		Last Modified: Wed, 28 Jan 2026 18:02:47 GMT  
		Size: 75.1 MB (75072046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385234f43440898d09ab8fd3d4d83618abea07a8b0033f4e89a01473ca9b0005`  
		Last Modified: Wed, 28 Jan 2026 18:02:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da64b9cf09c8d4c735504671a5a567e688e4ce8f1531c3abc739c3d36cda87a`  
		Last Modified: Wed, 28 Jan 2026 18:02:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:1ce65e22de36cf8b1722aea8c4531539acd8c7b85755cb97bc2595896a9f6083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccefeb9ce1163b33ae70c7e3baaa4d70ac01d7e129aa6c783e24bd359fae1673`

```dockerfile
```

-	Layers:
	-	`sha256:a48ecac58b5ea811f5f6ad6ece5716e7469530849cd550aff04e1b6bee2c08b7`  
		Last Modified: Wed, 28 Jan 2026 18:02:44 GMT  
		Size: 7.4 MB (7419370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81df89f46a33b3d5885989c6c4e972e9ee7c472e549ed4ddf2d58bc193b101ec`  
		Last Modified: Wed, 28 Jan 2026 18:02:43 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fffec171b5a4350c3d8ff5d915d46d89c5adf821a6998a74dc17b51a779a485a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238801229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64691baba9eb8de783396b466f3770b7bdc176371aa1f2dd723c464e4237619e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:01:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:01:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:01:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:01:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 28 Jan 2026 18:01:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 28 Jan 2026 18:01:39 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:01:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 28 Jan 2026 18:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 28 Jan 2026 18:01:53 GMT
ENV LEIN_ROOT=1
# Wed, 28 Jan 2026 18:01:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 28 Jan 2026 18:01:55 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:01:55 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:02:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:02:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e42c8001f1ba3226978f561841eedeaa61add98483e6352af937fbffc2aa58d`  
		Last Modified: Wed, 28 Jan 2026 18:02:32 GMT  
		Size: 91.1 MB (91052502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ddc6bab65ab78993da982534fe50ab4aa62c49890bfacf817cca5e95ea0153`  
		Last Modified: Wed, 28 Jan 2026 18:02:29 GMT  
		Size: 19.6 MB (19632811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab7f57679c9dc04ba98b0de7e7af85196dd07cfea989ec47992d5df5e9087f3`  
		Last Modified: Wed, 28 Jan 2026 18:02:28 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1be6c3d908f9a2164d04b24935476c79501afe35a0ab3241bb896864910a7f`  
		Last Modified: Wed, 28 Jan 2026 18:02:32 GMT  
		Size: 75.2 MB (75231038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9716f90d35ea495ba3ee6c3a45d4dd2a8754a4074c5cf7109d69ed4375634d31`  
		Last Modified: Wed, 28 Jan 2026 18:02:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7caaa1f03b6712babe6d78b9e485df5ab7b4bfbd746f0d3c7e26cc16c7166992`  
		Last Modified: Wed, 28 Jan 2026 18:02:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:294c74138cea16e94b563ede26fb901633bc99170e948872edb4bb82c57b5499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a66de461aa5bf081ae0fe4bdc539d562128c6de14a53e474e09b921ffed50`

```dockerfile
```

-	Layers:
	-	`sha256:b438559c7544f76113c351aa3b69ecd1d327eb65598c1e09efe7e25a63018fb7`  
		Last Modified: Wed, 28 Jan 2026 18:02:29 GMT  
		Size: 7.4 MB (7425106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd8a20b49958899c3cb7d04f817079ec9c4577399cf35e6c9e3abe1960bb8b7`  
		Last Modified: Wed, 28 Jan 2026 18:02:28 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:a26f9f8669673b19c22b601d1902a2e71dd8e6dc5872ac76b251d0f8a5aa1223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249155220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5c7caa22a5b31c7fef8adfec8a86540c645e366f4588fe324f434e6d985a93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:00:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:00:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:00:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:00:33 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 28 Jan 2026 18:00:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 28 Jan 2026 18:00:33 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:01:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 28 Jan 2026 18:01:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 28 Jan 2026 18:01:12 GMT
ENV LEIN_ROOT=1
# Wed, 28 Jan 2026 18:01:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 28 Jan 2026 18:01:17 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:01:17 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:01:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:01:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:01:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:01:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:01:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339fa589af2d7cc446e03d21ea40f1e5c774818b048bcf7c10ea2c7201d72d8d`  
		Last Modified: Wed, 28 Jan 2026 18:02:31 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311370dc73b996241b6d13f3927d320b4fe059c36075b1989f71f8caa5bc1370`  
		Last Modified: Wed, 28 Jan 2026 18:02:29 GMT  
		Size: 20.0 MB (20023781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88f868498dcc0448448f07fb6d9e40f59ca8c9d69269434739df009471683f1`  
		Last Modified: Wed, 28 Jan 2026 18:02:27 GMT  
		Size: 4.5 MB (4517778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cab25a748982f6a7d39984cb989b99756a49b70501b530d776639a46d21ac3`  
		Last Modified: Wed, 28 Jan 2026 18:02:31 GMT  
		Size: 80.7 MB (80674421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949cc50b17e8ea371cbb34478f0c02cd931bebb0f8626035c195c96849c05c42`  
		Last Modified: Wed, 28 Jan 2026 18:02:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506082c91ff4813c1b8079385784f3f742308f40c2f4dc73d4088e2932369a63`  
		Last Modified: Wed, 28 Jan 2026 18:02:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:966e412e7c80eeeabe5651772d4f0b5dd857ec80ae4bb662c8d54fca186dfc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c4185e820dfb3eb7ec31458baabb1c5af7e8985ad71f83169eebaeb98b6f09`

```dockerfile
```

-	Layers:
	-	`sha256:c0b8fb5bc60d38e576ce0597d9edb1bd4f5c81bd906d0a2af41feff357ba6ea6`  
		Last Modified: Wed, 28 Jan 2026 18:02:28 GMT  
		Size: 7.4 MB (7425872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42eea46a19f45ed6e26ec27d2433df4f0b00526bd8aac3c72406ce4ba46597e4`  
		Last Modified: Wed, 28 Jan 2026 18:02:27 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:5ac225c0ab4d2b43c1ab2f3ca3fecbee063dcb3e777fda3d0472d3476710a6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233552990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14ac1caa57d5b1dab0a4f24c2b1c3f663f2c69509bf769ddf5fd6ac9df447a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:23:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:23:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:23:06 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:00:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 28 Jan 2026 18:00:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 28 Jan 2026 18:00:07 GMT
ENV LEIN_ROOT=1
# Wed, 28 Jan 2026 18:00:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 28 Jan 2026 18:00:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:00:10 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:00:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:00:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:00:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:00:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:00:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d228a424ac43e5b633b49f78829dd5efa41560a237d73954164bfe619c713508`  
		Last Modified: Thu, 15 Jan 2026 23:23:50 GMT  
		Size: 88.2 MB (88210666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2998da82c2de22b3683aeb324ac670243a0b019d0846a317a54e4cc51b4fcbb`  
		Last Modified: Wed, 28 Jan 2026 18:00:53 GMT  
		Size: 19.5 MB (19463220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff4f9092834c59ba0377074c5a48642c7271127697c61342c670440dcf54ba5`  
		Last Modified: Wed, 28 Jan 2026 18:00:53 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ce821b1192cbfa41e86312d2d2dbf79ac20a35d35b05eb6b65ac9cb56ddb14`  
		Last Modified: Wed, 28 Jan 2026 18:00:55 GMT  
		Size: 74.2 MB (74221872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94633a891144b6726c3aa93e6226013950de91ffe92aee48925503af05d2b33a`  
		Last Modified: Wed, 28 Jan 2026 18:00:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3ba4bbbabcea2582e3c291f5120348dc9a0f14560a006cb485ba6037f9b1f`  
		Last Modified: Wed, 28 Jan 2026 18:00:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:51179240a6946320a290f56e8d7411aceaaee2c9dcc32e4e3e84477980c22ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c806ea71397dc87c0e27672f355da0fb989354c0bffd880a65a392b669b42a6d`

```dockerfile
```

-	Layers:
	-	`sha256:e94aa1e19e032c5e01a6b9704853f5e31a51527bc93ba6db7b2f2586e331be72`  
		Last Modified: Wed, 28 Jan 2026 18:00:51 GMT  
		Size: 7.4 MB (7413237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc8b6f35bbd64e0b59ceb1ff5bc0146d96f58d65b31ed33219db1d39a3767cb`  
		Last Modified: Wed, 28 Jan 2026 18:00:51 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
