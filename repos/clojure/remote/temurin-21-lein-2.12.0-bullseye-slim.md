## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:b9b5a58a34cd68e478572e13ba5e47ba946a00f67309b512c62cfd3171449457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d6019ba5148c670471973ebda535084b005c778ada18c5ee8fbcbd4429365f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207952232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa93b26123bf8586994381efc79f2bc3b6bb218a5539a53514e91335d47353a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:05:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:39 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:05:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:05:40 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:54 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:05:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:05:54 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:05:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:05:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6ba67a415326128cedd47380f69c607b6bdfeab674b978bf7ce68a61b7e9e0`  
		Last Modified: Thu, 05 Feb 2026 23:06:15 GMT  
		Size: 157.9 MB (157857083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f20745b005634324f0142ec56f6b3ff3ee84c40324a9b29308368efe0e212c`  
		Last Modified: Thu, 05 Feb 2026 23:06:12 GMT  
		Size: 15.3 MB (15318725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80645274cc9a0b7a07ee17db17cc20e296d58883f87835e10be5f0b8313b4c3c`  
		Last Modified: Thu, 05 Feb 2026 23:06:12 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcab3ba1fe737c1bcf1d0e6343d1f62cfa5d4add7c71365c1547f4a23253a72a`  
		Last Modified: Thu, 05 Feb 2026 23:06:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b8025fab2c5c532f1787da750ea93677d39f79725175e06526f7a2ca50aa0046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4a76d5d425e80ab11bd9e3071df40ae9ef42178cbfa7e88c7ec41044d23d52`

```dockerfile
```

-	Layers:
	-	`sha256:cc9c43909040fbd395f8fe45f2794db5c3d385969f01bdbd733f378e2dd9a034`  
		Last Modified: Thu, 05 Feb 2026 23:06:12 GMT  
		Size: 3.0 MB (3021014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1bd99858dcab4964f667c6db96f3cf18037f96af13d4fc004dd803c1688e5c`  
		Last Modified: Thu, 05 Feb 2026 23:06:12 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d02c71f60368cfb1f59e8cd17f445cdbf9a32dae578f13037b3128cf3c05f129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204701436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3363a21561776a9212c11f33a4788c45f579c5b8aa19952092dbd06bf969e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:06:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:36 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:06:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:06:36 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:06:50 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:06:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:06:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d501a9118cf0a0b21e56a6bfd60d1887236f37678af5b975abce2f412da3808a`  
		Last Modified: Thu, 05 Feb 2026 23:07:12 GMT  
		Size: 156.1 MB (156133061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d949439520b579f6eb3739b04308dc2deb9dc9421f8f988992c147178da719`  
		Last Modified: Thu, 05 Feb 2026 23:07:09 GMT  
		Size: 15.3 MB (15305801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a131ffafa3b5047b8c5594813cefea08e5794f31b265980d0424944f1c780d`  
		Last Modified: Thu, 05 Feb 2026 23:07:09 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53caab6355011ed87f8e8b827511b40e63513e05ed4ad1bee80e17c208071fc7`  
		Last Modified: Thu, 05 Feb 2026 23:07:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2429c52e8ac8a8e71b9f810cc70ab7c5c3229628a3b5392a875c893351ae2e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177e5077a1f63a20e9e99f65997387a4ffcfd0a5b10a1e05a8d87a8172e52621`

```dockerfile
```

-	Layers:
	-	`sha256:6f86f745b2758e84e7bf757d0a540cb688d3c4c7e2f94d839028de21ce372b7e`  
		Last Modified: Thu, 05 Feb 2026 23:07:09 GMT  
		Size: 3.0 MB (3020623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c2c8c202c24913e744041f782c80513ebc4f528b270fb4266720b0c79cdd3e`  
		Last Modified: Thu, 05 Feb 2026 23:07:09 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
