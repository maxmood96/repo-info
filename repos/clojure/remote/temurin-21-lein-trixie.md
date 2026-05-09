## `clojure:temurin-21-lein-trixie`

```console
$ docker pull clojure@sha256:70bf695b5a30e304a2ce36fdc4807fa0cfa7bae439d1c25dfe3c97a8d5b962d7
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

### `clojure:temurin-21-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2a6e432b315853b93dc0297d4ec38d95e96c46af0b4eec9f3df5b55a55cad324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230572943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e45a5c442cf762b47559bd2e7ed5f4fc7649b36ddb6830cfe5b342f9fed6a11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:16 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:18:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:18:16 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:18:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:18:32 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deef58af2d26605709799f89ccf0b7a19697e70666e067f35783f79f576ca261`  
		Last Modified: Fri, 08 May 2026 20:18:56 GMT  
		Size: 158.2 MB (158166923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e09c737968b879a2bf82f6332d3404bcbcd236953eeefb9c11425cf1b880ed`  
		Last Modified: Fri, 08 May 2026 20:18:52 GMT  
		Size: 18.6 MB (18585552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6db3333012e73aad473bb67e2fd9fe2bbf8135c1aa1640f8c2fb78f2d05da81`  
		Last Modified: Fri, 08 May 2026 20:18:52 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48c571b6986a4f78e98143ffbf36fbe930bcb84085a104de4310fe44ccfb6fb`  
		Last Modified: Fri, 08 May 2026 20:18:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e182c4d315e7983cebaf3bb8c75e939ff77271e6f6f786c3adffab63ebfe9d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b146997a8d7affa39690a9b460a73ad9abe5a49ebb49f4dcc36e0f76b8f2c8`

```dockerfile
```

-	Layers:
	-	`sha256:4e6c9ecf7f5746e41f66b34ffa5bba1be35717680add24bc6feacf7466dc52be`  
		Last Modified: Fri, 08 May 2026 20:18:51 GMT  
		Size: 3.8 MB (3818006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:344234dc25a3585848740ac60561b6af0df60ff30e6aaf3721f48badd85a9ae7`  
		Last Modified: Fri, 08 May 2026 20:18:51 GMT  
		Size: 18.5 KB (18506 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f403a658184ef0a0d26ec3330b4df1cf0a5727a0a90bb269d6eb80b9dd8e7264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229194336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d553d620e2117e7e30bd532ebf6679f14ba2f27d827bb8c0c355b59061c6407`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:22:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:24 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:22:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:22:24 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:22:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:22:41 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:22:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:22:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaea314d40f0c9320bb6e7a103589b66dd9247981c7640f8c6d00a576be4a75`  
		Last Modified: Fri, 08 May 2026 20:23:05 GMT  
		Size: 156.5 MB (156461272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9e325c6c8989fd29402c846dd7fa74f1fc62825b819ac2c6e4811ebb481b09`  
		Last Modified: Fri, 08 May 2026 20:23:02 GMT  
		Size: 18.5 MB (18545437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d637cdd54839f65da28326777165e7bfa3e904fe0bc0ed6ba63417cd1815de`  
		Last Modified: Fri, 08 May 2026 20:23:02 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cd1dbece31c10661d7bcc6f63eef5404c89b6180971236159c3ceeae6232e7`  
		Last Modified: Fri, 08 May 2026 20:23:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:818e64aaac34ff5a8314e228c93dc74b796b290804abe164fa70feb6b963e187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35edefde0ecd625050fcdce30563a05955a2d12274b61cf48fe2595c45193e7`

```dockerfile
```

-	Layers:
	-	`sha256:79c13f1aaf3cc1ba77069ad25dff3214327125a9baa174ed3560152f0a52af24`  
		Last Modified: Fri, 08 May 2026 20:23:02 GMT  
		Size: 3.8 MB (3818883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ee3cea2d2d400a1cf24736979bb7b302d87c471a77abdc9450d5d4726673af`  
		Last Modified: Fri, 08 May 2026 20:23:01 GMT  
		Size: 18.6 KB (18627 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8590f56c6541271c87a24d7099113a0b701694e8d01d50e5f89385bfd2eab556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234625394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd49b8044c353b2fd9ca0c5b4f368b8754f33a0803cf39e362b8c8156dd25ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 01:38:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:38:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:38:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:38:05 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:38:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:38:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:38:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:38:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:38:39 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:38:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:38:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:38:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:38:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef2aeb89dd432248a27be9658c9ad2fe8736e1bb0a40602c7b1b444a977ed1e`  
		Last Modified: Fri, 08 May 2026 01:39:21 GMT  
		Size: 158.3 MB (158343239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748cf280f6b471c4065778f2a810fbbb535e9293d68eb100b11d1d99a495581e`  
		Last Modified: Fri, 08 May 2026 01:39:18 GMT  
		Size: 18.6 MB (18641002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2929e2060c35294dec2e5300200e09d0d87897fb11382524a6f91c877dbb5d34`  
		Last Modified: Fri, 08 May 2026 01:39:17 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94318bc6637e9adc3364a12237a6d9526e686133933b8245043a549a423a619f`  
		Last Modified: Fri, 08 May 2026 01:39:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:780bdb11e1c0b25cb43481ea49c70c8d1c97af0504cff70b38a0716206ed77c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3837556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb63659f9f76a18c5dae576375ad799f9fd2aaf14aed41fc83884d615a6ee9a`

```dockerfile
```

-	Layers:
	-	`sha256:30f3a7fb178151bf2545f6d848c60abaf769e5a33cfd0f6ff9f9675dd9d7ee4b`  
		Last Modified: Fri, 08 May 2026 01:39:17 GMT  
		Size: 3.8 MB (3819006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211ef3a1a874b33e37722bbac3e1cbbed3d78a75e0a8e645a383c37c6ddd635c`  
		Last Modified: Fri, 08 May 2026 01:39:17 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e1e6ec957a18083d174010f72408db64d5b8bd96fe86abe5956b319085aa7ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228071525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bfa85d7ac8163066e446b62e13353e5d664441d8974da58eeb956c81d35eb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:09:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:09:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:09:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:09:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 24 Apr 2026 18:09:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Apr 2026 18:09:44 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:11:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 24 Apr 2026 18:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Apr 2026 18:11:21 GMT
ENV LEIN_ROOT=1
# Fri, 24 Apr 2026 18:11:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 24 Apr 2026 18:11:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:11:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:11:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d4384d0aaf4c67d90bf2e07cb4852bca10fcf970d4b6c61ba3f1acafc7915a`  
		Last Modified: Fri, 24 Apr 2026 18:16:13 GMT  
		Size: 157.2 MB (157216912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1abf9bd70e9a882571c42e9955460e7695282f7fd72cd7e61890ea7e182ff1`  
		Last Modified: Fri, 24 Apr 2026 18:15:53 GMT  
		Size: 18.5 MB (18538170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4d67f3c844d17dbaa6186223ea2349dd4c649c30eec5fde5aedf2ccf303b1d`  
		Last Modified: Fri, 24 Apr 2026 18:15:48 GMT  
		Size: 4.5 MB (4517796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142daaaac6e1affb28294d0bd80b652fd54e6dbcb1a43ff723b889d8ebeed938`  
		Last Modified: Fri, 24 Apr 2026 18:15:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1de1aec204e13ac6433d356457ae0968d7385e328a21a209e818efc5ea6cf20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77cd986089425f0474855e1835e95842fd042ad865be71a6ec99b891239b0c9`

```dockerfile
```

-	Layers:
	-	`sha256:4041bc6b43b8b25590af4627b8c0d455c357c78cd3a55deb8450ceb1b1d85910`  
		Last Modified: Fri, 24 Apr 2026 18:15:48 GMT  
		Size: 3.8 MB (3807856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fbdbc254298d730e1a9078c67f24c577048f9245838c8e8d6b4aeeedb9d2035`  
		Last Modified: Fri, 24 Apr 2026 18:15:46 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2db548eedea966ca420ac75180cebc017422438dfbcb6621e2acd9a4213d7d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219905483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cde28b12936712866ed24768193596853ac9c67c7bb943b7fbc4cc849ee0b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:17:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:17:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:17:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:17:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:17:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:17:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:17:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:17:57 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:17:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:17:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:17:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:17:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322bcf3d705f2cea437ef1917f9da7ff28c4e9884b7d8a103b1f9bdb9098e5dd`  
		Last Modified: Fri, 08 May 2026 22:18:28 GMT  
		Size: 147.4 MB (147388345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a817fbcfbf6d94c231ffd60ebab05c93da7e0e7a9afa8a38b991aeefbfe93eb2`  
		Last Modified: Fri, 08 May 2026 22:18:25 GMT  
		Size: 18.6 MB (18626661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685e99a7da41ee590618a76a5809ca87138ea606512922fb595053349c088a22`  
		Last Modified: Fri, 08 May 2026 22:18:25 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776db5b1c2a4bdaf3133640e23c1d8e8f48ae98d88cc9abb2d96e3f532706a6`  
		Last Modified: Fri, 08 May 2026 22:18:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4a1a7ad9084fc81797c2551107320cdfdbd69fc73f52f69b69006845f582cdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0f897d5eeaa45b0c5d6ade90ad187d82ceba7f6b5e6e01ba526c33fdb5f2a4`

```dockerfile
```

-	Layers:
	-	`sha256:971a7a2256d1e58cec77eecd9891d6ec52440d9500fd98c407c6348d6a697079`  
		Last Modified: Fri, 08 May 2026 22:18:25 GMT  
		Size: 3.8 MB (3814433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b8aa7a9391d86e1c08d83dddeadd1dcc5e2eeadb1e79efe3ace890afa0768d`  
		Last Modified: Fri, 08 May 2026 22:18:24 GMT  
		Size: 18.5 KB (18505 bytes)  
		MIME: application/vnd.in-toto+json
