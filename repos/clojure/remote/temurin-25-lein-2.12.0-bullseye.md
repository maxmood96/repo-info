## `clojure:temurin-25-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:dc02fdfb412286d846a3745dc66921f163f47b4f6b7864d08a5fa8fc10c86d84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:dab1601dedebeaaa8b2d2ac5f3858c36d9e1722f003ecc00e2d9488e71d1da0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167167195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41d4c7a3b5ba4d23193d56121313c573d1717784fed7bf43b0f172fd2c82dc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:42 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:20:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:42 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:20:56 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce2a1048a60554ceee874b36c9b3b9db654db95bf124d57baf30e900b44f6bc`  
		Last Modified: Wed, 22 Apr 2026 02:21:14 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5b91314aed75f0e62ae8f051d41e25808ee2861ece8618fcf169db56feff7d`  
		Last Modified: Wed, 22 Apr 2026 02:21:14 GMT  
		Size: 16.6 MB (16629560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bdb4e4fd488c2b308ae9a631d4dcb0697cc65bc104167e2610182e59f44904a`  
		Last Modified: Wed, 22 Apr 2026 02:21:13 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193a67992aee16f723c240ed8c38f054881d611e94ff59dbc74542070a37c98`  
		Last Modified: Wed, 22 Apr 2026 02:21:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0a94e4800917c4dedbd38b45acb3256ee29ce20cbdf0fb73d2262789a6ccae21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee7a700018ed9a1c9ca32af81d98c39e0eefaf8f9809373e28e23075cf7c56e`

```dockerfile
```

-	Layers:
	-	`sha256:25a69628b5f81c47a1688a453f95d9070b4fb500b06408f015f6841600fb33c9`  
		Last Modified: Wed, 22 Apr 2026 02:21:13 GMT  
		Size: 4.5 MB (4453902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42210bec663d92302e54b7087480ebd90cf8c7f78b13a00c21a19804a5d3ce79`  
		Last Modified: Wed, 22 Apr 2026 02:21:13 GMT  
		Size: 19.0 KB (19002 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be00e562a407726e8815064a8cd4a5bc2efc6d39c34d8814ea22af8766c5eef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164675965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6741a2e0277628ac2c778495fb6ca3971ca0d2a52830aa345328c2815615e991`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:23:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:33 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:23:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:23:33 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:23:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:23:47 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:23:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:23:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc3a7bb990c8494d5de34483e025d140c0c77aa6a3a7b58beac82d5f6555b0c`  
		Last Modified: Wed, 22 Apr 2026 02:24:08 GMT  
		Size: 91.3 MB (91288304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411815618e133e3545bde8811bb132d9d3b89470793423e56167f0eefdeeb4eb`  
		Last Modified: Wed, 22 Apr 2026 02:24:06 GMT  
		Size: 16.6 MB (16616528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac0280fc079b1947796dccb33a1ae2bbd839c00ca48695ac5034fcad0edc618`  
		Last Modified: Wed, 22 Apr 2026 02:24:05 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc471599720e6708341640e4e1dd4b8d0698892040cc122143a78318f95032`  
		Last Modified: Wed, 22 Apr 2026 02:24:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:87192664257a25ce96313a920ab575b96fddd1a175af340de85c51a25d433482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204bf04af390926a7ddedbc8d35f5173f5dff68f1acee59d235bd0805a7b6b13`

```dockerfile
```

-	Layers:
	-	`sha256:aeca7d679a781a2b29d7ea33184f9eabe7c5ce7b9ce7c53fc70558fe9ca494a5`  
		Last Modified: Wed, 22 Apr 2026 02:24:05 GMT  
		Size: 4.5 MB (4452897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1f7930b7a45b50119452b80e3f5d2002987e92b8a5c1386d7caabe416c7cc7`  
		Last Modified: Wed, 22 Apr 2026 02:24:05 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
