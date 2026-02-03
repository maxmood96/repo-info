## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:1a1806a33524b82502b991f2e4bf5943a4527847778bddc9765cd41957590f80
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

### `clojure:temurin-11-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b008bbaa7bace4411b47befec61022ea43dd8c22247eb8cdf61408b4ca8032c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195710158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62522f0ea5e49e99fdf6dfdc82474c4276a8dd49d678ab0cbb84885cae7afaed`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:19:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:19:30 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:19:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:19:46 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:19:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:19:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5d1dce3af5b6c3b6837270ebb3661d982e03006182c46503983456f7fd0e83`  
		Last Modified: Tue, 03 Feb 2026 03:20:06 GMT  
		Size: 145.0 MB (144966653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bec8e46b53433a14a27fce01c47ff3c3f0a7d671d674ba3f8cda71c13a079cc`  
		Last Modified: Tue, 03 Feb 2026 03:20:03 GMT  
		Size: 16.4 MB (16447163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de34eef88aaabfe81e0ec33764b07ed9b178bf9fa14385dea64730b011102d48`  
		Last Modified: Tue, 03 Feb 2026 03:20:03 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:735df4dc2cfd4e237178b6d22b1529e1b12c9328a6ad5bebe3ccbbbe0b3c0280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66549dd75e9850a4200502be57a6094a95df4dcca29c22dd2733a929e04415e`

```dockerfile
```

-	Layers:
	-	`sha256:dbb3197f9faa5a8decc12db91242f247f68de3ef41486e95c09f52f1eb375fe9`  
		Last Modified: Tue, 03 Feb 2026 03:20:03 GMT  
		Size: 2.4 MB (2383639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897bcc0bdf42fca039755a2da6a132485c38a3366b94823b367da71b03dbf84a`  
		Last Modified: Tue, 03 Feb 2026 03:20:03 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2d551518bf4e3dbab6fe85f7f4ada2de9acdb97682d9f696d74929cb318e5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192801373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6543f369c168cf555369fda5dc124699c80f99bab141359456bf310aaddd0fbc`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:21:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:21:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:21:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:21:59 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:22:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:22:16 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:22:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:22:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41cc8ebca434933b9c3b36a42ac84f992637439a8d759cd52a5e1f0d3d01f04`  
		Last Modified: Tue, 03 Feb 2026 03:22:38 GMT  
		Size: 141.7 MB (141729962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6b6f29c100f6fe5b98e4f94dc72d096a1234cbcca9e5b88db3c82e7614122b`  
		Last Modified: Tue, 03 Feb 2026 03:22:35 GMT  
		Size: 16.4 MB (16413604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5ece7ca0787981b9e15d12a1bb6b9682bd91dacfa7557d8aca37427ff3d552`  
		Last Modified: Tue, 03 Feb 2026 03:22:34 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7885352969fda7d790db6e2776ab98c7f286ff85c0a175e0108a8028d01e8eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8544cb03a582bd6b62f7f9ddcf5a94c6082bc9622e9b357c57a4254188c7d74e`

```dockerfile
```

-	Layers:
	-	`sha256:d0149d5b457e660a7e801b906f81a61561975a70e18c6bd6e0ec1b56df089585`  
		Last Modified: Tue, 03 Feb 2026 03:22:34 GMT  
		Size: 2.4 MB (2383875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4c00f70343393f5b8af0e7627688a3707e11c334624e19f5b97f5db1b0bb1f`  
		Last Modified: Tue, 03 Feb 2026 03:22:33 GMT  
		Size: 16.5 KB (16515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d58ea2f7b3a98f75044a1b26ae5fae246a7fd466a7c4300c4877ee58a2216845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186682490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdf97bdba0a3d73e8cfeb5d376d0cd05b73c78ca493dfd8b012b1c678697110`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:36:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:36:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:36:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:36:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:36:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:36:18 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:36:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:36:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:36:51 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:36:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:36:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b081e339f0b29c3868bc8c87fc56b395e364e87c2647c6a28fe757aa94dc76`  
		Last Modified: Tue, 03 Feb 2026 09:37:31 GMT  
		Size: 132.1 MB (132079786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6e7ea4da74d009e88f4518eb359e45aca1b493933427358c87b4a9463ff6b5`  
		Last Modified: Tue, 03 Feb 2026 09:37:28 GMT  
		Size: 16.5 MB (16484771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53228f15d85de25993be9f727021fdfcabc34eefaaec55430a5423d0fdf40bd`  
		Last Modified: Tue, 03 Feb 2026 09:37:28 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8097497a8ccb98ab9147b0bd0cdfe8c44bfaa49aebecc70d31ec3d2779686c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee85ca2072ce21884baad5a494bd303c6c581389fe412f48be7c410c0fb8e622`

```dockerfile
```

-	Layers:
	-	`sha256:a08f83bd61f6edef924445d996eb09ed2b2424d524d09759d17d7d389eb29a40`  
		Last Modified: Tue, 03 Feb 2026 09:37:27 GMT  
		Size: 2.4 MB (2384004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9870270d3ef2b9b3c5a522512851030b59b8ee174b5cdb21c4f63a800bf7be58`  
		Last Modified: Tue, 03 Feb 2026 09:37:27 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:377aba7d0fcef1865e3fcd4d34afb19991901f7abfb5c204250741579977af05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.5 MB (176534109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454daf9703982b55c9661d3d24251637cf4cdd52b0a38c12325cb60fbcceb11d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:00:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:00:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:00:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:00:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:00:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:00:42 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:00:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:00:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:00:55 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:00:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:00:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0e2d81bbd15ea30a3436c15b21bba5e4613dfa7471a0f7f15d836cbe0aecbc`  
		Last Modified: Tue, 03 Feb 2026 05:01:21 GMT  
		Size: 125.7 MB (125694848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbbf20edf505b5c9159685b113acf047c092d4725339c1571306d699b83088f`  
		Last Modified: Tue, 03 Feb 2026 05:01:19 GMT  
		Size: 16.5 MB (16483388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe293b23464ecd819d591e4444f86c0deee71a3d107552abb638e102e7a6659`  
		Last Modified: Tue, 03 Feb 2026 05:01:19 GMT  
		Size: 4.5 MB (4517692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5815476dfac25d1ce361b6d755e298b66997350b78f9007ce7eadeda76e0834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2396464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355135c592d540cbb1d41ebd0cf65e6223a070181907b0c4e669464b1bdda2eb`

```dockerfile
```

-	Layers:
	-	`sha256:71dad7508c44d114cf6b61eee40fda1ae08cc80380f50808db374e07cfdd244d`  
		Last Modified: Tue, 03 Feb 2026 05:01:19 GMT  
		Size: 2.4 MB (2380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ddf2740e1500c643be0c12c78d86417ded3c8c5133313fda51c5b3d367b349`  
		Last Modified: Tue, 03 Feb 2026 05:01:19 GMT  
		Size: 16.4 KB (16394 bytes)  
		MIME: application/vnd.in-toto+json
