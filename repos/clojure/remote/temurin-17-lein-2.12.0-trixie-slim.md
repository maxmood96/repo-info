## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:4da3a3e78174236e5fe34dfcd14a3db569454ff93e3afbf7248ddcf58f061275
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff62f0073ac2213739f40d3d0b04b53fe557e3be05f9be40b7c87d80e6c58ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195591773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6f628c5c598ad29a08df97bc73ac933b090a28cdccc5103291a867c92766cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:52 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:42:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:42:52 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:43:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:43:07 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:43:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:43:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5810115b625644d725d31563e21ff5dd20b0f2a1c50139aa9f95c860d58cee`  
		Last Modified: Sat, 08 Nov 2025 23:27:08 GMT  
		Size: 144.8 MB (144848044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5b15c8d67d7066f2244aa82c7676ed65a46210d1040b8f8d806f84fee32f85`  
		Last Modified: Sat, 08 Nov 2025 18:43:39 GMT  
		Size: 16.4 MB (16447433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5247fcbac9ffe7ec944d8289d673168eac93a3ebd671012a5a6e0a464325f889`  
		Last Modified: Sat, 08 Nov 2025 18:43:38 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664d0848ee14f44d8e4b47911f663cdc6a5ff70c0856f40e962051476f4b01a5`  
		Last Modified: Sat, 08 Nov 2025 18:43:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1798259c25d9ef5f18964eb30cd9392fb3162b69e773f0d6d8a236f2f7e934e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d6a2d3fb91008380697e6fbf784935bf97a7892748851d65e9f9db5c0621dd`

```dockerfile
```

-	Layers:
	-	`sha256:213a48f1649c6de9a7d0d65ee8f9237beae509842b17e77509de972bc3f920d3`  
		Last Modified: Sat, 08 Nov 2025 22:43:40 GMT  
		Size: 2.4 MB (2363444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1067ec3ea8c476d589d0ccba3d92cc831c9bba113c0aa40683eb7f807b152793`  
		Last Modified: Sat, 08 Nov 2025 22:43:41 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d7a6509f33bd23afb81c3572c05e15c87bbd94fb60268da5f4e7512816cd9053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194753981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d68ae634d20e7e7b7b1e07e6a3c951dd34e225aff7923951b1fdf50857d7a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:42:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:30 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:42:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:42:30 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:46 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e91295b469b4695cd6e05fcfb67cd0437fe34097f01c80e703f6aa143e9940`  
		Last Modified: Mon, 10 Nov 2025 05:25:30 GMT  
		Size: 143.7 MB (143679948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f104cb6f7dcda6f9d3ebd71314ba01ca03ba6acb0fd29bf2641adea24126f2ff`  
		Last Modified: Sat, 08 Nov 2025 18:43:21 GMT  
		Size: 16.4 MB (16413578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fec54fe2f0f426b4a0406664fb4d784cf8b8364415d59a6556411007337aefc`  
		Last Modified: Sat, 08 Nov 2025 18:43:20 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d4db72ea5675e283a9386623301a8f3bd65e5da78ac9b97e2e298c598dca4c`  
		Last Modified: Sat, 08 Nov 2025 18:43:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf50238bd31ff101760c77b187b50246748e91b338c2b63fbddfabc6ea0999cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0be9d090290e0d1807bc9ed3a4362bdcf1e4831428da5a20fb663c5ec15c8d6`

```dockerfile
```

-	Layers:
	-	`sha256:1348c58302b0cfe00145e8da4555209798cb557028b83a53d54abcca48f4e2b8`  
		Last Modified: Sat, 08 Nov 2025 22:43:45 GMT  
		Size: 2.4 MB (2363062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da49ea8760d0fc0551a27a59e1accc12dfb1ee5394846deaa818bd336d8f4ed6`  
		Last Modified: Sat, 08 Nov 2025 22:43:46 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e067acc985ad6673743ce56ea8b210dd7636b941c9ac354475c7f0601afefd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199128373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d578dc1ead1a47d1a82530bf5704ed0e755e6bcf5816099c5825a17b84d805af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:19:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:19:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:19:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:19:55 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:19:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:19:55 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:20:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:20:27 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:20:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:20:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:20:30 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:20:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb56603809314457cab77f3e6ee6113b545a14ddbb276ed775bd25c2e218484`  
		Last Modified: Mon, 10 Nov 2025 23:12:22 GMT  
		Size: 144.5 MB (144525174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eb0ce4b502464c966a1896016e6d7c2dbd48fd867a9a336c8f2eddfe62cd83`  
		Last Modified: Sat, 08 Nov 2025 21:21:23 GMT  
		Size: 16.5 MB (16486411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c47519581ff8256f93f4a069cdd1bed29c7251cc99f94f93bbf22097bf414a`  
		Last Modified: Sat, 08 Nov 2025 21:21:21 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986fc7acfb3bad9e09385ce11fc99b164fce475ff5640206290783a39c0d7015`  
		Last Modified: Sat, 08 Nov 2025 21:21:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b15f91aa7d871175c6acacbfcaef4a65d1775e7cba25feb16aa1e784075a508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b04295117e054bab39f43bfebb8901943f00db47e409678459a097fb19a112`

```dockerfile
```

-	Layers:
	-	`sha256:f33895a47aeb50b11bf11183689a1114d1dbc7b5fedb65123942ef2ffed9bb7f`  
		Last Modified: Sat, 08 Nov 2025 22:43:49 GMT  
		Size: 2.4 MB (2364424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c59c1c602738a3a5a0c3f520dd3187fd7738dd88b119ebb67c53d225ed148b1b`  
		Last Modified: Sat, 08 Nov 2025 22:43:50 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:bfd657c663d47f2d69caffc8913c0f975839a9b98619047ac8f63d796fc08ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191081577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631ac9b299b34e164bf1a41129608db2cc5d4e91f414675a42f9b2e2193d60bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:21:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:21:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:21:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:21:44 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 10 Nov 2025 03:21:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 10 Nov 2025 03:21:44 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 03:23:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 10 Nov 2025 03:23:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 10 Nov 2025 03:23:12 GMT
ENV LEIN_ROOT=1
# Mon, 10 Nov 2025 03:23:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 10 Nov 2025 03:23:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 03:23:28 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 03:23:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3bc662a464cc8c76c0909121505b0bd2314416266a8dac4aa9014c89143db2`  
		Last Modified: Mon, 10 Nov 2025 23:11:08 GMT  
		Size: 141.9 MB (141889561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c44e78203bac2406d972bd4c1933eec33592c631a1d691f190069714c3e67d0`  
		Last Modified: Mon, 10 Nov 2025 03:27:30 GMT  
		Size: 16.4 MB (16398011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e851f1bfe861a0b27b14d4addf4472f9bfc3aea72c006b40bda74e60ac4ab`  
		Last Modified: Mon, 10 Nov 2025 03:27:28 GMT  
		Size: 4.5 MB (4517789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f37dbe4b04db2f0450be2368fb73581ea89b7e8d9c41bb4ed680405104dda8`  
		Last Modified: Mon, 10 Nov 2025 03:27:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22a7881d0c549b57f6429b4e950899addb3fef8313e4d5cf76675965bd221520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45bb855678ff6d0cb404c1566760d99a019a95c8ee7242d44cf8aa09f2ea462`

```dockerfile
```

-	Layers:
	-	`sha256:3a20a289c748ae3a98dcffff5f3500712a838072522969c26ed18ca14272a5ea`  
		Last Modified: Mon, 10 Nov 2025 04:35:30 GMT  
		Size: 2.4 MB (2353573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143a0bd54851f19bdce02e17bffc553c0f65a5286bb0b256261b44541901a17d`  
		Last Modified: Mon, 10 Nov 2025 04:35:31 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a976fe231386cc50f7956ed344a71873d4ef66a64c93ea566dd0c270321a7550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185698403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a8628be96b5f16f20a189f105532bd26d211224bda4e5ab4b1d59ea913609d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:40:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:40:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:40:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:40:26 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 19:40:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 19:40:27 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:40:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 19:40:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 19:40:43 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 19:40:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 19:40:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 19:40:46 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 19:40:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbf71ad3f6894d76931b880dd5f476e305ae8ab269caecdca1b11a7c4ec76be`  
		Last Modified: Sat, 08 Nov 2025 19:41:12 GMT  
		Size: 134.9 MB (134859044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f571ca112e02210874641223783023fa1ef11ccbae3fd8eff094affd91c7ce`  
		Last Modified: Sat, 08 Nov 2025 19:41:21 GMT  
		Size: 16.5 MB (16483783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaff1f381a321ab8e1503d1ef3be99ce7d973da498e33341f945dfdd1acaf8d0`  
		Last Modified: Sat, 08 Nov 2025 19:41:20 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ab0911f2c0fa72c2b6904665a87427207c104cf5ac7c340bbf5fbe3656edfa`  
		Last Modified: Sat, 08 Nov 2025 19:41:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd0a887563c1949c4a875cbcbe2eba9560846754d833094a9d77e8d9f350d826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba8b105806f65b70cb4762dc9318196896ae9488922a68a8aedd9e98817dc54`

```dockerfile
```

-	Layers:
	-	`sha256:1b28d06416b7ed5befefaf1ef31d97d314fbb9b28955b77225e3f4789b891eee`  
		Last Modified: Sat, 08 Nov 2025 22:43:57 GMT  
		Size: 2.4 MB (2359871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22eb1bb0b1b673d7c56817669caa5805ab1d9669a2d333823ea3316c9e450ecf`  
		Last Modified: Sat, 08 Nov 2025 22:43:57 GMT  
		Size: 18.4 KB (18386 bytes)  
		MIME: application/vnd.in-toto+json
