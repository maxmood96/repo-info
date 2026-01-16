## `clojure:lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:d29587e4ca9748a05edc389324dc8193b1e61d6ca0b89a456e7e3b3ac8ccae72
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

### `clojure:lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eb55f4ddc6c0e14b4b06f31263429cb2d2de7fef4e18a7de8baf5ff87e458e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142550493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f209a6fcb8f1ab88ffb617e997f02b79daf773b5670ea5f46e55b83dce0dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:37:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:37:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:37:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:37:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:37:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:37:43 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:37:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:37:56 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:37:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:37:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:37:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:37:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f394921db33d440e268f7991e612125ee00292b4b78a798f905c059e4dfe39`  
		Last Modified: Tue, 13 Jan 2026 03:38:32 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1643b5e28db30ecb6b351ff5e203c7a69810e6401134ff5b013a76d641f17e`  
		Last Modified: Tue, 13 Jan 2026 03:38:22 GMT  
		Size: 17.8 MB (17758441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f4e7fb00083fc5414ae529ee9ad8bd50c35977e787a51bc8276b3838a77402`  
		Last Modified: Tue, 13 Jan 2026 03:38:21 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8a1aed3c79a1c5a484cfdabe597922ab6e634ae139c9b1466263b16274df2`  
		Last Modified: Tue, 13 Jan 2026 03:38:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:470b93ed71bbb7752ca626e9d4d4392fe534d9f5688be0d8dbea22e6efd34e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5786425ed70532065a3e0ac26ea73c54413c27691ebf265ecc336add0d306f26`

```dockerfile
```

