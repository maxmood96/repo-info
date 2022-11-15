## `clojure:temurin-11-lein-2.9.10-bullseye`

```console
$ docker pull clojure@sha256:5e43d9ed1b31f6152c440998922c9c8fa3fbfdcd385ac625b24a6ad5a6ea34ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.9.10-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a6c15d9afb7a910b8fe19b5e4afd5afa7d0a5dfc7120930f2223d3f442cc0e2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272160932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4607dd539a26308b9bf4aeca0579d09e286fbef1f03a389c289aeef093b3af3a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:54:03 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:55:20 GMT
ENV LEIN_VERSION=2.9.10
# Tue, 15 Nov 2022 17:55:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:55:20 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:55:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 15 Nov 2022 17:55:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:55:37 GMT
ENV LEIN_ROOT=1
# Tue, 15 Nov 2022 17:55:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 15 Nov 2022 17:55:40 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b1d80bdfeef6cb6cdf5a91dce43100373840e0ed893c308f6732d8bf622362`  
		Last Modified: Tue, 15 Nov 2022 18:08:18 GMT  
		Size: 198.5 MB (198455814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746b17a6a28db08122ebc62c7f4aeaa1dc8fd0a9d5ff9d4c4929732389e6b724`  
		Last Modified: Tue, 15 Nov 2022 18:08:58 GMT  
		Size: 14.3 MB (14267798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000fb273b46506ccf5bbf426e74d05e83c32b2bb244256451d660cd6b27ca38a`  
		Last Modified: Tue, 15 Nov 2022 18:08:57 GMT  
		Size: 4.4 MB (4398705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9826d55e22c800bab9cc5560fa30fedd86aaa5c4af9c2813ec1f71d9fa0e26c4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267555778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc661b8d7ecf64037f249ac5809139b6245e13b2af6d68f8be3d785970ec49c5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:51:26 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:51:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:52:36 GMT
ENV LEIN_VERSION=2.9.10
# Tue, 15 Nov 2022 05:52:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:52:36 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:52:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 15 Nov 2022 05:52:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:52:51 GMT
ENV LEIN_ROOT=1
# Tue, 15 Nov 2022 05:52:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 15 Nov 2022 05:52:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6410c82310e7ed376d2f9bdb09d5bba8c5586def41b40a45fc26ed1c405a8a0`  
		Last Modified: Tue, 15 Nov 2022 06:03:10 GMT  
		Size: 195.2 MB (195201165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9a48a4c3e71090d9430169c754bdb72968eacf6eebbb9094c945bda8768059`  
		Last Modified: Tue, 15 Nov 2022 06:03:42 GMT  
		Size: 14.3 MB (14256065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87569f32082e418ea02543095f23c46badb6e3847a1dbd3d354520f1bc8e82e3`  
		Last Modified: Tue, 15 Nov 2022 06:03:42 GMT  
		Size: 4.4 MB (4398686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
