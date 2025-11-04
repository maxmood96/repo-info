## `clojure:temurin-8-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:4bc7caf8b364dd174036c091538f6066ee07326460ada6d214e61f533d454795
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
$ docker pull clojure@sha256:6debbfdf4f2f70b777f331ea943f9b7224da6aba0b8148c2142503093c8fa36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105235714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573064d43bf3cf4de5ff0538f19e3db039c3d3f31cf378be31af6066bb9bb7e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:53:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:53:07 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:53:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:53:20 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:53:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:53:21 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7572ee753c33fc569db6994434e628949d18d4b1026ff1de70a76c299c91877a`  
		Last Modified: Tue, 04 Nov 2025 00:53:48 GMT  
		Size: 54.7 MB (54731308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68be3eb3015c35b8911757326f0d60eee525835091c272302226c8aef2e8b562`  
		Last Modified: Tue, 04 Nov 2025 00:53:43 GMT  
		Size: 17.8 MB (17758098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f717b8955b850818aed4eba4014bf69b6527ccf955cf8a03643ac181c72ee3d`  
		Last Modified: Tue, 04 Nov 2025 00:53:41 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f1e1991ba424e658b2e0df415ca51f6f23379e9ede55f9ef085aba5dc0d7260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009c07c9a6fe21738d352218e38bf2d3741c5e4f96d79c0d3bd59652b12a9504`

```dockerfile
```

-	Layers:
	-	`sha256:c3ffc5bf860278c208848a03a594a0798562e4be13ab2899993fb7df63d6f98c`  
		Last Modified: Tue, 04 Nov 2025 10:48:19 GMT  
		Size: 2.9 MB (2850398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59225acadc042a0db8adf2527576e13835ba725039e31f5edeb4ceb6825d5928`  
		Last Modified: Tue, 04 Nov 2025 10:48:20 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d41f2a6a96d51b5444626f1a35137f11695063062b810cf2b39f75afa934532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104046844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc47f20df9fbe2f3d7c341c3d4e6c933785f86faa6ceca0c8731aec6d7901550`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:53:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:53:27 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:53:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:53:41 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:53:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:53:43 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f80981a35bf59a644b0bbae3638014de812751edfdfba039da5678c29ec9a8`  
		Last Modified: Tue, 04 Nov 2025 00:54:10 GMT  
		Size: 53.8 MB (53835577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240672ff73be07315204429f3b1325148fe895dcf2748fd392847f1b1892fb82`  
		Last Modified: Tue, 04 Nov 2025 00:54:03 GMT  
		Size: 17.6 MB (17591115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a54726f23a368680de42cfbcbf6309ab1c72e6b3b14c2997fc078b819b260a0`  
		Last Modified: Tue, 04 Nov 2025 00:54:02 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:339762d59a426ca4070dd1cd01c0686d8036afb1459964113d998db4322fbc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac90d91d5ba2e316a29b16bbc86b69a556cbb7754aee767a2ced06eb7d7f30ac`

```dockerfile
```

-	Layers:
	-	`sha256:e1ff9264a40addd0e6d586709409f0f89815f3828fb2e54bd1e0ed9f612c0722`  
		Last Modified: Tue, 04 Nov 2025 10:48:27 GMT  
		Size: 2.9 MB (2850711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d87a108fdd249b513a99858648683c69f15744d5774ed217a69b24b688b41f`  
		Last Modified: Tue, 04 Nov 2025 10:48:28 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2e0d6772e976033595c2d692a689482c03ab952cf4ca6136c5ac7d751b5255d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106711691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0adbe8a0f92f9e534b0db8eeacbf8f340bf8d08e5a833d2b139277af1515dd2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 13:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:00:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:00:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:00:28 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 13:00:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 13:00:29 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:00:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 13:00:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 13:00:59 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 13:01:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 13:01:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39313f2fa991c0ee72406327d7c1e060d584356d7b42935e8a92e8e96b03d37f`  
		Last Modified: Tue, 04 Nov 2025 13:01:49 GMT  
		Size: 52.2 MB (52165369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60402dff1885bae81dc9adf8e20483794e04308853fc290208718af41d8ef61f`  
		Last Modified: Tue, 04 Nov 2025 13:01:45 GMT  
		Size: 18.0 MB (17959610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d8153fc818c23af518ff05d117fdbeb9e8ae9a7a93b6b4a0aad90c8cec391e`  
		Last Modified: Tue, 04 Nov 2025 13:01:43 GMT  
		Size: 4.5 MB (4517775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06acf11c2ceed6dde96ef8d23c1db5262cc9e3504c17f9b8909afe5cdccf6a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c748c8899a7da596f179f2fced9acb326d2433c14447ed722d38da8ef3b77f`

```dockerfile
```

-	Layers:
	-	`sha256:c6a11607fc1284542407f0077df301547795e0278a5725f02c5d906afa973dac`  
		Last Modified: Tue, 04 Nov 2025 13:38:34 GMT  
		Size: 2.9 MB (2852824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9686759b13e1243111427f11d68e6df74efe3071a5487fbee62d27cf940dec`  
		Last Modified: Tue, 04 Nov 2025 13:38:35 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
