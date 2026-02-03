## `clojure:temurin-8-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:412c5ea7033e228e7738cc459a444484655fefa76d463201f873e8247354ab17
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
$ docker pull clojure@sha256:8b4c2c880298a976a3e6893d0cba8545a261d4e5ede3638e50d3713f776d5aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127535559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c977764de933254015e12a8a1a7c6e1affc95b5a608e656c9b08968b0fc0206`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:17:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:17:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:17:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:17:09 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:17:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:17:10 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:17:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:17:25 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:17:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:17:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86dd9f3b9dca95dae93061d9d81277555cef684466edcbd3d782747f5078379`  
		Last Modified: Tue, 03 Feb 2026 03:17:42 GMT  
		Size: 54.7 MB (54733369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c82fd03d2605ed6211839a8268acbbc25f3663d2ad9fcd29092c6c78b4e886e`  
		Last Modified: Tue, 03 Feb 2026 03:17:41 GMT  
		Size: 19.8 MB (19802920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4574ddc758b9d0879a4ca50c2afa86a6178140614b814639146697cd8d259eff`  
		Last Modified: Tue, 03 Feb 2026 03:17:40 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:997c8794f09de7cec203f3ffbc7a9a92542fde0f168cd02086a13dd39e6bf9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4418459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818050d722345d2dff734fb17840fbabaa4a674596f6b3089dda96504ad44030`

```dockerfile
```

-	Layers:
	-	`sha256:b40083bfc9ff5188c2cc3f411dc63def02e54421b7b3bbed1316ddd539aaacbc`  
		Last Modified: Tue, 03 Feb 2026 03:17:40 GMT  
		Size: 4.4 MB (4402089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee4fbae226b0d7f0b7cd9443ad4a759c250b5841d0ddfc8309bc2c6ce8bdcaf`  
		Last Modified: Tue, 03 Feb 2026 03:17:39 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44282adfef216c6cea9cae946fd7f7f7694454c2dff749b285dd94fb826fd314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126331530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5119d61d8e6fc1d25245ca0f88e77a057625f12001f3630927e4b5a098045fb8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:20:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:13 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:28 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfcd22bd6506af4c63a39832b537c2f551c0a9554b22111172b23ba39b18b5`  
		Last Modified: Tue, 03 Feb 2026 03:20:46 GMT  
		Size: 53.8 MB (53814986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5af5f06534ca35ef9f6165ee3696f86ce9fdc78ff652cff9a8aab4c8786dca`  
		Last Modified: Tue, 03 Feb 2026 03:20:45 GMT  
		Size: 19.6 MB (19632818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a76f83984f06a5922d2a044179e6d69ba6cabc90b0b550ae64db18becc1afd`  
		Last Modified: Tue, 03 Feb 2026 03:20:45 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:66bc343ab93ada9c304e86bd75c7f76df5f4ebdc2aaf064228e8984e84010388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4418893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6b9c4027457845ebf34edf41ebd507d19c2118672d8bd4543522e4d0f36c9e`

```dockerfile
```

-	Layers:
	-	`sha256:482e3733b84fe46cf4be5644a8813d69ce1fee6bfcb661e933d03edb1481bb88`  
		Last Modified: Tue, 03 Feb 2026 03:20:44 GMT  
		Size: 4.4 MB (4402402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b2b07f4a38078bc07eec425e9b557121e5f14209ddfcf620c52d2aeb93f67`  
		Last Modified: Tue, 03 Feb 2026 03:20:44 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:0f5009831a37f333e5b282c505598865dbad070da5f01a66884b41bfab7e2d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129043875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb75d1f4ea6287b7a7166b0f788ab4a349aeb120084a27ed31a6f05773c6ea35`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:27:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:27:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:27:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:27:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:27:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:27:30 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:28:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:28:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:28:04 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:28:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:28:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0152da2a1edcedebd18f20ae48dc373fa9d98374038d8675769d04c15b5b32db`  
		Last Modified: Tue, 03 Feb 2026 09:28:42 GMT  
		Size: 52.2 MB (52175122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8facb40caaf43b6459a82b8931271ae53fb6e717ef30a9bb708d2a6c852e8707`  
		Last Modified: Tue, 03 Feb 2026 09:28:41 GMT  
		Size: 20.0 MB (20023714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48855188f665a7f2b058835ffff74a376b3cceb1ee634f19ec65b110bb74ce88`  
		Last Modified: Tue, 03 Feb 2026 09:28:40 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:523421ae2b46c8f1653cdafa075e155914c86fb16b441bde932a0082e65d92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4420957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df83d841eaf810782ebb9fde7cd7c67d007611122a7282cdaedfb491c22b41e`

```dockerfile
```

-	Layers:
	-	`sha256:bf1110029ce478ce39964f8c2a7e5ac8488ef873d75355fffc5c2b4a29b6cf82`  
		Last Modified: Tue, 03 Feb 2026 09:28:40 GMT  
		Size: 4.4 MB (4404543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c8f52d9cb8bae6b3885f217c658c2c1da08220d0866a4fd19778dc2ed57c3bd`  
		Last Modified: Tue, 03 Feb 2026 09:28:40 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
