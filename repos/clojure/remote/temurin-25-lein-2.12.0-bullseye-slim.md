## `clojure:temurin-25-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:8c662d60b6e1ea6ac445f3787003c52d7db48f2d0c10d7c7e323d31813e448ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:183b07c552b94b19d1998fc60662acb3b986a009a7766c837b9703d0ff21ae37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142140688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56e1caac0e3971762083f5be3a3c71b98a3c8b45e74640294ca0ef94d77d3d0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:56:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:21 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:56:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:56:21 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:56:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:56:34 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:56:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:56:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:36 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dfbc97782bb4ef5510715f43433bb0a8145e3caa8d14c9d55f353cb09197b0`  
		Last Modified: Mon, 08 Dec 2025 23:57:12 GMT  
		Size: 92.0 MB (92045289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c2b109684769413d64b06d7e4b3bdd519f7a8697d0ea8e53dceefa411b63fb`  
		Last Modified: Mon, 08 Dec 2025 23:57:04 GMT  
		Size: 15.3 MB (15318761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b34d04e1696ec293b036d4d563223c59a5606b6e805d56ef0e3f49f869022c8`  
		Last Modified: Mon, 08 Dec 2025 23:57:02 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b491e35ea6fa14ec99a28dd566127b51508455e00f366eb5e025f977ed2497`  
		Last Modified: Mon, 08 Dec 2025 23:57:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1fc69b1d5d342cfa1f52b7b50f7ead902655bda0e1fe942f921defba7c079709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c5bed37313ac02e540385aeed536f9b52e218aaa42638085de7448c7d1fa40`

```dockerfile
```

-	Layers:
	-	`sha256:04e3afcea035f54f2ecc8ec40a571d613dea7b31e7c4f864e66e1482e4738480`  
		Last Modified: Tue, 09 Dec 2025 04:35:16 GMT  
		Size: 3.0 MB (2969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50dc34f5641d3bd061dcbcc893d938f26e2321d73e3ac9c0985308063d998f14`  
		Last Modified: Tue, 09 Dec 2025 04:35:17 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:617b2fe600452200e8b6d0cebb7c4a8425aec868873554a2bdcafbd66660ccf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139624919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b573fee2fcc244c8514a240f9b12eb9228318894f883277b8dac08d4c10832`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:03:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:03:25 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:03:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:03:38 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:03:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:03:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:03:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:03:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f49dd9c71b414e81e153b23e77f511963df3e99e71ec17a83c3623244e7433`  
		Last Modified: Tue, 09 Dec 2025 00:04:16 GMT  
		Size: 91.1 MB (91052502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be8a876bb55250b9bfaf4df55af827d1c888f394ebff6d701db9fba69736a93`  
		Last Modified: Tue, 09 Dec 2025 00:04:07 GMT  
		Size: 15.3 MB (15305797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00676d7a53e5ab9b2b8c8bad1e2be2048f5792d026deda1839a508acace8ceb5`  
		Last Modified: Tue, 09 Dec 2025 00:04:04 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df348ad605cf8114e1fffb0e9e89e698ad0697d82c5a9e83ca39ca6cd0b39aa`  
		Last Modified: Tue, 09 Dec 2025 00:04:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8bdf6d3f524591d4bd1c90a9110fc10125585250376aa3b6542bc36328e4b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812bae1d6140477fb06df7329ef06d4aeacce01348bde48a39f16a230e9795d`

```dockerfile
```

-	Layers:
	-	`sha256:daba575ee1dab461dbfa89fa8098a2c1c74b013a43eaa45e550a94b7a820cbaf`  
		Last Modified: Tue, 09 Dec 2025 04:35:21 GMT  
		Size: 3.0 MB (2968864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b1841eafeedfc8c3efeb2a411bb7ea2c98e8414c1d5db94637b7794d3a7b291`  
		Last Modified: Tue, 09 Dec 2025 04:35:22 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
