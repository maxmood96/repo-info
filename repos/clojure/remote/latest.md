## `clojure:latest`

```console
$ docker pull clojure@sha256:f9926ec02c6efd18718ef1960b5fc211d9251d4e1e1f940cefde25221a60ad68
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:fe6d7a1fe9614d244758a7fad331061c3eff3b0d586453e757fc6bcc8b6345b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239918642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efd1d734dfe4888353624e0c23d0c717d8b2dc12b0a3c50a311d8028f521739`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:49:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:49:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:49:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:49:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:49:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:49:39 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:49:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:49:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:49:54 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:49:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:49:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:49:56 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:50:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:50:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:50:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:50:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:50:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbc3318a3556d58374dae698781f4b86efaff5cff0c6ab128eda799befc4fb4`  
		Last Modified: Tue, 30 Dec 2025 00:50:44 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c737a94c9cde5c1f35aa9810364861da7074494602296af6dac2fdb89ca6379`  
		Last Modified: Tue, 30 Dec 2025 00:50:38 GMT  
		Size: 19.8 MB (19803006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b9e39f22e1a597e93960145c7817032e4b7419d317e42e560934dda6bd1a4`  
		Last Modified: Tue, 30 Dec 2025 00:50:41 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5411b27e47faae3f0d90b64b53816f06a55c6e03bcfaaa3045f302f97d919528`  
		Last Modified: Tue, 30 Dec 2025 00:50:41 GMT  
		Size: 75.1 MB (75070733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e29793e3e15b9cde23293a047595c2f3a90d85e506125cd6cdb274f7c5a804f`  
		Last Modified: Tue, 30 Dec 2025 00:50:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0ace8302636b92542b39bc2f81b87b67ce55ac3d5048f479b1455a791d7bb9`  
		Last Modified: Tue, 30 Dec 2025 00:50:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:16e5f2d9fdef8038341223624a9ff58658ae75bd020e63cc76505cf442c4175c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f5359f0431c63ca0d22c997fc7252e87340c8ef68471a0df4636e0e603a66d`

```dockerfile
```

-	Layers:
	-	`sha256:52ece7a5ff635f14be1e9494269f5813d3b7e0cf34e75f169df33aef4530d623`  
		Last Modified: Tue, 30 Dec 2025 04:34:47 GMT  
		Size: 7.4 MB (7418725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711b7e7db33de63774c32262c0132d0c075fc8d7156a8bb6091c8e65fd72133c`  
		Last Modified: Tue, 30 Dec 2025 04:34:47 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:27c8130b062ce59e8dc4ff013f69eb7846e8679530876e4166a8c17c0d11260c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238685948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ae1570f154476190c83623633d51303aed5c216c4e83b4b2c596da1b939fbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:53:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:53:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:53:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:53:32 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:53:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:53:32 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:53:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:53:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:53:47 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:53:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:53:48 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:53:48 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:54:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:54:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:54:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:54:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:54:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453ed715d1772532ac9b9d28ca3bbc4264190fa64000f36b88ce0511ea71125`  
		Last Modified: Tue, 30 Dec 2025 00:54:44 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caeb3ae09db1f5ec5fbc8df8ae3304a1fe68a56cb335c7e1703abc7c1c223652`  
		Last Modified: Tue, 30 Dec 2025 00:54:36 GMT  
		Size: 19.6 MB (19632193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94488b85db36e8e36fbc586408a92a28c50fb7b924ecd7430a624dc5811b9abc`  
		Last Modified: Tue, 30 Dec 2025 00:54:34 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f5c0bc9987434cab51348def04315b6d50f951637fb1ded24bbac066768543`  
		Last Modified: Tue, 30 Dec 2025 00:54:39 GMT  
		Size: 75.1 MB (75123310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5e529cf016833047376d1603f5369d32d4370ecde7d6359bdc0f79c71af81b`  
		Last Modified: Tue, 30 Dec 2025 00:54:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238f75c42903cdf118e1c9b1f6ae24d22c807e203fae73c8401419d1e5186569`  
		Last Modified: Tue, 30 Dec 2025 00:54:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:0613837817c01c945cabe2b55283f14338ea529ea6f9ded9ea9a5e5a337eb5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde1899be25c05ee07938102ce42fae6db3a078c7a9bd8e96fadb422542c37dd`

```dockerfile
```

-	Layers:
	-	`sha256:e9081776855f9bd88df319d68850ce6785bfe2ad675d061b8fa7306bae9c2dfc`  
		Last Modified: Tue, 30 Dec 2025 04:34:54 GMT  
		Size: 7.4 MB (7424461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a28e58ebfe0f5a038a8cb2298827bcdbbb94f7de392b93c0b192c4bf7f1ad8e`  
		Last Modified: Tue, 30 Dec 2025 04:34:54 GMT  
		Size: 25.7 KB (25732 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:39eb965ce02c714d9f12d505cf47ee694a15ac016351d4b3e9d27f7ea006e589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249152020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5957ae227d3c9725abe4d5dac6464b701adc0ce9769855720c988d90d82df92f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:34:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:34:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:34:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:34:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:34:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:34:57 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:35:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:35:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:35:34 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:35:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:35:39 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:35:39 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:36:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:36:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:36:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:36:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:36:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9547de7380c379be8e2439a1f5f5648ea7e4adf222d1cde7b039d2d494b72f2`  
		Last Modified: Tue, 30 Dec 2025 01:37:19 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbc182c554299dfbf58a08793b74bd62a59a4ba8ffa2a25d0e3a62fedcdc5b`  
		Last Modified: Tue, 30 Dec 2025 01:37:16 GMT  
		Size: 20.0 MB (20021642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb9a2063afff667832f66c1402f909accc292f43cff781ae90caef5c10568e5`  
		Last Modified: Tue, 30 Dec 2025 01:37:15 GMT  
		Size: 4.5 MB (4517775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab54aa8365870af4064ecc0d4ec5588279dbe7d2163764ceafc3cc1da678763`  
		Last Modified: Tue, 30 Dec 2025 01:37:19 GMT  
		Size: 80.7 MB (80673745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49f54ceacace295c91f0b4c690b2fad37b6f68338e4e5657fbc1d99b5ddb52e`  
		Last Modified: Tue, 30 Dec 2025 01:37:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e08eb2a20f633d356750da02df4728b4c2e2dd418aca42b4d88f9f2ce18bbf`  
		Last Modified: Tue, 30 Dec 2025 01:37:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:9777df5e4c95002a35eb2e3ed2909272b56d835a716809d3397c9d49896d924d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ae08905ca68d5f6b4e1a211c1f431fe69e2ee4e1c44b659966162f34b8bd05`

```dockerfile
```

-	Layers:
	-	`sha256:e535fe9edff85f26d5f8ee3e8b3a3aa28c0857fae831f7e8a792b489944dc3de`  
		Last Modified: Tue, 30 Dec 2025 04:35:00 GMT  
		Size: 7.4 MB (7425225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2edb8770b2c49b9a057b181f2be83adce92dd7852a1435bf079608f657bb9f4e`  
		Last Modified: Tue, 30 Dec 2025 04:35:01 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:a098f28c854e8d1b0544d4d874493deb393d9054cb7d95071db400cff4b2497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233550900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c20435add05de907823d16191b378f761dbb1894ff8e59f6f145ca62ead6ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:58:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:58:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:58:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:58:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 02:58:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 02:58:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 02:58:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 02:58:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 02:58:23 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 02:58:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 02:58:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 02:58:25 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 02:58:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 02:58:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 02:58:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 02:58:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 02:58:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e073d043612954c1e53668a48c2dfae69d4cc5e464079017908645936e6a39c1`  
		Last Modified: Tue, 13 Jan 2026 02:59:26 GMT  
		Size: 88.2 MB (88210732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64637759525a80d3cb422e22021897c48620c960abfa7fd870df65c730149fa`  
		Last Modified: Tue, 13 Jan 2026 02:59:18 GMT  
		Size: 19.5 MB (19462026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083edcbfbf28fc29ba52382884593d70eda2dbf0bd64be7959681646fc927553`  
		Last Modified: Tue, 13 Jan 2026 02:59:17 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ad736d2bbcfc13e1b737efa86ae6903c02523ae118929693e05c136625f3f`  
		Last Modified: Tue, 13 Jan 2026 02:59:23 GMT  
		Size: 74.2 MB (74220899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b7d80b8b48b774d5d1983a19fc039f26a9bda00faede808e02240df163972f`  
		Last Modified: Tue, 13 Jan 2026 02:59:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f318fbbfe4fc0f9a9d4c6905fef9d8d771a18184fb58e1165ecb888ead95933a`  
		Last Modified: Tue, 13 Jan 2026 02:59:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:7f0e419290998e629d5ea9010010af22f7a5a613d89e842700d5c213572886e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f17feb2a3f93ce566b1842bd11fd413b30d5d089d11341b848ae10d24534d`

```dockerfile
```

-	Layers:
	-	`sha256:edf0d58fced0194c4f0db03360216846688a97518d01d2d8222cc7278d3f309f`  
		Last Modified: Tue, 13 Jan 2026 04:35:18 GMT  
		Size: 7.4 MB (7413235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e71236cf980d95f20eec0271ef9ed36fef74cf341de2ea68418220f0f3d094d`  
		Last Modified: Tue, 13 Jan 2026 04:35:18 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
