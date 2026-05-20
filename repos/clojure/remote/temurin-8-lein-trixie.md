## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:e2cfbbab8c206cf732266b122a6117e37d7bb6d894891be20888e21ef697098a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ebdded63d9b6a2fe248558f66b764a5c3df15999dd78b027c5e06436b24efb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127616454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874a2d0000ca4798408cbbe6c7aaa7356b6cc55d7b51b6bacb24e8bb88597c18`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:56:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:56:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:56:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:56:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:56:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:56:07 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:56:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:56:24 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:56:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:56:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c298f9831df4c7869ee4ba12dcae42b8743e797c2bce85fa2e163ca5a5c4ac`  
		Last Modified: Tue, 19 May 2026 23:56:42 GMT  
		Size: 55.2 MB (55198702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f3002a0c4682801ea2723c0476736cb42b766791a6da1a9864b5996f8f5a94`  
		Last Modified: Tue, 19 May 2026 23:56:41 GMT  
		Size: 18.6 MB (18589342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b0635fb5885a480a39fe8dd707927f0f98ab237eda25677b2f00a086d8177`  
		Last Modified: Tue, 19 May 2026 23:56:40 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:783430c7d01743c1893907264fd76d665d7734859102950ba056c97b5f30e9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcf7cddfe35bcc31617384c4e97934e60e70f98bb3dfbf5ef8f1cf29d99e7fa`

```dockerfile
```

-	Layers:
	-	`sha256:af5eb4ce6e69574faa77bc460ad0751f0b65c8eec301ee5cecfae58f00299d43`  
		Last Modified: Tue, 19 May 2026 23:56:40 GMT  
		Size: 3.9 MB (3936558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acae074133073c4eb56120b228998b4b8d785bd436286b1f5eba498fee29aba7`  
		Last Modified: Tue, 19 May 2026 23:56:40 GMT  
		Size: 16.5 KB (16506 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee5119e4d4cf0a2b1fe16f3fa0427a465593090bb67d3eda1aa82c096f7557dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127010477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f11f211096a0c55de2050febb167be8ec2de3c15d5205eab7383d81f1e372c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:03:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:09 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:03:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:03:09 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:03:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:03:26 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:03:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:03:28 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417494103773eca6dce729242fa226d69f1817b5ed6cde44b8e24b53db77313b`  
		Last Modified: Wed, 20 May 2026 00:03:42 GMT  
		Size: 54.3 MB (54272904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05154854874cd71b784a998e1fbd6e97ec4e5eeeaa395ec82be3c97bb357445f`  
		Last Modified: Wed, 20 May 2026 00:03:41 GMT  
		Size: 18.5 MB (18547609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bd3df5ae235fb7d682d18e49d6b90484dd39ef28c7ef03067f9b857cc0d57`  
		Last Modified: Wed, 20 May 2026 00:03:41 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c22e7b3330468d015b388aaa8e2a5d9a2a0fe88a30c56f7467100e9b83dc26ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3730b9406963f583ff1a215dbb2f91ff7227efdce1df929f570ca45d4ad0f24c`

```dockerfile
```

-	Layers:
	-	`sha256:3e454ba0a6e28014f5b393256fc46eae9eb9ea0177e0538aa4ed6b095f1b7c4a`  
		Last Modified: Wed, 20 May 2026 00:03:41 GMT  
		Size: 3.9 MB (3937498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc3f3e62bf34c3a0d97b0f58f291fd9325b59983c134be58fc372c2f0a5854b`  
		Last Modified: Wed, 20 May 2026 00:03:40 GMT  
		Size: 16.6 KB (16627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:683a61e5ec0655405369ce640b5b7770bfdbf0a40ea253f34590b7e64cd46436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128963836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4212ef0929c71b6c49287236f870f1ba97028ee83ae6943c00fc48256f6852d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:43:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:43:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:43:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:43:58 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:43:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:43:58 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:44:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:44:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:44:35 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:44:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:44:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb131e60882c6c99b34f1d0a5dae1d4e8aa1c48896f5ce690177030acaede9bb`  
		Last Modified: Wed, 20 May 2026 05:45:06 GMT  
		Size: 52.7 MB (52669123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb62f6f9031c4c5b9b4929599556a70224aa0d56615f3d0748a1427b9d551b6`  
		Last Modified: Wed, 20 May 2026 05:45:06 GMT  
		Size: 18.6 MB (18644755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b1f09f3ac3f6ba1574e0a5e17f5f44c7af113dc4494676e4298ef9f1698061`  
		Last Modified: Wed, 20 May 2026 05:45:05 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:60e87932b4d1c3712cff6107cff2c5497b44d0cd86dc2ce9ef241f8f146439a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365423058ca663e53f256f54d912daeccc24d60a21837eb4029646917f61a4f3`

```dockerfile
```

-	Layers:
	-	`sha256:18f633ddfa6a0d0e7e0dfe5dad743ce75a076bbaf6bf3a5d82c06f7334edf7fa`  
		Last Modified: Wed, 20 May 2026 05:45:04 GMT  
		Size: 3.9 MB (3938153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e929977415b02e3087c998ceae1db3abaf0fe1a5faa8dd5cf4db9a1e00ded19d`  
		Last Modified: Wed, 20 May 2026 05:45:04 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json
