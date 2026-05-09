## `clojure:temurin-17-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:b0a7249f83423e4e854c5f6990b516580bfe17da0f453bb96034eb930c87ac92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6820e31b539819fafbd3568fbc3f4ca4b27f0149d626f32ea708b555ac0d5996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220816593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308e69e2126880bb5e6dc07bce0d462d4e93674a86f34395b4771bd412e1699f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:16:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:16:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:16:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:17:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:17:10 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:17:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:17:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f66de5276bb76c65b4faa35aa77f9376dcf52e701862d9ee9760bb7c7a26dd`  
		Last Modified: Fri, 08 May 2026 20:17:33 GMT  
		Size: 145.9 MB (145905489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13797640f6c04535db7db3fb707e8e2ff0f68d4e65ea6ef49bfdeeab37994e`  
		Last Modified: Fri, 08 May 2026 20:17:30 GMT  
		Size: 16.6 MB (16629584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1fd5775cf9bd334aac9491caf014e07ff2366ba95d6266af262ede1eea5dc0`  
		Last Modified: Fri, 08 May 2026 20:17:30 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914c2779e92b100c996d1c0df6cb0f68e0b84d3bc574f223e1b4b84b80f222ac`  
		Last Modified: Fri, 08 May 2026 20:17:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ab080ba11bb275355acc7dff03cab68ec8abbe555b02013e96cc49042f155926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7988957b0c675191d614d7613ad9b1c50cb29952d9d2cd2e7f972c4715c2bf76`

```dockerfile
```

-	Layers:
	-	`sha256:87ff1cb6059185aef0f73903c7e30564745942d58ff71fd12ec36ee7b6ac964e`  
		Last Modified: Fri, 08 May 2026 20:17:30 GMT  
		Size: 4.5 MB (4486489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:316b32020659a4121f796405503e27f9b3c4946fe87bb0af07b044aa839e2ef8`  
		Last Modified: Fri, 08 May 2026 20:17:29 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44aeb49e484481f1ea415c477ef6df112a28a6994cc84f3791954d7bed720357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218112220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a15ecdfad0df6e6ac3aae59c0797ebecd2bda1aa42ef1a85eaabefdd73391a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:21:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:12 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:21:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:21:12 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:21:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:21:26 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:21:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:21:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bb1ac705581d814ff487013d6a8b4cc267bc9c16ab579ce177024b9f668c6`  
		Last Modified: Fri, 08 May 2026 20:21:47 GMT  
		Size: 144.7 MB (144724334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4835ed464b6b2c95eae99f22743c4201275d31da09b352fb8a5308ce2f2f3b4f`  
		Last Modified: Fri, 08 May 2026 20:21:45 GMT  
		Size: 16.6 MB (16616541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea28e40be38a5c9088eec622b62b8b8df5723edaa452c654c202869ec494e7c8`  
		Last Modified: Fri, 08 May 2026 20:21:44 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be68e4a63fbf0568f9e653e91a1dd675bcf49ad60aadd17eab6e4f905431fd07`  
		Last Modified: Fri, 08 May 2026 20:21:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0066bdde37ef81c73db02dbe77241c284b3268929c6c1ecd8d1ab80b2bc42784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3cdd46a75dbb3d302c9a33879a5117a2f6b9b37ea752c3cd5f60c865c5868c`

```dockerfile
```

-	Layers:
	-	`sha256:ac5bdd47ba82799631e10e03c8b10e4d6cf959603533b9232f63eac17241e5ef`  
		Last Modified: Fri, 08 May 2026 20:21:44 GMT  
		Size: 4.5 MB (4485463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5ea6991aa5a5ab68b80e0a06d3098bf98f0513f135c8cac7b01091bfb6d3d29`  
		Last Modified: Fri, 08 May 2026 20:21:44 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json
