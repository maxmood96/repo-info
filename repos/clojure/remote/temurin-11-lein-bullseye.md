## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:92aee51ce5d257b88c75d5b293ca565ac18eb114c3500f49f732251f66c22f38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b9a22bdb2baa889b634787f174869415d32eb79e168e02c47b30cf16e1a69139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219848697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac0aa5a74f4de68ef76717a0379ea6ba514f3ee51dda61bd866be013f446584`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:50:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:50:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:50:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:50:48 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:50:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:50:48 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:51:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:51:01 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:51:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:51:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc2d520c1e99ff71ad1b8e5d2e62521194caf3c3748a016f685b6b71fe72e2`  
		Last Modified: Sat, 15 Nov 2025 10:10:21 GMT  
		Size: 145.0 MB (144966604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda9614c8d037744ba69d08bb32f3d70b7cf2b027fad3d34a46ea308a21fb520`  
		Last Modified: Fri, 14 Nov 2025 00:51:26 GMT  
		Size: 16.6 MB (16607608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b7e1370f176b33f9793efe64dcd0fde44f95d013b1c96341817385d125e853`  
		Last Modified: Fri, 14 Nov 2025 00:51:30 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6c75f0bef9fb53b5c2ceaab554e6ad306f5a8e2b666f23d3fcea4a8333b73afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dad6d9fcc9abcd16350d81e56cf04e50be2e0ec0a1bcab12a42f6443df9029`

```dockerfile
```

-	Layers:
	-	`sha256:68e43c48d8032c9e7bca07ed8e408f28110fb9a5ff039162e5b0ccd3230d7d67`  
		Last Modified: Fri, 14 Nov 2025 01:36:36 GMT  
		Size: 4.5 MB (4496329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b6a073727d520ea5756ddc5f8e6351fb71ee24fad764fd6d4a36c7db7b2ee8`  
		Last Modified: Fri, 14 Nov 2025 01:36:37 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5ebe96b51b64b7bc4029ee87ec2c7600c254f057fc31407c1be03ed4257492b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215102260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67523dadff6c9813769abd2104a25895fd78a0bb02cc476781e6c26ef9553bff`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:52:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:52:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:52:44 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:52:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:52:58 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:52:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:52:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5634df8faffef515dd767f93d0439d91b4b847ae5ac85c618895dab766de47`  
		Last Modified: Sun, 16 Nov 2025 01:57:47 GMT  
		Size: 141.7 MB (141731550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c07cad2296f86d4db2216baf52039b6f08d615e67582e9b5fc36553a5f373fb`  
		Last Modified: Fri, 14 Nov 2025 00:53:27 GMT  
		Size: 16.6 MB (16594992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09fdfd5f3bb67925ca9de81d82cf831dceaf12aa66affce8f3b2fd40d1fc4f9`  
		Last Modified: Fri, 14 Nov 2025 00:53:26 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bfd8e0502093422327e6abedb803d5e77c3d5299f9ffee464aab287fb67c9c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4512423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e825234058c0b715c59f7789ba079f96bf3d7b036239cf1e58f02ee435510692`

```dockerfile
```

-	Layers:
	-	`sha256:cd9829ff8fcfa528069c155b10b06ca378d20232a2786eb8fdd823251146f120`  
		Last Modified: Fri, 14 Nov 2025 01:36:43 GMT  
		Size: 4.5 MB (4495921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49dc18e1a23032b6191e271bdc40aeb9afecba033555a6b5bf72b4d25040a06f`  
		Last Modified: Fri, 14 Nov 2025 01:36:44 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json
