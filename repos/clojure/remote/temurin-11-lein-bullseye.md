## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:bc789127d517d73623d68d11b02b918e2b179e0322717ab4db60629945d42393
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:11f523e59a4affe989554106e8d1faff9a2910a3a5f2b75457ae1377ee58e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220802390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b52b8616dfd2186b55bcbef0152efb1dac9483d6bc04357fe70a81f861e382e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:57:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:57:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:57:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:57:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:57:16 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:57:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:57:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:57:29 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:57:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:57:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84ec84199490fa153051b5c144217faa7ff2365bf99716865b1d944693386f4`  
		Last Modified: Tue, 19 May 2026 23:57:50 GMT  
		Size: 145.9 MB (145886255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3ef9e512c4789a843967c1f5811905c2ac40dabda2c05597d201a301b7787`  
		Last Modified: Tue, 19 May 2026 23:57:47 GMT  
		Size: 16.6 MB (16629528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcbf316df5418c58da4ded639c775776cc3069052fdb1889f0c9db420cfed07`  
		Last Modified: Tue, 19 May 2026 23:57:46 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dcc841383770229822b92600cfebf9df11353cb1eb2f6bc904227df66c4e5d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b0c8924216619a7916dde4d0606a863dd6332fe64f62386922d1cfcaf4e2f6`

```dockerfile
```

-	Layers:
	-	`sha256:2dfe0cb9e96fcd129b225f559aff249c6b68efdb4293120e6c15a4520eb6ef0e`  
		Last Modified: Tue, 19 May 2026 23:57:46 GMT  
		Size: 4.5 MB (4506005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5349db2c115babc9fc192e5b90eeb57096081de5a59f9f60c0bb4b64cf128a80`  
		Last Modified: Tue, 19 May 2026 23:57:46 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70411032dcbe132dda1f23b1b7a333238ea25aa8dd95b7daac5c873d0a24ce29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215973113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea77a157efb5e5073113303021e959075d0d7b207efe51cd0db65684689e5b10`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:04:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:04:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:04:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:04:30 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:04:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:04:30 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:04:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:04:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:04:44 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:04:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:04:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6c665acd1c43ae8d38eabcef4d4def1aa302000c7bfcaab94a0f872ff08f2a`  
		Last Modified: Wed, 20 May 2026 00:05:04 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df7283e853a943d4c670810462261afaf8a773ed214042fc4cdaee6209efbd`  
		Last Modified: Wed, 20 May 2026 00:05:07 GMT  
		Size: 16.6 MB (16616572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b457d8f2a930b148d5b32f206b0c3c4490d8ae45711102945ba9bd789cecbb2`  
		Last Modified: Wed, 20 May 2026 00:05:06 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b9587d2e3778c0e5b4de4a1920f1ef523d910091e8773f515c246b68e50f6328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267f74f4591cf4e1263f01ccd795805d9c4f8ad643fe229c9951cc95f3705c17`

```dockerfile
```

-	Layers:
	-	`sha256:02e2b4c9bf017b5e0a3c33e929a048a0909b3a3d76b9796a508484e14f6e2f8c`  
		Last Modified: Wed, 20 May 2026 00:05:06 GMT  
		Size: 4.5 MB (4505597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd4a69593a50298a9930a8e506be3ee11609d407dffc6454831ac172f1087116`  
		Last Modified: Wed, 20 May 2026 00:05:06 GMT  
		Size: 16.7 KB (16656 bytes)  
		MIME: application/vnd.in-toto+json
