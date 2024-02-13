## `clojure:lein-2.11.1-bookworm-slim`

```console
$ docker pull clojure@sha256:a503de5cf07f7ca2a1e1afaea60eaba5e99802987d8c2f34f7c3f908e1154f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:lein-2.11.1-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2907fc96161048b12bdaa7f60d69c79246943d730d95fbbd1de1d0abf06c53a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210590492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d32f5e61d000575f7eb1a8a2c68a5b7c2ef8cb1d4cdb81d18d5130e15744bf3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:04:14 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:04:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:04:16 GMT
ENV LEIN_VERSION=2.11.1
# Tue, 13 Feb 2024 02:04:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:04:16 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:04:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 13 Feb 2024 02:04:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:04:31 GMT
ENV LEIN_ROOT=1
# Tue, 13 Feb 2024 02:04:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 13 Feb 2024 02:04:34 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:04:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:04:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6584afe528baa6e2714ec675351d17acf5bdb28756f21582641fc558ac73ed`  
		Last Modified: Tue, 13 Feb 2024 02:20:22 GMT  
		Size: 159.6 MB (159582932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6604173251cbdd53b621bb57acee96044b19b6a6584b86bae486c7843f8902`  
		Last Modified: Tue, 13 Feb 2024 02:20:11 GMT  
		Size: 17.5 MB (17483893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c6a96a63c22025f67c2bf62a3c89f10251483036aabd36d26194aa3694b5bf`  
		Last Modified: Tue, 13 Feb 2024 02:20:11 GMT  
		Size: 4.4 MB (4399177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b5c48aedb494491ec65425fba32c4b33e42b61d704153f9c5a65153515461a`  
		Last Modified: Tue, 13 Feb 2024 02:20:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:lein-2.11.1-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70c83e8572ca3e50054fe584da111f2abec5b7945d9dfb515899ab4150bed53c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208648031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed538c61726b2556e366a6f341fd6b705d8c60df314caa13593486610e73020`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:09:18 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:09:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:09:22 GMT
ENV LEIN_VERSION=2.11.1
# Tue, 13 Feb 2024 02:09:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:09:22 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:09:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 13 Feb 2024 02:09:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:09:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 Feb 2024 02:09:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 13 Feb 2024 02:09:38 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:09:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:09:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52067d70268135532011ee3c716818e124283b635dfc7901c4412acbb040e6e`  
		Last Modified: Tue, 13 Feb 2024 02:24:16 GMT  
		Size: 157.8 MB (157784588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc370feccd661bfb26ebb8a64c0c3f85805e79461c9a5a0b2309be2862daa95`  
		Last Modified: Tue, 13 Feb 2024 02:24:06 GMT  
		Size: 17.3 MB (17307478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252fcb9ea37926f1f6f49cda17a4e6e93aff11335f324fd568a8096418bbde18`  
		Last Modified: Tue, 13 Feb 2024 02:24:05 GMT  
		Size: 4.4 MB (4399204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0d0419aad84b3aea7847e6a0a6d8ee6c66df9bff502875dff6e8b80bc80ad1`  
		Last Modified: Tue, 13 Feb 2024 02:24:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
