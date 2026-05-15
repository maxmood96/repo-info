## `clojure:latest`

```console
$ docker pull clojure@sha256:73624b850fa2b479eae7cadcd517e79441020ff02183706574c6f295063fd0dc
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
$ docker pull clojure@sha256:c492d734cca241a4f5fd1b4264a8b2becd6edd683520f05a7ef0e810a8e9eae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240510807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e67f7926b7312b24e256a9e1a64e9e7d1af0903b52d1a86dcddbbcc355cf9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:12:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:12:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:12:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:12:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:12:46 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:12:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:12:59 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:13:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:13:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:13:01 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:13:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:13:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb3ccf7b4096f1322bba7ad929d8e7d505bc9a67ed1f1d53fc8dac0fa97daa9`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1603951cc79d788cceabbcac974837cf7cf40a853bcb19c4a4c7a34fc433b108`  
		Last Modified: Fri, 15 May 2026 20:13:33 GMT  
		Size: 19.8 MB (19806574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502325176b164ae2dbe8ec392b33187b62bf38d504d95df459e71ac484fde2b4`  
		Last Modified: Fri, 15 May 2026 20:13:32 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738909b7d09d41a077c075b0e34fd1925869b88cb7066a7869fa5c956cbbc810`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 75.1 MB (75122161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcb8c7d0173da7cfbbf8d4567813fcc13c7e9ee0fa8959ec01e4db15c1d8164`  
		Last Modified: Fri, 15 May 2026 20:13:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea750dba1182b8562b8d47dd43b0718928ad3a62d6581aa1200e8e89912871c`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:fba146a9614659b4e56ceeeca16f41fdc17cb658fb5b900961ab056a22e6ba64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7465255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627c812589f8c1e4a819c152d7f6f296999612184783f8e6436479d027ae92cf`

```dockerfile
```

