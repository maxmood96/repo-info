## `clojure:temurin-26-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:cff1a85bd265d774bc3cb020559c7d36b787a8800239d5cc6b561c6b876d7045
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:877c6a6de6756243b03d3719a1760258cdd27272ccc1a1f9b80bea39665936d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144641595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be32856989411a66d2cb26ea2b870bcbcd98436a0d1dacf2601af35cd4c1e914`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:21:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:47 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:47 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:05 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfba4d5310b88b06f178623508f9ca7627ef7152819b135b3186778b821382b5`  
		Last Modified: Thu, 11 Jun 2026 01:22:25 GMT  
		Size: 94.5 MB (94524364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbaf589e0f868bc9c480f34ebe5e7635252a0e9116a37b931943b2f2cbf76c5`  
		Last Modified: Thu, 11 Jun 2026 01:22:23 GMT  
		Size: 15.3 MB (15338846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab2d0c800a3f77d6a011de0316894a1eb8f6a41c31fb6953a9d37e5f84c172b`  
		Last Modified: Thu, 11 Jun 2026 01:22:22 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f32a5432376b33609e5486eec552c37a5ed90372561b3c7d3d6f6f9bad58892`  
		Last Modified: Thu, 11 Jun 2026 01:22:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03561d03b2d4a085154eaade2d4fef43ac8f6e641dc414b82172eb72a868040b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cecb03818d3817b37159780a244ee205e3c1e4712c61daa3e430e18e13d143`

```dockerfile
```

-	Layers:
	-	`sha256:feebd200cb3f31e4e0bcd1141461d9b2d039cbd68f36a5e63713627aa9b86143`  
		Last Modified: Thu, 11 Jun 2026 01:22:22 GMT  
		Size: 3.0 MB (2993104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16c1b6499a1acb965aa784ea3fcd07b9e5aa90d56f8f28687ee786d22dd7b6`  
		Last Modified: Thu, 11 Jun 2026 01:22:22 GMT  
		Size: 18.5 KB (18548 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e1a05ab617264e6eeca1837f09b72410747765f43c6ef28628666352e0ad736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142095901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d68ebd2fcfa0fdb2559ad30df58448cd5d2638577ddda9cef58427c0c8cd9db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:26:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:03 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:26:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:26:03 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:26:19 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:26:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:26:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80dc7a7b7a5d949784a66311cad0ee83656706aed30d8b9ff71fb8161896d8f`  
		Last Modified: Thu, 11 Jun 2026 01:26:40 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a78d5e08b6f3e3240c9983bbb5911de8de77e99d96a979ed4c0b906c2edcaa0`  
		Last Modified: Thu, 11 Jun 2026 01:26:38 GMT  
		Size: 15.3 MB (15327266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6713f9935b1bd295f6e73d80bdd6dc342618c879db6261629085d68851e765a`  
		Last Modified: Thu, 11 Jun 2026 01:26:37 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526feed21664252b4d6fdd006fd6c76c61bdda14cc313549c2d9543daa61bce`  
		Last Modified: Thu, 11 Jun 2026 01:26:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec517b6ebb81edb5cd026fc60be9fdc8ddefdbee7b3697ca6d88b74b9bb57aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4f00a4b858967166ecd3e8d36c5a60f6671995e78bad7357800506fa18266f`

```dockerfile
```

-	Layers:
	-	`sha256:43f469b87c378ad2e963c215a01e7d10a9ed06b2adad52fee8a0d24e61fe8c5b`  
		Last Modified: Thu, 11 Jun 2026 01:26:37 GMT  
		Size: 3.0 MB (2992710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0678e40233deafd4610115b215c797e31203ec98a5ec989493cd45e8d672f4a`  
		Last Modified: Thu, 11 Jun 2026 01:26:37 GMT  
		Size: 18.7 KB (18671 bytes)  
		MIME: application/vnd.in-toto+json
