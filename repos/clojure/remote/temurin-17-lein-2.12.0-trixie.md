## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:ddfe40aa1cfb45ccc5d8f895f0bd78ffec0a9174d4783b74757bf4b253461d43
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

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:85e576b6b9649326d448f20fc3f2637a87119993be21277eaeceb9b11f189d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218323601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af680b30644f09453bc5d00190e3d96705a3c9db32afa204fa64190cb26bed0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:58:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:58:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:58:29 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:58:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:58:43 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:58:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:58:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:58:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:58:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fd41af518160f5cbdf66e6776fbfbb4abbbb7c43e2fddb709adc96cf6757e9`  
		Last Modified: Tue, 19 May 2026 23:59:02 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a23c7a9b57898f2a7cc38e1e5dc0db60b53817f0f396659434e56860d484fb`  
		Last Modified: Tue, 19 May 2026 23:59:00 GMT  
		Size: 18.6 MB (18589382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02bfb9eafe7c1cee0c6b3792d6e7589f980b2e40abb0353a8053e4ddb0bf047`  
		Last Modified: Tue, 19 May 2026 23:58:59 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a7934b8c27adfd8900e32d1cb41f8111c0ab1fef7158738cc8075fdc2489bb`  
		Last Modified: Tue, 19 May 2026 23:58:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:17ef5ca64ac607416af1ec7f6422a3b3d1aa800e93730447597a421004a36364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08922faa53fc3eb7eefb19101c06c27af996ce5ec28a96fc307b1e5a477523f6`

```dockerfile
```

-	Layers:
	-	`sha256:c7724ea6dad72c0bf8b416f6df93d43d0891a0a8f33951c798cc090b01e97ba1`  
		Last Modified: Tue, 19 May 2026 23:58:59 GMT  
		Size: 3.8 MB (3816196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d0760d04c26415ff160442dd366a2c8c1207c8fd1a0b021e7e7070ca985efc`  
		Last Modified: Tue, 19 May 2026 23:58:58 GMT  
		Size: 18.5 KB (18506 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:88e947a65456510600337209c3e660f5b9cbde12a2968f07736e1fadb7ca7095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217462303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c802092ba38b53efaa0ce2f4f3525500b80986c5ab16acb0e1ddd7d2f64b9b63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:05:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:46 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:05:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:05:46 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:06:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:06:02 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:06:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:06:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e395b328abc548dc329445cae6167baced61558dc1d79fe7ecce3a6fb7bbeefd`  
		Last Modified: Wed, 20 May 2026 00:06:24 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56242aa1e1dd78d8e1b7716ab01a4c99d1742a6eefca2922b997188265e793f`  
		Last Modified: Wed, 20 May 2026 00:06:21 GMT  
		Size: 18.5 MB (18547577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2009aa993ebc055d1cd104bd1dfc039ef4b710d94610c80e77a6ba82872944`  
		Last Modified: Wed, 20 May 2026 00:06:20 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f71d25adc42adbd4c140f904b33616420cb887c661c9b2e739281ba87bffea`  
		Last Modified: Wed, 20 May 2026 00:06:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:44c56c042fe551f86faa98028a2ed66bc1c50e4fd946539774c9a61b79bf2d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e545e35540443f7d092a66b7225c114adda249c2f3b91d32cfe1793a1e46c89b`

```dockerfile
```

-	Layers:
	-	`sha256:ad8423c38900b288cb241929e6b0bc10fdff277f49461a5a370ce88923cb4632`  
		Last Modified: Wed, 20 May 2026 00:06:20 GMT  
		Size: 3.8 MB (3816436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a533f4bc4dd25cbfc142b5a2940c543e8641180a37ee0baa11e3414824f72d8b`  
		Last Modified: Wed, 20 May 2026 00:06:20 GMT  
		Size: 18.6 KB (18626 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:eb007a99fa16cf543f2b6e2e76c8b2ae7af165febadf2cfccb52e9e4cdbad65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (222048494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0be49fd2b43b372a97995e7b8fb2acd4be92571b9d7a18481d5b423dcfbe61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:31:40 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:31:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:31:41 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:32:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:32:15 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:32:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:32:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:32:19 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:32:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06742bfd6f3a4c91a065b055265b2edf944919541ee9c7934bc1931edc1dd4ae`  
		Last Modified: Sat, 09 May 2026 02:32:54 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d678bf984fd54c9f5d4de48ea9321c04a88ceb2f9c84b8706416ae168a5e44`  
		Last Modified: Sat, 09 May 2026 02:32:52 GMT  
		Size: 18.6 MB (18641045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a104dac3ca1f09c4d9de71de40ac179a91789049e18ea58bc013b6d66077446d`  
		Last Modified: Sat, 09 May 2026 02:32:51 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae364de34402c24b14a500c49662186544839039887f7e22f70ef407d7cc01f8`  
		Last Modified: Sat, 09 May 2026 02:32:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6416f671d2f585552637e02c6dc9dc4d8b97da9926c1798c6aabaf280d2e41c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e15d6f25b4a06b659e6d12b77e559a892021a1363edf83498ade2a81d70862`

```dockerfile
```

-	Layers:
	-	`sha256:58963bc5b96e7290fbab12f3393dccab9b267468ee652cd8ce726a1f0c278e94`  
		Last Modified: Sat, 09 May 2026 02:32:51 GMT  
		Size: 3.8 MB (3817154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2679c55c4a837f0b3ea1f96c1f8d66f898e0bd6ac31b1ef4a109acb21ad8e7`  
		Last Modified: Sat, 09 May 2026 02:32:51 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1eccb35be5f6d37a993d4d8d33d7ca01ec6ba176fa9648ffa7371e67ddc11e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208427566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61ebc92ba4cfda8de9cf970a53368641c741f1c392cba3d74a6ae3f2a3a87cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:15:32 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:15:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:15:32 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:15:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:15:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:15:44 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:15:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:15:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:15:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:15:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ed7aaeed1c65fcc4999767a473cf745af3bbd97738b57ccdb46296b8107390`  
		Last Modified: Fri, 08 May 2026 22:16:12 GMT  
		Size: 135.9 MB (135910435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b67b4d1bf1cdcc4bc074f91690af820aacd1d92be8ce95524baef3da385b7e0`  
		Last Modified: Fri, 08 May 2026 22:16:10 GMT  
		Size: 18.6 MB (18626657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a467150d645ee242bad7e982ffde2c6509bf34b1e899090ecb999caf97ecc8a3`  
		Last Modified: Fri, 08 May 2026 22:16:09 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259415ca3477d355c8d3de6e5e47a5db3cf938cd0c6e7b091a300e4839df1190`  
		Last Modified: Fri, 08 May 2026 22:16:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:43c15cff495057b96c6959848cb7f764e07799033a80aaf6c15fde4d6cb9ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894c6d85ad7798b211453c5db00b98e4f9809949242a87824d83d777aa739b80`

```dockerfile
```

-	Layers:
	-	`sha256:db47241f7cf47fbf591ba6f2896fa4fc819e204dcb45832d0faecc1dca46e1a7`  
		Last Modified: Fri, 08 May 2026 22:16:10 GMT  
		Size: 3.8 MB (3812581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6b191dee65a8c5133dfd9ad69673f7b4a7d2ee2f88953b8fff5e1f5618285c1`  
		Last Modified: Fri, 08 May 2026 22:16:09 GMT  
		Size: 18.5 KB (18506 bytes)  
		MIME: application/vnd.in-toto+json
