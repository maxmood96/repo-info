## `clojure:temurin-25-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:58ec4ea49d08e5183c636f67a2299eb0f66afd51a93fb9569402a2ddb233ec4f
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

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e1a832fa9c4179c866d5b46724ad0e7414098c953b72182f223b7583068e9947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164657112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b13d3f326675d40bd8369fd55f8623384420017df7ef3c6afd268b209988d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:01:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:32 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:01:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:01:32 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:01:50 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:01:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:01:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887b1883591b98cffba4f9992de81d34cfdad14c7c5e1aaa14782fc0706adbe1`  
		Last Modified: Tue, 17 Mar 2026 03:02:09 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab07e5ea8afa40d78abe5aa1be89ddb913beed124c3835b1328108eef5fad397`  
		Last Modified: Tue, 17 Mar 2026 03:02:12 GMT  
		Size: 18.6 MB (18585112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490eec64be27bc4bce421e938979c41f229f447550e90405def746c5fc269e1b`  
		Last Modified: Tue, 17 Mar 2026 03:02:11 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5b0980e9e7452d74e47f17a19a818eea060015b0e505e3a1439c51d54253b2`  
		Last Modified: Tue, 17 Mar 2026 03:02:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:44cef42388741fb5cfb1d5610f19ca3886bca9955af63204f9e0294a7132534e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88b4e85010c0eec4ac378ffd6ea4d420f94f5ceba020c9bb8de2bc7f2a7313b`

```dockerfile
```

-	Layers:
	-	`sha256:d0d1b74ed2149e0d23c3944750c9467d94e205f7f0f138818294c7786ed0be70`  
		Last Modified: Tue, 17 Mar 2026 03:02:11 GMT  
		Size: 3.8 MB (3783559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:364548850cf1ed04357d97f1f5aace1a25d98e3d780298dd1458c81eaf21c8c3`  
		Last Modified: Tue, 17 Mar 2026 03:02:10 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c8baa9968328ff74f003a5c5c59ecff1e0fb9d1c3ede906a6f4218484d9f865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164016146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14409dbaaf695b4bf07624e86d2fae1962e5d8f43a9587c1a88e62ff9a2243a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:05:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:05:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:05:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:05:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:05:25 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:05:44 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:05:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:05:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69edc4821208584609ba50a1f7945b66c6105aaaf91851514f4b787b157b25e`  
		Last Modified: Tue, 17 Mar 2026 03:06:02 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bdefb7cacf36203ef71a5f06b1b32ab2c9345f154456688f83879bcf573a18`  
		Last Modified: Tue, 17 Mar 2026 03:06:03 GMT  
		Size: 18.5 MB (18544781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba734df7b3f30b66a820d9f8944f426ed9cb8d458c87507182ce225034f1c078`  
		Last Modified: Tue, 17 Mar 2026 03:06:02 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de58d3dbd4a48cb09904542f1981c185d5412404df1bf86db694421014ce9bd7`  
		Last Modified: Tue, 17 Mar 2026 03:06:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:668527d2b5a82d1b79783a758d940527bd2abee712dc500176fce18a92d6825a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b381c43d0364b85aadc24596215cffaad4590c60a329d723334feea7263429`

```dockerfile
```

-	Layers:
	-	`sha256:618978911205155c170cc460a1c2e5b7cd9454a1b0e4004f0dc317ece14b2cd9`  
		Last Modified: Tue, 17 Mar 2026 03:06:02 GMT  
		Size: 3.8 MB (3784457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d1a71123c562dc1f2734b411471ce8a1dd852c3a9c498acf02deaa8090534d`  
		Last Modified: Tue, 17 Mar 2026 03:06:02 GMT  
		Size: 19.1 KB (19123 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:bc067fdd557129b78641a93f74af15d4bf56728c85df1866c723d96d5086cb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167910134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e08b9f794a415a8b89fc9bc47693d8964e5f30ea5896d4c2ca94f0408eee79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:45:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:45:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:45:54 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:46:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:46:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:46:35 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:46:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:46:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:46:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:46:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dcd2e20d0ba59a0ceda7d174daf8edc831e31e2d722a352fbe87f7cac9ae5d`  
		Last Modified: Tue, 17 Mar 2026 18:47:13 GMT  
		Size: 91.6 MB (91632901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482206034e5374f9e7c61a9d73a80bf5c5bc2316f12baa807cc19d87a93393`  
		Last Modified: Tue, 17 Mar 2026 18:47:11 GMT  
		Size: 18.6 MB (18640739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39d98aac8be0c9a4147959fe2d893a778d58a2de9036aaef0708ef09ba25c18`  
		Last Modified: Tue, 17 Mar 2026 18:47:10 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e402c1c1abe40369ee3111ca75c31b757ba81fc69aea656e88e90733f29cd03a`  
		Last Modified: Tue, 17 Mar 2026 18:47:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:27a1526970eccfdb16c9bf8c69ae79dfc420b233dd5ba199c7d5de9abbe7f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7847b5b235e01a6071273b8c91b7ef46b560c5847aaced87ce11e4a95207bde`

```dockerfile
```

-	Layers:
	-	`sha256:fd2b992d5b4617ed23aad37cf124701d591db7b9b77ff186acda70ce7bdfa5da`  
		Last Modified: Tue, 17 Mar 2026 18:47:10 GMT  
		Size: 3.8 MB (3767883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d28d3622939342870566886ca1a315ef6694f9548e3e771910a5e3b1798952`  
		Last Modified: Tue, 17 Mar 2026 18:47:10 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:ec360eaf0c41f5aee82727b827a035dec24886aa802640f890dd40df3fb1ff91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161621598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0714abf912905a19f66224c94902a39b28a298c96a322d309cde93c6c09146`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 19:27:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 19:27:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 19:27:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 19:27:56 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 22 Mar 2026 19:27:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 22 Mar 2026 19:27:57 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:29:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 22 Mar 2026 19:29:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 22 Mar 2026 19:29:31 GMT
ENV LEIN_ROOT=1
# Sun, 22 Mar 2026 19:29:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 22 Mar 2026 19:29:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:29:48 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:29:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45c9549b3fd22069333772ff17a0ac1235b4853c85fca137130bf290f6f49b1`  
		Last Modified: Sun, 22 Mar 2026 19:33:35 GMT  
		Size: 90.8 MB (90773420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62952e36997a82b558bb88cd1eb56f7475ddc6cd9e385bd12e9ad59fd0e9ee1a`  
		Last Modified: Sun, 22 Mar 2026 19:33:24 GMT  
		Size: 18.5 MB (18537640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcfade903762f5c9059d61d4883e1c269145f75873568018e7bf832b0137fad`  
		Last Modified: Sun, 22 Mar 2026 19:33:20 GMT  
		Size: 4.5 MB (4517782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44daf5efe080b554ff20bfff1c69ec112c391114727d02d20c1809b6585ebe95`  
		Last Modified: Sun, 22 Mar 2026 19:33:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bbea51163d22bc2cf83e5f7638bde5d1316f4c8a78af1c74c6dc01a8e9d103ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6223dfcde3107659a87976d6b4f2e783c4bdbbff1d82186c5bc483a1a41c12a0`

```dockerfile
```

-	Layers:
	-	`sha256:cc89220eb71d0f4ed92f78997f491b7bb2a346947325f16c2363d8abe355739c`  
		Last Modified: Sun, 22 Mar 2026 19:33:19 GMT  
		Size: 3.8 MB (3756059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f263e597e4b8e1809357cf99934d864c4c8814329479cc3f02ac36ed6f377618`  
		Last Modified: Sun, 22 Mar 2026 19:33:17 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c67df2a2f85ffb0e8cffa6d6759c1100e5c5a7cb92545ef6e6d1b7d319fc2f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160743060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e162dd87853f8b4d7beb16f0f5c4660b710427f24921c4ec3aa3281ec1d71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:44:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:44:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:44:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:44:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 11:44:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 11:44:25 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:44:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 11:44:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 11:44:47 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 11:44:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 11:44:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:44:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:44:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ae47ba5b08d3cdfb94505570d925544515281d699f0a59f9331ccfaa09c970`  
		Last Modified: Tue, 17 Mar 2026 11:45:29 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809f3f897ad9991a9fea65ded1e446072500bc0c97873b3936ebcf417523e50b`  
		Last Modified: Tue, 17 Mar 2026 11:45:26 GMT  
		Size: 18.6 MB (18626287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e789e12d46b5f99d537d38a925d9db311f39506182218c5da26f1a729eed31`  
		Last Modified: Tue, 17 Mar 2026 11:45:26 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce298e0769932171a253948ecef99bd9a121d3b48ce5fd696ed37160c561e796`  
		Last Modified: Tue, 17 Mar 2026 11:45:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0ba4004f264e5ed6fe7736dc90e8a8b9a3f2946583adae868c759fd17f263f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c90c160334c1b9fb05478409b3200eac2565af3d540b589c8e94b3089e379a3`

```dockerfile
```

-	Layers:
	-	`sha256:7544f9b8fc30d619a84a9056e6078a7a775b9291060b02d76e5093172f000e0a`  
		Last Modified: Tue, 17 Mar 2026 11:45:26 GMT  
		Size: 3.8 MB (3764548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f39f05930641e02e6483d8c25c2a401c2f044c76e5fa617cf8c27502a7043e`  
		Last Modified: Tue, 17 Mar 2026 11:45:24 GMT  
		Size: 19.0 KB (18978 bytes)  
		MIME: application/vnd.in-toto+json
