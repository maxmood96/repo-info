## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:83d3fa6aa3baf01f8ba08f424078de5a713bab2146af914d7eb4afeee57c8a9c
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c17fa375f5bf6271ebceca8b44299be969a274749d01f5cbae25457f511923ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208600971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ca7e2392f61b9710bf2090b726ae733d7fec80b47e0fb98f4a1872c5e132fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:05:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:46 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:05:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:05:46 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:06:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:06:02 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:06:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:06:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd08e183a7d2fb938193b98730932a08bab17a792b0402497bff782aa94d610`  
		Last Modified: Thu, 05 Feb 2026 23:06:23 GMT  
		Size: 157.9 MB (157857046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adcfe37a5ccdce13cda9391bac011d75a50d65f21e8beee549ab329cb7c2b7d`  
		Last Modified: Thu, 05 Feb 2026 23:06:20 GMT  
		Size: 16.4 MB (16447153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7167ce819d45964bdc87b67497052c90f83563bc3afa324cf2b37ed7831d4b7c`  
		Last Modified: Thu, 05 Feb 2026 23:06:20 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb769e3c2972fbacefb2a1230298b2dfb198e11b1d24908b6e74b59ed06f2b17`  
		Last Modified: Thu, 05 Feb 2026 23:06:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c15a4019c09353b9b87ff0739b7646246e946a4b23d40b566d4323cabc24ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cb7941a5b0fe0c05a9ffbef886ce34c2fac08872e98be013ca42c2e494813a`

```dockerfile
```

-	Layers:
	-	`sha256:9ecd8c56c47f5b8f1b5e53d361dd3da99881adb56c223ce1311262fc00ce837b`  
		Last Modified: Thu, 05 Feb 2026 23:06:20 GMT  
		Size: 2.4 MB (2366604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3bd6b817d1beeafd0b734dd20fd6d697f3efe5ea6849e764e4f0e3696c4146`  
		Last Modified: Thu, 05 Feb 2026 23:06:20 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3218319bf46dc1a08629fd34cfb66f97e4f3b44126b4f280dca9c05c06dd6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.2 MB (207204839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0d6e4b2e42b3b16bb8de1741ede6503bd8015b6b5e2dafaa9121bb92ba603e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:52:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:52:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:52:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:52:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:52:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:52:18 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:52:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:52:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:52:39 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:52:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:52:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:52:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:52:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911ea0f5728871c5dd3536a37eb64005a8c1ff2eff8f07102b4f84210f7f9281`  
		Last Modified: Fri, 06 Feb 2026 00:53:03 GMT  
		Size: 156.1 MB (156133048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ddfbcdfdafea9a9a0804035032f7af4aa728a2383db4abffe92316f24d867a`  
		Last Modified: Fri, 06 Feb 2026 00:53:00 GMT  
		Size: 16.4 MB (16413559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebf37fa9bf85a31ef74847daef2d16d06550aca600dd0aed0e82f018684b82a`  
		Last Modified: Fri, 06 Feb 2026 00:52:59 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84123a939e4f43211ab2ada78e3b767fe41b88bfc688f9813929849e20c6e43`  
		Last Modified: Fri, 06 Feb 2026 00:52:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f1c27e141878c5819558c892366397648d10f704ce7d9d09210550d72cc153af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99111d422df7d2a2b36c0c846600939af16dfaf683dfed0e738aa52d53b876b8`

```dockerfile
```

-	Layers:
	-	`sha256:00a6b88a8463520a8d567373562819fe99ceeff0cce1df88646dd8101b9de667`  
		Last Modified: Fri, 06 Feb 2026 00:52:59 GMT  
		Size: 2.4 MB (2366222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bed33d40c4557c3daeabae553fafe0dcd3d275da6d812980b9207e6af65b70c`  
		Last Modified: Fri, 06 Feb 2026 00:52:59 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6a098492bf9e47e906022c27f621e849d93b89fb123c8a87dd64791ce564e255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212580804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3923759fb16359eff6899a2c7089cd376f24b214f46e4582fcf9bcba130cb3c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:37:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:37:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:37:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:37:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:37:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:37:56 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:38:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:38:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:38:52 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:38:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:38:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:38:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:38:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d803d46010c6f6fae7ea82f881a836bc9d2bf4afad631cfb7ffd52616e4eec`  
		Last Modified: Fri, 06 Feb 2026 00:39:44 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac57f01c5b92fad24b39c36f9e6375f1fd3713ca19c23f5c2ef5eac1d73a501`  
		Last Modified: Fri, 06 Feb 2026 00:39:40 GMT  
		Size: 16.5 MB (16484945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e409008fd3b109f379b391ba22cc3f20a6c64f4b9e43e4b3a02877937109969f`  
		Last Modified: Fri, 06 Feb 2026 00:39:40 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cff37a16b7901e326316ec37f7901195f754605954dbaa47e9a1191600cbce`  
		Last Modified: Fri, 06 Feb 2026 00:39:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5207b1f2042f3616e4a73fa15dfc4d1f44cae6d3b7777ac34923d19dc949df36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64bd7f838493cd0c558a4386ee13aa5e3a6a9e779c543f37106609db5071a1c`

```dockerfile
```

-	Layers:
	-	`sha256:adf84ac6aab0a88cc7fe7d6a4c6eed37d6560f5ee69ba9ce22e66aced215e254`  
		Last Modified: Fri, 06 Feb 2026 00:39:39 GMT  
		Size: 2.4 MB (2367584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d569012a5f1d2a7ab440db89aae2080d4d28c96121e427c9dc95139504663f4`  
		Last Modified: Fri, 06 Feb 2026 00:39:39 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6e7e983ba9d919f4981598c3cfeb5d815d26ebfec62124dfd2d044ddd957ba0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206386856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17da8088b109f4e238361e68f4ff3b335a216b8fbe0eafc2dc62a88121e83853`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:50:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:50:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:50:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:50:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 20:50:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 20:50:06 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:52:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 20:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 20:52:20 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 20:52:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 20:52:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 20:52:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 20:52:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080871d584089d7c07fc75a8f84b6f61cae2c9a7204a550f8b8dcad13b49c423`  
		Last Modified: Thu, 05 Feb 2026 20:56:46 GMT  
		Size: 157.2 MB (157194292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97e6f78beb50f120a1db4fe214aca9f727ccdf9498d4adadaf8faba3728dbc`  
		Last Modified: Thu, 05 Feb 2026 20:56:26 GMT  
		Size: 16.4 MB (16397963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe26a13fb2c3e8fb7d5412ed6eef1c695c8dacb51475105e7d529528d3e28093`  
		Last Modified: Thu, 05 Feb 2026 20:56:23 GMT  
		Size: 4.5 MB (4517782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233192a5272aa44d07fc64a8e3dce7cc616724e5f5e319a2c0a5f66bc607c5d8`  
		Last Modified: Thu, 05 Feb 2026 20:56:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ca769090d0bf621a8ba604fb46f269788fab6aa6ad8dae1b8557ab653c97a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592ec89fb3caf359f8dadf828c7f441c258805bbd4979f428084afe55f6e851f`

```dockerfile
```

-	Layers:
	-	`sha256:63a83bf9d858b8ecc7a600f1383bd1e7a73601eb6dca6f046cf7bfe90c661414`  
		Last Modified: Thu, 05 Feb 2026 20:56:22 GMT  
		Size: 2.4 MB (2358650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e799f640f3b4a2e2fb51db95950a0678fa8a5743aca52ebf464e3dfa724e11`  
		Last Modified: Thu, 05 Feb 2026 20:56:20 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1f3ef9b002638308a8608fa3bbc83f838824d3f2f41428261458ea0d6acd623e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.9 MB (197944989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b247ee19265e5729e56e7cfd9c5dd16b7a36d98c1f87b52e899a8e08ca57bb0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:06:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:19 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:06:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:06:19 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:06:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:06:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:06:33 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:06:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:06:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:06:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:06:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769ffe98f1f85deeca0741693ed0eb059952a75303a3abdd0b790d146eddd060`  
		Last Modified: Thu, 05 Feb 2026 23:07:03 GMT  
		Size: 147.1 MB (147105305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7bd4e4544ce0e5a1a500b7b9b6140ae3292a0d8cb22f5665c44cb5498776`  
		Last Modified: Thu, 05 Feb 2026 23:07:00 GMT  
		Size: 16.5 MB (16483399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd9378c09451da27c2b8b94b4ed5d95e54fae1643bddd844b981721dda02675`  
		Last Modified: Thu, 05 Feb 2026 23:07:00 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa67daf191a102e054fdff463346c432ce5bac88117059dba89831783b0477`  
		Last Modified: Thu, 05 Feb 2026 23:07:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:185886cf42584c60a0de96182c880a8a4e996a0795ef11714899f0f116551422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3556d9306bf14060068d85867da1d3ca0cd124fd882df46ff501c8d96b05dc`

```dockerfile
```

-	Layers:
	-	`sha256:99df85e5167920602ca77923a4a5683712c06b90a0ab8ffcedbd1d717d42dc97`  
		Last Modified: Thu, 05 Feb 2026 23:07:00 GMT  
		Size: 2.4 MB (2363031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff74c65709b3721fe1d0b4131372236babefa55f935be63badf2bde8457688d`  
		Last Modified: Thu, 05 Feb 2026 23:07:00 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
