## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:58971688f2b37c2ed0b03bbc215998cd923b73f9417d768f1ab455016036c097
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

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d20853c38c68bf6229a9e5e5691e72174cf2f4d5d8216ba5dc0b6d08fa06a54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218029290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a7289099c7b7f8cfed05f4c440356e5c46e84fe8f7781bf5779804ef1d13ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:58:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:11 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:58:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:58:11 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:58:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:58:27 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:58:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:58:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:58:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:58:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc605cc0616805b5d9120b28f2157dd5afb24fb8994ffc9b79a40662169cf8`  
		Last Modified: Tue, 17 Mar 2026 02:58:49 GMT  
		Size: 145.6 MB (145628437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31b8f9ca9aa8b714d733edb6be0042b820485a940c49e8d3f039fc8437b38b4`  
		Last Modified: Tue, 17 Mar 2026 02:58:46 GMT  
		Size: 18.6 MB (18585136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6cfc0a4f577bbd76ac569f97161a240cb0e2d84d2ed712c0e49db7834e09c`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72d0db2eaf968d60d1b6e970855b4de9790896c7afe362e7737e1ee8b9def8`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:42924efb72a5284814654df9986a97ab21263b60b3f28341aa98d39ddebb1ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66cb14ccb45d9e9786005eb81352aaf877c88552e264695b2dde57812094c77`

```dockerfile
```

-	Layers:
	-	`sha256:11cba14e99e6a5b0f69201bdb3e9a21763a62fe76f06a8b30fa25801c0b1a400`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 3.8 MB (3815527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5471e0a11e61014ded9840c02fa95ca841bdf9f0f58eacec8e77168f7c4578`  
		Last Modified: Tue, 17 Mar 2026 02:58:45 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:48253dba6245c766f57866bd7b299410c0dd948f3645df172aded686cdcd7542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217164142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d95ba6e666d0e68ff3b9067da1ebac1011e377bdb2f4c3c3ad8cce1eef48b0b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:02:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:02:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:02:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:02:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:02:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:02:48 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:03:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:03:07 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:03:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:03:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:03:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:03:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c406556972d3988e697c739fa1035e11afcb9a37be82da19b1d2c3501140c6d`  
		Last Modified: Tue, 17 Mar 2026 03:03:29 GMT  
		Size: 144.4 MB (144436242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76950ec8629bf73578716dc2310e1854f9fb5af3d32934f0fbf14b91fe81cf68`  
		Last Modified: Tue, 17 Mar 2026 03:03:26 GMT  
		Size: 18.5 MB (18544804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2df7eddfe45f70dd4649f8593f16da3ebdf0bd6354bf29d63ad913b218840f`  
		Last Modified: Tue, 17 Mar 2026 03:03:26 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e140fdbba27b8690055ffd37b70753213d02ed1fc107ca0213a7ffcc8bfd1fec`  
		Last Modified: Tue, 17 Mar 2026 03:03:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:09639f62813eb1fe10582745ab6c04b6d08ee4017b697920876429b74aa28c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c66ab447faee3f06d3fbf15d3e678d5c802d83c2a92ab02cc7e7bee59aad7e`

```dockerfile
```

-	Layers:
	-	`sha256:9af6177d9fb338109d32757b5df2f23c53ce8c33a0f2aa2a9efbd33ee6b68b9f`  
		Last Modified: Tue, 17 Mar 2026 03:03:25 GMT  
		Size: 3.8 MB (3816404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2670ee167d513ebc17336edf594f1a6ecf4fb21d85e8d24266efa4ba0d296553`  
		Last Modified: Tue, 17 Mar 2026 03:03:25 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:be2e40e0b00db607dc7d9883b1a1f0c64bbaf523df8c8c5c177086091e11b2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221715468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cadea1fb53bf0986b9efd2663f2fe0b8a943b6d38b82517f3857505e15de123`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:27:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:27:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:27:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:27:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:27:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:27:35 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:28:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:28:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:28:19 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:28:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:28:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:28:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:28:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822c66d457280a71230ad4487fd70323ef90d3d8e95b8850297f2bd84ecbef19`  
		Last Modified: Tue, 17 Mar 2026 18:29:06 GMT  
		Size: 145.4 MB (145438236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b528a977f62c6359b5084d66f0ac4e79588ccc308138f37b19394c0108e79b76`  
		Last Modified: Tue, 17 Mar 2026 18:29:02 GMT  
		Size: 18.6 MB (18640712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb93ba68642c09537ad53f111b059b17d2405dd45ad00a80f3cb277da829af`  
		Last Modified: Tue, 17 Mar 2026 18:29:01 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3304635e2ae724cb75a91e14fc9ac39045508ff16ac560828ed8c5aa306697b1`  
		Last Modified: Tue, 17 Mar 2026 18:29:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f0e2babbce63e762022043a1ceff537a59bbb3036d491d5a7e43bbf477ae73f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af20e07fcf77cd1c6096fe28578b4b45fbe091de64026c1e092ba2e13bd3ceb`

```dockerfile
```

-	Layers:
	-	`sha256:ebccbee2fe49a64cf025b9c15d6e8af06b5934f5caa7a17c9eb149a678f76d98`  
		Last Modified: Tue, 17 Mar 2026 18:29:01 GMT  
		Size: 3.8 MB (3816527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391dfd2dbbdd924f3048ae67f96e11415991472a8fe62020102229127ac4b72e`  
		Last Modified: Tue, 17 Mar 2026 18:29:01 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:98b4c00885c8437c727ade4d192c9a84c7dd69f8237a405608e138f9aad4d612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213511088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae975a97bc5ba36ea20d8701a66c63cdce293c0e643fbfc6a9b2b299c0ff4ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:22:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:22:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:22:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:22:07 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 22 Mar 2026 18:22:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 22 Mar 2026 18:22:07 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 18:23:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 22 Mar 2026 18:23:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 22 Mar 2026 18:23:42 GMT
ENV LEIN_ROOT=1
# Sun, 22 Mar 2026 18:23:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 22 Mar 2026 18:23:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 18:23:58 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 18:23:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6add0609c3b541666acbd64d7040bade8e52829cb99e1fb5d81f0474186bee1e`  
		Last Modified: Sun, 22 Mar 2026 18:28:10 GMT  
		Size: 142.7 MB (142662936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55be4ea0c1ee06c11a110f2ca1292625092b351725993ccf40431a588b6848a8`  
		Last Modified: Sun, 22 Mar 2026 18:27:52 GMT  
		Size: 18.5 MB (18537606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b16623a925b7659eb63a387ab9caeef41925ac177b389149592d4b15b611f`  
		Last Modified: Sun, 22 Mar 2026 18:27:48 GMT  
		Size: 4.5 MB (4517788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ff99418dad4a2515ac33cc2bcf1b57353294ddb7c47be9a923befe8f994593`  
		Last Modified: Sun, 22 Mar 2026 18:27:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:811cb3ffdc978416643a416da8f8d583a2c846041468cb540116f991d930751c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3822480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93fd791df8766b5b1fbca10739708355093dd65b87a48eea941c825b69d1c2`

```dockerfile
```

-	Layers:
	-	`sha256:8fb773cf69b529dcc6faa381562409384f810bdc0a4db643037d2f17cdd5fa89`  
		Last Modified: Sun, 22 Mar 2026 18:27:47 GMT  
		Size: 3.8 MB (3804085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:426f81b9ea92c021f09d8f1617735cb8da6f380d9dbdbcf162761ffe14c48f3d`  
		Last Modified: Sun, 22 Mar 2026 18:27:46 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c4261a55cd6714504268209bafbbaed64a04cdd1321ce96330513efda68245e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208136231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57721d9877c7cced354461c302c87dcc8631610834fe90b1cac67e145a5f4fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:35:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:35:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:35:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:35:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 11:35:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 11:35:16 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:36:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 11:36:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 11:36:04 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 11:36:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 11:36:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:36:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:36:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e566dbad59a73eec61586be81332c4481cb285b91c1570f8f84af13c0b0914fe`  
		Last Modified: Tue, 17 Mar 2026 11:36:59 GMT  
		Size: 135.6 MB (135626829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b920ae706a97126ad4f281107cc6118960da99f915dffaec3d083c0b47dc0d`  
		Last Modified: Tue, 17 Mar 2026 11:36:50 GMT  
		Size: 18.6 MB (18626437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45ca7ea98bb5250fb4bfe9058555525943b6565834925b354ed4bc112d00f79`  
		Last Modified: Tue, 17 Mar 2026 11:36:47 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db51aa38748e486c3a90a4b2368dc3951d76efe9c08147b596bfcd7918ad8e0a`  
		Last Modified: Tue, 17 Mar 2026 11:36:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b68691a8612e57cecd86dfc235021a73729464a01d15cf427d0218e977f0b2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13aebaabfbb1b5964ce59e0b412dbbf944c81556829ab3c87c40530e814f9c8`

```dockerfile
```

-	Layers:
	-	`sha256:5878cbeb6a0b3056d1fd432563013a4534160e1399f2cd55edd151b0cf7d06f3`  
		Last Modified: Tue, 17 Mar 2026 11:36:47 GMT  
		Size: 3.8 MB (3811954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c417c6a364a717545971d16016ea3f783baf0a51cba167d36194ec0283fa63ad`  
		Last Modified: Tue, 17 Mar 2026 11:36:45 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json
