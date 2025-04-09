## `clojure:temurin-24-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:a1c1033b1e52bf31dcbbaffe47e236da2f9d60abcccb2e083663498f0abacdc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4651ee01042a1dcaff5975f84ef61174b3db7343fbabd3831c5016afa633707f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174156808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417e488c46c7d909fa5d14a67cfc718a388eb089386785e13fda607c93f97e09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2837057b00f3a97cbb44bf7bf871cbea8e41ea2418d052d244713d3dd68629e`  
		Last Modified: Wed, 09 Apr 2025 02:19:30 GMT  
		Size: 89.9 MB (89949048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ec9427ad8ea5498b3aceeb6b8dae4d480f3d9112655a2261e2075d6b1cbe77`  
		Last Modified: Wed, 09 Apr 2025 02:19:32 GMT  
		Size: 51.5 MB (51465911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da52e8eb4f93579a05c398de8db0e4f37a165e7be59bbf88964c25c2141decbc`  
		Last Modified: Wed, 09 Apr 2025 02:19:27 GMT  
		Size: 4.5 MB (4514161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66229cd02d634d3b494b09c6dd4dbc864b3976ba4f0e931bd242652826374ad1`  
		Last Modified: Wed, 09 Apr 2025 02:19:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ab55f22925605691f066bd4b022451a75fda9e381ab231d91bf8236ccf8d773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0783e5b572eadab72ad7822a7c0c7cb3c6f7671f2330e20d5ea299e6962272`

```dockerfile
```

-	Layers:
	-	`sha256:2297d995a367ff9bbde8213a27895b5245748c326b3ba6bd76de596a2c179cdd`  
		Last Modified: Wed, 09 Apr 2025 02:19:27 GMT  
		Size: 4.3 MB (4272457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e03cbadb4e462657a5ed07c6a80f06b1feaacdbe64cf6461c7bfea9053984b`  
		Last Modified: Wed, 09 Apr 2025 02:19:27 GMT  
		Size: 18.5 KB (18451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61b0e6267bfbe824634e8def8e4f62cd3a0554258381f58fe61dc4bac7db7f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173102797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e267d9e51fd26d336ef32789fddd1037ad1c6dbe7f9bfa0e137388ac9963a243`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6e889996bf89b2f34eaa11526c26b2694b9cb20d1a4dfa0c7b5d26a120d225`  
		Last Modified: Wed, 09 Apr 2025 17:48:36 GMT  
		Size: 89.1 MB (89092721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa05b0a17574ecfb66f549c0de2019a16e469cd7175592d23a4b37a09bedd074`  
		Last Modified: Wed, 09 Apr 2025 17:48:36 GMT  
		Size: 51.4 MB (51429165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddcd803dc04d64701fbc574319f2bf4897a031ef136faf26ce5b6c2ec7ed5aa`  
		Last Modified: Wed, 09 Apr 2025 17:48:34 GMT  
		Size: 4.5 MB (4514162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6ad6db48c0ca6a16afd5c504cf4a22904b688c6307d2b767511039930fd92e`  
		Last Modified: Wed, 09 Apr 2025 17:48:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90de2c3b7494b23814f10c0af84a0d28c53e63b203e14fb05ff265020759d202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8579fbe152a6629ad209cf27e5f379843358a8d82cf92040222caedc007cf712`

```dockerfile
```

-	Layers:
	-	`sha256:574c9ac13479a8e727e346b43f15770fd0135e5f092ad917b99afaad5ac73c61`  
		Last Modified: Wed, 09 Apr 2025 17:48:34 GMT  
		Size: 4.3 MB (4278146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2b9f6bb0fd4a29a6e40bc6091d3b6b252c9c856a3861e2d2db0ad7e407ff07`  
		Last Modified: Wed, 09 Apr 2025 17:48:34 GMT  
		Size: 18.6 KB (18572 bytes)  
		MIME: application/vnd.in-toto+json
