## `clojure:latest`

```console
$ docker pull clojure@sha256:4941c8581ddccfd204db7cdb0f524bbb330a17ca757b031d8915062e713e65ed
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
$ docker pull clojure@sha256:271c5e44edac4825c483d1ba1567438f18cb510a44698c4950ea9a7f2d7232d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240131382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6224521f9a4fc378dd9a78b36fab65e903b82249b338ac4f459edb0d9578f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:40:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:40:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:40:00 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:40:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:40:14 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:40:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:40:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:16 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:40:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:40:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:40:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:40:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610d8aff44cab4e61ab8ceb7ad4d381850653509b22bbe6011785d05659bf673`  
		Last Modified: Tue, 17 Feb 2026 21:40:52 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6d4f511222cbc7b07c02aa8911e8a155da9fe7e5643205be3128381430c3d4`  
		Last Modified: Tue, 17 Feb 2026 21:40:50 GMT  
		Size: 19.8 MB (19802891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da189dfb340a2aaecf2410dcd2eb8339c652a5c5f4bd98fc0702e392acd8423b`  
		Last Modified: Tue, 17 Feb 2026 21:40:49 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fcde875a0eddb305525e48577f7ba895b1d0303adbdc14f2b6ffb68adecaf9`  
		Last Modified: Tue, 17 Feb 2026 21:40:52 GMT  
		Size: 75.1 MB (75071933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ec3d52434e916b0e97f4324ef0db6c238635a2a178a251247d876c974a1167`  
		Last Modified: Tue, 17 Feb 2026 21:40:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ddbd57a000945fafdfb482255d7f585476afe2514aacdbd96502c4791118d2`  
		Last Modified: Tue, 17 Feb 2026 21:40:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:596460b5a44c411780aa9c3cd0e9cc5a9646a622b33add9013daf7a5894fccb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e31175a08737528f9ba94241dd31ca0b69b2975804ced048742848a81610d25`

```dockerfile
```

