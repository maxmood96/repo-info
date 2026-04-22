## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:e7481d620b755fea8c34228c634aff74d414bee0cdcd409393f1c79bdf7ab0bc
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

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:86c2698eaf20f7317882f0e8c6fa9d013417e67388c131f441a9ed28f69a83d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196142717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258f7a02f02775eb7fb31f7a23646d70da800318f714a1d5356ab4f8b52288ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:00 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:18:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:18:00 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:18:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:18:13 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:18:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:18:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:18:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:18:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030cf6075a93730afc50f6622a35e7875bb1bf7021474ba3f3b7d7d5cb81b38a`  
		Last Modified: Wed, 22 Apr 2026 02:18:33 GMT  
		Size: 145.6 MB (145628750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1718132fe2495873c6170a7ee395179f9ac678dc9ff1da92435aca4aa7cb5e93`  
		Last Modified: Wed, 22 Apr 2026 02:18:30 GMT  
		Size: 17.8 MB (17759556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1461d13cff0be2ba520ad2e1857c48b936a15b49e5b269e76f9b0da71014a89d`  
		Last Modified: Wed, 22 Apr 2026 02:18:29 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4029dff522c5ca7f99097aed7327c051bd1753ec409af677d04b33d17f004880`  
		Last Modified: Wed, 22 Apr 2026 02:18:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:89040c94df995a0ba8c1a82d14c8f1378ce6299db894fb3a289b5ceb5d1721e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794e9b88586aa09166142209dbb97d5c8e5624a02f69bbff5136aa556a13d599`

```dockerfile
```

-	Layers:
	-	`sha256:e98695e40942ca0e8c38e98f80f80856f9fff7560ed54872afaa2134ecd83a9b`  
		Last Modified: Wed, 22 Apr 2026 02:18:29 GMT  
		Size: 2.7 MB (2730050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bfb6c39240d4d78b97d605d10e1babaafcd81234ba36659021944d92e2cdff5`  
		Last Modified: Wed, 22 Apr 2026 02:18:29 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab04a93bbbdb81212e81520c692e0b9f3edb0b59e496af776a6f19788b7bb80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194663414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60095035b4c33ada7b1b787462a8a1aabc18e2f6d4e71d4b9abead19d4421395`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:21:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:19 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:19 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:33 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f4206269014eaf3fc33b432856c69069a4987151750dfba8852af2c7c43ce2`  
		Last Modified: Wed, 22 Apr 2026 02:21:54 GMT  
		Size: 144.4 MB (144436188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72333a5a2501f3eab583be7a80e8f10df62de40a092d34a3a4cf1bba4ed89c3`  
		Last Modified: Wed, 22 Apr 2026 02:21:52 GMT  
		Size: 17.6 MB (17592969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b9cf2626539e211c7460e2c6a30d05977bd3f7c68b04c2e569786913b99cb4`  
		Last Modified: Wed, 22 Apr 2026 02:21:51 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03749c57125b671f3c9d09e63fc5ee2fd928823778cb349ecec66f102a224bb`  
		Last Modified: Wed, 22 Apr 2026 02:21:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88c844b7a7a03b63823f0583b1eda8331cf7c35544b8d9316897b7dea99c17f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5377e9e10f696b8c855e39c5607bd2ab33d3e2f2df57e7c76165810e64cbcf`

```dockerfile
```

-	Layers:
	-	`sha256:0f001f550a4ef99e4d9490ca5dde789cc1e89aa5dba17d2ae1c76d8fcf622101`  
		Last Modified: Wed, 22 Apr 2026 02:21:51 GMT  
		Size: 2.7 MB (2729665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a662485db0eab9670147505133496d08e95a56fe78ad13301c6f6f4e0690433`  
		Last Modified: Wed, 22 Apr 2026 02:21:50 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bf8ecffcf62291cf05ed9753921943b4112eebf06c4a46d70201e7485129d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (199996331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95150bd5daadbda7a8c000b3ccc075c14bffa10569818014ac231af276f3fac4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:49:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:49:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:49:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:49:09 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:49:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:49:09 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:49:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:49:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:49:42 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:49:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:49:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:49:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:49:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac07d766af011abbea5aa154cb16be5509f5ea8687e2050966b40181dcca495d`  
		Last Modified: Thu, 16 Apr 2026 02:50:31 GMT  
		Size: 145.4 MB (145438295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80501e0819dba5a7dec88d486b640b4316e8ccd6d2bee41c9bde7aea2bdd12dd`  
		Last Modified: Thu, 16 Apr 2026 02:50:27 GMT  
		Size: 18.0 MB (17961381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3078a5436072fedfd326ccd48df71f9df9ac9b09e6cf4a1bf701719c3f3f1444`  
		Last Modified: Thu, 16 Apr 2026 02:50:27 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eac77b347fb2640b693197971c89dc5cf0c94ed73e05f153912a5ffabfa708b`  
		Last Modified: Thu, 16 Apr 2026 02:50:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1cc1f5a8ddea8ca5732fcf22d5e7267a12b370860677ef780c33159882826bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf31e9fc96a5eda177cd11118ab9345e5f41fe688658b19f989b384f8d0ff57`

```dockerfile
```

-	Layers:
	-	`sha256:b09804ee520af5972cf59ba6e8ab148016d1f26fd9b3f91bbfbf6ce13d91a79b`  
		Last Modified: Thu, 16 Apr 2026 02:50:26 GMT  
		Size: 2.7 MB (2731883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95908b664a7892874a1953a00e4eefa32c842ee6e9a654ff9df658818e7386c8`  
		Last Modified: Thu, 16 Apr 2026 02:50:26 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a30e44672310c9e95ba4132651ee59fed339f5efba591c1a044e1548eb61e1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184458821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649024d5303c9721269fb319026ef0a60b3529004d61d1ada5b76099c2f674b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:38:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:38:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:38:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:38:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:38:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:38:05 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:38:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:38:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:38:15 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:38:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:38:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:38:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:38:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c713317975041bf27c66cb35f6d637abc30dc9f0e4406c9dc6ab930521f9b233`  
		Last Modified: Thu, 16 Apr 2026 00:38:45 GMT  
		Size: 135.6 MB (135627010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15794faee5162ead825970e19ef0948dc9b3e7f06b7160e96496e47ead006898`  
		Last Modified: Thu, 16 Apr 2026 00:38:43 GMT  
		Size: 17.4 MB (17422005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7898b2471a146349a4b4a9d2c6ac69b1584e5e31ab1d2749e35f31688e4d00f`  
		Last Modified: Thu, 16 Apr 2026 00:38:42 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbdec7da14d5b67c4e5fc3c0d42dafb60235f3fc4ac2b7db517666c8bdd55ee`  
		Last Modified: Thu, 16 Apr 2026 00:38:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5beaac8ce292d120df4c71cedd499fc2d65150f462851c81f85b89ff4d77f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2740266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ca2d4556089fa1d55d2ff96d7475262646a11d25cadcea2784eecf2e22c519`

```dockerfile
```

-	Layers:
	-	`sha256:f3a8a48bd95cb2f8a4696524b5b38619c3410ebf0f76156de6c6327931deec3a`  
		Last Modified: Thu, 16 Apr 2026 00:38:42 GMT  
		Size: 2.7 MB (2721864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb43b14b6f1b6db0be379532ed88e6151a8025803f9e67938debfc4fe2c10053`  
		Last Modified: Thu, 16 Apr 2026 00:38:42 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
