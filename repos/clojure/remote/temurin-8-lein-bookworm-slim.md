## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:79d031a16d25897720f5dd10d5aa60379c0ad243305c96b8e20c0b3e4543f1e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fb2496d13f17feeb4df336c7620b597f59ce928f2df2cae4aecdec4b947bb8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105712352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56db30febfc1eeb59cc2a7a336e51306294698123a269da207d861e0af90a3e6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:45:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:29 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 12 May 2026 21:45:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 12 May 2026 21:45:29 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:45:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 12 May 2026 21:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 May 2026 21:45:42 GMT
ENV LEIN_ROOT=1
# Tue, 12 May 2026 21:45:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 12 May 2026 21:45:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cd5b9a796bf61474fefbf37bae0af6e1f7ab1332191ba315b9a1cef8449698`  
		Last Modified: Tue, 12 May 2026 21:45:57 GMT  
		Size: 55.2 MB (55198695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec309659be918cb7fceba0da006c83cb1298a5cdbf26a74e6600982de47ed37`  
		Last Modified: Tue, 12 May 2026 21:45:56 GMT  
		Size: 17.8 MB (17759631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2d7c1ca279aba672366e14d86a13025a23ecfce66e85184008c8b74da7b924`  
		Last Modified: Tue, 12 May 2026 21:45:55 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c4cf6a13bf58e63fe59f61a357d92138a91d62e0cf2a8a5c25e6e5fbe1a24a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1d7796aaa55c555c0b0d378c7c74eeaca59536fd2da430edfae642299afbdd`

```dockerfile
```

-	Layers:
	-	`sha256:68183c286935629690154541d4e8ac7275be7d8cf3a59b79afae65c443b2f31b`  
		Last Modified: Tue, 12 May 2026 21:45:55 GMT  
		Size: 2.9 MB (2851039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e16148f28b5f9a1b194531c81ea57f69c75be7dbc722233283eb29697fd37e`  
		Last Modified: Tue, 12 May 2026 21:45:55 GMT  
		Size: 16.6 KB (16554 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:29c965b6065d9090bbe10a80cd16a2bc7d6149917035d3e4e7cb1256514f5c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104499926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549dd0ee5b9700eef9b7ab96260ee670917aa3c5970a37e1e0dace97926ee952`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:45:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 12 May 2026 21:45:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 12 May 2026 21:45:13 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:45:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 12 May 2026 21:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 May 2026 21:45:26 GMT
ENV LEIN_ROOT=1
# Tue, 12 May 2026 21:45:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 12 May 2026 21:45:28 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a34428d67344230f0ebe1eef2c4b3ffd13852d02512f091ef2eb5ea922c533`  
		Last Modified: Tue, 12 May 2026 21:45:41 GMT  
		Size: 54.3 MB (54272927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1c90bd54c2104d5cad33d458e9462f3811d6e742d860976f9bff46c1afe258`  
		Last Modified: Tue, 12 May 2026 21:45:41 GMT  
		Size: 17.6 MB (17593039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8914aa759387fa30865f64472da57352986e418c2e65877ad15bef19194a5e`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:223cbe59bd138d084bcb7f915a228ac803e180284c348082c0805d75a471b8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5bd895813406e815baee0f0ff2d368e752ac3eb5eb677a46ce6c824b76872`

```dockerfile
```

-	Layers:
	-	`sha256:c1aab3b6539d337770193c7ea68ed23d516c209c69023481f4ca0c4b8b22e3bb`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 2.9 MB (2851354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9526e34a2c95a53a653ba73b6a2c7d072b309941b936b9ee14a200385be29a`  
		Last Modified: Tue, 12 May 2026 21:45:40 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f02f8bb2d1381500ba2403ad3f20714cd6ec5b32dfbdcf92bef87386610c288e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107226777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074d7618e8102e789d6233c7373c428ac46170b3e7917feb6f50484876ec9d81`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 12 May 2026 21:46:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 12 May 2026 21:46:26 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 12 May 2026 21:46:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 May 2026 21:46:59 GMT
ENV LEIN_ROOT=1
# Tue, 12 May 2026 21:47:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 12 May 2026 21:47:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a4137454cc0810d06042c272eb08276000e4b66a91f77145ef48d12c8463a`  
		Last Modified: Tue, 12 May 2026 21:47:32 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6cfe1d41dcf341ebabc597ccaa4f4d59e9f602ad649017b07be63a762b6ad5`  
		Last Modified: Tue, 12 May 2026 21:47:31 GMT  
		Size: 18.0 MB (17961366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c984397ba6c7b276639908aa59253378e89ebeac1cb9737e14c418e0f8ca12bc`  
		Last Modified: Tue, 12 May 2026 21:47:31 GMT  
		Size: 4.5 MB (4517774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a57e67e498f6241578e9c9af39a670c414d4de3cd777c46d1f9e57238695993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6a1094d0a547ad11b56251ab611e2e6a214a7cb6501ea66583a537c708cf2a`

```dockerfile
```

-	Layers:
	-	`sha256:91feac84b570ea4457300a2f3c94c23b244a09671ea5174e03b8606827b0b857`  
		Last Modified: Tue, 12 May 2026 21:47:30 GMT  
		Size: 2.9 MB (2853467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00d82d26853966c581d6a87dc3ae32374bf867e121e23002c6507a38196cbd1b`  
		Last Modified: Tue, 12 May 2026 21:47:30 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json