-	Layers:
	-	`sha256:f988ff7a0f1e403c7c6cfc049cab2de2e947e7209b5e5ca726214534849d00da`  
		Last Modified: Tue, 17 Feb 2026 21:40:49 GMT  
		Size: 7.4 MB (7437358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6ad4c0c5bdfb7ba8372ddf34c70d49716ebc2091d89cc59f8a80ddd34dbe09`  
		Last Modified: Tue, 17 Feb 2026 21:40:48 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:901266414e9cf36bf8bcb3c1fbbb29954177cae5eebbca8107998a022be25ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (239036797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b7c8f9bf07aa1155f8ecc862ab5d65cf646341783a2ca84748e1afacfcd357`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:39:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:39:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:39:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:39:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:39:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:39:42 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:39:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:39:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:39:57 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:39:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:39:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:39:58 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:40:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:40:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:40:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:40:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858542b8e2e517ea26bb4f6d87625c4fe88269edd99a370b458e90f658c69623`  
		Last Modified: Tue, 17 Feb 2026 21:40:36 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77610c1612c7a13f6b2021a83dd19b3fa10fd680018e55cbf15db51c3f81441`  
		Last Modified: Tue, 17 Feb 2026 21:40:34 GMT  
		Size: 19.6 MB (19632827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fae20d7f4070c01be4bb53a21022182845309dafa519af30b38ecdd69846d7`  
		Last Modified: Tue, 17 Feb 2026 21:40:33 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475db3e9f1d7e58767b7d6c539d8f7c36730f92acb01f53ea3a4546d519a813b`  
		Last Modified: Tue, 17 Feb 2026 21:40:36 GMT  
		Size: 75.2 MB (75230952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46abddd917b42914dc0e1a86f89918b6d996f6297be153e9bfb921f03570188c`  
		Last Modified: Tue, 17 Feb 2026 21:40:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5680e1fc0ef3568c622bb37b86369b7a1a46f898ee597ed2f2221d0947dbcc83`  
		Last Modified: Tue, 17 Feb 2026 21:40:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:3a597b093990894c730e517e2c4a3d131287c3204f87be8ddf5664b1b6366739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c945329a5b8cfd67d9da70ecc9707c5199c6b0fef959b09a71f634e011a766e`

```dockerfile
```

-	Layers:
	-	`sha256:fc76a23f4fd5632971cb230bd79f0fd40a2af57072a0dfe229a8a779d5006b44`  
		Last Modified: Tue, 17 Feb 2026 21:40:34 GMT  
		Size: 7.4 MB (7443094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc4d65d94b4ffb53f29c20d607c3e4dc6ebb14d424c0832ec4726c8955c2a8d2`  
		Last Modified: Tue, 17 Feb 2026 21:40:33 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:3c7c67bd36fdb88626466df25f9020cf97fc19efbb5e6f683696dc8aa9ac53b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249177563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fc393e75f7dbe7263478d838e6065522f9f5f726acb3accdb687bcd4f6b4e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:54:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:54:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:54:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:54:17 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:54:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:54:18 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:55:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:55:16 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:55:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:55:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:55:22 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:55:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:56:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:56:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:56:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:56:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413bd0b8c6c326da16c676c4dc2f9ba6260e745418e4f97b3a2d3fb7fa2bf0a6`  
		Last Modified: Thu, 05 Feb 2026 23:57:00 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ee63883eb7370fe869840f959c32e522f55502f68e9aa093f5bd69c7b5fe53`  
		Last Modified: Thu, 05 Feb 2026 23:56:57 GMT  
		Size: 20.0 MB (20023902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d63a17432a85a5c1fa33b95c3df6d9fce8bda1634781eb8e0632debe5c1748`  
		Last Modified: Thu, 05 Feb 2026 23:56:56 GMT  
		Size: 4.5 MB (4517772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54656baa8262f884518d48ed2479f0edc73c2e4283096cf1e4d96c511b62fe53`  
		Last Modified: Thu, 05 Feb 2026 23:57:00 GMT  
		Size: 80.7 MB (80674650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb4abe5fa41ac2bf53c86a4f9164f00f1329d47d74ea8c35e6c77b8f1e893f6`  
		Last Modified: Thu, 05 Feb 2026 23:56:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ed7325a693c07d8ba95d7363b30b662884509d75e908429b37d3e53a70448`  
		Last Modified: Thu, 05 Feb 2026 23:56:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:9e7fc87ee639b8604560be9e2245e4624a1a760d5c4fcdf51f0e9d1e805bfabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72857e983ed04aac77864a11144a1ef7e12156d2275ce8d94f6146c5e177cb4b`

```dockerfile
```

-	Layers:
	-	`sha256:6de541bc2d517381d22e5e098a4786c21911103059a53ca924dd728a474e6a6b`  
		Last Modified: Tue, 17 Feb 2026 23:26:30 GMT  
		Size: 7.4 MB (7425874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37427ce4cfe2599d751200b91251f1f106a568bb3db6d51a68b15b160560a8a1`  
		Last Modified: Tue, 17 Feb 2026 23:26:30 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:e1f53305099e182cea087db5e7c15828feaaf91a3d645e6c8b0182746f5fba42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233576807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a51f37020943bd2c5f8fc855f2f2df48c29f38b03b16919e0af6554254be93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:58:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:58:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:58:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:58:47 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:58:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:58:48 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:59:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:59:26 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:59:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:59:29 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:59:30 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:00:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:00:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:00:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:00:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:00:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ddd6b52413df94c5b77153988cb465952a04b04e872416aad5e899eb4746fd`  
		Last Modified: Tue, 17 Feb 2026 22:01:12 GMT  
		Size: 88.2 MB (88233833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab7babec2f2cedeaba6dcb87663c061dce9bdf5d0ec3bf51d7095a59abb99fa`  
		Last Modified: Tue, 17 Feb 2026 22:01:10 GMT  
		Size: 19.5 MB (19463318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c28b85339d5ffc4be0a5ef78da53348540cf6da307aa439840c1f4ef8164809`  
		Last Modified: Tue, 17 Feb 2026 22:01:10 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946fddf9d0ea75f962658a467c4fafb130358ae7a9baf2024492288dee3c18b1`  
		Last Modified: Tue, 17 Feb 2026 22:01:12 GMT  
		Size: 74.2 MB (74222490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f5bb11454c0f02c7f9ff48bee6cafe72bdd19abad38bfa63afc442c625aef5`  
		Last Modified: Tue, 17 Feb 2026 22:01:11 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01c1432ad256c235e5d7298f2f2b28810580412baea4ce7f84ad9378f89bff3`  
		Last Modified: Tue, 17 Feb 2026 22:01:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:e0359e16ec9ccd33c6a25aca871eb7c9af981c8bed496b794a55d36441f622e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052f05e7c00b8fbe020a741547f226715477430d6fea8e96fce0b68ec0353098`

```dockerfile
```

-	Layers:
	-	`sha256:b2d89af2023221be6ecae2386fd81c7fc9b8ca331ac08de69b275d057a2f414b`  
		Last Modified: Tue, 17 Feb 2026 22:01:10 GMT  
		Size: 7.4 MB (7413239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e9709c60146cee012cba3224eec9ce02c5aeb432474632cd92b08bb87dce76`  
		Last Modified: Tue, 17 Feb 2026 22:01:10 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
