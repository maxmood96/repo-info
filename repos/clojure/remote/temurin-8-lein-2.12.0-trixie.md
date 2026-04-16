## `clojure:temurin-8-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:3565f18cceb01b56ac1107753803002d30de6c87e4f1b073bb3a4f80fcf803ac
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
$ docker pull clojure@sha256:b997253cf41ee733494bab084f6e8bcf6461302455c831c18143698b0ca933cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131074913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74080542a0adb7e2bbcf30628a9b80aca650af7a0c665151b2562a8b4a5322ab`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:01:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:01:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:01:16 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:01:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:01:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:01:33 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:01:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:01:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cc69f4bf26264994826fa7ccda4a39ea64b2bf56d3687c1c48f18d4743498e`  
		Last Modified: Wed, 15 Apr 2026 22:01:49 GMT  
		Size: 55.2 MB (55170111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e326b14545e78dcbdff4790b16fecd791d7c45b4990fabe6a37026ce9bc83f`  
		Last Modified: Wed, 15 Apr 2026 22:01:48 GMT  
		Size: 22.1 MB (22089219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168a94fd71437405cf4b303ba64c3ae64bc0ae163b86fba50cad1b1e7209f070`  
		Last Modified: Wed, 15 Apr 2026 22:01:47 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:371176d612beeaa640b9ba919232a78ab0082ccb1feb5f2b184949605ce15cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb021e0acc0e9857da372653a5a1339187b7b1b7ec2a455b9c4eb551ff004b7`

```dockerfile
```

-	Layers:
	-	`sha256:943027266bfea6143b08dc7d29f363660cc217776e3e034c1d307b9fd19ac297`  
		Last Modified: Wed, 15 Apr 2026 22:01:47 GMT  
		Size: 3.9 MB (3936516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa920ee2c13bcb9732711790eb71151d534b1a9584bd51c769076623e59253fe`  
		Last Modified: Wed, 15 Apr 2026 22:01:47 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1950955ade1e70f629be5d7337a60268472db86252f848a95fdb8bf61ff2dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130858897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6edc3016aa83fb0d165496367d261b380ce425675201fadd436000998098f9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:12:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:45 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:12:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:12:45 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:13:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:13:03 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:13:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:13:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b837cb74508b420fa79654beb94facdeb83d096f480f9bbfabf838c0bfe02`  
		Last Modified: Wed, 15 Apr 2026 22:13:21 GMT  
		Size: 54.3 MB (54251623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db16c1675e92506f815acb3b1c9c60d8c9f86677ded32f8e6673d1cfb2991b0`  
		Last Modified: Wed, 15 Apr 2026 22:13:20 GMT  
		Size: 22.4 MB (22424271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9baa9683a778f50d4c8512b1a250dbb4cea17d1d1d8500ac827d494445d4cf0`  
		Last Modified: Wed, 15 Apr 2026 22:13:19 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e4c5f74ef33d3c81186ba3fe01d58998cbf479e0d3b41f726f91bbcdc6939014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5bde516cdcb18bf73c8489512478dc7201560f9f7496c9e83d2a15a04226e63`

```dockerfile
```

-	Layers:
	-	`sha256:01e2777603b2c74f07b7e6794f3eecaaeb7f16d96eb61acd4354496e4a0852a4`  
		Last Modified: Wed, 15 Apr 2026 22:13:19 GMT  
		Size: 3.9 MB (3938093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6670beb587077383949ff4159e79b92c80fa1d6e219ca575fe986174453b7ffc`  
		Last Modified: Wed, 15 Apr 2026 22:13:18 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d91ab5f094dbcbd11e0e07f2d2722ba806f93298439842720673fcbb2da04cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128927706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2998a122062395c8a46f3995240c9a9f0557a0869ce828316cb62d58faab0e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:22:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:22:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:22:58 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:22:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:22:59 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:23:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:23:43 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:23:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:23:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de41bf7fd798d7a67da7d6002cac62ec5cd96ebd90175ee55ba10334fc7bac0b`  
		Last Modified: Tue, 07 Apr 2026 14:24:19 GMT  
		Size: 52.7 MB (52650418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a8f48c0d8c868ee86565114de7ed1c8bcfc4f51f6b96f4b94e69ce7df54dbb`  
		Last Modified: Tue, 07 Apr 2026 14:24:20 GMT  
		Size: 18.6 MB (18640815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab0393b20aacf31166c49ed4de6a170a699c5ebc5c7e9a7b0c588b8bbb639f`  
		Last Modified: Tue, 07 Apr 2026 14:24:19 GMT  
		Size: 4.5 MB (4517772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:257fa37bf23fafbc18995e27fcf2ac5628833d01d1fe40c1b5dcbd45ebff6247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae40d6b980f5c1384fca8d01d5922e1778d62502ed017a201d76e68143f41c0`

```dockerfile
```

-	Layers:
	-	`sha256:4176c4c50f5763f17cf2fc41eae0eb9e5b7e01a8f77c52d5ad8594f18f5a362c`  
		Last Modified: Tue, 07 Apr 2026 14:24:19 GMT  
		Size: 3.9 MB (3938111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dcd47ff174902b450c57b31ddcd6d15940b04974e17a497f742b44c6e1b07c0`  
		Last Modified: Tue, 07 Apr 2026 14:24:19 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
