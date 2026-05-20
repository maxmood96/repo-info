## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:06a3225e6470ece788d19aa21a341a7b35358d729ae269845eab2b3c177bafb8
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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c61428f21c1068aa7c037b58401108d4095c76759a609a60fe525db819070f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196651698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ec810d35e2a490125fb15c4189b0859237eaca5382224b1e761d3f851fda66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:58:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:58:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:58:34 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:58:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:58:49 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:58:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:58:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:58:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:58:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c460328ab7e4e043ff2065f9f7f929b7ee5039b8d2b63ad75056169e915a9d`  
		Last Modified: Tue, 19 May 2026 23:59:10 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c0e2570970f42f85381e07d193224961209c5996821db25ebc00c749fbe9be`  
		Last Modified: Tue, 19 May 2026 23:59:07 GMT  
		Size: 16.4 MB (16448141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff45fd28bf1276324835c3442efa0a3eb55a34d115c45c532700556744eba1`  
		Last Modified: Tue, 19 May 2026 23:59:07 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5afe74a57fbb29de800eeb6cdc743d0cc24c07588372ed95647ccdaaa5532d3`  
		Last Modified: Tue, 19 May 2026 23:59:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba0dd5f844f5aa73990ead0b76b81d4a31eb99a8f9e9632a2f09be5e830e4f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae50a06a5de61686a455ebaac0b911245e58e3e0564e6a364a525530929eadc8`

```dockerfile
```

-	Layers:
	-	`sha256:3e4de572b192fe6771e1725720928db30052125d1632f7cc432b00cd3501c275`  
		Last Modified: Tue, 19 May 2026 23:59:06 GMT  
		Size: 2.4 MB (2365457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061cafb567a597d55dc36e5ec3c9435cf9920e29042a4e3ee32a9b0391d47ad8`  
		Last Modified: Tue, 19 May 2026 23:59:06 GMT  
		Size: 18.5 KB (18540 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2cd5da369750666bdacd06311dc3ee2e73c1171035c6ac5b4c99894b5dcded6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 MB (195798650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3247a1d2ffd7ba3edc5dd69c87ba4a22de21e60dbea8cc849e8af7df7543cbcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:05:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:48 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:05:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:05:48 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:06:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:06:05 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:06:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:06:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b178e5b51b932bef865ec8f66a21c0d2bce569a621fcde0ff7bd526b9fd6c`  
		Last Modified: Wed, 20 May 2026 00:06:28 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826c99556422161b5ea8a995a7de1fa3e09399ccd5f1869fd347dedc1f63c0aa`  
		Last Modified: Wed, 20 May 2026 00:06:24 GMT  
		Size: 16.4 MB (16414214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17146df6a2c500fedb22604ca688c1d0356fe2013f2fb8de76d7144c08934fd`  
		Last Modified: Wed, 20 May 2026 00:06:24 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89456523d98428bc4530f7a553c8124a1b35f7028315cbd252418951a99d80d8`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:48d5eb2f9009613d8f9c1d0b4e7397da1bd6bf52b8758fb54c27d0be4023de89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1fb26ca8a62a0ac1e8a0b01bb45f7971a0b9ca590507331657713565a31ea2`

```dockerfile
```

-	Layers:
	-	`sha256:06282ed9cf44e622a54543ab181e543e200a3bf6f767f8f960d16fe7536fcb2f`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 2.4 MB (2365067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f6bc90b5292eb9d2043c34b491a815aab57345935736d52d3e27a72d90a225`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 18.7 KB (18662 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:eb5a5de98171d6e73ba77c09d48a161e1bab5acd4dab70693f99f0cc72ef64ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.4 MB (200367811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a6eeceddfcf682a6b636d9331a3175c63c7dbc3243dc513adea4730ebe0137`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:32:03 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:32:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:32:03 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:32:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:32:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:32:32 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:32:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:32:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:32:35 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:32:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72cabc9601635085bc11fa48d74114d9e1765a07685bad636cd3a7da9370ac`  
		Last Modified: Sat, 09 May 2026 02:33:09 GMT  
		Size: 145.8 MB (145766215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d4e01966977f286a183e524fb5e6e1f4d586e4408a4099e71ec090fa83e6c`  
		Last Modified: Sat, 09 May 2026 02:33:07 GMT  
		Size: 16.5 MB (16485353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c752a269480c7303def8c34741e3cda5808df134dcdc6c9388e9c0573ef3b6`  
		Last Modified: Sat, 09 May 2026 02:33:06 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a0b1cf8be33c7a571d9c10c66bb16981553ec5fa8da3d5ecde8d4014ee07ef`  
		Last Modified: Sat, 09 May 2026 02:33:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a13b199cf8cbfd0641f738f2eb309178c2a161484fcdb7d154c6b012b00424c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb251010752ecc073051ba9261c96697777debfac833e7025ae61331e897b9b2`

```dockerfile
```

-	Layers:
	-	`sha256:5cf3e0d3701476acdbde769c3218e588dcfa7b0ca3573d233cb59b8e97df7411`  
		Last Modified: Sat, 09 May 2026 02:33:05 GMT  
		Size: 2.4 MB (2366395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856994a51c2c30515b5108fd4b1f34d4e9e5555d88b033132fd255b8d877dc0c`  
		Last Modified: Sat, 09 May 2026 02:33:05 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:abbfb71210341675f87b0724f27aa14f632e83373e3da2cc51e0fed94877755f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186758671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c73c07238c44d6a2bac64e5b66ed199805829b3db5832a578d7d3023abf0ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:44:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:44:03 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:44:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:44:03 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:44:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:44:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:44:17 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:44:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:44:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:44:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:44:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b7061a0b137c526c9908a364ab29b9c6acb42a84835c646b8c4d2dde37fd77`  
		Last Modified: Wed, 20 May 2026 01:44:44 GMT  
		Size: 135.9 MB (135910410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2061fd3083a2b521102f3c7c534d83e8409264a842667f28047255ae3c7a18a5`  
		Last Modified: Wed, 20 May 2026 01:44:42 GMT  
		Size: 16.5 MB (16484163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf3645584dc644ec6997f5ceefcb709874e001a081070c122a4e463d1ea4278`  
		Last Modified: Wed, 20 May 2026 01:44:41 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f04b415a3635d5c5e3f180275917274166f555027cb20ce718293a7a793cb7`  
		Last Modified: Wed, 20 May 2026 01:44:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e81a748cd56db58d30cf2c814679cf6492751a5285d90f5926d8e1ee01e14c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638eaa6e959b4b7bb9191c089d28818b0f02000731022567a29ae48162b6e367`

```dockerfile
```

-	Layers:
	-	`sha256:fce195aa40cf9d2e9a9d79841eac0432558203b742bd2289c4f24cae369c8f06`  
		Last Modified: Wed, 20 May 2026 01:44:41 GMT  
		Size: 2.4 MB (2361884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71a050bac2636c3297ca74585a0cf7688ee8e21164234961ce594b1c4654c95`  
		Last Modified: Wed, 20 May 2026 01:44:41 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json
