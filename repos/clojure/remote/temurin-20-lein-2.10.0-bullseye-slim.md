## `clojure:temurin-20-lein-2.10.0-bullseye-slim`

```console
$ docker pull clojure@sha256:1b2e3f09471d5411759eec3127561dd6fb97229fa07058d9776fb009ac26c7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-lein-2.10.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ab3cbd278d22badcf8de697f777c966003d05e8966a7d51763838bb2fa996122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202185439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4795e4a4d522ae0a41ed4fe029915b39d2ec8cd09922706257e6d1da662a24ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:31:08 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:31:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:31:10 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 20 Sep 2023 07:31:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:31:10 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:31:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 20 Sep 2023 07:31:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:31:24 GMT
ENV LEIN_ROOT=1
# Wed, 20 Sep 2023 07:31:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 20 Sep 2023 07:31:27 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:31:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:31:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54609089935fe1ea947dcddf61947fe2eb3d029159a79ff7091d0d6c63ca4682`  
		Last Modified: Wed, 20 Sep 2023 07:39:30 GMT  
		Size: 153.8 MB (153791726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67c680245353f6b0f79d58d325da6453c060b590b854e611a675e85b80295da`  
		Last Modified: Wed, 20 Sep 2023 07:39:19 GMT  
		Size: 12.6 MB (12576350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a642754c9a075e795a9311ad0d43740e9c052eb550c0619feeade554c3976095`  
		Last Modified: Wed, 20 Sep 2023 07:39:18 GMT  
		Size: 4.4 MB (4399252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd557e76c54b0e2903647bb2d6afe7f8d098b6d127465dc692f693af3acca1e`  
		Last Modified: Wed, 20 Sep 2023 07:39:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-lein-2.10.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b791f9dabde0707e3c83b6ba308acddb4d6448779d4485e1ce24a608696889e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199146264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b12981ef2199cd88de1fff07650535dcdc9ed043a07c95d5fb4116ac85ead85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:12:11 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:12:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:12:14 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 07 Sep 2023 09:12:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:12:14 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:12:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 07 Sep 2023 09:12:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:12:27 GMT
ENV LEIN_ROOT=1
# Thu, 07 Sep 2023 09:12:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 07 Sep 2023 09:12:30 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:12:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:12:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafa72c7ae14770a22f427e0e8f845d7d272129d4cdc17983ea6e3a5a747cab`  
		Last Modified: Thu, 07 Sep 2023 09:19:28 GMT  
		Size: 152.1 MB (152120058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0a91aba54426fe4963db3e9ec726263a2bbd395c33e515b18070eb504581c9`  
		Last Modified: Thu, 07 Sep 2023 09:19:19 GMT  
		Size: 12.6 MB (12563672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bf12b6d9f6e5553ba8bc1720ea15fab08c1eefc785f9c5895b3fb4d939537b`  
		Last Modified: Thu, 07 Sep 2023 09:19:19 GMT  
		Size: 4.4 MB (4399232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf793d03a50e6dd064cc607188e34b1812216e715ba3cb40f9aa0571d7550f`  
		Last Modified: Thu, 07 Sep 2023 09:19:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
