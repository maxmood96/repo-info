## `clojure:temurin-8-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:44b7ac4fdb4de2f0e267fc4a057042b665c796f43630f17cd8953dd0a5c69efc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bbdbb197017e2efbd023dee6f3ca876ad4b56a23c8db6697176ac5fe4520d842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127979575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f324e4dbf69b67494ad6f8a9b1b61a11fe9be1fc6e5d22dbb95d0c0e49beb9a4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:20 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:12:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:12:20 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:12:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:12:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:12:34 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:12:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:12:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4d6af1c974d450f20472eeca9a58bf86e16db0c70a270f1ff2896064c992e2`  
		Last Modified: Tue, 07 Apr 2026 03:12:54 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175a085de941776c7cbd0010b907718ef0c88e024065384c071609eb0ef12af`  
		Last Modified: Tue, 07 Apr 2026 03:12:53 GMT  
		Size: 19.8 MB (19802856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f586358bea02d08a9c733e0745789ca7d45a7bfb000496305298f23d3456ad7c`  
		Last Modified: Tue, 07 Apr 2026 03:12:53 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:380c648520d758623003267a9c5cdcc2369fe089ee7f278fa9c1177f7908ca3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407607af2193a0debc15c0e43b35d5e674aa8dcd70527b7e8daa9bf7d0e96d12`

```dockerfile
```

-	Layers:
	-	`sha256:5c787fb2686df6a4671b833a7bd9a59c4784cf7b23d8bead135b018fa16dbfdc`  
		Last Modified: Tue, 07 Apr 2026 03:12:53 GMT  
		Size: 4.4 MB (4402720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d9a56bc26d10bdb7ee45f4490049acc0ece5d1a735a1e5ed670f1da68bccae`  
		Last Modified: Tue, 07 Apr 2026 03:12:52 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:583ec6c4ac0fb8026ec9f2a8ae99ccd15525633d28d9896329278e3efa0073c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126775443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1260952fd75c44fc632e49459b4104463c7f0b0f02c84dfe6b23a911806df35b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:22:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:22:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:22:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:22:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:22:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:22:47 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:23:00 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:23:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:23:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da62b28ec00a3bedfec498c778ff32347b94037808959e4c39657bddb7fd05`  
		Last Modified: Tue, 07 Apr 2026 03:23:16 GMT  
		Size: 54.3 MB (54251631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc2e31745b4a9a3c47d444fe6b9159c0ca769909d18b4e6cb5a0f5b93c0965b`  
		Last Modified: Tue, 07 Apr 2026 03:23:15 GMT  
		Size: 19.6 MB (19632804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc4b363376dec217f1766aab6943b88bd43d5c9423fbd59acd54b5c18412f82`  
		Last Modified: Tue, 07 Apr 2026 03:23:15 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5e2186c7f350b4661cf4c962c4e95b0689d5654636c43da6352ad415eb84e8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1f413a68282b0f3ed891fe61ac7820c0bbd11693c84d1883a67ef9f1b1f7c4`

```dockerfile
```

-	Layers:
	-	`sha256:e73ce430240d93a678874fc634fe168f15d3a97d94e059055ec3e20982900c04`  
		Last Modified: Tue, 07 Apr 2026 03:23:15 GMT  
		Size: 4.4 MB (4403035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3fb80569fa5a15fc4343f955ff5f0f0a2e32a75c41f70ab1db690aff0601d8`  
		Last Modified: Tue, 07 Apr 2026 03:23:14 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0208d0dec1874cc4fc4485c4e7e845ddbd1406189ec83cd53088347420f54a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129528635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f68004e79229e70f4bba9a5c78435276b8c0dc473cb9a8ea5a171c796a011`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:05:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:05:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:05:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:05:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:05:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:05:08 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:06:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:06:46 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:06:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:06:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd8a512f09ca4bc519a670ed8fd28c926eabe017586c8482ba206fe3cdd0ed`  
		Last Modified: Tue, 17 Mar 2026 18:07:16 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d64d8fe264b1b10b1d0fe8089e32c9d1b52de91c402503e83bd94349a339ce`  
		Last Modified: Tue, 17 Mar 2026 18:07:15 GMT  
		Size: 20.0 MB (20023753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98272585dad32d121c7fdf4d258f2060f3cb8b020a1232e210d2ee630490695`  
		Last Modified: Tue, 17 Mar 2026 18:07:15 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7f1bdc28a9f6f4528d56ecc63764f154180dfef38f1f98d1c7601949f1432453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4421590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac8bf63113225cacc032d64c07627723670edbdaa3251329aee300cb2f52d1c`

```dockerfile
```

-	Layers:
	-	`sha256:79029979e50ed12c0e7e1a8836d05d91f77e12ad729c9380b47f0f97a886c6df`  
		Last Modified: Tue, 17 Mar 2026 18:07:15 GMT  
		Size: 4.4 MB (4405176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d56ad637e1508d1d07791006a5786951df18626617a2d44723a4b5f2c28f85e`  
		Last Modified: Tue, 17 Mar 2026 18:07:14 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
