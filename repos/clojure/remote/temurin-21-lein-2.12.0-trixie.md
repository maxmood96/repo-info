## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:1296c210a001f3ce3d27db4479794e2bb131870620ecb30f4b255e7a2caa31f6
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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f6e7797293cdbe1810eb7988e478d70e85dc8ba427ce01ba05ca025cb3eb9102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230585058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e85083c0c16a85d113f14bc6960310467be7ff7eaf05abd8e5a77e5f52a59a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:59:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:59:45 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:00:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:00:00 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:00:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:00:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:02 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c40d9f9302c8984917c4703944ceb8d09c1bb8dbabfd382aa6a35b9a26018e`  
		Last Modified: Wed, 20 May 2026 00:00:29 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9a03bcdab2da37e1b78d9f441bb26e5742bdb714914c81eeb6cd6ebd322b4a`  
		Last Modified: Wed, 20 May 2026 00:00:25 GMT  
		Size: 18.6 MB (18589326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00488bb56e08a896ea489f69654bb9153a557e76f43a94715e394114bfca0c98`  
		Last Modified: Wed, 20 May 2026 00:00:24 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f95b8c7fea5128d4fc05bff311da1771c75f1edfedf05e72dc96d1c24b1497`  
		Last Modified: Wed, 20 May 2026 00:00:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a03172298fd587f0a6c5317c6d8e966ef855b0a94e0159a4d5b291affd3e7eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02139f07f32df0476c79d208cc219465b0d40ada14a3c6c25e072da6c4796a17`

```dockerfile
```

-	Layers:
	-	`sha256:ab2da3410435150cfc52d5cb90ca7faa58f0574f655bb05d56c3055136a85641`  
		Last Modified: Wed, 20 May 2026 00:00:24 GMT  
		Size: 3.8 MB (3818048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a775f3a7c319178422094b51395cd579ce1422eef363cef645dda8936f7762cc`  
		Last Modified: Wed, 20 May 2026 00:00:23 GMT  
		Size: 18.5 KB (18506 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f03863ea7552324c7c4b08521ebec5f80ce7753f62142ed8119f898a4954690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a63eb6e411a33b2a6b9b163c7ecdd72ba169cfcbb2209e9481fc0af623aea97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:06:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:50 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:06:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:06:50 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:07:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:07:09 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:07:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:07:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195153b3c0e0f783ab63e38ff82617531a912fe0c6ca7408e9c4765e3fd2a3ea`  
		Last Modified: Wed, 20 May 2026 00:07:33 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed868a8a98356cc0e3d5fd10692c75b6198238dc218e451723b36b9ad4dd7c`  
		Last Modified: Wed, 20 May 2026 00:07:30 GMT  
		Size: 18.5 MB (18547588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cc5a34798373dd38a27f11566a8fe0d67d963cd6fa4342e469617141794ba5`  
		Last Modified: Wed, 20 May 2026 00:07:30 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a42e4efae6c71cc32f82dd73e52e25419f1370a3a0ecdf262fcd5f63adc707`  
		Last Modified: Wed, 20 May 2026 00:07:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2365d86c84259a58d64e572e9e89d4e24f6933615377d25e16d3a6175c14c6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4841bffef5bdc6b2e1a94a928cfa6e051b65fced938750d9caf4c05aa5dd2960`

```dockerfile
```

-	Layers:
	-	`sha256:fc6f426e3a0cbb4c262c3ddb2470046bca4ac12889cfbfae9644057208634fdb`  
		Last Modified: Wed, 20 May 2026 00:07:30 GMT  
		Size: 3.8 MB (3818288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53744d42533092f05d8d0df71cb166ac423a79df9fb7c3962bbf84b8f0e6fcef`  
		Last Modified: Wed, 20 May 2026 00:07:30 GMT  
		Size: 18.6 KB (18627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:acde57fe5088f3084ad67eeb54d51d738155c4abd689ccfd1b69dfdb3a3c6df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234638428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9e644c74a1f9d2eafd7bd9715c6a3b39398ba2cbf316b4a82717902d2e37f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:02:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:02:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:02:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:02:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:02:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:02:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:02:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:02:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:02:56 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:03:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:03:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:03:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:03:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b629dc606e724e659e7094cdede449bd2fe74e4594977f7749e2b2b2395027`  
		Last Modified: Wed, 20 May 2026 06:03:43 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ced106a7143259ab31619c144e40128c884b6db84584b08e21ea649257ae8`  
		Last Modified: Wed, 20 May 2026 06:03:40 GMT  
		Size: 18.6 MB (18644814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb34cd3ea3d14556fc879e047075785cf6d65d9fb63215da2cc1114f3ff3da2`  
		Last Modified: Wed, 20 May 2026 06:03:39 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a0eb149ee39f546897b49a61c7698f21e46772905c736a59df26f1de415d6f`  
		Last Modified: Wed, 20 May 2026 06:03:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c0eca5e469382e713ae4cc7d0ac2acca831a99a77b4a752f17a62031147893d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb9d27454ed91c1a7cb06c3fdbbd13fce702ef2d6a6407635f93c4556f1c0e9`

```dockerfile
```

-	Layers:
	-	`sha256:afb45f690b17f7b45c69c2fc95eaf386bacc47412b1f3450a7ab3aceedb540fc`  
		Last Modified: Wed, 20 May 2026 06:03:39 GMT  
		Size: 3.8 MB (3819048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d32a53d5031faa9495e0fe6ff325d1659023423425b34838fc6a88ae5cce582`  
		Last Modified: Wed, 20 May 2026 06:03:39 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d8f81d4b5693e0539f8a66cc6c3c0e86f88f0517c6c5ba49aabc79544b764fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219916926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aaa459cb0120bb8728ad06c84bd68c19ed50eb52d1a925a813c44ce8838fb82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:45:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:45:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:45:42 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:45:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:45:42 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:45:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:45:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:45:56 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:45:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:45:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:45:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:45:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90ee71f8b40958ba47717d21c25ce285c57d654b11f27c92ffe42a254dc7008`  
		Last Modified: Wed, 20 May 2026 01:46:25 GMT  
		Size: 147.4 MB (147388349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232617944b072b63f601f445579aefeaaeb42efdb281a6804929ca15e08945fa`  
		Last Modified: Wed, 20 May 2026 01:46:23 GMT  
		Size: 18.6 MB (18630618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ba156c51a5444c09072b96a97c2b932e6f0333f3d286d7f69e2ef339f6078`  
		Last Modified: Wed, 20 May 2026 01:46:22 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481c7d27e9f5e9f2a761e81dac0c6791efd38b4d8585bd45b52b17703d66e6c5`  
		Last Modified: Wed, 20 May 2026 01:46:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:062c7c5e83bbaf4dc331e8ceef68b766e090174c4b942ff7e63378d0781c9d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cfe9eb28bd72a129eb1dbd401147671cebc45350b0f2169ccaadcd716c480d`

```dockerfile
```

-	Layers:
	-	`sha256:44134700d7044a9eee840e0c4b63251d13494f4574da92dc3402777706ce005f`  
		Last Modified: Wed, 20 May 2026 01:46:23 GMT  
		Size: 3.8 MB (3814475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7461ef7cfc781d5fd35fee4f6f1848099af7c186dd40f30269e81d5662632938`  
		Last Modified: Wed, 20 May 2026 01:46:22 GMT  
		Size: 18.5 KB (18506 bytes)  
		MIME: application/vnd.in-toto+json
