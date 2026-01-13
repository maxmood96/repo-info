## `clojure:lein-bullseye-slim`

```console
$ docker pull clojure@sha256:0568800bf65caee5597126066143ef0118a2770395681125de50e8a2eb2dec23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5329778b20874a1631fda3b73ebfafa1cc537616de22c851371481477aecfda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142140685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1b466173241383d1dfa346976bc45acb47797b971a22df29c08e1469980bcd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:38:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:38:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:38:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:38:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:38:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:38:33 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:38:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:38:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:38:46 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:38:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:38:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:38:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:38:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2529a4fd232e5596a180ee7a887f14917cc1756197880c951f3bbafca75cbe81`  
		Last Modified: Tue, 13 Jan 2026 03:39:19 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cbf58a472c3170ca384766b0007eb49525cefbf522710bca45f065bf4256b7`  
		Last Modified: Tue, 13 Jan 2026 03:39:13 GMT  
		Size: 15.3 MB (15318705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e904901502028aceadefc024f16f2ecf8727857bd3c2d37596877a5a081e77`  
		Last Modified: Tue, 13 Jan 2026 03:39:13 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7772a915ac7f5fcdbe12aa2cfd6362ef854f05d12aa5cb715dc5f47bce687819`  
		Last Modified: Tue, 13 Jan 2026 03:39:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fffa06479d63bcc1ff6c17fd83877b0367a6b6a690e9de3eca83284fe4e09d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8013c1c11a8fdaba9c9eda224110988adcf29fd5ca3268e8b82343f9a653ad52`

```dockerfile
```

-	Layers:
	-	`sha256:1ee907db750846d5bfa47c142d10df63a2067d5b89a7c0ca49901bdfa697f3b9`  
		Last Modified: Tue, 13 Jan 2026 07:35:45 GMT  
		Size: 3.0 MB (2969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79c29eae0827fa61152eeaaa1fbbf8f0bc7f2aa0660f4a215511d7cbf190d31`  
		Last Modified: Tue, 13 Jan 2026 07:35:46 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:465e47ccfa41df7ea35e4870234b317260a0cfcb0b03bf305014d8eff9cca926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139625038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ecd6fddd0be4607d4f52e779bac2d7649b92d6d44d11dc6bb302b56e4e1b35`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:41:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:41:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:41:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:41:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:41:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:41:59 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:42:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:42:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:42:12 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:42:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:42:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:42:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:42:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec94b5ed3bdec080d06541aa1dac56db20e2cfa0ed2999b33c628e3616269c2`  
		Last Modified: Tue, 13 Jan 2026 03:42:53 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34571263d0e59852e3d3fe729a6b6386838a0cb44b49029bb4e454bb5c541fb`  
		Last Modified: Tue, 13 Jan 2026 03:42:42 GMT  
		Size: 15.3 MB (15305841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b9bb25db468b54f6e5f2813148e73866ca9fda8ccf60a58f97f23dda2fdb26`  
		Last Modified: Tue, 13 Jan 2026 03:42:40 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2d2d80f91e4afa54015bc7e5974d4f1ff94bb3e0dfeed59f53a1f60b5dcf14`  
		Last Modified: Tue, 13 Jan 2026 03:42:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:37cb0b9e43414c5e0d4370a76298f56e84a3a59e1d828fc51fa8bc470651cbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3731c8e28d6cc6b3b6135e743b16cbba8a56bf20fae475b59896f6c38f11b48a`

```dockerfile
```

-	Layers:
	-	`sha256:969ce52c54a2dfcd5d47561b3a1d693873e09661b57b97c61bde54a16a372336`  
		Last Modified: Tue, 13 Jan 2026 07:35:56 GMT  
		Size: 3.0 MB (2968864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81e639ddc86f29a8eab2d810bfba7207bbdd8ee4a82363fd6e78065dc01068f0`  
		Last Modified: Tue, 13 Jan 2026 07:35:56 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
