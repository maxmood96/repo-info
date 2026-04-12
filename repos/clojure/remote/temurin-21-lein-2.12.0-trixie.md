## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:55346dd72029d5bbf9ef435e4034542b2d4242bc2a5ccf31d6746eb2725c1686
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

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:298f7fa59240f7ed9eabc16e399054526d2b55a38eeaa028f369133f566f65ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230258239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62c67c156350a55482f0a890d0671a012163d20293300fbc164968d1a8bc764`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:15:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:15:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:15:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:15:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:15:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:15:44 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:16:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:16:00 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:16:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:16:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7d56698ac12496fc7173df7fa8345314be2e5798b9ad56aabb97d30582640`  
		Last Modified: Tue, 07 Apr 2026 03:16:25 GMT  
		Size: 157.9 MB (157857091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a77e2b2cfa7c886f79ab35fcd36c22aacd9c94f7399eb0455c6cbe562d0070`  
		Last Modified: Tue, 07 Apr 2026 03:16:22 GMT  
		Size: 18.6 MB (18585146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad4103daa5b5af4b8c9dcea6e7d32f1286e2f321bec6b7e3fec6d2ac632a4ea`  
		Last Modified: Tue, 07 Apr 2026 03:16:22 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b022db2d45149bc367cf38f391d3904cc2716337c3bfe17593b5587d637750a2`  
		Last Modified: Tue, 07 Apr 2026 03:16:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2b4e7c272c4ebd6ff73c955ca0d97b6484dbf81d3c8c72a4c2e4a71cd0f82a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158923a6340018cf93909259fddfe6a50f3aee34dde01ad57dff2002073fa407`

```dockerfile
```

-	Layers:
	-	`sha256:f79c82459083edd54e4ea69cfde90775ff654cfafa4b4c490097f231124effd8`  
		Last Modified: Tue, 07 Apr 2026 03:16:21 GMT  
		Size: 3.8 MB (3817379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d61ce0d014400c28b610b8fbf3a04e238445dffdb2b68520ba1d078835d242d`  
		Last Modified: Tue, 07 Apr 2026 03:16:21 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e1abf7dd3a620ba924f8a4bbd175f5f1a6f46e5a096651c4c27f0bb1d5fd6f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228861175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbecb2a4bc23e426d606008da76505a55d0202b26853d0105bf2e85df3ef515`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:26:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:26:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:26:35 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:26:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:26:52 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:26:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:26:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c1c3a34ef57280cf5c0e533c81d90c0e60f26075860ec24985d325b0935a93`  
		Last Modified: Tue, 07 Apr 2026 03:27:14 GMT  
		Size: 156.1 MB (156133064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2caa4c52f9ed7152013135c948cae429ddb8788a2776dc988fde2481433f75`  
		Last Modified: Tue, 07 Apr 2026 03:27:14 GMT  
		Size: 18.5 MB (18544726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f074a21ebc2cfda1a558a094bbdfbe6ae3d724ea3d3ce55b922f3a9d4ba0232e`  
		Last Modified: Tue, 07 Apr 2026 03:27:13 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2886928c9fccb94bd16c58a574ba0cb61936e6dbadeb1d788988349226c4f14c`  
		Last Modified: Tue, 07 Apr 2026 03:27:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:efc00b11b3d7cedb6fbbb006687995f20300961ce64c7f95be9ef3c01743cab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a53bc530753ddc1d6b30de52cf19df26617ee4bea6b09742f309e9285bb8a0`

```dockerfile
```

-	Layers:
	-	`sha256:a5b8632d7b63c9a3d0f4280ed6ee8757a282d715f3358a3768e77669f31420db`  
		Last Modified: Tue, 07 Apr 2026 03:27:13 GMT  
		Size: 3.8 MB (3818256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f3d71bde48b54dfd3fc601d9a43b5105e6cfd88843f51982e4b555c024f33d`  
		Last Modified: Tue, 07 Apr 2026 03:27:13 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2454acbf5939706a20f352e34d8f3b44efff9981c356bea79d84bb1b558863b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234255251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba39f3c7d918bf52c7588a47a56968703b43a8f1cb3a5e690edf3478d4ce93d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:47:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:47:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:47:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:47:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:47:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:47:41 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:48:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:48:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:48:32 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:48:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:48:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:48:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:48:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dae9dc83e459c0aac03f4da141b2222e67e4c531d619bb7dabf0549311b9fd0`  
		Last Modified: Tue, 07 Apr 2026 14:49:20 GMT  
		Size: 158.0 MB (157977541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776aa01d52077d6c0143b43bd6d28a8953fd333afb636ca91e350d9f92c6e725`  
		Last Modified: Tue, 07 Apr 2026 14:49:16 GMT  
		Size: 18.6 MB (18640845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a0fb9d7c2ddecc99307cc822d4a0bc6eb0c7386b1dd3b0b883df447080ae9`  
		Last Modified: Tue, 07 Apr 2026 14:49:16 GMT  
		Size: 4.5 MB (4517766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec8b5243d42ec54a6e45cfbdbf61e7c6f7a355cac787f4a3e0688d5f51ca581`  
		Last Modified: Tue, 07 Apr 2026 14:49:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f3ebb3f6eecdda6905352cd3adf67b7bd33d4a291f86d22638e80a4bb75a45d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9de31357d81c042d0979464017e3b039d433c5c7cdf343ef7e81b7bf468bab`

```dockerfile
```

-	Layers:
	-	`sha256:b826b7451d15dfc49ccd0f7ed041a28d690449ff8436439bafae83bfb6441fdc`  
		Last Modified: Tue, 07 Apr 2026 14:49:16 GMT  
		Size: 3.8 MB (3818379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaaeabf77fc6adba192d7143b49db9d31e8a5cb95e8338922b2e11196d4c7084`  
		Last Modified: Tue, 07 Apr 2026 14:49:15 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:342c836a2424754be1fdebb843a977294078eb0e5ef6273cc1dfc77907376838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.2 MB (231223921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd5f22a1787eaada79e13f6206a261026f87c452104abda6d0e3ef936bd447a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 21:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 21:53:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 21:53:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 21:53:48 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 11 Apr 2026 21:53:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 11 Apr 2026 21:53:48 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 21:55:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 11 Apr 2026 21:55:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 11 Apr 2026 21:55:24 GMT
ENV LEIN_ROOT=1
# Sat, 11 Apr 2026 21:55:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 11 Apr 2026 21:55:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 21:55:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 21:55:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2e07983918932b6a7d3f5b469a0f96350899d0eb2de01a34ca1ec47825c8ec`  
		Last Modified: Sat, 11 Apr 2026 22:00:22 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e5a28b485204477d524eea38e022437aaeff4d9b3784e1cc57e569a9647aab`  
		Last Modified: Sat, 11 Apr 2026 22:00:02 GMT  
		Size: 21.7 MB (21696175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b29c807c1ea424013655c38985382b6edd4cda882bfc561933aa8c13cdc6d2`  
		Last Modified: Sat, 11 Apr 2026 21:59:57 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3258811f6b3373510ac2c8fb02d7ec3056f6c7ec3df3764e4ccbbc44bdd22b18`  
		Last Modified: Sat, 11 Apr 2026 21:59:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5e87e66027e72adeec6f0356c8e8a1f47dca1e76ad7fa87b34f3bf7c13d74ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d1bb772adcde47b077efee756cbd15db07663157f6fbddda2e7337e36b81ae`

```dockerfile
```

-	Layers:
	-	`sha256:bdab5e961fda88046fb66c9f287b652f5e470d755decc75299509f0a7f163d3a`  
		Last Modified: Sat, 11 Apr 2026 21:59:56 GMT  
		Size: 3.8 MB (3807856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c12aee0c6c2a9a6765dad4fc04e9eb80cfbbec9a90a96b2816fbb33ae1113d27`  
		Last Modified: Sat, 11 Apr 2026 21:59:54 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:70329516c1dad2f82b3647caa46a1e5f509ec8e64197c69d397090016c8406aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219614842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe938c64b35f89689816e8d3ee1520d93e60e2eda7507863f75efda06798831`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:44:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:44:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:44:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:44:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:44:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:44:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:45:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:45:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:45:08 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:45:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:45:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:45:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:45:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64db56f7965b765f0e39653c084418dd2902ad80e13793882547069cfd06d5d`  
		Last Modified: Tue, 07 Apr 2026 05:45:37 GMT  
		Size: 147.1 MB (147105311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4217f88a61aec13e11290047bac3d519eeff01a23dba12b7605ef3b7cc218826`  
		Last Modified: Tue, 07 Apr 2026 05:45:35 GMT  
		Size: 18.6 MB (18626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf90cb2d8df1765e9d76060227db3d14c720613b9bccecd70c14483fc381ed0`  
		Last Modified: Tue, 07 Apr 2026 05:45:34 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa55b355208291ef28cbbc4e9c63890303ac0b6c6bba0a5ac16f8efde3a672`  
		Last Modified: Tue, 07 Apr 2026 05:45:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:991cebf083385c1f638fe95a1e25dd431da22ff985e082f612a1269e4e6d38cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab492c4c9ff373c133df7930e254a20cd746b2cd72b79693b156d1bd3c000752`

```dockerfile
```

-	Layers:
	-	`sha256:5e56a3245ec9ccefe386211170898d87319a2d35d1265c73a0dbb1b75439d063`  
		Last Modified: Tue, 07 Apr 2026 05:45:34 GMT  
		Size: 3.8 MB (3813806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125055f75787030304fb88a6702e991b877cacd9bbe5b551f42c2a4cc5fa22b1`  
		Last Modified: Tue, 07 Apr 2026 05:45:34 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
