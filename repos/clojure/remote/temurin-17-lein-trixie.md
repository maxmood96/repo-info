## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:3c1dfde436d6656a5a6660fdc7ca3084f53f88e8f6738bdbe18f33a2f99bc311
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

### `clojure:temurin-17-lein-trixie` - linux; amd64

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

### `clojure:temurin-17-lein-trixie` - unknown; unknown

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

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-17-lein-trixie` - unknown; unknown

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

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:519be0557a434e1269304d25b5d8645ed5ae2169f4e2654f188c583b0ada8c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222061256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55552af8e8fa0d4a2ae9bb391fbe809d99f72fd5c23559dac19ad1890031ee51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:55:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:55:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:55:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:55:54 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:55:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:55:54 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:56:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:56:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:56:31 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:56:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:56:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:56:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:56:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27b520fdf7e3554efa0af356645dd5dc149e4ce0f85e4af1780a538faa30f86`  
		Last Modified: Wed, 20 May 2026 05:57:20 GMT  
		Size: 145.8 MB (145766112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5662abbf61819ff1be60e82673cc86785c4d72c0a14ad754f049afe15bb39830`  
		Last Modified: Wed, 20 May 2026 05:57:16 GMT  
		Size: 18.6 MB (18644814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e3726c47e17c79162263d0fa5f41b7bb4bfc6a1efaef9b0bfc93e1f57c5240`  
		Last Modified: Wed, 20 May 2026 05:57:15 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2171b6653b0ade1490048de49fe379ce6424531004d630ac5373dff33c8af40`  
		Last Modified: Wed, 20 May 2026 05:57:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9e66122ab3168c1fbcba128747335b25eabd2acf572a778d2fd54f1bbecdda37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67a8dc532a482288699828bbc1a0481e1407b446dd120e54f423d01c00134fe`

```dockerfile
```

-	Layers:
	-	`sha256:1a46e0354f58a2e14adc11a2d214f4e76d9d00df573fcb911f0ecd373b434acc`  
		Last Modified: Wed, 20 May 2026 05:57:15 GMT  
		Size: 3.8 MB (3817196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c8e86789922275921652ffd497442bafbdd0066c2e2b79f5402f5d859ef69e`  
		Last Modified: Wed, 20 May 2026 05:57:14 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:31996f7eb5f21fd8e00b5c5bf460fffb8ea16762ca48928b0386c81fa5e7bd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208438992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172e0097778189f7f0ed0b8917c4d247e7ae14df490537808dcdf00af35759e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:43:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:43:42 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:43:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:43:42 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:43:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:43:57 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:43:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:43:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:43:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:43:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e6aeaf690365e231d191405438cab335606f7f662847488b61ec9fe50ce0af`  
		Last Modified: Wed, 20 May 2026 01:44:23 GMT  
		Size: 135.9 MB (135910432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0e53c4fdf7635878ddaccaf1c7353264f04e9e47fe100545719918b3cf89b0`  
		Last Modified: Wed, 20 May 2026 01:44:21 GMT  
		Size: 18.6 MB (18630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d824e1a7f28d598fc01e18a9dfbb45c97b795230db12a140b2d2db13760506ed`  
		Last Modified: Wed, 20 May 2026 01:44:21 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e9d5e82e6e5c036f7f8031b40951fb281e8770bcd992f33207fe8679c2c151`  
		Last Modified: Wed, 20 May 2026 01:44:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:23e0b729d07b45a73a45eca465dbb1f7732ee1be1d48643ae40a1df8d6d7c5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f43e30485090c30d51808068d2bedfddbdd96322afa3fc8e24830820e88d4c9`

```dockerfile
```

-	Layers:
	-	`sha256:96cf3c1fb79ea5f3914a70cbbb389a557f608193752f58b5520bb63a666f6e6a`  
		Last Modified: Wed, 20 May 2026 01:44:21 GMT  
		Size: 3.8 MB (3812623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db3347b51031b95b497cc021c2869bdbcb618eeabdae47c9bb7504f4ea02b5c3`  
		Last Modified: Wed, 20 May 2026 01:44:21 GMT  
		Size: 18.5 KB (18504 bytes)  
		MIME: application/vnd.in-toto+json
