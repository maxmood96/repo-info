## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:0a41766813c67193a8075fb4a2e56c30e059694927a164f1cc429d39daa99911
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cb5135f6096c38fd24ba44fe885e536ca9a1dff2b83910fc3b6dfbbb137b0ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194943290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7749d8ebadedd89cef134a39c7b8a127744ad0e8ccaec6e8ff8e6efee366033`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:57:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Dec 2025 23:57:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 29 Dec 2025 23:57:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:57:52 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 29 Dec 2025 23:57:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:58:30 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:58:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:58:44 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:58:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:58:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:58:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:58:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26724fb5ef68658026fd131936ac622b8c5e573971e660624d5f1ad0045adf39`  
		Last Modified: Mon, 29 Dec 2025 23:58:55 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b50d700690c78eef0b646b5452218a1325b4fc7677bc8556c21494573167f`  
		Last Modified: Tue, 30 Dec 2025 00:59:05 GMT  
		Size: 15.3 MB (15318731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c6efbda19caf96d6b069463499c23499f02e21435205764c5ef5ed76353a0b`  
		Last Modified: Tue, 30 Dec 2025 00:59:03 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef4c26bac490b7d1a9a14b843f5aaae84c6e7557a0ed591c711b6e3cf1f27e7`  
		Last Modified: Tue, 30 Dec 2025 00:59:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b8117f10cd01e2a30b12c49bb064404f59b659982770caf35c424ac5d7efa9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3035512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40df2bd338773f720f87dce8aabebc8ff19020a6d8a6d885122089d78d642287`

```dockerfile
```

-	Layers:
	-	`sha256:d51a02e65341d9d27c6f3c4455f8a7567d0754f8f166f24c6dc41d7904554492`  
		Last Modified: Tue, 30 Dec 2025 04:40:43 GMT  
		Size: 3.0 MB (3017910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a18de2ab55696633671072df0290879a46eef808a32054423ccdd66af43ead1a`  
		Last Modified: Tue, 30 Dec 2025 04:40:43 GMT  
		Size: 17.6 KB (17602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c83adba2482fd4b95d7f227a5165f895fc3f8973c5c7a77d2cfd9fce25b660fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.3 MB (192252318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecd25690081566109d208eb7187778a2fb1d0fc5157cf7ffbe4514244916012`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:57:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Dec 2025 23:57:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 29 Dec 2025 23:57:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:57:50 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 29 Dec 2025 23:57:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:59:26 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:59:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:59:40 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:59:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:59:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:59:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:59:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff17433fd932beecf4e830c2a6049049e273974253fee3dddab17e88c05262ba`  
		Last Modified: Mon, 29 Dec 2025 23:58:53 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef57c58e649ffd58b44b5efbc8fc43b1b4b569d5a94e43521937ba18172192a8`  
		Last Modified: Tue, 30 Dec 2025 00:59:57 GMT  
		Size: 15.3 MB (15305770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7707b2ffdc9f3905670c498b884531e771b5355ce12e88a6671334f664d13d9`  
		Last Modified: Tue, 30 Dec 2025 00:59:56 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40290da468e848da99a66a3823f40d8a866a249222468acb78848490f66cc604`  
		Last Modified: Tue, 30 Dec 2025 00:59:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3485819a6f88ccd1860e7da2496ee3eccaa4722a308e6a7e0d956cf6fc57bf38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3035240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb7b5e5e91651917b4a89bd66f7fd639234eed76421029d5a43d6285868c92c`

```dockerfile
```

-	Layers:
	-	`sha256:b51d224fd5b29128fe13dfa4647e6207a6ba85eb792a57f0614708654d216f08`  
		Last Modified: Tue, 30 Dec 2025 04:40:47 GMT  
		Size: 3.0 MB (3017519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b4ac6d3bd5bc7e979c62c92f588a2de5737cee18f631c41428e11565aa0434`  
		Last Modified: Tue, 30 Dec 2025 04:40:48 GMT  
		Size: 17.7 KB (17721 bytes)  
		MIME: application/vnd.in-toto+json
