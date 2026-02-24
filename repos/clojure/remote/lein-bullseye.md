## `clojure:lein-bullseye`

```console
$ docker pull clojure@sha256:7bdc1716bc5fd0d8f72b58bcbcca6cc8c017cab96b092b211c5a4f6be7ff7ac4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c9cb63d4661080df69d6b096eadbfbe61b2b19217cad56272a5c9cfcb9f7eb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167160484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d79a53858ffb04bfa3f2952020d41ae2810107e93f115affd2d734aba8dc33e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:56:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:56:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:56:39 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:56:53 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:56:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:56:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfe6abab7c131faaf6ca575f405a5eae442030ddc22760733a0a05dcd8ad48c`  
		Last Modified: Tue, 24 Feb 2026 19:57:17 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66432ce373f8c98859dd373d64db977c3cc6bf3157e937cf8663ef773e30cf`  
		Last Modified: Tue, 24 Feb 2026 19:57:15 GMT  
		Size: 16.6 MB (16629567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26de45438ab8c4eec6b2362127cd1294623f0eb7aa632af94e7df25545a4c97c`  
		Last Modified: Tue, 24 Feb 2026 19:57:15 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b9b39b3d31db34919f042864ad97cf1665b2e8a813e8cb3d61211f79ac393b`  
		Last Modified: Tue, 24 Feb 2026 19:57:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:baafd4f2b87b216117d82365996aa33fa60a67f5ec639045a1204a216fe301d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4474529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a884934da3929c9f4d4718665538fa67f452c07d0081f9cf59b883a214be813`

```dockerfile
```

-	Layers:
	-	`sha256:b8d2b1e61d9b6423e4fa0235bc5fb995adf6f5acbb31cff4a0e2385b61d60685`  
		Last Modified: Tue, 24 Feb 2026 19:57:14 GMT  
		Size: 4.5 MB (4455526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a67ca31611b6891c590f38ee80ea9244271d587adb0521ca5184ea4ecd557e2`  
		Last Modified: Tue, 24 Feb 2026 19:57:14 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fe4a5f9b8924b10f67d125cdd4e35c26d4ed22bfcb0f8428ec64f1a02944f6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164681338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83beea085c88e8c23040a5ce69be4114a6fc512e75244b57dc6196e963840311`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:07:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:07:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:07:39 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:07:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:07:52 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:07:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:07:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129490d27d481b954cc4a66671ff2b3c724c404a46382697a275cd0dd9f4ecc`  
		Last Modified: Tue, 24 Feb 2026 20:08:13 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff01c4b1666b2436fe3974c9f6177535f352c14bda6b8ece744e60fa070bd99`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 16.6 MB (16616494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648df0bea3687c03e5a9b297cefafa7b66d78ebf5b35db5165ff94a5aa494b6f`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffe459496018c72849eed9410f85159776de45ad8c6142c5fc18a4ae2f32ebf`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b7cd1c783478da967af98d7ba49b36fb7b206215dd2f844e9a4c1c06cafb62dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b9274896188642d7dc95a9b045d46fc1b491532af423d2b02723f7b378078f`

```dockerfile
```

-	Layers:
	-	`sha256:7231187aaed29cf482bc00cc9664df7e4caf7831b4279b81a6131ab07ba2524e`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 4.5 MB (4454521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc3a903b810996c67cc8292415a742c2e2b1e4d5547f70d7010acfb6a74e2c2`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
