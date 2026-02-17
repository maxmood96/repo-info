## `clojure:lein-bullseye-slim`

```console
$ docker pull clojure@sha256:c81b3bc81834e7462e1150acf9e99cc5df596c39dadcb0a85b309357d7a698ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:85b6550f7b60b10dbd86a9ab108be7661f1abc06926d0104a28dd8fbfcd4b745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142351383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5657e8f9b9d29a72f74a93bf9851f436a4982792c162a3c9d53edd7017befc86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:45:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:45:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:33 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:47 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe0cb615dfdd3429f39497aeb9163ac7e8e2a881e6eed8ea1f18ab6e7a7085c`  
		Last Modified: Tue, 17 Feb 2026 21:46:06 GMT  
		Size: 92.3 MB (92256280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9782ef66ac76754e125497b83c1a12b84d01144dea36a13a7d00bfb51e5fbb7d`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 15.3 MB (15318688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7339ebcd8c84936a6ad379c9abd0b0b08d54e2488b8bea3926be2c223fc3b4c5`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace6025cbea182ed1950d1f766fe53156b486777a016ca5df116fa7cee0e5679`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:11e2afedca111901d2d8716bdacda193ea25141eeb43b1e3252fefd769448b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3006280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e32def3a7744463babab9a63977ccf5b9f00c6681e42266077109455e19b60f`

```dockerfile
```

-	Layers:
	-	`sha256:b36c5ece4023f3c419fbb8d6f76a676f74513a038a7961edad7aedb27e470d20`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 3.0 MB (2987222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44449629bc7ede86ca825c4d84cc5702c8b2ca4d48b562ac8ef81671d0379f03`  
		Last Modified: Tue, 17 Feb 2026 21:46:03 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:00f6ffb46c442d7419f7741e8d270eb889c5be82e39cd39a82df91dfc5b26ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139856650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0feec60b745886b42a6217c52feef21d77d1d3b54ef0bcaec7d7ce1a75827f39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:45:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:45:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:21 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:34 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9d6b7c9cac728d8023198b6cfd66e4b814e2828501900c43feaef51d0c42f4`  
		Last Modified: Tue, 17 Feb 2026 21:45:54 GMT  
		Size: 91.3 MB (91288252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4823c40e9a5eaefe58016ce9bc187f99cdbe07e6f71f12f7cb2945948f7eef11`  
		Last Modified: Tue, 17 Feb 2026 21:45:53 GMT  
		Size: 15.3 MB (15305814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baf2f5b36c15a6cc073f4f30d0f60cf2bc3de114e6459e88fcef47085e39dc1`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279290b3846789bc8919136ec71eba313fa7cbfbee2a92891c01068a4e0625e`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f045719b7cc7226f4cfeefc3dd69a716cc847688174f9d4e1549a3f679a15e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3006055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b136cac0249b313e36b113b560327c894227d58456b5484aa8eea56402d331`

```dockerfile
```

-	Layers:
	-	`sha256:97bee2d06016545f0dec5659f35f55c2e95ddaa7fe2164a364d624bd53e7a537`  
		Last Modified: Tue, 17 Feb 2026 21:45:52 GMT  
		Size: 3.0 MB (2986852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a201ec9ce2b458ad0386f55c9bd8b19acb0fa350258c737b58faa06ad3f5ea`  
		Last Modified: Tue, 17 Feb 2026 21:45:53 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
