## `clojure:lein-bookworm-slim`

```console
$ docker pull clojure@sha256:f7207ae340bd837baecee1c0725ab6c087b89d68593bf931e0435b90bf18ccd2
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

### `clojure:lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9f6ac13fbf3bb3df2af2a282217517326ff0a30fb27f71292ed10499f216d86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143090458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59579c5864c8909e565da2b12bbbc084d05f3f088937a883f0359eb1e1f36096`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:29 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:20:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:20:29 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:45 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9584490b5d916d34491c3b0757b419a294be78ce12ce6b43b3adff4adc6478d6`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c53a3289a9f76de42ac9396ef9cdc29a813e261b1569ce395448ffbaf34b64a`  
		Last Modified: Thu, 11 Jun 2026 01:21:03 GMT  
		Size: 17.8 MB (17760094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8034f76099544f44ce2f6149cfcae1b4fc96ae1688f991fc0d4e88030bf5955f`  
		Last Modified: Thu, 11 Jun 2026 01:21:02 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1258539728c0e2a94e076d571540842d12f9a9a3d77dee137c2f0b38f439c903`  
		Last Modified: Thu, 11 Jun 2026 01:21:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:583510b70decafcf9d70318c0c7d5f6cf7bb45e58b8e7e26efaf04beb86352dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d36929f24e0e2e6f675c2107772295eb4a3b740654905f77c53d3ba822d0329`

```dockerfile
```

-	Layers:
	-	`sha256:8b34684e02c27f9122e607fcce954997f412be4ed67146321993eab6c6fa9a05`  
		Last Modified: Thu, 11 Jun 2026 01:21:02 GMT  
		Size: 2.7 MB (2698769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9612ee8bb95b0bd2fc012d3a54a6b680b32f4677d53288c914cace0026bae8b0`  
		Last Modified: Thu, 11 Jun 2026 01:21:01 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e02d9a5e7db57508d649f306c6e8c4d07d1def82b88b3cddfaaaf0acd944a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141776793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee2bf656141cd404201e11ded446a71a84b6aeb0774e031930b4dd6cc049899`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:24:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:32 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:24:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:24:32 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:24:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:24:49 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:24:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:24:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d12c52dd26f47dacdbdc531cd76fae08cf3c44e5d971aff305b54b61241243`  
		Last Modified: Thu, 11 Jun 2026 01:25:10 GMT  
		Size: 91.5 MB (91542261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972fe893852bc1c9f90c73e340689fef9990435d7a6620567270a56d47a7d3f9`  
		Last Modified: Thu, 11 Jun 2026 01:25:08 GMT  
		Size: 17.6 MB (17594049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c91b66e56b8e3a8a4b4892f5f288217de205fabf0664dc6710a0e7fda7f563`  
		Last Modified: Thu, 11 Jun 2026 01:25:07 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017dc5680858713e24134f4aba38b962bf10f8b578b05e0f994d0d49aca9bd1e`  
		Last Modified: Thu, 11 Jun 2026 01:25:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc4ac813082b143cbf23aacb22fbb412d46a2a44cedcaad9da219b5713d95d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16aceeb7a770301dbd5d0ed4fc6bbdb3565e9e9749399da5e79190ae87d67da`

```dockerfile
```

-	Layers:
	-	`sha256:51e29ad4a7168e4464dfe22dadef0328cfa0b53fdbb50847b1d742f7440d42fb`  
		Last Modified: Thu, 11 Jun 2026 01:25:08 GMT  
		Size: 2.7 MB (2698405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989b51ba4dca0c2fead07e1ac4d1d64bed375732d66ffbd5fc2d702a6bd8e523`  
		Last Modified: Thu, 11 Jun 2026 01:25:07 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a76b627d02e927c02fd089390007660e45cd275a71efa1a1398ff92e5742df32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146477723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bd5e975fa1d69812c4d2f787442455cbab628c48f5595db739cf50a5e33a2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:44:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:44:03 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:44:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:44:03 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:44:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:44:36 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:44:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:44:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:44:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:44:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982932670843cfc9826334cdcfb7557104e8613cbf39950f8bd63bcb7d5d496f`  
		Last Modified: Thu, 11 Jun 2026 09:45:18 GMT  
		Size: 91.9 MB (91914010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9474762605aa2699a7860c4d5a9f80480be7e05bfb365ed490d9fb9d9d6a5cb6`  
		Last Modified: Thu, 11 Jun 2026 09:45:16 GMT  
		Size: 18.0 MB (17963639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94113bd7839224dc75abf8dfa1345b40e804db45eb73a4dc3041e73d3f6faab`  
		Last Modified: Thu, 11 Jun 2026 09:45:15 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9a6296f80d17d05e4e542d600ccda1a87c6cd1d67ebe81a6726157f79a1850`  
		Last Modified: Thu, 11 Jun 2026 09:45:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:330b0044a45e60e3313708d40e327911ffd271e950390995bb1b5d5ba77dfe0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e8cade5cfaf14e9a128c9c3a6487ea106b12ac9b17b1334217316f7512dfd8`

```dockerfile
```

-	Layers:
	-	`sha256:ecce15466969f2fe5b7df75847333e1391da13417b0fa989437cf74214f8f6b6`  
		Last Modified: Thu, 11 Jun 2026 09:45:15 GMT  
		Size: 2.7 MB (2683926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85d0b3107e78a98d785547967031dc9fb9c23926004ab1ede005a7c11fdcf93`  
		Last Modified: Thu, 11 Jun 2026 09:45:15 GMT  
		Size: 19.3 KB (19268 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2ccdb796605c187ba4b27019c4e59f0e20e1afac3679237e9c1156521f5a6bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137255972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a80e1971c1e812d32920464a007b25881d288af521ca8aa3d5c1b0c8e6eb16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:13:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:13:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:13:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:13:15 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:13:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:13:15 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:13:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:13:26 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:13:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:13:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:13:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:13:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d5d28a9b892aa865b958e34a0eeffbccb54b6231b8f8f42d3512025b674cad`  
		Last Modified: Thu, 11 Jun 2026 03:13:56 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b731af3bfd326f2e1db54b7dc09b00d8d90bf421a4f4a4b2b36da77996f69`  
		Last Modified: Thu, 11 Jun 2026 03:13:53 GMT  
		Size: 17.4 MB (17423964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bc19bae5d3a71441a946a6ffc8cd0d3d0cbeb82f7718a4c3d946fe852eecda`  
		Last Modified: Thu, 11 Jun 2026 03:13:53 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e286ea844b7625c84ebc3852410d084e52cdb8bff4d42e8860684071a0df62b`  
		Last Modified: Thu, 11 Jun 2026 03:13:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:53d3d7bcb4497d2450a9cf57757ee4a34c5b26d9a83f1f47c0aae6c2197a66ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef58daa7900811a7f50f15652c0ea2a2f3555dc916f43ecdea41378301e6a26`

```dockerfile
```

-	Layers:
	-	`sha256:09447b19f5d94bfc40b4a8245924379c3e596d230e25c43f3809366364a40d58`  
		Last Modified: Thu, 11 Jun 2026 03:13:53 GMT  
		Size: 2.7 MB (2675145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ac5b68f8d2983e7578afbecea0f258f7e6fe24628b4701c76a904594ee9c67`  
		Last Modified: Thu, 11 Jun 2026 03:13:53 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json
