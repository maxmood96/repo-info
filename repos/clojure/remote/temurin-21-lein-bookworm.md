## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:c274dad2ac816155a824211ec581dd659728432e1fb18ea127499d99161194d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b4d372cbf2245dfe73049eba4f04102b4acb841109334301012491b058459035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230606908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c382831d3cba8d5673a942451bebaf0dd9426d4f8b31c1b7d19b324f67e66b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:55:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:55:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:55:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:55:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:55:48 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:55:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:55:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0932b189c59363c2bcbb734d72a0a0b13cad5f319412669b3de14419af67365a`  
		Last Modified: Tue, 04 Nov 2025 19:10:21 GMT  
		Size: 157.8 MB (157804741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955579c7c129a0c746c761cca54cb9944f1e6deee51a12d8696703573858f048`  
		Last Modified: Tue, 04 Nov 2025 00:56:18 GMT  
		Size: 19.8 MB (19802970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b982bf0cdebfc87c4544f5c9d4f3c64bbe1962966e43e6d4a9ac11197efa89`  
		Last Modified: Tue, 04 Nov 2025 00:56:15 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8676ea967ec6d9dbbacbb8f15696e4a7ae743bdddb5f727a75606b873ec4ff`  
		Last Modified: Tue, 04 Nov 2025 00:56:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3bf24c999d231a65a7184104bc63438d5dd519358b74c55dc7e942def1faea87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ed783a84d4fbe6c43d225f06512dd0f24a84856cc65f9880c3f84eefd5cc06`

```dockerfile
```

-	Layers:
	-	`sha256:3f2cbd308a78e7611a594914c18206b41e0074e45a95b1571a2808fc5d8699f1`  
		Last Modified: Tue, 04 Nov 2025 10:42:54 GMT  
		Size: 4.3 MB (4283586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da8e6f09f9c8f0f269e1983895552e9e3e0a61b2b1f317210a08959473257b8f`  
		Last Modified: Tue, 04 Nov 2025 10:42:57 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:37b3dc1084f6b08155ff7bf4e999852dd626dc4b169090dfb5127344c1942f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228591029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d1bfea0db7036c996ab6a7cdfc6c20cd7151c652c12efb46b389e1a1b50f22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:56:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:56:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:56:14 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:56:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:56:28 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:56:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:56:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe3f059f414eafdbe1749e41706610d982dcbfe280c42212d7fc2612dfd9c5e`  
		Last Modified: Tue, 04 Nov 2025 21:22:09 GMT  
		Size: 156.1 MB (156081238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23a5856581a18f50855d3e4040aba6d50e6484d47ae561999d2d53d275110e9`  
		Last Modified: Tue, 04 Nov 2025 00:56:58 GMT  
		Size: 19.6 MB (19632172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dc90ea78180c565e0f368290f584fec8f7f5887dfe750ed6f41fd531887f73`  
		Last Modified: Tue, 04 Nov 2025 00:56:57 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6cefc03ff5b870110f0fffc31d2d0fe0f799f3d4c84ec4c31d084d7cdd9bcb`  
		Last Modified: Tue, 04 Nov 2025 00:56:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2497630c5383ac4a14052ae6257b4df3c7b953805903dbe8c4011a06c87ed2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d909676b9c343b3611b09857001451a2b2e3fd8d6e48fcea0a5a6d082590edf`

```dockerfile
```

-	Layers:
	-	`sha256:6dd03288928ce88d674f7ee2b270ed8186f53ebc2b6aed1718dc8ff6883c9c0f`  
		Last Modified: Tue, 04 Nov 2025 10:43:02 GMT  
		Size: 4.3 MB (4283225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fa27a03bc1f3eb916cd9518a8e4d55ee2f36e622901ed039acf9d75eee14f4`  
		Last Modified: Tue, 04 Nov 2025 10:43:03 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b15a48be29e0b0820669c5778f107467430bf88914071ccecc8184c54c4e565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234830524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e0f799df25b79d1a74bb6be13958681275ffed91455c345a8281f273422481`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:53:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:53:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:54:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:54:00 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:54:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:54:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:54:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:54:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfed681a131059fef5f258e337944be0ad4a0ab0a0f864dd465487a2c1aa3a3`  
		Last Modified: Tue, 04 Nov 2025 11:07:07 GMT  
		Size: 158.0 MB (157963427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaed89c22088d6cbf8cbe39a7d5a9b252186d55acfa2bb4ec309022647a286f`  
		Last Modified: Tue, 04 Nov 2025 00:55:05 GMT  
		Size: 20.0 MB (20021633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43247246430a1afeb1589f54424cc9aadb12459a61438b8d65e95ac3ac6579e3`  
		Last Modified: Tue, 04 Nov 2025 00:55:03 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c49b34f0b1ed039cd568e2c39e7a3495b586be31ddb8d5747174bd2c74e18c7`  
		Last Modified: Tue, 04 Nov 2025 00:55:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cabff374803da4bbe2a3c8be7ff36ed91d5dfa5d9f9f055e6f849c06c9357b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78247c83d017fea31c15d2bc386816a9d860d1a3e9d166b7bc54181c292ad039`

```dockerfile
```

-	Layers:
	-	`sha256:8c57ae4ac97452b61947abef8b10090cda86e57c6f98e4326656727ea9b175a5`  
		Last Modified: Tue, 04 Nov 2025 10:43:07 GMT  
		Size: 4.3 MB (4285457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5646185b7ddb06bc457229d49f557608e8b82a2844d1b26a79f801a32fb7ff52`  
		Last Modified: Tue, 04 Nov 2025 10:43:08 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f49a810e33016147456fe04f9f9e5902e4561678bb319ca75954a1a63739de28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218143878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fe478d03b03156e5194cd22f27e7a8c36d513ef3f5475864ab5facf9680718`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:29:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:29:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:29:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:29:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 06:29:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 06:29:41 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:29:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 06:29:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 06:29:52 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 06:29:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 06:29:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:29:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:29:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fde30b14cceb4c80b5871c74f0422e956b7c7142270a5d3a1d99ea678a172e`  
		Last Modified: Tue, 04 Nov 2025 11:07:42 GMT  
		Size: 147.0 MB (147026950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9f2bf83b27c162e03476cce5b328d765b5996dd615ef4a2568affadc9e57b3`  
		Last Modified: Tue, 04 Nov 2025 06:30:31 GMT  
		Size: 19.5 MB (19460667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9d76b33069b02b0c0ec5b771132eda0359c1a095b458c954fbbc4e130fb97c`  
		Last Modified: Tue, 04 Nov 2025 06:30:31 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da389248fcbfcff7ecf6e489ac510d412d0f536573a85e9ceac66501856356f`  
		Last Modified: Tue, 04 Nov 2025 06:30:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ecdbb8d1dd920fe022283fb78ed6cd2466884dade1d7a4a6de8931d876edfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63be0831ad39a981aa5e09d7ee30e67e9c78aacb1b4c901cb752dc7336eaf11`

```dockerfile
```

-	Layers:
	-	`sha256:3f9529ac6eba82e6a25a942f8e016732ecaae2e299f2215fa87aadaa3ecd4f03`  
		Last Modified: Tue, 04 Nov 2025 10:43:12 GMT  
		Size: 4.3 MB (4275400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:572f7c107d5ffea5956a96b99bd789a6c34ee3dc08bc447ae8ec2c3e607a4fe5`  
		Last Modified: Tue, 04 Nov 2025 10:43:13 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
