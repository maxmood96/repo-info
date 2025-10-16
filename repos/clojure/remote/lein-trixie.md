## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:200db63c148a3d6211bfc56fff561f0680c3e46517c9479ccbd180fdd5179b34
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
$ docker pull clojure@sha256:c48ab5674d0addb5079cbf42135e714656bc9df804648b79812347a51ba13ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167383193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc6d215a170f0e949e37d5edb101cecc17c36d9769a08e8de463be99fb2a1fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcc0490128d8aba942c07561bfd349b3b6f5c69fff1e19bdf3c123025e0fb34`  
		Last Modified: Fri, 10 Oct 2025 03:58:39 GMT  
		Size: 92.0 MB (92036050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25985f1788eac03fc3177871ba49207b85588090280215419e4b555ae01b46df`  
		Last Modified: Fri, 10 Oct 2025 03:58:23 GMT  
		Size: 21.5 MB (21544334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55270a250185758da763a73c68822576dfc7da17cc8914028b1d4197a64e544c`  
		Last Modified: Fri, 10 Oct 2025 03:58:23 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ca69c92e902eec119363250994ca796659c8c5a71572b6d1462d46d6ee7550`  
		Last Modified: Thu, 09 Oct 2025 23:27:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6ee054d7734f1c00e49f557605b379ce0819a600ca0009a49da5f3b920adff74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08d87f35954c06aca7218bff1930d2b67e9e15a1837f8b754d952f59fc5cccc`

```dockerfile
```

-	Layers:
	-	`sha256:78a2c5e1c9e258de7f857dd0b307deb38def933d04fdfcfded2ea34a3b550681`  
		Last Modified: Fri, 10 Oct 2025 06:35:26 GMT  
		Size: 3.8 MB (3764668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ede90817c54f914bb462495dbbae7f4b14878ac003bfe137a68abec8737d82`  
		Last Modified: Fri, 10 Oct 2025 06:35:28 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2ca0b6ff895dc36e07b7ef578fa53d8e1ab9979d5e86dc0c8d958201af4ef2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167088381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02548db5fec3d3ea1ab0efdf2c8d5fae2c5bba1b7ed45d06c551f30f973a80a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad528d635b419c80f955d1d02ea9708efe3f0481798c53c8ea7ed54ebcd3e389`  
		Last Modified: Thu, 09 Oct 2025 22:31:14 GMT  
		Size: 91.0 MB (91045228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb07ded9c4d57f65300701471db6cf974c486c57b06be739f1c0f3d2f9c7315`  
		Last Modified: Thu, 16 Oct 2025 20:06:12 GMT  
		Size: 21.9 MB (21876284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c2909ab3faf09eaa748243555cd9b4c422673761b899f3b228da402a92c513`  
		Last Modified: Thu, 09 Oct 2025 22:31:03 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500e3bc01df3f6e026318a40aba60de1128e432e0b16dfc842b7c5a946c4a381`  
		Last Modified: Thu, 09 Oct 2025 22:31:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:74a345fd5bd563930f8312ad937493717d62103f1fd975943190e0994fd82360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618f7c7ec905fe9510dd405479beaa7035eff20ce4fcc441d9a2937c4c41a7fc`

```dockerfile
```

-	Layers:
	-	`sha256:292d25cf900c73f9312f09f25e7e6d0eaef6e07da2829fd2d46d696df40ed638`  
		Last Modified: Fri, 10 Oct 2025 06:35:32 GMT  
		Size: 3.8 MB (3765566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:522cf70a442b17d898797a9b1057063515a6c003c18dad00f6387c7574735553`  
		Last Modified: Fri, 10 Oct 2025 06:35:33 GMT  
		Size: 19.2 KB (19167 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0bc7c9d77e5863edb2bb077b3dc05caaef4ce200393fa04936316bec757bfb3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171075727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ff295af3d42b6c271b2d77cbeddc25503e7750b617e318d8f21f4623a027e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc92fde2234dc8f32a119fed41daaf6c83b22fa10ffcee1fa59c6b6dee4280b`  
		Last Modified: Fri, 10 Oct 2025 05:55:27 GMT  
		Size: 91.6 MB (91601717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2f7a0c52296be710a45ca6d7c493776117d9bc40018c561fe9353f1d652d1f`  
		Last Modified: Fri, 10 Oct 2025 05:55:17 GMT  
		Size: 21.8 MB (21846635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6a9ee36155baccf67965ff15a14ec000a3e38cf9d4ac27c032de3a5762d5d7`  
		Last Modified: Fri, 10 Oct 2025 05:55:15 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e099401f118b380161b2ad1e5874e406c6356ae0b0bfe8944cdfd1f012069f`  
		Last Modified: Fri, 10 Oct 2025 05:55:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:93231393722706ea2931adcad7dba8d735186c3103b56c9fcf37cddd521a6e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d72ccfc3e9d7ad37a6c64a3687b7ae46c6e4d165f8e18e94a2e441cbeedb36b`

```dockerfile
```

-	Layers:
	-	`sha256:52c04b8a422093ad47f775974f49355eaebe435c706cea9683bf5568c5f195bb`  
		Last Modified: Fri, 10 Oct 2025 06:35:37 GMT  
		Size: 3.8 MB (3766976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f76ccb7db9001376aca5358073483417693a34546ad653ac5bc3d506f0ec29b`  
		Last Modified: Fri, 10 Oct 2025 06:35:37 GMT  
		Size: 19.1 KB (19078 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:50e6dcbf0112de57634a1d0c62fb712bb4855d83bc47ae70ba2e660b64627316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164190752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2858734d47de2127e7b336a406f0e84f0a85da7b7a53dbe5cc875b54a108d56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15c689286839ede10d92025dec031597f1addd346fcb57828df1d0a46794634`  
		Last Modified: Thu, 16 Oct 2025 08:52:21 GMT  
		Size: 90.8 MB (90752401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315f38d91d783f8975bcef0cf9f51593c89ee3ea091e66d945d8acfb39f844fe`  
		Last Modified: Thu, 16 Oct 2025 08:52:14 GMT  
		Size: 21.2 MB (21150111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ac5dd0c687902ceeec392b9bee3e6b14109a468981175c4adbaa96b23b762`  
		Last Modified: Thu, 16 Oct 2025 08:52:12 GMT  
		Size: 4.5 MB (4517801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3564d9e1d6711dd19b6d3fcd0b45a8045ffc3bb72d35fa2fdea5e06b2467ce4`  
		Last Modified: Thu, 16 Oct 2025 08:52:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3aa2b43f4f9a850529e05677c6227f971e9d511fb3e97e55edb619cb587deb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80466ebe7b6e0bc6536f5caed9ff39e31a95e5579cd9007670351948f45b20c9`

```dockerfile
```

-	Layers:
	-	`sha256:7db486aea7244f694f819d6f69f06d8b57ca3adf1e15e0d7597c7a6df8cb5327`  
		Last Modified: Thu, 16 Oct 2025 09:35:05 GMT  
		Size: 3.8 MB (3755152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8309d13e1b8e602e6de7259c1159293de9803f442e348ed5b485fe3dc656d08d`  
		Last Modified: Thu, 16 Oct 2025 09:35:06 GMT  
		Size: 19.1 KB (19078 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c327e8a3b04a404b2e09b253ff4525a3a26aa13f651302335d92a6335f069bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163307404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12145e01bc42a5065e926db801c638f93e2d7107c59b92c9aea6d6472d7727d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Sep 2025 15:53:20 GMT
ENV LEIN_ROOT=1
# Fri, 26 Sep 2025 15:53:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c472da08548dcf037f943b616dabad9bb86cbf698dd3af1da4c39e1dc1031b7`  
		Last Modified: Fri, 10 Oct 2025 03:42:21 GMT  
		Size: 88.2 MB (88206430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f934842c02fda7b227900f9827f389d3b636d3846c224a33ba8248319ba9c60d`  
		Last Modified: Thu, 09 Oct 2025 23:46:12 GMT  
		Size: 21.2 MB (21231351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276bd9ca139520d19223032f58ae2e658bacb48fa05eebfa0fe4b4562fc80123`  
		Last Modified: Thu, 09 Oct 2025 23:46:17 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb062e9f05befb42371833cc7fc164fdcd62a8008f1e90e01ed245d920d904f`  
		Last Modified: Thu, 09 Oct 2025 23:46:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5b6b952b262af2108bea552e174976b8e71cee32269b452331aa591744bb7667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fe5b8e30e18679e802fa638be2f036d8408dfa189f1a77bc2befd65c1c9518`

```dockerfile
```

-	Layers:
	-	`sha256:6f0af29ea8c3317748e7b68007fab59c19b5b32a3b03a23505f92ffdd044f412`  
		Last Modified: Fri, 10 Oct 2025 00:35:01 GMT  
		Size: 3.8 MB (3763643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e8f0497aeca1c002e9c6447bf0f016dcf1ba17a2d0b6d2118002cb5a9985a6`  
		Last Modified: Fri, 10 Oct 2025 00:35:02 GMT  
		Size: 19.0 KB (19022 bytes)  
		MIME: application/vnd.in-toto+json
