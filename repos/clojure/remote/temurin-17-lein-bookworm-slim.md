## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:b5a6778bd2911950ab0667125448964b004f35067e6f437f6363e2b3f38e29fa
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
$ docker pull clojure@sha256:f730026b26364ec8f3d7eb69b8e6dbc5f43bcac64f9f61a7dd1eb14d3f6e1a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195352594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054245f87d361c2defaddb46d7375a41c1db5920cc06a49e3be286156fb5bb0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:52:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:52:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:52:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:52:34 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:52:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:52:34 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:52:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:52:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:52:48 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:52:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:52:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:52:50 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:52:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df9974598ff4ac66333953ebc4d59a47e9edd5bcd6ebf2d8b605dff6fc55352`  
		Last Modified: Mon, 08 Dec 2025 23:53:28 GMT  
		Size: 144.8 MB (144847890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e220ca55a109e691e5f0761973658116988e77f89b7c60d65faab7e4a18a140a`  
		Last Modified: Mon, 08 Dec 2025 23:53:22 GMT  
		Size: 17.8 MB (17758098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f690bbc29345b0770af65b7d9d5f2ffecab020fb1b56f3b8735a6c1ff48d0`  
		Last Modified: Mon, 08 Dec 2025 23:53:20 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f6b1d56198d734036cdf6ca732f732ccb1a267559a04fcef1259f68fd85300`  
		Last Modified: Mon, 08 Dec 2025 23:53:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bd34b3802f709616bf7e3611b403d6d7d5d2d685b746d48f960ba7af7d906992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef48efadfac5224c17f257a8d149231aeb90ab27e218812a16e29f47985c111`

```dockerfile
```

-	Layers:
	-	`sha256:483847c819b2e39054f234c44d830bc80a7376457c03e98cab39ae6991f11879`  
		Last Modified: Tue, 09 Dec 2025 04:39:55 GMT  
		Size: 2.7 MB (2728788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16447fef0bc88b94e4ba77140c9ecdddfa6f795242a63915740635fcdd9aa722`  
		Last Modified: Tue, 09 Dec 2025 04:39:56 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:16f3e42ad2aa870b3143758d866e4d0953d01dbed3abfe98ef156fbd83d742ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193891283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0f8b691a13adc709a44c5f869ce5e9fd32418cc1dee1641a9b1ea11630591b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:00:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:00:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:00:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:00:04 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:00:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:00:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:00:16 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:00:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:00:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:00:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:00:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6cb3bb025c548d34af527d20916277ac3521f9b06388d5e0a9b86bda6d2fb2`  
		Last Modified: Tue, 09 Dec 2025 00:00:59 GMT  
		Size: 143.7 MB (143679885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267e117a32acf82b0ab6e19f4b43e1207a1a8118589174db7dfd2880ca0480e8`  
		Last Modified: Tue, 09 Dec 2025 00:00:47 GMT  
		Size: 17.6 MB (17591016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5826760071fac35dfa29f7b712f3cffa1042df3fb985e765111054a8adcd4318`  
		Last Modified: Tue, 09 Dec 2025 00:00:47 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780fd27e37ed84017585d2ab05855723bd685eee49720263b5d77d788f310266`  
		Last Modified: Tue, 09 Dec 2025 00:00:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:62765c1aeeddc17b318ec71a07f760515d8eb273b142a55f0e2fcfec8ed412d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7060259ca71dc570388edd42b1bf2ad74243cdd3674a1201b473aa6e95211c84`

```dockerfile
```

-	Layers:
	-	`sha256:a1ac55212a78f6cddb0595b1d298125cd61aa7fbee9992bc723b18ddec6a0a48`  
		Last Modified: Tue, 09 Dec 2025 04:40:00 GMT  
		Size: 2.7 MB (2728403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d446de2b895932655cdae7c09987aff2c7ee2f888b6b49c6ca6b943bc24edb`  
		Last Modified: Tue, 09 Dec 2025 04:40:01 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d01d4be959dd3bbdf2e754c1430e88643c549246728f28438775aeeb33c3aad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199072013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166530fb753279f63124d6aea7f3211d9abe9090ca458e9c8dd65b362ac9c1bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:19:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:19:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:19:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:19:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 16:19:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 16:19:42 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 16:20:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 16:20:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 16:20:32 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 16:20:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 16:20:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 16:20:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 16:20:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca5d6201ce1f6df8beca96bd758c86429f17de7a899d824f11ee65b7c98225a`  
		Last Modified: Tue, 09 Dec 2025 16:23:43 GMT  
		Size: 144.5 MB (144525256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877385a5ca0bb82cc323675625e760dc1a8dd5f136dcb084944f228e5fbee890`  
		Last Modified: Tue, 09 Dec 2025 16:21:44 GMT  
		Size: 18.0 MB (17959771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68699bf1f8a850af639d66070c5c6057372cedd9038586dbb06a5b30401ef1a4`  
		Last Modified: Tue, 09 Dec 2025 16:21:43 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbbff94c7e9d96c9e018a749db4735323d231754ead8add8c713260548c522c`  
		Last Modified: Tue, 09 Dec 2025 16:21:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:89309f1bae791dcdcec5130c55a7dd4faaa4487b77d66024851b8a4bb447b325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bb44a6f0c1394c09c5f2b03bde31c196da0fd7672c39657bcefa588b729a67`

```dockerfile
```

-	Layers:
	-	`sha256:89ece7d3c92e2b7eefaeff651ccd67a651216e7d6aca246499ac2653f73f675e`  
		Last Modified: Tue, 09 Dec 2025 19:35:48 GMT  
		Size: 2.7 MB (2730621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3faebb5e58199221050c4476e761d1c92aad436fc0ae21828a9e78ec5722ad16`  
		Last Modified: Tue, 09 Dec 2025 19:35:49 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:153c5406fd6568d15260b5292eb461be476187ba31e4ec24442d33cf66c55ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183681371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5f465e39718cf25eab9178537a7a626280209c8d1a6800355a95bf687c844a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:28:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:28:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:28:38 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:28:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:28:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:28:49 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:28:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:28:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:28:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:28:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e50b79de06901b4ac24155509c29afa77758151aad26c6b4026f26a3ea1d70`  
		Last Modified: Tue, 09 Dec 2025 01:29:29 GMT  
		Size: 134.9 MB (134859048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cb5cfc10893a10579d9f1ade73092ce4d6d33db71394c8fd70457fb9c3849a`  
		Last Modified: Tue, 09 Dec 2025 01:29:24 GMT  
		Size: 17.4 MB (17419746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb919bd68efb50a9917cd6be261a6d0bc387d761200b5b09dcb4fc6ead1eea7`  
		Last Modified: Tue, 09 Dec 2025 01:29:22 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c128cf5f02e645921d2eacba57e3635fcc5663fdf16b8a52ca163c68356026c7`  
		Last Modified: Tue, 09 Dec 2025 01:29:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a119ee09bf2db6471da2f2c2634e20b02b9a9c213ce30020e4a6415ead2724f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2739004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478b67d32a332cf03f0c92ff59d3002c22ad268129c2a887380f27f29785f5cc`

```dockerfile
```

-	Layers:
	-	`sha256:364a02fe56591c3c9139ec9c7dca64ef1527b08c583ded90afa6737161ad482b`  
		Last Modified: Tue, 09 Dec 2025 04:40:08 GMT  
		Size: 2.7 MB (2720602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f305f55d3611fcee11dbcbcca1a12463c39985ac006aa02251d9855a42c0bd5`  
		Last Modified: Tue, 09 Dec 2025 04:40:09 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
