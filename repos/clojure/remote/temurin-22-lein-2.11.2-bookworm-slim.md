## `clojure:temurin-22-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:7805d1891c9c034e0d7bf734b1150962d317bfaad172121ff0a9c69085e24c33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-22-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c86ec8aa83eccc03a8421216b20a14041d004c9279a6ea12fe7d2a0b0c4b3368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207557423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfceae8b04c0bbdd67592d06efb8520df4a4950703d30f5b394225a0e540e72`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc20e2c2e36424d15a7b12be4722137d66570570a0685648ae46142cc91e24e6`  
		Last Modified: Wed, 29 May 2024 19:58:19 GMT  
		Size: 156.7 MB (156715529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48190e4025b7ae2cccf9a8d9d295d84f41a496875e8e023e1ff330f42f066c09`  
		Last Modified: Wed, 29 May 2024 19:58:17 GMT  
		Size: 17.3 MB (17292936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921fb47d726d24d4cfbf87174aee9154b98db3f90b83dd471d0bb22c2ae26ff0`  
		Last Modified: Wed, 29 May 2024 19:58:17 GMT  
		Size: 4.4 MB (4398116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a650c34baa73019502a48e3051ac8721c87bd12b065953a00c82e9171502850`  
		Last Modified: Wed, 29 May 2024 19:58:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5137c2d5bb2a1f1ed48c937ddfbdfb940dae0ddec9bc3c71fb1e3adbb65c3ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b2e85b402153d6d630c36a762cc51bdc039b16b6e3081bb06968f4411024e5`

```dockerfile
```

-	Layers:
	-	`sha256:f8af2906c80da08bd0ac9d0fa11c63116eb89a694b30f640fbf1245d8ee3d83f`  
		Last Modified: Wed, 29 May 2024 19:58:17 GMT  
		Size: 2.4 MB (2398408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6354e78df3467556ed9b72dd0b50ed8b5ec9ed84789292ba74541b99e9064cb6`  
		Last Modified: Wed, 29 May 2024 19:58:17 GMT  
		Size: 18.0 KB (18030 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f8856d189cfa11963337b1fcabcdefcded3a2f9d522aaac8c77ae1d1fa0e4361
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.6 MB (205627026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a999f54cdc184a9fc6b3a677bb9c339eab845c8ac1ad0eb9c97ad489c5d78b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:02:15 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:02:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:02:19 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 20:02:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 20:02:19 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:02:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 20:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 20:02:34 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 20:02:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 20:02:36 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:02:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:02:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0d69f3d78e64bd747e1c78e304dba8ab3618928d50e632af98143081a1774b`  
		Last Modified: Tue, 28 May 2024 20:21:56 GMT  
		Size: 154.7 MB (154737693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414a38b49c48ebb44a10ba8d2612d043fa0a624ef707441a727dea884c7344a2`  
		Last Modified: Tue, 28 May 2024 20:21:47 GMT  
		Size: 17.3 MB (17311269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f0bb42e3338b60ae2bf6c616402d9245044d6c1382c2fb3fa272b3700a57b0`  
		Last Modified: Tue, 28 May 2024 20:21:46 GMT  
		Size: 4.4 MB (4398162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad3cafc77645192f09dce7191df73d543ff39df00308ec8ff3b737b0e004eb6`  
		Last Modified: Tue, 28 May 2024 20:21:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