-	Layers:
	-	`sha256:9cd5acf49f219c094122a8209c4a290da2d17ae9be5bebda8d56dd08ecc34422`  
		Last Modified: Fri, 15 May 2026 20:13:32 GMT  
		Size: 7.4 MB (7439492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590981da733b7ad8c7fc2d8e3596e9369e5b9fffc6c43544f221d0dae005aaf0`  
		Last Modified: Fri, 15 May 2026 20:13:31 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2fbc972892052eb9fc5e960c0de57c0a48585f80c339c90f0bcbb9094e946042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239350853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbdf852f7c39180298af5cca8530c1686e666ec6149420b0d84330e7a5b9f10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:12:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:12:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:12:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:12:42 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:12:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:12:42 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:12:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:12:56 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:12:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:12:57 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:12:57 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:13:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:13:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08b3b8b4753dd68c7c44d1b23ce6662dc2e12503e8400aa559b956db2f8141`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d973fec030c70536e2348754c2b3cbfe686771746acf5f9f561b53bd2a77d5`  
		Last Modified: Fri, 15 May 2026 20:13:31 GMT  
		Size: 19.6 MB (19637142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc3543f7dbfac11023d87953abe160797e352b0edc3cdf3a62cf26615d633e2`  
		Last Modified: Fri, 15 May 2026 20:13:30 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4ccc0dbcdd10782b33abe3a56edd9edc7d84649b4999f65465016004401b99`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 75.3 MB (75279522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2138ea6ca93fa3d540db6b3776e9dcb6a89b802bdb4ee428814313bba7dc29ff`  
		Last Modified: Fri, 15 May 2026 20:13:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82f1ff945b62ff1bce9d3d15c5bef474b065711e88f8c5acdb60c68f07f5af5`  
		Last Modified: Fri, 15 May 2026 20:13:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:6d8b6990b52032d4ee67371122b4181c7b0085e6494eb9a6ada1940d8b3dc9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7471115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3793afae99fb64490939063c20df0713e9ff9d7d98cb03ff0012ee656072e4c4`

```dockerfile
```

-	Layers:
	-	`sha256:c1b1b53f15cdb2e28e366cd8fb5b51cff75a2b81cbd6b629d14d7ee8863baf1f`  
		Last Modified: Fri, 15 May 2026 20:13:31 GMT  
		Size: 7.4 MB (7445228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc1233753607ab364fbbba4b793e034a6e4d8f9d9faa48c823aa35778ed74a0`  
		Last Modified: Fri, 15 May 2026 20:13:30 GMT  
		Size: 25.9 KB (25887 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:55a240316a9d920b8c143c79aff1408ee1ad873dcfe5d0ae91513b6513c039d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249523361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcc406576ae5b8966cc33a22962825202de5c20036bfe9eb491676f2801497f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:18:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:18:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:18:51 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:19:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:19:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:19:17 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:19:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:19:21 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:19:22 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:12:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:12:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:12:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:12:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:12:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de956b7a11284f1a158aa4d174299365ba072baa5eadc5c41d537c7ba7509c`  
		Last Modified: Sat, 09 May 2026 02:20:31 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7c27935ce89344c9f2063adaf35463730e2c3db3cda2b4435240ccf8a48f5f`  
		Last Modified: Sat, 09 May 2026 02:20:28 GMT  
		Size: 20.0 MB (20030513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8435cb421dfc3e57ae86315bbfd20609e9a621d5a198bd965880b6dcdf4018b5`  
		Last Modified: Sat, 09 May 2026 02:20:27 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3480ccbbc6ca8bf80dc87ce587b39b4507c07b2aa5473a93c91d33d7a03e4e7e`  
		Last Modified: Fri, 15 May 2026 20:13:24 GMT  
		Size: 80.7 MB (80723211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccef7e77db703a0184bff31647a6cd0f4e14f89be88d913d0d638eeae7d45c9`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a02d671699b84d0d277341c964795f1b0962eb9c424d321fd0c4d02e5fa08`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:cdb241f98659688e7695c26df10cba176631eba0c909268d5fae0803cf5c5210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7452857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6562b6cc3eecb9798b8d8baed4d6ac432f3a06fac42a50a9afba2a6010464309`

```dockerfile
```

-	Layers:
	-	`sha256:91b161329b75c3fcf02284e734135e0e321ed41332ed724fb26e0fce17892050`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 7.4 MB (7428008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d160b5023e98a93cd0ae79dca4af677d4c80b54f96f7bc2b23abda4328be5fad`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 24.8 KB (24849 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:02e673048812166aa47f446c40047909db422f3505a300578737ce8409cb7520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233825195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec886ca843cca4d17b3cc9a509ed20ab2adcc4d81715edfa9395e0ec0ea21414`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:32:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:32:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:32:13 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 14 May 2026 23:32:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 14 May 2026 23:32:13 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:32:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 14 May 2026 23:32:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 14 May 2026 23:32:26 GMT
ENV LEIN_ROOT=1
# Thu, 14 May 2026 23:32:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 14 May 2026 23:32:31 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:32:31 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:13:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:13:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:13:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:13:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:13:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b6df7c9202b34e5001f1810110d9cec30a4c24152183a755a378cbd2825b9a`  
		Last Modified: Thu, 14 May 2026 23:33:14 GMT  
		Size: 88.4 MB (88420318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea434e4bdaff060dd5d86848dd71f8fef7178355b899145cf2fcc6ca8551dbdb`  
		Last Modified: Thu, 14 May 2026 23:33:13 GMT  
		Size: 19.5 MB (19466847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302e9e28690038c8afdfe1a08c88ca42f5db41d05a25ae8720270cd48ac7cbc4`  
		Last Modified: Thu, 14 May 2026 23:33:12 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3174af8f703173f423fe49f9bacac707ca1b5536d1508ecdd417a30ab549b4`  
		Last Modified: Fri, 15 May 2026 20:14:05 GMT  
		Size: 74.3 MB (74271184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e144ea544e7de2fdff53881c159143b14b53986f086805c52d82dcc165a9edb`  
		Last Modified: Fri, 15 May 2026 20:14:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb92a787871937c5810b85fb16bc5a5f87a120ebba52a30f72d58f13f73ec14`  
		Last Modified: Fri, 15 May 2026 20:14:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:1a7f9e96fb9dc039a9e2614483238b1abe737a794f2b20da01ed6335cf785f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29169c8a5279befdc4b56dd2dc04922dbb7ff335dba90908034b314a0c7e77d2`

```dockerfile
```

-	Layers:
	-	`sha256:55ab25741b1cbfb5010d4a0300532fcfa650b1c32356965fc6bb6f449794f6f2`  
		Last Modified: Fri, 15 May 2026 20:14:03 GMT  
		Size: 7.4 MB (7415373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4352184a9c11d76df233e0fcee3639ca5169c536600f2b8e352e0919511db21`  
		Last Modified: Fri, 15 May 2026 20:14:02 GMT  
		Size: 24.8 KB (24810 bytes)  
		MIME: application/vnd.in-toto+json
