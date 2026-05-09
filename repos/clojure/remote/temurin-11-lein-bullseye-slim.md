## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:3979594e753d0d16f605745b4e731e41ea1ba5e2d15566cf410a52d284ac6152
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fa60f2b4a6abf428f03af2e25d17c5a0500a36b037ebcdb96a049c0adf0c76db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196000786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e14a052f4873b76af431e621c81c2d792642c19c8a40a511a7be95509980b7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:15:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:15:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:15:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:15:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:15:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:15:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:15:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:15:53 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:15:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:15:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8933fbbfd2bcbdd10ad10af7426f35bd8e79b422c8fe93035e5f1d39bf31844`  
		Last Modified: Fri, 08 May 2026 20:16:13 GMT  
		Size: 145.9 MB (145886217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6da01d9aaa113c2ebd2970cdb3377cd87210c6d4fd41f87ab29da09b3d74c4`  
		Last Modified: Fri, 08 May 2026 20:16:10 GMT  
		Size: 15.3 MB (15338860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62e1f97944ec92ef056172a91bebd5d0a0fd2165ce97d4a2ca02afa679c38da`  
		Last Modified: Fri, 08 May 2026 20:16:10 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:739db0da47b16530f07fb381d28e3ebbb22615cd6a90fd8a82170da6cf7461ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8510b601e1f52472295bcd431975444abaa79be270e00f5530f924862ddea5c1`

```dockerfile
```

-	Layers:
	-	`sha256:e9e50692d2eacfe01dcf656d98e3fdf6bdfb16ec0a59b76b88bd33aeb0c6d339`  
		Last Modified: Fri, 08 May 2026 20:16:10 GMT  
		Size: 3.0 MB (3047725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0585bf45931d86c4e336a0e886f7829a42bf5773f23aabed3830b70202ca6a5a`  
		Last Modified: Fri, 08 May 2026 20:16:10 GMT  
		Size: 16.6 KB (16566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ee5c5adf604d77779d4268085037f9269a32ad971f929ce3561a51469bac3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191169807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b8a20fd3ab418b97bac744ca11fc77229f97bb6b84eeb45c22bce944b20cab`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:20:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:08 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:20:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:20:08 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:20 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081bf989f44e52f67a926dbf1daac982fffde71f099551ce8561862d0c55092d`  
		Last Modified: Fri, 08 May 2026 20:20:41 GMT  
		Size: 142.6 MB (142582243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32958c11cf00259043f626faa59fe091663f00adfd5f1c1cd204cf871a2cc66`  
		Last Modified: Fri, 08 May 2026 20:20:39 GMT  
		Size: 15.3 MB (15327208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75812b98ddbdb50cbe37e568c2f630c663a04ff08047f165dce3b79ac9ef4377`  
		Last Modified: Fri, 08 May 2026 20:20:38 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7abdbb111f21faa41e91186c2198cae8d904c245e623c28eff855aef33451f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3769a9a67f4e0ebc790e6dfabe6fc2a2b5fd2554c026741099959143cac1cf`

```dockerfile
```

-	Layers:
	-	`sha256:8c2f7b721405e004df986e5a4e0cac5e675f10d1ef81d660950eeea26151aa40`  
		Last Modified: Fri, 08 May 2026 20:20:38 GMT  
		Size: 3.0 MB (3047952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aea669a2049c84c43f3a02e0a503c33f4f40477cce06a69bfd9f6f40104eab`  
		Last Modified: Fri, 08 May 2026 20:20:38 GMT  
		Size: 16.7 KB (16687 bytes)  
		MIME: application/vnd.in-toto+json
