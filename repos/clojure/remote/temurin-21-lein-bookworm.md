## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:ee7ac1f875eeb0697b311c36a55932fe172187087f7679bdfc6f1ce47fec6d4b
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

### `clojure:temurin-21-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9220daff80f8fe4abbcd998de26220d861f6c62fb2072a9fe900c88bca632a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230980266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3821ea006fba5d6c39de60d9d9172641e454fc18d5bf58ffd63fe67f9ca0bb63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:26:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:26:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:26:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:40 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f11661ff1e0429f0c7434e465d66c42d45cc84dca5317d1b833dc543c78dd`  
		Last Modified: Fri, 08 May 2026 00:27:00 GMT  
		Size: 158.2 MB (158166935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc3323a4f2deb31c4928567d9d79dadfd4be06a8b3af03888119fb5e99b3b2e`  
		Last Modified: Fri, 08 May 2026 00:27:03 GMT  
		Size: 19.8 MB (19806516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd757e625910ce90fe00b5b72bebce8acc4af572e327e966ff32959aaf8ae58d`  
		Last Modified: Fri, 08 May 2026 00:27:02 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c964459b8579ba766edf23e4696980238f8e4560a0f8e32e8f7d789cad93d72f`  
		Last Modified: Fri, 08 May 2026 00:27:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bbb9d320b3069652af1d1257306db186ee6de7a1329e5c5eed1548e394cb761a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8b337036d7f573bf9d68f8dca6ef179854e3db26b7dbd1721cbb5acb23db32`

```dockerfile
```

-	Layers:
	-	`sha256:3f229accef227b318d3a519ed470aa4ac48700408ee48d9637800dece317ae8b`  
		Last Modified: Fri, 08 May 2026 00:27:02 GMT  
		Size: 4.3 MB (4284860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc81f31560071ed0415e6d8ac1e4d0ebd54973b8a87a98bf92fd0fe23088f5f`  
		Last Modified: Fri, 08 May 2026 00:27:02 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:35c3653eabd385fc8d4322505f6a7ca137293ad39cdf11e5f03ec04f23310948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228989470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65074240839b141cf452951c765c92cab079b1dac5d86e792d44f85ec8425810`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:25:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:25:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:25:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:46 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:25:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:25:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:00 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f247c09c346552e5b6a19f3e3bacce6e3b75f9d4c879692747fe6f216b20a85`  
		Last Modified: Fri, 08 May 2026 00:26:34 GMT  
		Size: 156.5 MB (156461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effe63ef3dbb966f54a18b385fa3c83651bb354cb7473fc373ed6b4397e2ad6f`  
		Last Modified: Fri, 08 May 2026 00:26:24 GMT  
		Size: 19.6 MB (19637064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cd60449a753bfe9236207423a8806bc8d08d0ae447e19cfe1f77886280f5d7`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4454bd10f761ba3d1885f14e6fe26bc4f7f7f78760a7206bb26ab7b0d1e976c4`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8a1a03dae952b8ba6d5d05d145ef61405f1bb08e8555f2035057f17c4f6e9ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9ad5e8fb0550a3eb48e9250df6e0cff5428b50c2414a70a2ad6bf11a12fd01`

```dockerfile
```

-	Layers:
	-	`sha256:26d592247920f3120e5ca11dea4811e256aacf2600a53882fe5530222ea0901e`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 4.3 MB (4284499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d2480867bdfdc234bdfe874181b3cc6f31497f03461ab7e313d86671167353`  
		Last Modified: Fri, 08 May 2026 00:26:23 GMT  
		Size: 19.3 KB (19317 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cda5e3cea133b5a1a1fd49edb9d1b9a946d4f640f68107151515c6fdd03c38bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235228643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44186dca7312c123e901a2cf2b9aaa40803561a77ee00ab7dcbb0adda6a7060f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:35:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:35:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:35:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:35:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:35:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:35:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:36:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:36:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:36:13 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:36:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:36:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:36:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:36:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0398f5f2459bce57485cbf20c7c00c0cc4acd23743ed54d0ac36f4b1a739a3a`  
		Last Modified: Fri, 08 May 2026 01:36:55 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541c5703a7b7340507844b07f8d626073251d495efb65ccf0abba853af9fa90b`  
		Last Modified: Fri, 08 May 2026 01:36:52 GMT  
		Size: 20.0 MB (20030483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ba6f28e124233c168e6fa2940e67395ef6ecc70f915af44d9579c97386ce1`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc0362590cb2d90b00932e39ba3a4c486c5f75995d0bad62a98ee37994c2b65`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:52d79e74749c3b78aeb88160ae0cd5a4384799d21df9d15780c144dce3a4a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930aa8d66a5d1b702bba596dafbd52acd1d5c75512877818c5bed150c971959d`

```dockerfile
```

-	Layers:
	-	`sha256:bb184743dcf9d4630f1d1976eab5baa103172ee362c6649632a3b47196dc4358`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 4.3 MB (4286733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd93ebee90bd62fd0559638452e406f272606081c49e5fce467e095d15ac7a7e`  
		Last Modified: Fri, 08 May 2026 01:36:51 GMT  
		Size: 19.2 KB (19228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d595546822cb30beb390a36a2425c1fc6c014b276e37e8ae5396ed8a7deabc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218521241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc9f8ec2be573da87d563bac57574eefc77bc89e86e3da40a98fa2bb3ce49db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:31:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:31:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:31:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:31:20 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:31:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:31:20 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:37:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:37:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:37:24 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:37:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:37:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:37:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:37:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e128a9aae85e9c715e158acadc4f1eabae844fa259e97340ec467a999b6a5c49`  
		Last Modified: Fri, 08 May 2026 00:37:56 GMT  
		Size: 147.4 MB (147388364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d689f07601bae4080b7522547987b2762675b0da90dcc25cffa46a3e4112b9`  
		Last Modified: Fri, 08 May 2026 00:37:54 GMT  
		Size: 19.5 MB (19466764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdddbdc70614ed5fbb7ecd2f04d82cf18a30ebf5b2c44eadab21f1c558296ffe`  
		Last Modified: Fri, 08 May 2026 00:37:53 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835a9465f95a2575456ca1d918c7caef3b6f6f0f07a153498749b6747d239fc2`  
		Last Modified: Fri, 08 May 2026 00:37:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cda2f5b3e696fe1175995c2c8425e349ecf7e1eeed7702df1098b27942695725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb00d5dc92a0b998bd9aac1027a0d3605f4cc2a4f1fdcea61042806b36d30df`

```dockerfile
```

-	Layers:
	-	`sha256:5d42ecea97dece5954210e889e75268b547d68f0e20927719140395d117ca7b3`  
		Last Modified: Fri, 08 May 2026 00:37:53 GMT  
		Size: 4.3 MB (4276674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c89d82afe3c7a65dff52ffd2418d53444ae7b74c42dc79db120325e4cfcb824`  
		Last Modified: Fri, 08 May 2026 00:37:53 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json
