## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:75822fdcc496fc6e63799f8f549d9930668cb2462b20649d866a5295bc30ab65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1c34d318144a39644f06737be08138dd3cee094bd333eabc57824cccdfd8dd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164999676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7035238b98d8a5e40aab5b905a598ee3261fe4c300850c0eabb2621244b1cbc7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:41 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:20:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:20:41 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:58 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54019d623ce18f1fcb7eadcfea68092b6aceb179bd1ed6bfdc6256eb693874fd`  
		Last Modified: Thu, 11 Jun 2026 01:21:19 GMT  
		Size: 92.6 MB (92574599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed866ad04c6e01da923796d872752ef5ac0a956ee2e2c4b17d37adf092a1d7e`  
		Last Modified: Thu, 11 Jun 2026 01:21:17 GMT  
		Size: 18.6 MB (18589822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1467a5358fb527f160e32e40c96de1c0ed26f0a8d7f5fa38f15e7c01b74b7c30`  
		Last Modified: Thu, 11 Jun 2026 01:21:16 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fc4fa46cccbe3a730b170cc7e0a3f7e94bcc215ca9df146b503f05bcc3332b`  
		Last Modified: Thu, 11 Jun 2026 01:21:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9d0bc19cc4d8d3f51f024677c6aee9d235ce67c27be8a9b7be48c71d661c695d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db76708a30a2fa322c62596426c2b5596ddcefd7c6b4142064b584ea81b07e88`

```dockerfile
```

-	Layers:
	-	`sha256:86d38381b56dac001c5ee8dce2fc62b5a22e24cb2bf1a282ed3d2c75f0a0fc93`  
		Last Modified: Thu, 11 Jun 2026 01:21:16 GMT  
		Size: 3.8 MB (3784224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc948e9181f09a63218d039947f243acb1d549048f57778207594f7665863e9`  
		Last Modified: Thu, 11 Jun 2026 01:21:16 GMT  
		Size: 19.1 KB (19133 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4168bd02d04b8be338d9d08da16e6fa78c1bbb4f8ade4bb2b61bcad2718ad6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164286845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403e248e27226b8bf6fef36240544add7288c43318db2c4c5e97935693a2eb57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:24:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:46 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:24:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:24:46 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:25:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:25:04 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:25:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:25:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b3c9e26f0edf929aed1eac338e3baa9e3e6ede1feb155b74662670ba4e80c8`  
		Last Modified: Thu, 11 Jun 2026 01:25:24 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4caecd739220750e3c067c88beb9a4d0c6f1159a9bb8448b318e046e9106c4`  
		Last Modified: Thu, 11 Jun 2026 01:25:23 GMT  
		Size: 18.5 MB (18548284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c3a2399629bf31d8e034dd66b764dfe280514dd44a52c487d72b1e445976d6`  
		Last Modified: Thu, 11 Jun 2026 01:25:22 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c518a76e272b09e434161cfdb26e9a6c752d4a94dcad092e453a0c1a5fd3271`  
		Last Modified: Thu, 11 Jun 2026 01:25:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:929c7df72e79b5ead86e15aa61c1b681782d0303fb4b9978a3c43d1243cb0bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c4595cb4c505176197e7c88643552f5a05b93723fdd0cd8713851261bc56da`

```dockerfile
```

-	Layers:
	-	`sha256:950de529bf4bd652dbd54f2aabfa55a2dc07fbcf121ed835d2a113051a801277`  
		Last Modified: Thu, 11 Jun 2026 01:25:22 GMT  
		Size: 3.8 MB (3784485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6e615fdfbda94539b7c2869fc040221a53fa57b5f8a9227a0f6979b8c0b085d`  
		Last Modified: Thu, 11 Jun 2026 01:25:22 GMT  
		Size: 19.3 KB (19278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:844acab2a4447a53f735c2b0ee961957284f333367592bd7a40797edd1234696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168209178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdb97191990a5be2d5ad63b80c52f1f1bbc43fb1177e94c665857bf8a4042bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:05:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:05:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:05:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:05:58 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:05:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:05:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:06:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:06:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:06:35 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:06:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:06:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec19a238e74deea8797932477dbefdee56677e4d3a52ffe0c521942846410b8`  
		Last Modified: Wed, 20 May 2026 06:07:13 GMT  
		Size: 91.9 MB (91914019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135f69c042fab34199990adc50bee60749486a1e3da6f331dd15c6f2c547c347`  
		Last Modified: Wed, 20 May 2026 06:07:11 GMT  
		Size: 18.6 MB (18644786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e994daf65831ad119a5946a367b4aa43ef9caf86482153d6b5eeac12ce9eaf`  
		Last Modified: Wed, 20 May 2026 06:07:10 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9602a3689cedc52880f00c9ab09eb3c6d7625bfb0efb5a610a1f5e23b5f29`  
		Last Modified: Wed, 20 May 2026 06:07:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ff219bf58b4a0c02f048f86b7ba33746a0a068ba432e3e568085780e318385ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3787736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4213b2255d66a7568c954d4c2972d671e1d65607c53cd60748f6cbd1ccd0de`

```dockerfile
```

-	Layers:
	-	`sha256:6ea4959c3ddcb28314caa929758b64076c64743873f82fe300f486b8db804c07`  
		Last Modified: Wed, 20 May 2026 06:07:10 GMT  
		Size: 3.8 MB (3768548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee158af642de5a66dcfa5338d341af53b3843242ce3efeaef1413d4e5602bf9d`  
		Last Modified: Wed, 20 May 2026 06:07:10 GMT  
		Size: 19.2 KB (19188 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:870bd4b1939ac3c802d3b5a01d72c40c702fb6ffa02143a10ee3dba65be86cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160955329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e2b8d0b7f326d2b05e4d27113a2ee11bf30352956ad4c7dae7f87f3752676`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:13:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:13:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:13:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:13:33 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:13:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:13:33 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:13:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:13:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:13:46 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:13:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:13:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:13:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:13:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d7018c047dcfb3a1d71919456a69bf9d583fb6c58771bf17729ad5a401b79b`  
		Last Modified: Thu, 11 Jun 2026 03:14:13 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c3a7cdf2a9c36ee139543253660f59fae4a14311ecf8589649642dd6b1392d`  
		Last Modified: Thu, 11 Jun 2026 03:14:12 GMT  
		Size: 18.6 MB (18630945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e47edc05f1e950d9c913fde619c7a522ccb0ae85112458c200bc7511ee13bf`  
		Last Modified: Thu, 11 Jun 2026 03:14:12 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf95a6884af260573aa320f8ae4d863e00f19bfbdd997796babb1153f9cba0b`  
		Last Modified: Thu, 11 Jun 2026 03:14:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7c9a07fba1a576014836594566782e2c1de8a2a14d7187302ed2d80982be7464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c148144cc13215396137639bac93b77fe11aa008d87ebe3ed870c3267fc1bc6`

```dockerfile
```

-	Layers:
	-	`sha256:7f636cd4a3f8902056a18d8197c6cf19c7a2855b9e1eb9f54af07890d0ae29f0`  
		Last Modified: Thu, 11 Jun 2026 03:14:12 GMT  
		Size: 3.8 MB (3765213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:059c1018ae642c60971e11232f5bd165c2cf86d0569a07d3b7b3f7fd23ee6f57`  
		Last Modified: Thu, 11 Jun 2026 03:14:12 GMT  
		Size: 19.1 KB (19132 bytes)  
		MIME: application/vnd.in-toto+json
