## `clojure:temurin-26-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:306bb875449e91eb508a2da7b93250ca35dc64bbfd75dc4f32cc0335b58b740e
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

### `clojure:temurin-26-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7eabe4d22de8d089b2c8e1eef8298e3c28119743f1e148f12c8a0e3682bf6ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144969686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfa94a9e46aa2e4db3086695649e5462f7057c927d910b8d1f37240f01a732a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:21:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:27 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:27 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:40 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47833512b9e23c9c2dfe8bcdaa25d638496220f7ef8bb021f0cb4964ee3e2a7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:00 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f4a7a994ccb79f2be5d48817d3b56b466cde921fc25d0ed08b8a2f585a389`  
		Last Modified: Wed, 22 Apr 2026 02:22:00 GMT  
		Size: 17.8 MB (17759570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c07948be4a6e571424237623f07a3d55c3f7be3ba761f25d5c8b624a5b4a4d3`  
		Last Modified: Wed, 22 Apr 2026 02:21:57 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc77618d7012f579570e7a56ca5e7b59493bd57f1d9075b959b215b65544cbe`  
		Last Modified: Wed, 22 Apr 2026 02:21:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e58585c65b1abe7599df24aa25c9e4e40410cfc1af00481abb8f572732e10509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec74332a63e32dd1432f6f80c635b48121eba362dba7645198ed72894b493ca`

```dockerfile
```

-	Layers:
	-	`sha256:d6cd0e2ebc7d41995d5b7c615b58569b6c5c4ae15754a1728d0cad31525bbb01`  
		Last Modified: Wed, 22 Apr 2026 02:21:57 GMT  
		Size: 2.7 MB (2695554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d10271cf44e073fc0eedc9ca67e57161b230b6179bf7d50a01ec3f30aa1008`  
		Last Modified: Wed, 22 Apr 2026 02:21:56 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89d63d8e04259e2cbe8e358401df335ed9cc3a2f16c4ce62461c9c8de5ff6d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143622515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18874c4172e088e1a5188e90fc94e7b4677e7cea3e74604b172b6f100f6cf753`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:24:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:24:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:24:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:24:21 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:24:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:24:22 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:24:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:24:35 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:24:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:24:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d60a3acb34a95760fe0accc757f7e75b70257d0264cb0e2ef0b8973574c240`  
		Last Modified: Wed, 22 Apr 2026 02:25:01 GMT  
		Size: 93.4 MB (93395205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3eaea9f589499698e3d593fbaf666938fdcfef7543c8e4cc33755254022da`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 17.6 MB (17593038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32237eb58eb4b027a572e85e9a414ab311e4ff7e1897a7da71edc671ff41cb3d`  
		Last Modified: Wed, 22 Apr 2026 02:24:54 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ab178e8a2bf3f0ccb825ff4cced384c9e1ced7ad0d34476b084f3811958f81`  
		Last Modified: Wed, 22 Apr 2026 02:24:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6632d2cf41bec37dc954cb94577c929b80ed052d8abb18d82ed3711629d08ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071556bdb046850198150c063a6f5144b5385f31e364c082c29021f28975aaa6`

```dockerfile
```

-	Layers:
	-	`sha256:4961fb12c00cb740ca0bdd546ad09b5c9778d9e36a163ffa7e8dbccd94bf9f36`  
		Last Modified: Wed, 22 Apr 2026 02:24:53 GMT  
		Size: 2.7 MB (2695166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e134bf2e518f99f0014cc8efbf1f06ecbac6d254e56c46376e3eae0d7c47cf3d`  
		Last Modified: Wed, 22 Apr 2026 02:24:53 GMT  
		Size: 18.5 KB (18517 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6c17efc445bfbe0ef77a0e9c6ef84ad74fddcc2c23778b076559bf3e7853651c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148339476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73008806e5b6213b53d214b7c27633ca6d9adaa43a6108e84f94e2f26b6b8286`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Fri, 10 Apr 2026 00:50:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:50:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:50:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:50:35 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 10 Apr 2026 00:50:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 10 Apr 2026 00:50:35 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:51:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 10 Apr 2026 00:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 10 Apr 2026 00:51:07 GMT
ENV LEIN_ROOT=1
# Fri, 10 Apr 2026 00:51:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 10 Apr 2026 00:51:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:51:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:51:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecfd0096cf42a4b346149c8884e2883a5327fa6421d13906fd62b73146a1a3f`  
		Last Modified: Fri, 10 Apr 2026 00:51:58 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad0fbf3e1ecbbf0669e4b03587f323afb7aa3575a91846d71ba266a05e6c6a6`  
		Last Modified: Fri, 10 Apr 2026 00:51:55 GMT  
		Size: 18.0 MB (17961351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49023ada903b3d745ee4badf76fe5f8237ac7f8f22171c166a11b59e4ef0a61b`  
		Last Modified: Fri, 10 Apr 2026 00:51:55 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0988cb60a31b7a53e9235db8a37da9fe5d517cfa9eea999a0425c94d53f105c`  
		Last Modified: Fri, 10 Apr 2026 00:51:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4a550b25d562baf13d4bae4f5df6625e860c82268536792bc2256ce390d48ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23964c1ee89d86656d448c66f0ad6971eb597c3d2d50c6c34e36b57b23671548`

```dockerfile
```

-	Layers:
	-	`sha256:cb790e2d783cc96aabd8e94b0d076548802e58426684300727f43b3299d08c2c`  
		Last Modified: Thu, 16 Apr 2026 03:15:45 GMT  
		Size: 2.7 MB (2681323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818a12b7092d3fe89de578253a7b497f1818ac2845d5b2ddf006b3ec83222840`  
		Last Modified: Thu, 16 Apr 2026 03:15:45 GMT  
		Size: 18.4 KB (18440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d6c3808cf3ea0a8ec52e6baaf4989c7d7da5d173b0913cfcd1e653c05afdb0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139379447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1124e3f0a35c871f7994bc1cc43f4091d34575ea03aa262cc92404568fefff9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 09 Apr 2026 23:45:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:45:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:45:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:45:01 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:45:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:45:01 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:46:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:46:09 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:46:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:46:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:46:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:46:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37956ed1201c9f27285d3d4f966a731d8f7ce39846b58d097d35d447fa5c8676`  
		Last Modified: Thu, 09 Apr 2026 23:45:45 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de407e24ed72f8d0f0d528664eb1aca11d8fd7378a535390bed3cc5328f30123`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 17.4 MB (17421954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2108c1211edfb39692aac3eed12f9434e91fa4a865ebc91fed79d831e3b77d`  
		Last Modified: Thu, 16 Apr 2026 00:46:26 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98063b8b39936156d6de6e4b1c3d09f7d2704d74f9cc37173296d78d4351efc`  
		Last Modified: Thu, 16 Apr 2026 00:46:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8056d835cacacbaa1baae1e1276a5be13bc579d1285ffe05a5c3ef45ae32bcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9788c0ba36f72a23e7713d8914270a70d069fd40533975efda5d6fbb3a0e714`

```dockerfile
```

-	Layers:
	-	`sha256:d38d2cfb60836c41398a1b3b32e37e31fbcd78626b09f85c58ceada400d52180`  
		Last Modified: Thu, 16 Apr 2026 00:46:25 GMT  
		Size: 2.7 MB (2672554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4364a700b1848fd8cc739122e783ccfc293bd4fd26e3ab9a22c2c1e5de645765`  
		Last Modified: Thu, 16 Apr 2026 00:46:25 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json
