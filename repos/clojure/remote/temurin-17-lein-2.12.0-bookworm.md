## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:300ae47fa28dd8edd784e7a3541a95a1396a89fd151f2b8a69b698614a4244aa
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2a06aa5cf249918d5856cedb5966ad42fa2a86bde4d9fb1026d3e590166e7383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218442295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba954b98933fa7ab003b8fb7b542b32752a184a5fb723a1266fbef90a598e0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:03:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:03:25 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:03:39 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:03:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:03:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:03:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:03:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b252c630167cf24ddcb96e9049c357a8e53c23860234b17f2484c8a6938db5`  
		Last Modified: Wed, 15 Apr 2026 22:04:00 GMT  
		Size: 145.6 MB (145628767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb73b36cd520c620cd62e934579b8db443e1fcb137eff7fc5fd866ad0c2933`  
		Last Modified: Wed, 15 Apr 2026 22:03:57 GMT  
		Size: 19.8 MB (19806562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29f71da71587f4547304d0edf6f937169b2ec24e947270616e5323d25e3c0d5`  
		Last Modified: Wed, 15 Apr 2026 22:03:56 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8369d8ebbd1d0f801785398d94b22c3a30fa2e3349362557f02e498c1ca78e7`  
		Last Modified: Wed, 15 Apr 2026 22:03:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:50a204a0b7ddd85e9d0ec93c5d9753e1e75577b1cc4f4ab2a6290d62da43dd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cef8932e762c9ffc09cc66067e16910e819d7abeab918893f2b22ef9df8124`

```dockerfile
```

-	Layers:
	-	`sha256:bb84e8e019ef597883060740a5657da294eb07f0abbad05dd8ac28909868d9bc`  
		Last Modified: Wed, 15 Apr 2026 22:03:56 GMT  
		Size: 4.3 MB (4281731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9f15edcce852d6a2156b8c2f9ba08a571672ae5c25fa3ebc5a138ddea9b462d`  
		Last Modified: Wed, 15 Apr 2026 22:03:56 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:793fa752668401be07bfde5c0b27ba88a9c0e40b9f50a6b42bac1d636d18b5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216964404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7269098da4bf18e801461a0c74cbe8a517265e32d2050e59b7c3881581a76e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:59 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:20:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:59 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:13 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5eece84e2be11411e9957cc2e1d66f7c3daea620e37acc625a9983bd675e4`  
		Last Modified: Wed, 22 Apr 2026 02:21:35 GMT  
		Size: 144.4 MB (144436187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b689b2d37c8211b54e39b9d21a9e7517ce4f2f8a748558bb55d8b7c2fdd5da`  
		Last Modified: Wed, 22 Apr 2026 02:21:33 GMT  
		Size: 19.6 MB (19637015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458e7b06a9f05f92189d2631174a8532d990821d41c5cc206001081b7a2769b9`  
		Last Modified: Wed, 22 Apr 2026 02:21:32 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291297c99882cd6d995e0425b0fb3d6f47bfa004f2d3b25542783441a695e1e2`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ae64661ea7cbc2760e60fce70b415567fda48ab76caa8de635a702998ef62ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4299835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2605d59e333bfb238c11195f6b2c8e1b25d84371e2882f6e7a1d2bc1543bec2e`

```dockerfile
```

-	Layers:
	-	`sha256:f270aaeefecbe1e709ade8d60ba451197366ef0e6dfc33bb8c0af9e1c6eb0f15`  
		Last Modified: Wed, 22 Apr 2026 02:21:32 GMT  
		Size: 4.3 MB (4281346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a83648a268ff627d94a481cf057dbf9d195a5a8329d889598735e4835fecf1bb`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:e92f7e8a4b7ce985d0255e7ccdd94d2955db89ecf17c8581a360ae0f2bc2c41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222323829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d673d2918bff97dcd815470ce00b16103f9808712b04155268c0d5e59b3326c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:49:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:49:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:49:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:49:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:49:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:49:07 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:49:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:49:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:49:44 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:49:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:49:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:49:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:49:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25284de88594517d85a7360eef895de970f33043b86caf252b64664918c3e557`  
		Last Modified: Thu, 16 Apr 2026 02:50:31 GMT  
		Size: 145.4 MB (145438294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fc2b3f39cca3de97a110f6bf4f04fade87d054de5702b8b3e194148a2bb099`  
		Last Modified: Thu, 16 Apr 2026 02:50:28 GMT  
		Size: 20.0 MB (20030453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08b5bf79cf6983eec6f22cd4712b48cc5737fbce6e21853c0a50cafc12c736`  
		Last Modified: Thu, 16 Apr 2026 02:50:27 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ff5fa56081899b3e2a164073dde6192367ec401bf2f44b7fdff7af21f51f5f`  
		Last Modified: Thu, 16 Apr 2026 02:50:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:05ee9a78e752a02bf5e7a9ee1f0f7c3a193ce1c0bc941f44b9d2266a0219bb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ced877ea8c197f4a32d3c7ddda9b05968c1ebd494a7ef4a84719f15f9772b4`

```dockerfile
```

-	Layers:
	-	`sha256:b86542a0c8160fc771360f6bc93243d7bcbcd2a9976490dbec3f752a730eea49`  
		Last Modified: Thu, 16 Apr 2026 02:50:27 GMT  
		Size: 4.3 MB (4283592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ac5d2160b4920a41f902a419ec8c1f7e5de17027406b22366b1e8ec50ff20a`  
		Last Modified: Thu, 16 Apr 2026 02:50:27 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:26beb62c6992af72470c4cbb89f1e1f1860be15ae7c4ce72fab74214a2912331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206760056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131497afc9aa3283dd8d57217bb3f1b089197638eaca3ae4b34392b08c387823`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:37:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:37:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:37:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:37:55 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:37:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:37:55 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:38:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:38:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:38:07 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:38:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:38:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:38:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:38:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d779a8613edca5b69035d6c0c92c01b0a4a763bd78341f5f58fd98ed1021aab7`  
		Last Modified: Thu, 16 Apr 2026 00:38:36 GMT  
		Size: 135.6 MB (135626974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8359a9ea6fd8314306210689aadafd132d61691418b2a919f0808d34cba48a7e`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 19.5 MB (19466858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d016f495f61dcdafdef85f8e0b47c7d64c1acc94c05f87d0b2efaec85e3800f`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e40b111bfccdee8f7d9eda3883766d60ae4e506280701f24c8e0a5aedd2896`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1f2ab70986dfacc4005d2565e523a645ba397fe1be1e21a6c70259155815a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02d0ceda7d06d5143fc653eedb1326859bff73ca3ecfd2cf1e17c1cca70cfea`

```dockerfile
```

-	Layers:
	-	`sha256:ae144a745cc137cc91cdc70555f2f304e8ef6f92429d10c5fb8d44fbf403e1db`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 4.3 MB (4273545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24e75150fafcc2171203112797d1520f2a0d83301e0a531d2b9f0d71114c217`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
