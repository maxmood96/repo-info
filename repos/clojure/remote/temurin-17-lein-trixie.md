## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:33098042606589c9703c40ade2a5fcb25b0c551a14ef0d8554927f2f6019d318
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

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f81cd787b5696d94b01a4dd424880d8dfc71a5a779a7fa6ad35c8fbf3032ed41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217235234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6c4a3a6641f8713a79365bb5fa70bb44e8c84731ecccca91c8f5c841c3e78e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:52:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:52:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:52:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:52:38 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:52:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:52:38 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:52:55 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:52:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:52:55 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:52:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:52:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:52:56 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:52:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c004c76ad269c6a5f9209b691a771fc3493b0c6bf5d2f77101c203df66bebc7`  
		Last Modified: Tue, 09 Dec 2025 06:17:04 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4d2321fafaae0aa36b9285deaea02142d87fa12161091043ff855d6e8d3961`  
		Last Modified: Mon, 08 Dec 2025 23:53:21 GMT  
		Size: 18.6 MB (18579625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df00a015d2f2299e080a37b7b132a09dd9145ce6d20d0b945015e6125f96f74e`  
		Last Modified: Mon, 08 Dec 2025 23:53:19 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80679642a6f9034ec9e685d09a85ccfa7cd6c0c6d40e1446b9adf11449f594d9`  
		Last Modified: Mon, 08 Dec 2025 23:53:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d2efc3767a23c1db3082a5a7d8f0fdeb1f6c8cae41f2db6a68e813a4e3346d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb67772b471fabe194e205f366c0effc0923e71054d6685946440f580827ef2`

```dockerfile
```

-	Layers:
	-	`sha256:0210b252407bed69ddae80a5a337131d1abf34fff8a2e6e1ab0e3f024de3ecff`  
		Last Modified: Tue, 09 Dec 2025 04:40:25 GMT  
		Size: 3.8 MB (3813380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2532979320f41f98405cd74ef106dde147d2dc5025bf83e1c4ed0fe8fb5ac9`  
		Last Modified: Tue, 09 Dec 2025 04:40:26 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e12c891490355e5800c219490fa217ff1528ddb6487e9f8ece607824d6376394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216388856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c6dba46924d703d70113358710cd0ab9aab4f3b36e8d378d520b4aa5b8ac14`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:00:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:00:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:00:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:00:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:00:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:00:30 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:00:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:00:47 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:00:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:00:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:00:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:00:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146eb1db881b7f2871fdbb0cd39f909c4e32194b125a3963c3dfe82385c88ad`  
		Last Modified: Tue, 09 Dec 2025 00:01:31 GMT  
		Size: 143.7 MB (143679914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb371539c866c3665ad0442deb750d6035ab04cac0b117fca66d499532c9b13`  
		Last Modified: Tue, 09 Dec 2025 00:01:16 GMT  
		Size: 18.5 MB (18540587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe244f42a4f1e13cfcfe5958e479744cf7c75bee111dce70eb120f612540c0b`  
		Last Modified: Tue, 09 Dec 2025 00:01:15 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c2c0db2c0ae73472e9b75301b4ac47595807ce76f1e941798f0af43e35d4bf`  
		Last Modified: Tue, 09 Dec 2025 00:01:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:39764278f2f988a0834e18472abc1c99e582549fd51be67d868cef426046ef71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6284703d6810619dd5440be69f0e6b72fb4faff3221cb2aedb0b13dde63ebf`

```dockerfile
```

-	Layers:
	-	`sha256:b510f3389fc88184cbe9712ea98e46c06552c74c48fbdc82c07247d6246e9266`  
		Last Modified: Tue, 09 Dec 2025 04:40:30 GMT  
		Size: 3.8 MB (3814257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce2a7cb1c9cbd1035ee73195c9d9d53e308170c0c88e5fac7396e6c4441e194`  
		Last Modified: Tue, 09 Dec 2025 04:40:31 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa6ec330a0cfcfe6acca13bda56b6ac916b29d62c6cd6603c6d7c63bc9ae4e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220788909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb0b181cb5e8cd1fd8d28d051ef196ef58f6b0f81fea77df0a755863e65dad7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:27:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:27:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:27:14 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:27:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:27:14 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:27:49 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:27:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:27:49 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:27:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:27:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:27:55 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:27:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a185af1bf60cf57d1da0f13bf5f3a56964ffa7635cc2b99d41cd3ba11696aff`  
		Last Modified: Mon, 08 Dec 2025 23:28:59 GMT  
		Size: 144.5 MB (144525284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d836e470d6cec0f854b72142cdff34bb9c0de7e67933641b13df830e03ce198`  
		Last Modified: Mon, 08 Dec 2025 23:28:48 GMT  
		Size: 18.6 MB (18636979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6859bda0b162267d24d474ae573b7e29c35cc4d58932fe49fda36e4d14078b`  
		Last Modified: Mon, 08 Dec 2025 23:28:48 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e25af8a384e042b1abb04a8de7847416624b9df4ee51cd10aa5ae57eba1949`  
		Last Modified: Mon, 08 Dec 2025 23:28:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:692e52ec41448fe5d5dc0e85a3737c6edc3402c59856798075b9bd8f0548f252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3f7bc9155c16dac031d6acb0ed6089ca235571092ef48ea06ef1203c52a0c9`

```dockerfile
```

-	Layers:
	-	`sha256:9443b073c4250be3d9acaf20549d089739f9db2f12e1815e0227943709d5124c`  
		Last Modified: Tue, 09 Dec 2025 01:36:44 GMT  
		Size: 3.8 MB (3814378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd8dea29da84ee0886db00052806d4d00a817e9af352747a004d9d4658a0ae4`  
		Last Modified: Tue, 09 Dec 2025 01:36:45 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:39c489903e667f42f59e4f570514065496a40385c34d25551f6531534f7a7581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212710522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4fecf5981559ac2c0f742d1230652d931ccd26953039647adecf67e71fa019`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 18:39:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 18:39:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 18:39:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 18:39:46 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 13 Dec 2025 18:39:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 13 Dec 2025 18:39:46 GMT
WORKDIR /tmp
# Sat, 13 Dec 2025 18:41:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 13 Dec 2025 18:41:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 13 Dec 2025 18:41:17 GMT
ENV LEIN_ROOT=1
# Sat, 13 Dec 2025 18:41:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 13 Dec 2025 18:41:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 13 Dec 2025 18:41:35 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 13 Dec 2025 18:41:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed11f364842f3868a4bd6a1452b0de55321419b5214a37e282efa4a365d37af`  
		Last Modified: Mon, 15 Dec 2025 01:28:47 GMT  
		Size: 141.9 MB (141889568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f83a1ebaf81b6c4c255228aaae3d55e7ec8d2c0bed461793ec3bf4c62c09b3`  
		Last Modified: Sat, 13 Dec 2025 18:45:51 GMT  
		Size: 18.5 MB (18531590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e133195a3704271ed0de5bb489cff5b1ddcac701004c167630d77aa56fd550e8`  
		Last Modified: Sat, 13 Dec 2025 18:45:50 GMT  
		Size: 4.5 MB (4517799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c31055540114335a46f391a3a63aa5fbfdbb49abcfbb69280d3adeb97de852`  
		Last Modified: Sat, 13 Dec 2025 18:45:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a273e24317d99fc656e9525dcfbbe11a94150aa4453cba91d132dd3b70309ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3ced06e7951a4535dfe5010d004ecc1999e4b5fa65731cc9b60d7081ff7b99`

```dockerfile
```

-	Layers:
	-	`sha256:060e1aa3fda25c294d3c8a245b074be3766fcf0d789ebbcfeb2dfb71e2e516a9`  
		Last Modified: Sat, 13 Dec 2025 19:35:19 GMT  
		Size: 3.8 MB (3801936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e291896bf3ce21b20f95aba0394c72775ce8cd00cb0cfbfb257ea979b3a3c4bc`  
		Last Modified: Sat, 13 Dec 2025 19:35:20 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1f39ab482e3ff34287ae5177b2eb5774dfe9a40a3ee8fd3c6b6e2570d1b3bd64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207343638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aea5e1be1b7e5daa6c78a8ec57be76babe034bd637e6dc159f4699ef97672e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:28:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:28:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:28:41 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:28:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:28:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:28:53 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:28:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:28:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:28:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:28:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adddff6e60525e3e5935f4cb8d230990cc26cb84b97bd2bab8bf590bd0472c`  
		Last Modified: Tue, 09 Dec 2025 01:29:57 GMT  
		Size: 134.9 MB (134859044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a90f87610ff4b0e9b83a03ac7d859a0797bd53fcda0e847e6a4ec6c58695d9`  
		Last Modified: Tue, 09 Dec 2025 01:29:28 GMT  
		Size: 18.6 MB (18620529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48d8fac8c86473c71b95d1342a4157699de8f1814addd1d3365d864ddfb750`  
		Last Modified: Tue, 09 Dec 2025 01:29:28 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a323be1202d5052d3455346c686b23b320a4848c2e77a28a81320745353740f6`  
		Last Modified: Tue, 09 Dec 2025 01:29:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d49aa09f53b4d29ea80ac1ab402e6ee37fd8923deecde237d616d1c86b6e37c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c4cc99898df113af21252e7fb000766f5d461c66d8e255a7680d87188a00ac`

```dockerfile
```

-	Layers:
	-	`sha256:a02bcfe934634bd93307c8b86d19e5724ef50eeb7d0ba88a88a8660e390ad60e`  
		Last Modified: Tue, 09 Dec 2025 04:40:58 GMT  
		Size: 3.8 MB (3809807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b919590101e899f2720951c8c1955bba15e50937b3b838cef3299446a2d52fc8`  
		Last Modified: Tue, 09 Dec 2025 04:40:58 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json
