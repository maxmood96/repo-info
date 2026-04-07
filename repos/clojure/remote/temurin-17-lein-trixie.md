## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:817f86ca9ebc7a0c0a9db1bbfbf39465b93acf2b883ac78df441154f600aebfc
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
$ docker pull clojure@sha256:bba3fa3eff2b99c4ccf2a709fed9df773f052d956cdc95e73de53d2a73831f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218029931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd963aaedc43c1bca6a71d85900e6781d084e5d4096b665de46c738b8fad9a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:14:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:14:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:14:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:48 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:14:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:14:48 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:15:05 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:15:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:15:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262148b22b1411203e65f6431bd70b45c706e2c5736042a75bde88172d5cb392`  
		Last Modified: Tue, 07 Apr 2026 03:15:27 GMT  
		Size: 145.6 MB (145628776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035309520f42f132e11dd4fe4e171c9ca64ec4bf70d2e7edd82f453615362603`  
		Last Modified: Tue, 07 Apr 2026 03:15:25 GMT  
		Size: 18.6 MB (18585130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd507d090d8edbdbae151cb30610ab681e925d7f251af0d5bbac6993786f17b9`  
		Last Modified: Tue, 07 Apr 2026 03:15:24 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375a5f027b63cb78d1d06bca81ed8708e69546a8c3cf1c1ed0e56e7dcb00e95d`  
		Last Modified: Tue, 07 Apr 2026 03:15:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:97c0ffbfc4930d03aa99f8148a305bf14748ed12987cad72dfc7d9faec9527f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f102e80267e34d813159f727161907ec3748d039053c9341d9c22793e8cf72e1`

```dockerfile
```

-	Layers:
	-	`sha256:317f97735cfc1b82b678c38ecba1f1da88bd99bf9381e38ec534e4fd47fbe666`  
		Last Modified: Tue, 07 Apr 2026 03:15:24 GMT  
		Size: 3.8 MB (3815527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1efd8b96abb15d87a509a60c23bb2188e57bfa4f1b371bf2750aba136b2fd7`  
		Last Modified: Tue, 07 Apr 2026 03:15:24 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a84d334e16738294a5939e39da76ad5cd344df451fa633217b75f1eed3a53d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217164477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9007fe32078a13ba647a6c65dac5d41239dcc9dc6deb96232534faa7ab14548d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:25:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:25:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:25:26 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:25:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:25:44 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:25:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:25:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2ba943967bd2f218ec614c93686e9e3bcaa22caed24809fe29982dcc170967`  
		Last Modified: Tue, 07 Apr 2026 03:26:07 GMT  
		Size: 144.4 MB (144436252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9558338dc3640852d41401ceaa1f3e6202330a541493a7e2acc0aa993343d6`  
		Last Modified: Tue, 07 Apr 2026 03:26:04 GMT  
		Size: 18.5 MB (18544798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda12fe00e3f4ceffacc74b2285019dac7e8601859d431290ef5f61a53d52eb9`  
		Last Modified: Tue, 07 Apr 2026 03:26:04 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ced3b97609124aec2c3bb6c02951bdee07b91236f58bbc38a9c0f469c5db90`  
		Last Modified: Tue, 07 Apr 2026 03:26:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5956d763572e251d5b1bcc410722527a5018e41dd0424f8ba5e5968c56ab0f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3590662ba4f7186bdffdfd3a680e98900cb290c7ef8587ff922f10b91fbc390`

```dockerfile
```

-	Layers:
	-	`sha256:f4c51071f92e48850640e10e9c111c9d736a1f84c871690a31fa080b87e58cac`  
		Last Modified: Tue, 07 Apr 2026 03:26:04 GMT  
		Size: 3.8 MB (3816404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91e14bebceb47408ce75b2b509bc88f49ca5ac8999ed857bf800a93797d92005`  
		Last Modified: Tue, 07 Apr 2026 03:26:03 GMT  
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
$ docker pull clojure@sha256:b00a817537cb72906a07f650e8a6d9abecafd2a1655e6dc827f6eae2bb84f6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208136339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda206e9865777f07e231247df4a63fc7c995e5d7d11c00e964cf33e12d62e28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:42:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:42:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:42:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:42:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:42:18 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:42:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:42:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:42:32 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:42:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:42:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:42:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:42:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5be30173782ac514fe3cc2acff6571642739faff5843cc6d1d0067cb9203c3`  
		Last Modified: Tue, 07 Apr 2026 05:42:59 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef7aa6bd601d924df55dc8437106c6b1f3701bbb1f73fcfb36ad369101db143`  
		Last Modified: Tue, 07 Apr 2026 05:43:00 GMT  
		Size: 18.6 MB (18626239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb11744534dbfe790d3d31841467a0b3db80ff588f88d73b32e46bb544eabf2d`  
		Last Modified: Tue, 07 Apr 2026 05:42:59 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4565c1f733466c10bd9dd33552f21f8c9b2708e305b5f734daa712efc905ee3d`  
		Last Modified: Tue, 07 Apr 2026 05:42:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:59f7d7e1c5626dd7fd11a1024f126a0129547c52a9fe5826f4c2a30879648a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db19e85730db27de162a4a79d0cb6a3c6194a0c01b73a1358ffa9fac32646606`

```dockerfile
```

-	Layers:
	-	`sha256:aea8e50bce39d71530b8b6566d664d718bdf5a775e0ea3aea049e28ef22281d1`  
		Last Modified: Tue, 07 Apr 2026 05:42:59 GMT  
		Size: 3.8 MB (3811954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b16ceb38b71a24b30397494d5a502e15ba053db0f13714eb1b4fac63dc5594`  
		Last Modified: Tue, 07 Apr 2026 05:42:59 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
