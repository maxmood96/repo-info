## `clojure:temurin-25-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:0939e3055f1718707598a26b09684de699014cd486dcf1c6599b8d4ff8ab6371
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
$ docker pull clojure@sha256:3d3e2faa751b98f747f58e146af2873283a95f0d7b78058027eb4667f553f923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164980285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df372e6e3c7cad3c6198580384268c3996e9d36334d6e8728f0264592eff223`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:53:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:09 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:53:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:53:09 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:53:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:53:23 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:53:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:53:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d2d49f87fd2d57ede492fbe31dc54f4b65d8d16d535d52f100f32b5b44b935`  
		Last Modified: Thu, 30 Apr 2026 23:53:42 GMT  
		Size: 92.6 MB (92574580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039de12b24db47ee2fbabe30b99baa55ff5c240d3c0799b491a9161936ae8b30`  
		Last Modified: Thu, 30 Apr 2026 23:53:40 GMT  
		Size: 18.6 MB (18585464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f310b15765ae0a5d2d5b8d0b6a9f0da6930c899a440ffe817b816dd7f07801a`  
		Last Modified: Thu, 30 Apr 2026 23:53:39 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34426819347effb3f7213df2448700432b4988bd41257fc05b468cf45b0e50f3`  
		Last Modified: Thu, 30 Apr 2026 23:53:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:22f706e5d9a026b7324bdae1681bc9c015e4069cfb22128a445fed4bfad0431d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331a38227ce565ea8fea1984fccbae5f300c8008b5f08aba9cccbaa402755e0a`

```dockerfile
```

-	Layers:
	-	`sha256:af9d6aaf4d881ba283ac0fbcf80d9cd4b68f85766459661416a3407134baa1c3`  
		Last Modified: Thu, 30 Apr 2026 23:53:39 GMT  
		Size: 3.8 MB (3784182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e3e3611453eb0ac58f49826ca1c75a550e443861dd0d9e6e166f6a7c15c044`  
		Last Modified: Thu, 30 Apr 2026 23:53:39 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d27c98bf647b080fd1254b78d41d7f3f35548fca5857cf2600a295d7bc2c4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164275201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a687c8fbd2b5fae11d9d6e6d463818dd4d6c6e09c68e2d841f2f4630795fe1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:52:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:40 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:52:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:52:57 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:52:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:52:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132e0bc6b677117ec7856a743068380bd62e6fb8a5bd51f5702157d8773ca7fb`  
		Last Modified: Thu, 30 Apr 2026 23:53:18 GMT  
		Size: 91.5 MB (91542288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b900be68b4bbc24891d747839eac34c52e48176b9c77276a8f93c070d79b58`  
		Last Modified: Thu, 30 Apr 2026 23:53:17 GMT  
		Size: 18.5 MB (18545497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e4409f842ee6f585a3f5e60a4b91409d440cc71a71296bd9150d618829e23`  
		Last Modified: Thu, 30 Apr 2026 23:53:16 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1f66d8168ed264f89f8e5d743151f9c8b586c8d7ce1d58583b4810297ea2e7`  
		Last Modified: Thu, 30 Apr 2026 23:53:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7846546444b166e7e989d7eb762ca796e17544647d941e817cae985abfff6889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad0d36bb4260d54a8a64de8a37f5fe07e25cfa0560d7e47aa502aef12357e2c`

```dockerfile
```

-	Layers:
	-	`sha256:78c2b9222239081967f57255c1062da1daf9827bd29e41f4e90b8e6f07fd8bdd`  
		Last Modified: Thu, 30 Apr 2026 23:53:16 GMT  
		Size: 3.8 MB (3785080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2de221c0103e35618929a129da9fe5deda201eb997095dbb91ecb0f977d411f`  
		Last Modified: Thu, 30 Apr 2026 23:53:15 GMT  
		Size: 19.1 KB (19123 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d33967d459bd33403068e09006ef8e8a7abaa32f4bbcd5848312bdc4245bcc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168196262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acc4c55281f6e142c6f27b456aa6a0be5877205c7cdcc1854b260d4866d52db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 00:10:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 00:10:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 00:10:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:10:25 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 01 May 2026 00:10:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 01 May 2026 00:10:25 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:11:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 01 May 2026 00:11:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 01 May 2026 00:11:12 GMT
ENV LEIN_ROOT=1
# Fri, 01 May 2026 00:11:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 01 May 2026 00:11:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 00:11:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 00:11:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d590980a89e49f373519dea262c7495fd62a199b44a41ded9f5575c826104460`  
		Last Modified: Fri, 01 May 2026 00:11:56 GMT  
		Size: 91.9 MB (91914031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19bd8a2d8d038262e5646061d6eb559bdbe8a5bb1fd70603157655501c96f1`  
		Last Modified: Fri, 01 May 2026 00:11:54 GMT  
		Size: 18.6 MB (18641074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc2da636f82bd0deace45aacd409f9230e90518009163b54893771b6307ae45`  
		Last Modified: Fri, 01 May 2026 00:11:54 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b83f6349e2e34c9d4cf0c089cff7d4ad663c214f7da63cfb5b7ccd2e1d5b041`  
		Last Modified: Fri, 01 May 2026 00:11:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7cd2e883b20ebc833fad6436b3165f5cfa3ba2bfc4efc9cce3e2f5cf82f03549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3787541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc082dd747b871178b99b502692a06935a64ca79be565daf63c64d844b6a4a50`

```dockerfile
```

-	Layers:
	-	`sha256:d605a2d7bb7f470a1579dadbdb6d113afbdbc7a3e2a6d37a369f9145043e736a`  
		Last Modified: Fri, 01 May 2026 00:11:53 GMT  
		Size: 3.8 MB (3768506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fbf8abcd4eebd248a7cadbeb5df88f5ccbe9f6fbf4166d0d1198d1c8de3816`  
		Last Modified: Fri, 01 May 2026 00:11:53 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:652b07943ca0027030613ef5fca1438e50bb1741d94317b0b07d50b3dff6c6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161869572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6254f2e8d49e0cccd59ac963edd77ae649374fa17e1c3296e6d5c60176fd8907`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 01 May 2026 01:11:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 01:11:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 01:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 01:11:16 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 01 May 2026 01:11:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 01 May 2026 01:11:16 GMT
WORKDIR /tmp
# Fri, 01 May 2026 01:12:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 01 May 2026 01:12:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 01 May 2026 01:12:50 GMT
ENV LEIN_ROOT=1
# Fri, 01 May 2026 01:13:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 01 May 2026 01:13:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 01:13:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 01:13:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af697d12e7ce2f4ea84af1fb9a0a596fbf93eb7670e91abadfbefd74c762bc67`  
		Last Modified: Fri, 01 May 2026 01:16:52 GMT  
		Size: 91.0 MB (91014936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647da42d45465834ca9d726dd6ba8ab7154229324a906125aa4f54ed182068a`  
		Last Modified: Fri, 01 May 2026 01:16:42 GMT  
		Size: 18.5 MB (18538216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea677db7cda1fc11a1df54732e5c0a35b177d6fea9dd5b9fada24b296b0c912`  
		Last Modified: Fri, 01 May 2026 01:16:38 GMT  
		Size: 4.5 MB (4517773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c5993422fd9895d407148ca9d44146ad1138892aa640404299ccf263d81b5e`  
		Last Modified: Fri, 01 May 2026 01:16:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f6e25d1b01cc0e7e93bcb1474083c896239daa5e3049d6b69f98e2c7a413a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b64e4ddcf916f155ad45057af1f2377f1c7a46f30b4e3c74427a952e035f81e`

```dockerfile
```

-	Layers:
	-	`sha256:7ef6ce2ac8ccf2db60d0fa69cba6ed091477d82acf938c822bc39d97d9b90b33`  
		Last Modified: Fri, 01 May 2026 01:16:37 GMT  
		Size: 3.8 MB (3756682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1af6d1abe7c4b12bbe52c6c840923bd739f49c1d412e3329b135def5fb5630a`  
		Last Modified: Fri, 01 May 2026 01:16:35 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4ff9302c74cf47ef07db878ec45ebd2a5ed8fc4751ae127a139aa95ba4a4bfe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160937270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef51d96c60012d2e9ebee2a62642fdb4e99e37799442282b3b9a23a1b4ca898`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:50:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:51 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:50:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:50:51 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:51:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:51:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:51:14 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:51:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:51:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ee46c033b5990060b9acaa5985a11a008290bfbbb27b32d546e2487a9a5e65`  
		Last Modified: Thu, 30 Apr 2026 23:51:37 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036aba4cd2f1bfc6185738b104fac521ee625e68f7a0f033a27d86d71c54b556`  
		Last Modified: Thu, 30 Apr 2026 23:51:43 GMT  
		Size: 18.6 MB (18626693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7969b6187c6556ea2d12b19793fb918d01dbbc2469c584fb909e5e702b4c41e2`  
		Last Modified: Thu, 30 Apr 2026 23:51:42 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4839e5acb38a045fe58a88bfe15a4abca491e2196c9ae20b82652e7ea42e896`  
		Last Modified: Thu, 30 Apr 2026 23:51:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e762b611167ae21a5a6f3b9bd1fc78574bf7866cd664b2cd5a47b35e9da1f69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3c07a13d10bd338bcb7a6bd77252320adfed729b647243bb8efeeea76a733b`

```dockerfile
```

-	Layers:
	-	`sha256:faa5372faa38ac4be8617389c83c50a790d776e2e3f9cbd24da7b441ee5b118a`  
		Last Modified: Thu, 30 Apr 2026 23:51:42 GMT  
		Size: 3.8 MB (3765171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9b9b1ec81d9b125df7204409607260da7bc4aeca300965042a776ca037bc0d9`  
		Last Modified: Thu, 30 Apr 2026 23:51:42 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