-	Layers:
	-	`sha256:5536255ca2937c0573d61605d1f66dc332c3f10f35d286caaf47a2deabb40b4c`  
		Last Modified: Tue, 13 Jan 2026 07:35:28 GMT  
		Size: 2.7 MB (2680122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:705253f922b33aa49f65a9924f97bb2698210a98c74b0ce55f82dd4c58ef43c2`  
		Last Modified: Tue, 13 Jan 2026 07:35:29 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:24474f52a19647d0d344900b1ceec3e8fadf40c6208cef232f4e1c79d5e32291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141270664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcfd2f7d25009def118afe5a8a9964b0a736aa1fb350cfd3bf41f79df6b0b49`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:41:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:41:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:41:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:41:17 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:41:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:41:17 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:41:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:41:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:41:30 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:41:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:41:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:41:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:41:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39d2eb48dd0d21cb9e633c7656fd3fd88aad269819ff4604f9f0281cfd87bff`  
		Last Modified: Tue, 13 Jan 2026 03:42:02 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2269f46f02fc4ced64b8c587c63574b5c2e619fba8dfba1bd9908b709ab26b0a`  
		Last Modified: Tue, 13 Jan 2026 03:41:57 GMT  
		Size: 17.6 MB (17592093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e76f4a997fc56bb650d4cd0306c401829c389a0eb53392f43c48d7f27732106`  
		Last Modified: Tue, 13 Jan 2026 03:41:56 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc60bb7a5793fda1c1eef97107552f49e458fa5562b20ed48d12d631a66d8d1b`  
		Last Modified: Tue, 13 Jan 2026 03:41:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6aae8552ac7bd3dfead7e98561fe69651dccdedf569074a54f6b08693de65e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2698961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b261a44738554c7b06e4fcc9490e1465d4f0846a94f4b079cf183e22739d3f26`

```dockerfile
```

-	Layers:
	-	`sha256:4999fa773d04261c6897af31cbc161a6bc8d994c83101544fc82ba765d114d73`  
		Last Modified: Tue, 13 Jan 2026 07:35:33 GMT  
		Size: 2.7 MB (2679758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c287f3e2cc3796ebee39d3a4f6a7ce6726a39f7504a16dde0f196501050b4e9`  
		Last Modified: Tue, 13 Jan 2026 07:35:33 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:22f1ea1f17eb60534061ce8e4750ca958cd544bc2d4c810bbf2230e6cc57fa7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146158337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca980463487194e5fb317734b1f20b7a47c8e85f5945a8c7aa40cdaefed227a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 03:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 14 Jan 2026 03:04:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 14 Jan 2026 03:04:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 03:04:56 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 14 Jan 2026 03:04:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 14 Jan 2026 03:04:57 GMT
WORKDIR /tmp
# Wed, 14 Jan 2026 03:05:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 14 Jan 2026 03:05:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 14 Jan 2026 03:05:49 GMT
ENV LEIN_ROOT=1
# Wed, 14 Jan 2026 03:05:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 14 Jan 2026 03:05:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 14 Jan 2026 03:05:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 14 Jan 2026 03:05:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba039fb3b2b15cba47b5660c224de13e9c3a8dc2e1d3bd3d3b3a8bd6852d6414`  
		Last Modified: Wed, 14 Jan 2026 03:06:52 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5582100ee3f97be61c9cde1d5bdd858cb105935d7fbe31008e121b22ccd31b71`  
		Last Modified: Wed, 14 Jan 2026 03:06:45 GMT  
		Size: 18.0 MB (17960689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c20d80e669a80bd9827182636add430e424e942b3809a4d9cd2c0c0a69e59c`  
		Last Modified: Wed, 14 Jan 2026 03:06:44 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d694e356099cf3aefaba3407d8cf85341fb57fb21be82de1d3eae268d006dc4d`  
		Last Modified: Wed, 14 Jan 2026 03:06:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7754151db6bc7533f4972d1d4ee30ad19a4205d6b07aa05d25762527aa690687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2702379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c305287cd99292fd148936a2ec189ad4f39593f24ed64ed5c46241d2884210`

```dockerfile
```

-	Layers:
	-	`sha256:b1215e9d90793a9d90479f31bed1101fc8770791d2651cde03733a88b0df9288`  
		Last Modified: Wed, 14 Jan 2026 04:34:35 GMT  
		Size: 2.7 MB (2683265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cdcb4661fc455526ce10ef57ec7fd4c6479fb9545bde506a59796d1a38b9c34`  
		Last Modified: Wed, 14 Jan 2026 04:34:36 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9073ce42ea9bbbf6d630d1eb690d4bf5575d94dbc0f6af1d9e183d9874b0e2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137034108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014102fa617e8f49597b024c27e04c911d7fd25afe48ce39d3182d88964b654d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:08:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:08:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:08:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:08:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:08:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:08:22 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:08:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:08:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:08:32 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:08:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:08:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:08:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:08:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fedf639c136731205d5f1e19fbc4ea363b7ab6ef5576a3c1b39562e2fceead5`  
		Last Modified: Tue, 13 Jan 2026 03:09:14 GMT  
		Size: 88.2 MB (88210715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de96067426d5d0a91a17824c2ad8c3bb0b6ed2745d5b5bc331bdf299ad4f0e50`  
		Last Modified: Tue, 13 Jan 2026 03:09:05 GMT  
		Size: 17.4 MB (17420839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaa151df2a46cc9ca62e267ea9d22ad4e0fd6be6aba7cd8037f0ca99ea83a7e`  
		Last Modified: Tue, 13 Jan 2026 03:09:05 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590ef031ac21ec2a0f866e8f0ff335940219c81ee27f23641884453148458a81`  
		Last Modified: Tue, 13 Jan 2026 03:09:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2fe0d08106bc2f2e0f38e2b67879f7b39e8e84ef097286b92d6a2196da742407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313a3a34bf93fd63c5eba573589735a5e37321ffd6fca41fb7254816401b4999`

```dockerfile
```

-	Layers:
	-	`sha256:1bd300ec88b9fd14ebea3013deeca269461e1a375e41165badb1f7a17c26d849`  
		Last Modified: Tue, 13 Jan 2026 04:35:35 GMT  
		Size: 2.7 MB (2674484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c27800049deb148b4685a0da1cb4d4ee14ff6b91cb2fc88a0df27bd70bb4e1e`  
		Last Modified: Tue, 13 Jan 2026 04:35:36 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
