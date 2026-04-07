## `clojure:temurin-8-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:538c4cd39dd46aeba91aebb5801a361329c29b531eae2a520b142e0e4526721d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0d996edd92c2d1d5c4a00d85e4c2df3780d07ea9ecb05d19f8c80d833c3adce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105683028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a49695344dc440e541c7fcd1697dc5c12a74914429a42f72157dad18c7162d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:12:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:12:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:12:21 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:12:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:12:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:12:35 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:12:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:12:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c25179dec74c347ebc26bbb8e54d224b2bd35964ab810f07a204376927d16a`  
		Last Modified: Tue, 07 Apr 2026 03:12:51 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097ea34df9e780fbff6719f5a18cd5ef1898478c3907a7118afc1ac124db794`  
		Last Modified: Tue, 07 Apr 2026 03:12:50 GMT  
		Size: 17.8 MB (17758797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105a63be629b06437e3809cd56c111706a8823be682c776e0be6dd8d6e403ec6`  
		Last Modified: Tue, 07 Apr 2026 03:12:49 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c77c9551fb3cebc73a5093b93c8e33197241257f27b093787c2247e9dd87b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cce5f05eb0336157587c8b648520f765d84478f90b8080b5f19f92d0b029a1`

```dockerfile
```

-	Layers:
	-	`sha256:d50bd90d58f0a91f48ffeb776e1e5fd8b504b458950481eff68c2320693b2b8d`  
		Last Modified: Tue, 07 Apr 2026 03:12:49 GMT  
		Size: 2.9 MB (2851039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21d1bb9205234755bf98fbbceb71685144cd0b67137f1f3935672fa4c40f17e`  
		Last Modified: Tue, 07 Apr 2026 03:12:49 GMT  
		Size: 16.4 KB (16399 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7bc56310be54d007e9fc6b7d5dce93d13df70921719a2b9aaef81560b20c50ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104477345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67e99579da3b1381936bd995242c4e5a463d7a348d49e9b329745930b4e9d59`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:22:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:22:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:22:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:22:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:22:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:22:50 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:23:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:23:04 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:23:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:23:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01df2f5078bdf13b6c4d9b3ea36eaa5d418800129ae832d6df1624e64b776deb`  
		Last Modified: Tue, 07 Apr 2026 03:23:20 GMT  
		Size: 54.3 MB (54251611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e682185a80d862731efb7f3dfb7359090168d15179ef5a45935a02c54bebcaed`  
		Last Modified: Tue, 07 Apr 2026 03:23:19 GMT  
		Size: 17.6 MB (17591795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a16f25ca5c4ac3bf55946f69461b77b96dffb5c0244278c3c940ae1fe51f862`  
		Last Modified: Tue, 07 Apr 2026 03:23:19 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cff9965001dc9f70a4d168e16a27842e76630ddf9d66beb12b8acc51d70092f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1f6c24ac767382cb837c550055d3411b0d3f1a7dafa5383269d6ebd01eb85a1`

```dockerfile
```

-	Layers:
	-	`sha256:b93a14ab5fdee54aeb1a5ecd855e1006aaac8a3e9926ebcea75dcb7b278770f9`  
		Last Modified: Tue, 07 Apr 2026 03:23:18 GMT  
		Size: 2.9 MB (2851354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f702785c80df4c0d3efaccd60d1570da42a234d570974306616d6e72c49c4993`  
		Last Modified: Tue, 07 Apr 2026 03:23:18 GMT  
		Size: 16.5 KB (16520 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:41288b35a42ae00f1f3edf9a76c67e28e6c9b3f5a5d7bc95d03e1184dd70df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107207555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7495660a35eb7a0b959f48597a0a8f22f1db37bc83c0555395294ecfd74da2ae`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:06:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:06:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:06:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:06:19 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:06:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:06:19 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:06:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d87cd97df95540bc764bd675651a228c43a8bd513ce7d2048e612519e294f6d`  
		Last Modified: Tue, 17 Mar 2026 18:07:15 GMT  
		Size: 52.7 MB (52650377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7960e2499fa45d3877d1f6f095fc9b733e7af7e7c90008029c5c7a8e550555`  
		Last Modified: Tue, 17 Mar 2026 18:07:14 GMT  
		Size: 18.0 MB (17961007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe9db16c817bd44cdf17481c29b4a18b5910b49dcac290d6717fdf8b144c11b`  
		Last Modified: Tue, 17 Mar 2026 18:07:13 GMT  
		Size: 4.5 MB (4517771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b8dc820c306e90b38139f28c9e88dfd47a333255de515a095651dab118f3d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae98a98994767e081a4506c3e7668b8ae2d7abfcb5deca3ce80370953cd876b`

```dockerfile
```

-	Layers:
	-	`sha256:3a6627adba40e669b6a2b8c75915f9dc8becbbdb9a2e6d79d3f883ec6dc7d883`  
		Last Modified: Tue, 17 Mar 2026 18:07:13 GMT  
		Size: 2.9 MB (2853467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:237e500800ffe149265c00078dc4d6d1641894227f7b4e1d0f7910c59f9f661b`  
		Last Modified: Tue, 17 Mar 2026 18:07:13 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
