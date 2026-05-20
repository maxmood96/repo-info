## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:c68093b23e9d285ec0301f0993458f2bd4c80b5bd2f4014eb67ec4532b406d09
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

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:88bbd958e275a769395c152c0346e151c5ed1bd304d85ab24415d0cddb360950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208678870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9517607bf452fa1a0afec2b26d38ca422f8893fa0ff56e1647860d26819388f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:59:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:59:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:59:21 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:59:34 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:59:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:59:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0fcdb49b8e254272da9537b745d5fef38839244b0a68ba42b4b939bc50846`  
		Last Modified: Tue, 19 May 2026 23:59:56 GMT  
		Size: 158.2 MB (158166905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc390b8f8446aea8ef5b75580e02918e98c925873f1de43904dab69b2dcc4df`  
		Last Modified: Tue, 19 May 2026 23:59:53 GMT  
		Size: 17.8 MB (17760252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc0144dcaa8f758583b1eafcfb6eaec9a8a756a7cac1d79c6d0e5f5b869a87`  
		Last Modified: Tue, 19 May 2026 23:59:52 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39951513752286b7466ce6b1bd9311f7c5a6c7eb75a6f76c74f65919cd76d474`  
		Last Modified: Tue, 19 May 2026 23:59:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6096bf4ac608203c239f85c388e495ff7c37beb5e52c14e5323e06ddbe62f552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4a1d10dea657c4b46f8680e7de494fe3a9816ce01036da4ccdb04710dcd70f`

```dockerfile
```

-	Layers:
	-	`sha256:806f4ff1a04b0c8b93e09df0d6ad723a87417d907944476abd30931501591dfc`  
		Last Modified: Tue, 19 May 2026 23:59:52 GMT  
		Size: 2.7 MB (2732547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c7e53daf49b789f20446098dc5685e60c7853c39cfbcf6ee6963ccfdbf8c88`  
		Last Modified: Tue, 19 May 2026 23:59:52 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:665f9ef575633466144dcac383ba348123861acaf010529c56ff2de0e8fa5dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206688354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae99842aadfa8b216262e6f9108abc03235d5c3d4f8dff7d34f4df7f022ef003`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:06:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:24 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:06:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:06:24 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:06:39 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:06:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:06:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb5d28b6b51460a4141c63a81487cf3a86bc74895d1999dcd6483deadf2b8b7`  
		Last Modified: Wed, 20 May 2026 00:07:03 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a3deb41ae88998f6876568ebcfb47f77768a8ba38c3db3534d11ec9cfe5a32`  
		Last Modified: Wed, 20 May 2026 00:07:00 GMT  
		Size: 17.6 MB (17593807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ff55c1f369a0a756856b609447a81936a6eb32a0d64260a35b14b5f231ff1`  
		Last Modified: Wed, 20 May 2026 00:06:59 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c4a206631a4b160c60a205ab7a8733f6d775bfc6386f4468c71aa11861015d`  
		Last Modified: Wed, 20 May 2026 00:06:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c86f04329ac4642e2a733120f881913275c4d01acd02a0004952ea86d8c5ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc00446035c63fa093aa84a47e63a9b6139f435b9a6f9b652708107d81c14954`

```dockerfile
```

-	Layers:
	-	`sha256:bee193c034f8966e362d71b001df3c7de325792c97e54e7ef71a462bbe4dd716`  
		Last Modified: Wed, 20 May 2026 00:06:59 GMT  
		Size: 2.7 MB (2732162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96ea11eb47c3cab582e024b717651995f48961e54ac7a84588d3cc13ace68e53`  
		Last Modified: Wed, 20 May 2026 00:06:59 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b6d61f1c79b91d4f01a7dd6521bf66b81c712a36a0448ab5f3749b75efd8ccf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212900520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b772bdfcb222f1d5841452b28195a795323e517018e906f3f43a4a468128e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:00:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:00:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:00:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:00:42 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:00:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:00:43 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:01:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:01:11 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:01:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:01:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:01:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:01:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d008dd95981b1b59ab835b2a9f56525cb5f9f85252c9b44387bde9e179bb164b`  
		Last Modified: Wed, 20 May 2026 06:02:07 GMT  
		Size: 158.3 MB (158343249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e8707e029fa96bd9cb81953790ae1450a4c844285d18eca3309c33dbea1882`  
		Last Modified: Wed, 20 May 2026 06:02:02 GMT  
		Size: 18.0 MB (17963356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d0e5bb3f1d689aa2b13f7a2bd327ab15368cc1ec9ec5bdb55228cffc4e8dc0`  
		Last Modified: Wed, 20 May 2026 06:02:02 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e54e535c9e6c8c8ff99952f9e6c24875a71e12ae2b39f4b6952dbd1d0ccfc6b`  
		Last Modified: Wed, 20 May 2026 06:02:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd70a1699c1768687b3a1c714ed00bde9d6bf6baecbfd31adbade1371fd78c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc6d9a0c5ea48984c56a5780915815f3f2446cf128ef2218e73d6f80f24d970`

```dockerfile
```

-	Layers:
	-	`sha256:69468eb62817897fd7ff2244fb9c63ce7d5633d0413af98d1a5b7e8588a6dff4`  
		Last Modified: Wed, 20 May 2026 06:02:02 GMT  
		Size: 2.7 MB (2734380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3e00834467773cf4ebd8bd8f9862e21978c744d2ea24e113cac69c35eccb2c3`  
		Last Modified: Wed, 20 May 2026 06:02:01 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ec1a8470db6af06fb75b62e704704500a7c9d24b083d89ebad38460d960ddbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196218735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a7b05669f8572824934355d8e35664b0e10b5c3bcda9640335fbf625e371e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:45:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:45:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:45:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:45:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:45:30 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:45:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:45:42 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:45:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:45:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:45:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:45:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f59c7ebea2b6007773062b922180dc57776e79bbece633a441c340904337864`  
		Last Modified: Wed, 20 May 2026 01:46:11 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac84abccfa13d0f249b3cb8a705b5b8fd65b46150c958c4b7ead2c4d4055d10a`  
		Last Modified: Wed, 20 May 2026 01:46:09 GMT  
		Size: 17.4 MB (17423664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6d3c6d7c9b7051a8dc73b74d01393fd92e09c2539bd388c31b4601e10af132`  
		Last Modified: Wed, 20 May 2026 01:46:08 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dd698582c09bf2cfeb9fca053be03047a3bde959e620d54f4a92d4c8f5a0e9`  
		Last Modified: Wed, 20 May 2026 01:46:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1af45aab322a0dddc796e3b6a7f22a49c721db990666a6ed3896f7eb1b84509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a34acbbad2c0b06539cc196023077939a3ea1bb2cfd311757e29538516a47b8`

```dockerfile
```

-	Layers:
	-	`sha256:f18d7a0520e9501a9e99fbd6f781d53217fb68155835dcd8fafbb85553ea123d`  
		Last Modified: Wed, 20 May 2026 01:46:08 GMT  
		Size: 2.7 MB (2724361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1096b28733030dbc9907b9120f87db812707099b965f90d5ba205164337b4fe9`  
		Last Modified: Wed, 20 May 2026 01:46:08 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json
