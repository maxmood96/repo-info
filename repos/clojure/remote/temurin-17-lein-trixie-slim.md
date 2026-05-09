## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:a87392dfc40975448e1be88379bf6f6074c76e51328be69b2b06a396cca26ff4
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

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:62e581f30d35c2c48ffe25e0c6a1e9b6ad2ca8fb121e15bcaee59b3c534e66fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196651865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e7289dd5c0fe3ad363aa2a9976d27b27c45ecdbbdbfc3bd09095710459945e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:17:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:02 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:17:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:17:02 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:17:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:17:19 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:17:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:17:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:17:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:17:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139ece3b7980d31ce0838e31c65853e36802cbd8af108b3ee9181768ead6cfe7`  
		Last Modified: Fri, 08 May 2026 20:17:39 GMT  
		Size: 145.9 MB (145905473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91441065ed181a7bbacdb28b5ac41c9ffb71947cc552fb80bb833bfde661d8d`  
		Last Modified: Fri, 08 May 2026 20:17:36 GMT  
		Size: 16.4 MB (16448019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a5c7aad12a0b1c8c6864baf2afe0c7618ad21c3c83d68a7365a4ce5f49c7e`  
		Last Modified: Fri, 08 May 2026 20:17:36 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba51219bc5e13334a570743ef89d3da739775c297f29a5ba9bb04f27e612e398`  
		Last Modified: Fri, 08 May 2026 20:17:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc512d1caf2d654595354b3e7a0ec2688c869fe0bff1b6a5f5e00a02ec2f2c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110775df1c29a09c71b26b71edae76eb1c039b86274bf41ebd57e36ba2a723fb`

```dockerfile
```

-	Layers:
	-	`sha256:d62eb7e4687e5511859ce69c705dfc2878ddfc92b73a3c356d0ddef4eb32855a`  
		Last Modified: Fri, 08 May 2026 20:17:35 GMT  
		Size: 2.4 MB (2365415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6a3e4d0cf8286a77b3d3a961d4d7b98a7922e68bf6fee343e57a6a0946ab34c`  
		Last Modified: Fri, 08 May 2026 20:17:35 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9fdd8f58c1ccc7e294183b8fd2f2de4bd7adf10325adad85dc6e2ba94a35a14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195800051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17312ee70ffbbf8566d7c757087797ef6a33ccf6a6219c6abc2b848f65fbd17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:16 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:21:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:21:16 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:21:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:21:32 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:21:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:21:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304d7d18bca0b80fac43cafc6f88c8951c109808d6ab2c71d9e40627996f3e79`  
		Last Modified: Fri, 08 May 2026 20:21:54 GMT  
		Size: 144.7 MB (144724307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dde6966a5a4f500fada8e8473a86d6b9f6e49b2bb613d9b88da8d92b8c6946`  
		Last Modified: Fri, 08 May 2026 20:21:49 GMT  
		Size: 16.4 MB (16413966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79b2c693b6a45f1e66274e8795d819e9fcfed185552e4f7a0b6ef41e42cce22`  
		Last Modified: Fri, 08 May 2026 20:21:49 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c55445a46e264e271ac8da253c788050858ff0870bc812597df381e49550183`  
		Last Modified: Fri, 08 May 2026 20:21:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0859385307453680941a5001180452a57f779cfef07cb0ba6682d838bc300863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354ad769411ac60037b9bb540cb76d410753855f16c7b99038edbde24f2a764c`

```dockerfile
```

-	Layers:
	-	`sha256:beaf376631303391f6be25552954e8a561d9927e6947f67764f890ca825ef974`  
		Last Modified: Fri, 08 May 2026 20:21:49 GMT  
		Size: 2.4 MB (2365033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef147aa1e557236bd3cc4b4d1d033d98bfe14a8af01ef083958d533677f16534`  
		Last Modified: Fri, 08 May 2026 20:21:48 GMT  
		Size: 18.7 KB (18662 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:eb5a5de98171d6e73ba77c09d48a161e1bab5acd4dab70693f99f0cc72ef64ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200367811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a6eeceddfcf682a6b636d9331a3175c63c7dbc3243dc513adea4730ebe0137`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:32:03 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:32:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:32:03 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:32:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:32:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:32:32 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:32:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:32:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:32:35 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:32:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72cabc9601635085bc11fa48d74114d9e1765a07685bad636cd3a7da9370ac`  
		Last Modified: Sat, 09 May 2026 02:33:09 GMT  
		Size: 145.8 MB (145766215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d4e01966977f286a183e524fb5e6e1f4d586e4408a4099e71ec090fa83e6c`  
		Last Modified: Sat, 09 May 2026 02:33:07 GMT  
		Size: 16.5 MB (16485353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c752a269480c7303def8c34741e3cda5808df134dcdc6c9388e9c0573ef3b6`  
		Last Modified: Sat, 09 May 2026 02:33:06 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a0b1cf8be33c7a571d9c10c66bb16981553ec5fa8da3d5ecde8d4014ee07ef`  
		Last Modified: Sat, 09 May 2026 02:33:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a13b199cf8cbfd0641f738f2eb309178c2a161484fcdb7d154c6b012b00424c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb251010752ecc073051ba9261c96697777debfac833e7025ae61331e897b9b2`

```dockerfile
```

-	Layers:
	-	`sha256:5cf3e0d3701476acdbde769c3218e588dcfa7b0ca3573d233cb59b8e97df7411`  
		Last Modified: Sat, 09 May 2026 02:33:05 GMT  
		Size: 2.4 MB (2366395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856994a51c2c30515b5108fd4b1f34d4e9e5555d88b033132fd255b8d877dc0c`  
		Last Modified: Sat, 09 May 2026 02:33:05 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:f061e3a46c2867c60e62b9aceeed551d5b6f7d4f0dd9cb5a6d18bb8e85926280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191859448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977485e2efb1353503f3ac6180bbe46d961c9250c1f4b1ca693336b52d3e1a40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:48:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 17:48:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 17:48:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 17:48:07 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 24 Apr 2026 17:48:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Apr 2026 17:48:08 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 17:49:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 24 Apr 2026 17:49:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Apr 2026 17:49:43 GMT
ENV LEIN_ROOT=1
# Fri, 24 Apr 2026 17:49:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 24 Apr 2026 17:49:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 17:49:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 17:49:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839a829e8fec6662efa3cab7ad2470690879a00890c2cd0f31b7ec868d89805f`  
		Last Modified: Fri, 24 Apr 2026 17:53:53 GMT  
		Size: 142.7 MB (142662943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a63cb7f24431be7843c560553bfc41fd321192fa7ace6c612a765eaf4478edc`  
		Last Modified: Fri, 24 Apr 2026 17:53:35 GMT  
		Size: 16.4 MB (16398086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5393fbb19d4380082fdf0f934a236944b80689cb977467b59f0afda874f740a`  
		Last Modified: Fri, 24 Apr 2026 17:53:32 GMT  
		Size: 4.5 MB (4517794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4452329a97615c454a49f949ef3448a69bcd310d8a5e5724505f027657a99d23`  
		Last Modified: Fri, 24 Apr 2026 17:53:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ecc0bc4f738d47dd14b25a2fa0d3a7e2d3e03687a1b834ad422cd27691de715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483d06150b11a8737b614cade529c32d54a0e5af48f342b31f35fd53a01237eb`

```dockerfile
```

-	Layers:
	-	`sha256:12b7cb006b8da21e6dccde98de8a8feb86e4d42c10bfcf97f7bebf4f442248d0`  
		Last Modified: Fri, 24 Apr 2026 17:53:31 GMT  
		Size: 2.4 MB (2354917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc82aa0e0053ea9bc25c2e23df8e1085aa5b49f5b20ab9d265709775b1bfd2e`  
		Last Modified: Fri, 24 Apr 2026 17:53:29 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d93ffbf0df47ba5dbcd0ea795c8f28c9ac284dc59fed6c79a23f27ec07c29bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186752823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfd60906407a3e0bd97f3ec50d40a40afe1ebb37a00086e6c299533005fc4c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:15:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:15:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:15:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:15:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:15:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:15:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:15:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:15:56 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:15:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:15:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:15:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:15:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512e6532304b09c89615bfcfc7e7795be56d90f51435c3bb6a021ae95aeb07f6`  
		Last Modified: Fri, 08 May 2026 22:16:23 GMT  
		Size: 135.9 MB (135910435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6bc46b2d13ece840025aba291a724fd74f409dd4ec5eeb96a0623eb4ca094`  
		Last Modified: Fri, 08 May 2026 22:16:21 GMT  
		Size: 16.5 MB (16483876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e399a7f77ec18fd4d445e7718bba6bd3bda4a22ffaffccc7bf73ff9e496b6b`  
		Last Modified: Fri, 08 May 2026 22:16:20 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7868bc01d2492183a3949558bfb6580ed8e966e0346bf3e545a7c43a54313ade`  
		Last Modified: Fri, 08 May 2026 22:16:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2742453616cb76ae7ed28103c56eef0715597900b0579df4ccb7dbfdb9e2a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9ddf8f8de6e72aefda6118b55e93c5df65e7805d2b8f29c59d72ba15ab6507`

```dockerfile
```

-	Layers:
	-	`sha256:3407379e1f83f77df6e16b62d69e3db78b7ed8bf02f3ee217beb5d3a76e58a92`  
		Last Modified: Fri, 08 May 2026 22:16:20 GMT  
		Size: 2.4 MB (2361842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25240c354f53261c9181bf7f9f933b64858deaf60c0da1f9467273ae1d542ddf`  
		Last Modified: Fri, 08 May 2026 22:16:20 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json
