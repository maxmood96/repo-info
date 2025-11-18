## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:b5663a7cd4b882a897a6e8720a469cae8fda2086705563e2144483562b803848
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

### `clojure:lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ca99e27b42b3ba260bf6b2592319801f09a526bcc023affc928713d9bde4b75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164428259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19147a69698ad9b8a6f89517c2dd2946d0479573e37512495d71bf5ac8bc67a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:55:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:53 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:55:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:53 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:56:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:56:09 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:56:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:56:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26240918ed29e7a1f6f95cb371f7f2e163c3315f5188fb12c0229b4cb929be`  
		Last Modified: Fri, 14 Nov 2025 00:56:44 GMT  
		Size: 92.0 MB (92045286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470f79aabf541de216b8f895295f42d0cd7f1975f634d71387ac9b9834adcfa`  
		Last Modified: Fri, 14 Nov 2025 00:56:36 GMT  
		Size: 18.6 MB (18579215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3956dfc8f7bcec5827814fddf62233514e9e5da00522973bd64271461ea594b`  
		Last Modified: Fri, 14 Nov 2025 00:56:34 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95804850ae56e7509a41b5215014739de03bdecc61aff81ed31a06c9aafd54f9`  
		Last Modified: Fri, 14 Nov 2025 00:56:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:39726331c89a515848d95d41787e844bf5b25644fa5a840451b8b277774d27ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e4658498c5376133387b7513c26db216cb575b22b04a4ff2ff031d441cff88`

```dockerfile
```

-	Layers:
	-	`sha256:a6d35f8bd83c9870ff3443d004b662b869529da37f13c78ae95ca4209cafca33`  
		Last Modified: Fri, 14 Nov 2025 01:47:09 GMT  
		Size: 3.8 MB (3764682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4b08525403e78862b164f68c0bcc66f812517bb4827f424b3a65fa0e0d3534`  
		Last Modified: Fri, 14 Nov 2025 01:47:10 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85f6c41df6a0f18d97091bbeb14844e61bf527cd3de86cc6c2340a5bde2ae62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163761602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810297664034ba1302d9d1a0d2b07807dc8ffc0df3b32dc1938021de3d182c54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:13:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:13:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:13:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:13:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:13:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:13:46 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:14:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:14:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:14:02 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:14:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:14:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:14:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:14:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a34b5239753bd9abb4f6cdf7dcfcb68d31fcde530e94e8c07ef9debf944139`  
		Last Modified: Tue, 18 Nov 2025 05:14:37 GMT  
		Size: 91.1 MB (91052512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedc04479da11d41ac5b6db3d978cc06561506d6ed4f2e992991aa2d06e45571`  
		Last Modified: Tue, 18 Nov 2025 05:14:32 GMT  
		Size: 18.5 MB (18540682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dbb3e39391a99dc98965a554c2c9314723cc54fb5b84b7d70f1ddd91bf5b9e`  
		Last Modified: Tue, 18 Nov 2025 05:14:29 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08382fcaf969401760316f439f693ac8f3ff3176cba6f724c1e6de0911b10943`  
		Last Modified: Tue, 18 Nov 2025 05:14:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1650b93f7dd08be1cde3dfad3d108ea54c256b070418acd744c51872d9317c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ffa4601527d63a5d18f98d3c26260bc91c327be07c4327eccedab774b201bc`

```dockerfile
```

-	Layers:
	-	`sha256:70832ed5a34983d4684675dc1171050cc6922d45cf827eb91c9c1bd9b72b72c5`  
		Last Modified: Tue, 18 Nov 2025 07:36:36 GMT  
		Size: 3.8 MB (3765574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e506149f29b66508c3194df61e5b14b3b8a176c99c8297681de793c37eb29d`  
		Last Modified: Tue, 18 Nov 2025 07:36:37 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2d3bf83087e19179970045d2bba241fd8f7aca898d8fcc3845f67cde53638455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167874520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef62206963b5b8fda33c637fd94bd7f67a0bfb0ee4f347be7cf6ab773669cb8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:41:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:41:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:41:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:41:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 06:41:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 06:41:17 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:41:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 06:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 06:41:51 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 06:41:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 06:41:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:41:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:41:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9af0794116b59f75955358fb63fbfaa3b3dbe4c37312d256c3296d2bbd7e31`  
		Last Modified: Tue, 18 Nov 2025 06:42:55 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499d024016a87e662e230ce1d9d9d125665a8e2d40835482884b9d17d10b81ae`  
		Last Modified: Tue, 18 Nov 2025 06:42:46 GMT  
		Size: 18.6 MB (18637143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cc127857f5171c76dd1fae6a49d767e4fc3182c09b918abf4c2c710bcd49d7`  
		Last Modified: Tue, 18 Nov 2025 06:42:46 GMT  
		Size: 4.5 MB (4517719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a5f936276f33b2ea2e1a3ccfd8e9327660fc6b3aa369c1251e370384df628`  
		Last Modified: Tue, 18 Nov 2025 06:42:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2f9e57fdb8c097bfadcd7dd6e71481667d27cf89c9e344764a7ec10f330a0557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54028ae8d07f739feda51969e3506b777f0477f7605d54654332b8dbf4cb6229`

```dockerfile
```

-	Layers:
	-	`sha256:3417a0baddad0b8cd4882ae01234b1cabd63d52080952b07ffa324525c929178`  
		Last Modified: Tue, 18 Nov 2025 07:36:41 GMT  
		Size: 3.8 MB (3766984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2449935389e761330b8a8596d12fe7d7a444192edc63d294941d94eb6d69b02`  
		Last Modified: Tue, 18 Nov 2025 07:36:42 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f1b6287879e3d06bd98205151da01e55127990ecfa0e4e1ace6a6d86b0dccb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164724188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9d0a1247b2680b95edeb833b37073c8a5aa94c774c3510e0a79a9649d47786`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 22:18:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 22:18:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 22:18:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 22:18:32 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 15 Nov 2025 22:18:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 15 Nov 2025 22:18:32 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 22:20:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 15 Nov 2025 22:20:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 15 Nov 2025 22:20:07 GMT
ENV LEIN_ROOT=1
# Sat, 15 Nov 2025 22:20:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 15 Nov 2025 22:20:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 22:20:25 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 22:20:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a46ebd6f56fdb6d1c0e17f14db200e703d8de3e8f2d436ad48d3420edcd35b6`  
		Last Modified: Sat, 15 Nov 2025 22:24:32 GMT  
		Size: 90.8 MB (90752842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8686d2d2bcffde798f6788424fb2c4210142caadd5112f8d09bcca3015ec7a64`  
		Last Modified: Sat, 15 Nov 2025 22:24:31 GMT  
		Size: 21.7 MB (21682202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fc351e41199be0c1c8ced35856d73a5d3eeb61b8075692bb476b9b390ac5a5`  
		Last Modified: Sat, 15 Nov 2025 22:24:26 GMT  
		Size: 4.5 MB (4517791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb652f67b2883a1c9cd340eec0e4e79d2fbf3552c9624c1052c839872a210012`  
		Last Modified: Sat, 15 Nov 2025 22:24:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2fabcdac608057e8b58abaab97c71eb34495c7ce89d68bf140a462eb237bd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b3dfbcb28f4ce7c39500419bfbd475f1611e339c10cdbd82ef8c28609e7a18`

```dockerfile
```

-	Layers:
	-	`sha256:7ef9a7a9cfce5482b2ae0c35a161b015c727afa4cb0da6f2768a02f76486ad79`  
		Last Modified: Sun, 16 Nov 2025 01:34:32 GMT  
		Size: 3.8 MB (3755160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7cb402949819222fd08391799916071d981d2f8f57e108e77801803743c6042`  
		Last Modified: Sun, 16 Nov 2025 01:34:33 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a7b34606895fac5d05cbf9449c3bb097928629280d0f5cec376e95b45328bb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160695572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeab96a44f12011f8ca1ee640b04d37303b16a299df3ef8d775bd2b511979ffe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:32:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:32:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:32:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:32:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 18 Nov 2025 05:32:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 18 Nov 2025 05:32:00 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:32:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 18 Nov 2025 05:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 18 Nov 2025 05:32:13 GMT
ENV LEIN_ROOT=1
# Tue, 18 Nov 2025 05:32:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 18 Nov 2025 05:32:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:32:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:32:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397af5166fd73ee2cef9eabe1783921f6bc4bfd9e6898241297d3a8f17d82763`  
		Last Modified: Tue, 18 Nov 2025 05:32:54 GMT  
		Size: 88.2 MB (88210739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409e148779e47c9d390c1617595a3cde9f3e90e921bed36f21f739be3c5e902`  
		Last Modified: Tue, 18 Nov 2025 05:32:47 GMT  
		Size: 18.6 MB (18620640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394ba326f64abd51971839c533bf1981ccd83207303b9a6297480b5c9e213606`  
		Last Modified: Tue, 18 Nov 2025 05:32:46 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62bcc081dceedef56ebb678fa379883ae8b55a7d35b4a1cb08115ffb62153fa`  
		Last Modified: Tue, 18 Nov 2025 05:32:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ded4881071850259f454b21c61beb28fe79e2653972e9b48f402c6061f26afee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181a980d77b4f8b31f632b6c36a32272ce54e4b67a3e7f9a87938b08de2885c2`

```dockerfile
```

-	Layers:
	-	`sha256:9b6be6703ad64592dbea900dad887446cf15295a3f770af48ae1a9dcd0d21e5c`  
		Last Modified: Tue, 18 Nov 2025 07:36:49 GMT  
		Size: 3.8 MB (3763651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08aef416f6714d1495032990b5ccbab606c5f5531f42a4f6fd85386f683733b`  
		Last Modified: Tue, 18 Nov 2025 07:36:50 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
