## `clojure:temurin-21-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:167fc889fce217f736bed93f5c70cf6f834c7aad2f93c962104eb11f7f60b883
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
$ docker pull clojure@sha256:639d74bb76d7c009461390f83cbfede97c76346788355ee2f8d3d7a5b9c52492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234254745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d9a974770fde16d709f9fffbdbd3e33b925ca0a3684b2fca37351b7c43b7a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:37:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:37:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:37:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:37:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:37:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:37:33 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:38:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:38:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:38:13 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:38:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:38:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:38:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:38:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3ec6fdaa48a78814b25d06b8958fec2609466001981f561b8114f6360e796`  
		Last Modified: Tue, 17 Mar 2026 18:39:04 GMT  
		Size: 158.0 MB (157977471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a206e281c923444f8491394c9b3e03f099c48161a173acfd41ff41d36b8a898`  
		Last Modified: Tue, 17 Mar 2026 18:39:02 GMT  
		Size: 18.6 MB (18640735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5bc9386983f29420bf635f5e6972ada5958cadbda0c925ec21188bbd9b5991`  
		Last Modified: Tue, 17 Mar 2026 18:39:02 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc8489d45e8db423d8cd6325703cdb9d8771f22d0ec806c733000a085e7953e`  
		Last Modified: Tue, 17 Mar 2026 18:39:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a7d3e0d46f799e4be2c8f0d2bdcd733a372d6b4106148aa25daef694a6e8e432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10c66b53f5dc243c0435a77f47cb2237d03431fd23d828ee50b345e694a2398`

```dockerfile
```

-	Layers:
	-	`sha256:9061a040991a7717ab17d44968b39104e1f42ecb28aba18e3f203348201db209`  
		Last Modified: Tue, 17 Mar 2026 18:39:02 GMT  
		Size: 3.8 MB (3818379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3ac0745069d7e38070bc0e1fc3c7475696f67edbc65b2635a7c83bec9c6978`  
		Last Modified: Tue, 17 Mar 2026 18:39:01 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:64106f8f930715a06be69a77d234a8343297238d793adf82227ed728a44a3bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228065053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4bd868e4701e75e8420c681a8e7ce069a9adb2a821827fcab0bbde567fce17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:48:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:48:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:48:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:48:58 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 22 Mar 2026 18:48:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 22 Mar 2026 18:48:58 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 18:50:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 22 Mar 2026 18:50:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 22 Mar 2026 18:50:33 GMT
ENV LEIN_ROOT=1
# Sun, 22 Mar 2026 18:50:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 22 Mar 2026 18:50:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 18:50:49 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 18:50:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248da4038c4f4bc829cf60fb1b9101715933fefeff01226fdf6e29839b9227b5`  
		Last Modified: Sun, 22 Mar 2026 18:55:14 GMT  
		Size: 157.2 MB (157216869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5540ac904245cc5cb695f1c81cc7cc58f62d8d50930992ba4ef2c152e4b4eb29`  
		Last Modified: Sun, 22 Mar 2026 18:54:54 GMT  
		Size: 18.5 MB (18537645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bf9c0f29fee294ced0923ce19ba3752b82b9b4e621f20c6dcb9abda09911d9`  
		Last Modified: Sun, 22 Mar 2026 18:54:50 GMT  
		Size: 4.5 MB (4517782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215fe0511e8b7ed9e752676d4fbb0c881b72de6ca660d9444790a226aa0715f1`  
		Last Modified: Sun, 22 Mar 2026 18:54:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a50109a0f9fc97ae0d268bd123dd9943979684e01ee7cfbbf0b8c15e05c8dcf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83f1d5e1b9c5d756414d76566bb5597fb1fb0cda21dcaeb687167a7e53d7b3b`

```dockerfile
```

-	Layers:
	-	`sha256:447b747542756b057a0afc6683ea96a146935e0061509b7eed1f636631c4a30a`  
		Last Modified: Sun, 22 Mar 2026 18:54:49 GMT  
		Size: 3.8 MB (3807856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb603839bf21cdae004d19812559eb7cdfc28bfa7183bb510b208442f71a71da`  
		Last Modified: Sun, 22 Mar 2026 18:54:47 GMT  
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
