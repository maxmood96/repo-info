## `clojure:temurin-25-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:b7cd086962d1a40a64ccf1c461955316bebf4d0a335a00bdd6af6fa9e5832aeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:87168442b0409498c0e5dc10da07f1c2a5a94be20434f6b50c404a4e87348f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142691747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4aa280bb9366f6b1fe86052477ee768d08d70e1f26560984c8e334aec49feef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:20:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:36 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:20:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:20:36 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:48 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8a5023c5d359c1bf789f27b2b150e75fb7a388d18b476d6b851b2fa18cd4f6`  
		Last Modified: Thu, 11 Jun 2026 01:21:07 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e544ded665d138a8f381911150291c0510d59f59da4a18dd13c4b6c9812eb0`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 15.3 MB (15338760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d262891a1922f1d4fffe8719d2d32e78cb58702035a5e2ad2970284611b81e61`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b25e279922f27d05eabffac5bc133d37a7320486978fd071960f9885694432`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7496b99b458724ba4a4b85c075c596de33313ce939205cb059e9a0bac6b6c89a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bd8b2c3d11cd47a44b40e5bcb0f7c1d04173cfd81940c095d7e7e3a8f27854`

```dockerfile
```

-	Layers:
	-	`sha256:4b7a1522911bacd0571d496de4b110206984233fe85f5f88ffdfb4b043dda680`  
		Last Modified: Thu, 11 Jun 2026 01:21:04 GMT  
		Size: 3.0 MB (2996269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6b4c739e650d1e5c691eaa520d0768c5cf92c6afe61dace77ebe8656370d107`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 19.2 KB (19211 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a681922b7d43ac4f1625019f3c3c78e6b97ec4c70f18eac47e8bbfc1e33f55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140133785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cc61cd00c74e3e92c19d55cead69367339c19f5904f37ac5e46b18d81bfc58`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:43 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:24:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:24:43 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:25:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:25:04 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:25:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:25:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe09dd2f44ade222168d8f17a99c5e66e21b373942e782d2ff2a58c1b54d3f0`  
		Last Modified: Thu, 11 Jun 2026 01:25:25 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87a453aa12b96ddfa82c37c8d311ecc461d91d4d8b9cc4943646947b56a1b06`  
		Last Modified: Thu, 11 Jun 2026 01:25:23 GMT  
		Size: 15.3 MB (15327227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db50e3800e3dd92995f8e478808f371e1d3759777b7f2461a19419b6713b9e1e`  
		Last Modified: Thu, 11 Jun 2026 01:25:23 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537cc88cd49557b04dd92c047781de6081ed4b8d474d8660638c11248c528548`  
		Last Modified: Thu, 11 Jun 2026 01:25:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b0c5379395d949728a5ec90e9247ea34dc66f8613b88cf3be3833642aab6082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a191bc4e560cc890063728f907e8aa124a422b9f1d4ca86b38ffb5b951b9f798`

```dockerfile
```

-	Layers:
	-	`sha256:a4f2733b1ab0bdf62d3e38e93303680a52c8b96b15fbe90c4191b1926b59aafe`  
		Last Modified: Thu, 11 Jun 2026 01:25:22 GMT  
		Size: 3.0 MB (2995899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c3343c0bce28f58f319b577c0dea06c3b854bc6731933a8ccd41aa8b4d1532`  
		Last Modified: Thu, 11 Jun 2026 01:25:22 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json
