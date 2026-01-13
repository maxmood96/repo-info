## `clojure:temurin-25-lein-trixie`

```console
$ docker pull clojure@sha256:450c45b3875de6aa55809900692f9689815f081dede308757e26f5b2d0432462
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

### `clojure:temurin-25-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9efc95db0e5159a909209b6ddc174bff6b5ba1faba6b3e6cf41b048cfc969f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164432694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baeb251a73e7aa9b4c5fb641f3bf0a4b14a3156874b0642205fef5fa5daa3e35`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:06:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:06:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:06:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:06:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:06:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:06:52 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:07:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:07:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:07:09 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:07:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:07:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:07:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:07:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227272bb6fee0e9648b13cac7ee8733c4b2a30537072fc4f92ecbeaa211faad5`  
		Last Modified: Tue, 30 Dec 2025 01:07:57 GMT  
		Size: 92.0 MB (92045301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f512fa03d26eb24d3348bb80e9d5168cb1d68d3d54dccd17b3b95b07f1e576`  
		Last Modified: Tue, 30 Dec 2025 01:07:43 GMT  
		Size: 18.6 MB (18579666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6993c2e34340a9406b94d41445caa69e0a154cfbfbbdeae0da09f94f29e16c`  
		Last Modified: Tue, 30 Dec 2025 01:07:37 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9b250920759377c7ca85057faff5590748597f30cb30c32920d2337b67ec5c`  
		Last Modified: Tue, 30 Dec 2025 01:07:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:19a2d7dd8fd9c3fe714ed20fed7da9be4d0722f5028bf9dc49dde78f159daca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8dbddef8d35bc584123eb4445a96849afc1598286c604c1c5fb79ec1c56956`

```dockerfile
```

-	Layers:
	-	`sha256:eba04ab73616b44a9c0b5c905dbb3d38fe3389b9f1f626cf2e8f1ca8bb6b9d73`  
		Last Modified: Tue, 30 Dec 2025 04:35:43 GMT  
		Size: 3.8 MB (3764676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f301983fe43a3c382113a49d9c70d87dca038f52ee8c3890339d8b2387aaa840`  
		Last Modified: Tue, 30 Dec 2025 04:35:44 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0da0df28e0ae48f12376fad54ef3cd730914c4c73dca6015b3b92f8ead9ebd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163761507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52355b79a7ab0c99ccb47dfb161ee164664a29e06614509e1412953b107c066`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:08:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:08:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:08:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:08:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:08:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:08:46 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:09:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:09:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:09:02 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:09:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:09:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:09:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:09:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe7e2dddfe235eba0b8e030a147bcc827f79303f5922bf6cd6675504a64b88`  
		Last Modified: Tue, 30 Dec 2025 01:09:41 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86b1563d7b9639d62df019f74163615272bcb38c151bef366bd28679a881b89`  
		Last Modified: Tue, 30 Dec 2025 01:09:34 GMT  
		Size: 18.5 MB (18540615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d302373cc3b70a22b35d1de839eaccbbfef7427e8a8e92bf0eeda5956c6285b`  
		Last Modified: Tue, 30 Dec 2025 01:09:30 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ecdec4e5cb219780e889a57e3fc7ba0fec0367a7c044fd7a8418b769ca8d0e`  
		Last Modified: Tue, 30 Dec 2025 01:09:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:349ff9021c1767894f0f5dddf94ef28c881eb4ad639f06ad22ae81d3a87bbc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae9e35c0d59b60a870be577d39e07c2bb8fee5fb0e5e1a07c352085d7603438`

```dockerfile
```

-	Layers:
	-	`sha256:e72a75c83ec13f9eb08c054e0d83cede8c3f990f79836720f6c21ddc9e9e21fa`  
		Last Modified: Tue, 30 Dec 2025 04:35:48 GMT  
		Size: 3.8 MB (3765574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b99f079fc89a8c01342e2e5156eb84c4c62448ff7ead2465ea2d65a6197015`  
		Last Modified: Tue, 30 Dec 2025 04:35:49 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:98e5f97067f85fa1c1c4b56ea0d287670ec84f1f0261f882509ee79780ab003f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167874399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec5972fc0c5c2758af79b40362adc461d49064acb3f2c9eaf806f84c46920da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:29:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:29:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:29:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:29:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:29:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:29:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:29:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:29:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:29:53 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:29:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:29:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:29:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:29:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b337200b6e61d16776f5501182cfaee70700993bebbb12367907868e271e3`  
		Last Modified: Tue, 30 Dec 2025 05:30:49 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff71bdade7c0a287d0528469f6301f9582c6222a9142f2fede970bc8e9080c`  
		Last Modified: Tue, 30 Dec 2025 05:30:42 GMT  
		Size: 18.6 MB (18636966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb2a01b3f9d39856a9b75bf6339cecda19123b6260b6d50f0744ec35df70e8`  
		Last Modified: Tue, 30 Dec 2025 05:30:42 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8261a10df30d94601fa3a642c57f8296b69a6c6b6c370c09b42ee5181e778977`  
		Last Modified: Tue, 30 Dec 2025 05:30:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a141131b7dc0ccf7c88d9de7aa480474191245bfea3ac21b5bd9c02edce71dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0c726f129ac0556699d70d45a61a2c519f1ac1af143677d52c31733e1dd5b4`

```dockerfile
```

-	Layers:
	-	`sha256:fc161f748aa0e7d44f77523164bc1cea23c81e0e0e096cab0c2ca9a1053bce7d`  
		Last Modified: Tue, 30 Dec 2025 07:34:42 GMT  
		Size: 3.8 MB (3766984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b10c42f93f47a546a23c18d5be175f5d3ddb3178f1fb34105940efccd013fa`  
		Last Modified: Tue, 30 Dec 2025 07:34:42 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:7d3beb28017b32f2bec89adaa52edd88ff7487285f0e4d7193a3835ac7018027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161573955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d7896431c5a438871f78be2ac2b109b669073da0117f7a422c9f7cde6f9123`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:24:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:24:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 07:24:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 07:24:27 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:25:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 07:25:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 07:25:59 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 07:26:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 07:26:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:26:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:26:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e72db194620f93f57207f61aa544e094761861bb8fbdbf65160d1e1594a9c91`  
		Last Modified: Thu, 01 Jan 2026 07:30:30 GMT  
		Size: 90.8 MB (90752893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578a725406d0222a0bf716fbc6c412a59b379add08b579b0f52661319f9d7926`  
		Last Modified: Thu, 01 Jan 2026 07:30:22 GMT  
		Size: 18.5 MB (18531712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f2f88cea93c0c8393673eb3323f2fbd3e6018f4174e602a2db3723f6c72c93`  
		Last Modified: Thu, 01 Jan 2026 07:30:22 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3accc15121411f29d0f0ea48151052f15acb2d0e86d47d3cedd606e0ea652d4d`  
		Last Modified: Thu, 01 Jan 2026 07:30:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c545cdc29e233638050236122a869cdbfeb250c8a42010cadb4f8ec4f3c3148f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92526daa2701e44923f18530ea5502ecc1e44190dbf79dccf90c5cecb416d1e9`

```dockerfile
```

-	Layers:
	-	`sha256:b41e981f2201942c5e1463c6b2a34018151d49fc0697456cceaeeedd5e0f2d57`  
		Last Modified: Thu, 01 Jan 2026 10:35:04 GMT  
		Size: 3.8 MB (3755160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2508d55783bc7450628b328666c52bbe4595f38a44e43311673860bcf0d1d3e9`  
		Last Modified: Thu, 01 Jan 2026 10:35:04 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c51e3bd93fad7eba6b9d2146ef8ebd5b258ea94d59b9bb00ed6abcb59e0bd90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160698205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdea05be7e15341551fc624a3cd97d9845cf46084862f25639a731928860888`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:08:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:08:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:08:23 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:08:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:08:23 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:08:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:08:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:08:35 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:08:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:08:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:08:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:08:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea00514fb389056b53c87e8e91db6d088d164ca6598331cf137dfcbdfeb44c6`  
		Last Modified: Tue, 13 Jan 2026 03:09:15 GMT  
		Size: 88.2 MB (88210671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d5f8bbc8bd18ccc615c1c0eb65a6af4e29c48f65b1d8cb6eda28b42e4abb7`  
		Last Modified: Tue, 13 Jan 2026 03:09:12 GMT  
		Size: 18.6 MB (18620649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fcedec4d14a1b225acf0e2e8b2948691cecc6639ee978d0061961aace43d59`  
		Last Modified: Tue, 13 Jan 2026 03:09:10 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697eae000a7dc1142ac5de162dd814d3ad4c3280031f4c7d0f370f139dd8f128`  
		Last Modified: Tue, 13 Jan 2026 03:09:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bdeeaab03fdb521fe9a05b13d3fc4c4f40ddcb902b0b70c72c1269c1b9ccb937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc299be91f43364cc5e7265695e03a0068268730893a326b7e8cea8fae46f573`

```dockerfile
```

-	Layers:
	-	`sha256:037d517361c36744405a6b78cb67b0718c64615d41d07c9c5f6f4ae087c0b9e1`  
		Last Modified: Tue, 13 Jan 2026 04:35:39 GMT  
		Size: 3.8 MB (3764510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc2448ebcf5ad8475dfe8cd45888425d6ad444ebe5e3d88a215bb56ac382ef47`  
		Last Modified: Tue, 13 Jan 2026 04:35:42 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
