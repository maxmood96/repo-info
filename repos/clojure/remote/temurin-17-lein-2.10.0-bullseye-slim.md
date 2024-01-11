## `clojure:temurin-17-lein-2.10.0-bullseye-slim`

```console
$ docker pull clojure@sha256:1bc1beabda89171ad36096e000a76992d7ddf2d031c58366a7456a49654909b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.10.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5ca8605f948f9fb1623bb540e8ffa410229c72d9e03be2a48d26f481ffb633a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193269844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28a245086587c0f53609b2cdfbadcceadcdc8473041944379fc4c473452d605`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:07:14 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 11 Jan 2024 05:07:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:07:14 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:07:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Jan 2024 05:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:07:29 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jan 2024 05:07:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Jan 2024 05:07:32 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:07:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:07:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05930f449cd0d717815eba1657d275e9612b8314bc91a3f58fc1aa148cb32e49`  
		Last Modified: Thu, 11 Jan 2024 05:22:56 GMT  
		Size: 12.6 MB (12578346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c1b88c1e2b7fc96d394a0b695f1a2fd244e850711a3149eb93a620d063b5fa`  
		Last Modified: Thu, 11 Jan 2024 05:22:56 GMT  
		Size: 4.4 MB (4399238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb67aa8255ff71db0518ad5d01a62a2191eebc49df9349de592730cfd1417c5`  
		Last Modified: Thu, 11 Jan 2024 05:22:55 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.10.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d66b12716b8287f6af05ded8dc044854949a4a2c0f07af9ddd68dbb243694ef9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.7 MB (190711033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4730d17a41724321cc958dbbec665dd7eb58ffc0a360258fa97174bb4c2fcfa5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 03:00:20 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:05:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:06:33 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 19 Dec 2023 07:06:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:06:33 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:06:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 19 Dec 2023 07:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:06:46 GMT
ENV LEIN_ROOT=1
# Tue, 19 Dec 2023 07:06:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 19 Dec 2023 07:06:48 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:06:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:06:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80ad0f784bba75d76206ff4e1034310f072851273c25fd54ef00422a8861cef`  
		Last Modified: Tue, 19 Dec 2023 03:03:38 GMT  
		Size: 143.7 MB (143681709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dea3c0e8bad49b80e07bdfc89b1a5653afab2db33feb91fc610cd361b25ee62`  
		Last Modified: Tue, 19 Dec 2023 07:20:16 GMT  
		Size: 12.6 MB (12565671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52581b4952d04b5a9a70482ed288556060ec55e32c7a067beffa129ec9853d14`  
		Last Modified: Tue, 19 Dec 2023 07:20:16 GMT  
		Size: 4.4 MB (4399201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ac91378872e559d697748907fb4ee0b15849744bba6aa2222b0a159fb82bba`  
		Last Modified: Tue, 19 Dec 2023 07:20:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
