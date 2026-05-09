## `clojure:temurin-8-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:d00c11d86951fde3bb448ad2686b8aac47c69670d9ba27c30dd324997cf93ee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dc57268ccfbc3607e6046e2d3a216d399d3adba2cde67c510ecd8fa3b2501f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127982974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6286e392791afe99976d321fb8c332d6d566c9471436b558bfd6bfb2cf0a6040`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:13:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:13:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:13:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:13:26 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:13:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:13:26 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:13:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:13:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:13:40 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:13:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:13:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f888ddcabfc846ce292a7444ce0db14f9c018beeb9a46b6f53b1c414799760df`  
		Last Modified: Fri, 08 May 2026 20:13:55 GMT  
		Size: 55.2 MB (55170061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4228c01108e3d2bf54b5cccabdd03812f6cb7b4661b0af6b6b550ce9c26a4b2`  
		Last Modified: Fri, 08 May 2026 20:13:54 GMT  
		Size: 19.8 MB (19806499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04252c2417764b8ba21a6f37a460906a0606cf822e6db3f324c13d1acc18c4da`  
		Last Modified: Fri, 08 May 2026 20:13:53 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2830b61d4e23976aac1890964e18556c65c98e0ac3019a203ba162849e8dc262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0f169e8b7bae6abb98ca3895ee6b002137d6c746142dd7706e3b5ed52984a0`

```dockerfile
```

-	Layers:
	-	`sha256:31f7acbe2cd5b9e045025b6a0f70c54bb17ddddd5dfaa171f6081de76ae5aa9f`  
		Last Modified: Fri, 08 May 2026 20:13:53 GMT  
		Size: 4.4 MB (4402720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f1ebc071ee0848c2f40ccbe5aed92d9761df4b991b0e0b7e6632324d5b82004`  
		Last Modified: Fri, 08 May 2026 20:13:53 GMT  
		Size: 16.4 KB (16369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:163b9b7d656cf818ebde30191c4784ecd61f8462bb48f0efd3dbbb7df8b58a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126779564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706b11511d84bab6cece29daf40423e4a4b3dc27e9c314a87a6bd65cb196d1df`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:18:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:02 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:18:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:18:02 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:18:15 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba84624ef38066c593457da764bf197bbdaaba9e502a5a4e6fc4d9bb83edb7a0`  
		Last Modified: Fri, 08 May 2026 20:18:31 GMT  
		Size: 54.3 MB (54251617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a27adca459abd57154587fe3bc3f30ddd4057866fcfeb6189bf9adb71c1102`  
		Last Modified: Fri, 08 May 2026 20:18:30 GMT  
		Size: 19.6 MB (19637020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1c2cab167709f2e676572906f5db65ed69c95c8e4230a5e90379b078c80316`  
		Last Modified: Fri, 08 May 2026 20:18:29 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:960b976b9290c568e8402ce470c68f3fc24772e33ed904d703bc910fd174881a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff06bbf34af770a6361a22306d7d21eb321413898f479f5cfd4ac5f2db39663d`

```dockerfile
```

-	Layers:
	-	`sha256:466563c1b540e20b646f10b698b7449ff74e2e4df379329b44a0f297de5d3ec5`  
		Last Modified: Fri, 08 May 2026 20:18:29 GMT  
		Size: 4.4 MB (4403035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9cf11087c5bc03256cd245029bce1da161c6d5b6f56ac5f837d45d15dc4ca9b`  
		Last Modified: Fri, 08 May 2026 20:18:28 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:bb0256d40144230052159f6c75ec579b661f552a80b9fd24dbb1a450378d341b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129535437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9d0320a846757606faec59e6df0553e69b941348b5142c2078568b7b2154b7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:13:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:13:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:13:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:13:14 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 08:13:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 08:13:15 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:13:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 08:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 08:13:51 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 08:13:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 08:13:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d0ad1b604097f835cf3ae8697f2202d5324bd2127f91a122d7bb0676b31fcc`  
		Last Modified: Wed, 22 Apr 2026 08:14:28 GMT  
		Size: 52.7 MB (52650391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69b7e04c2d1d980dca1614a1671fb165a339020b3bb7fdce97d5e458737b170`  
		Last Modified: Wed, 22 Apr 2026 08:14:27 GMT  
		Size: 20.0 MB (20030511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad387dac5c365c94b5c26d4de288ba219d898c7f7aeed718dd4851f561957477`  
		Last Modified: Wed, 22 Apr 2026 08:14:25 GMT  
		Size: 4.5 MB (4517768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:af920dd7b6afb88a5393e0fa200eb7ddf1ca8d77a59ea3f6754396771d50ddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4421590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30cfc04e135e895a893827a6252194e2ed155e3509aec6c99ef0c36ec0810124`

```dockerfile
```

-	Layers:
	-	`sha256:a108fc07072a09744dcadb95062e5b565288fb5ba572404d78809321cb698437`  
		Last Modified: Wed, 22 Apr 2026 08:14:25 GMT  
		Size: 4.4 MB (4405176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a78e685905c4ffd38745348b83291bc5088fa61182664eadadb36547304118c5`  
		Last Modified: Wed, 22 Apr 2026 08:14:25 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
