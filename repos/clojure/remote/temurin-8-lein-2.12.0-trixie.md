## `clojure:temurin-8-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:97bc53556d5398e479fd24dd960732edadc8dab5f65fa4c93c34525b80838183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:75b6935aaa54a47dd91abbd49dd6e741f9b83ab142e541b5f79182cb6224711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127575377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa551e17e17cd536c2d065c01139163ff51842e3ee012d7f25cf5d46b3e533d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:15:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:15:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:15:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:15:33 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:15:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:15:33 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:15:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:15:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:15:48 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:15:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:15:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4c6eddb49a6dea41bde5b5139d9e28a0787e2120d7ec0340d083af949e53e1`  
		Last Modified: Wed, 22 Apr 2026 02:16:04 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cb09ce1997ddcbb2474942f84101555d2fe9b660e1ca664b2a1cb84f3a23b2`  
		Last Modified: Wed, 22 Apr 2026 02:16:03 GMT  
		Size: 18.6 MB (18585461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d077cd79c2a16ad6ab4fb0ac875bbf2c0b3f9e388201d72615394c3f339f9b53`  
		Last Modified: Wed, 22 Apr 2026 02:16:02 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5ae713c890ad238ae6bcbde8a7d5635f65157f9ffd06d6b32a31ddb168926481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9edbb19286dfe01c6336e1f944499f5a1abcb49737fc470e5baf7f22247eb7`

```dockerfile
```

-	Layers:
	-	`sha256:5460d5399b3b839a3fffddb671a794c4f73ed4d62b66f0b219621d559ae8a850`  
		Last Modified: Wed, 22 Apr 2026 02:16:02 GMT  
		Size: 3.9 MB (3936516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ed8b565dc3a1c9594553400c2fbbc5b436807bb8e4b4f88843e911a75fe821`  
		Last Modified: Wed, 22 Apr 2026 02:16:02 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1776717920682b3712fe684198a3dfe748329346582c591bb4310d15b465fe3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126984102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3e61f2cab0aa33219068d2c4848b0423b530c6680f6472f48fa8ef877f19`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:10 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:10 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:27 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22606997067ab8451bc232fe95c1c369bdc4419b9cdae694d6baaed69249f329`  
		Last Modified: Wed, 22 Apr 2026 02:19:43 GMT  
		Size: 54.3 MB (54251621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c0b37507ab1de090cb9ec7376dac169693cab90919c41411d4832c6960fbbe`  
		Last Modified: Wed, 22 Apr 2026 02:19:43 GMT  
		Size: 18.5 MB (18545480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80902da9882fdccdc434b4e602de787ebac6f19a754b493949f15f012d51f293`  
		Last Modified: Wed, 22 Apr 2026 02:19:41 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:000f78f0a2b1161781bc08b546208ae08851afa42a493effd50e222a1aa4c5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db6d088699fa2ef4228db61aa3a12b74e60312c756c11d300b5586a3671dac5`

```dockerfile
```

-	Layers:
	-	`sha256:76e121aa1e27210c679c48911c32571688e14772abcbf02093889da20273ac88`  
		Last Modified: Wed, 22 Apr 2026 02:19:41 GMT  
		Size: 3.9 MB (3938093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b8e09bd0701d6706693429708a42fd79e8602098ad990f08ed606b252b3202`  
		Last Modified: Wed, 22 Apr 2026 02:19:41 GMT  
		Size: 16.5 KB (16472 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8d11682aa19d6ad95252ab13603bd5bf4072418c95c1065e49343cad730a4eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132678435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f90470599e1c8b63a0d82bd446c538a9c693f1ef33c6edb0f976aed08b46908`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:32:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:32:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:32:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:32:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:32:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:32:59 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:33:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:33:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:33:37 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:33:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:33:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d12c2460cb3461975521962c8f8a97ebe891068bcf626491de7565aee72a3dd`  
		Last Modified: Thu, 16 Apr 2026 02:34:16 GMT  
		Size: 52.7 MB (52650393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35262fed6978e00366e607f0905174fb118d24c23862a851f40b420c538fa702`  
		Last Modified: Thu, 16 Apr 2026 02:34:15 GMT  
		Size: 22.4 MB (22391583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7adc91acbda0fa8fa4ba09617ccb51b67da8dca03a432f1d8bc741c4d989aa`  
		Last Modified: Thu, 16 Apr 2026 02:34:14 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b8d0740c0b596f8afcdf735784db7d3e438a34d2cd598b2cbc8b09b5b6c83e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16bbb2dfc3f9f68543ea1f5e9937d0025bab340e95b45e7dd78962f2d60f224`

```dockerfile
```

-	Layers:
	-	`sha256:08266bdc74d02f50dbfa731f8518122fe3c341d2d566f932a1978a571701f6dd`  
		Last Modified: Thu, 16 Apr 2026 02:34:14 GMT  
		Size: 3.9 MB (3938111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a499e2bc98011620f5ae1598d5b69f0e156584ca9170919500c21f21dd2506f`  
		Last Modified: Thu, 16 Apr 2026 02:34:14 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
