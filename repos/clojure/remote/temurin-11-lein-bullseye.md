## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:55966d554c8e2573e24ded05ec9cf70152aca228db440c6d7b97eb4a7f98eb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:dd6ad214839aa10d0635bb64c459531759df773f72561f236b174e02d9dededa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221114062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72f3bce8e5fd6ec2436e8465be40dd0034a0f7c07bc46bd0e76c4c17e378ae2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:23:49 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:25:53 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 10 Apr 2024 06:25:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:25:53 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:26:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 10 Apr 2024 06:26:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:26:09 GMT
ENV LEIN_ROOT=1
# Wed, 10 Apr 2024 06:26:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 10 Apr 2024 06:26:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c507d9904bfeb82b742f3c4fa084d1261c4ed6c24cac8b9671dce60380a20c`  
		Last Modified: Wed, 10 Apr 2024 06:43:04 GMT  
		Size: 145.3 MB (145271259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81841c577bd32db64f02b5ef2b8da4116d5ba517f77adcde368ec0e876b6f8a3`  
		Last Modified: Wed, 10 Apr 2024 06:43:54 GMT  
		Size: 16.4 MB (16353381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8a189e2ab7336a2394fa42c4386f384acdc6fcec3f4214401f9085b24b6dd9`  
		Last Modified: Wed, 10 Apr 2024 06:43:53 GMT  
		Size: 4.4 MB (4399158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fd840a84ecd05c373bb3baa2afc2af4326c2e7be5c7c5635878b7229eee7ff4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216477237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a310974b6cb76bc8b6085f663804ade5930cdb9c5a31ad5d5c261b2d8c6e0c9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:33:45 GMT
COPY dir:337eb37873e2fe424b3d62c18ff2640cf50898156a884981e9e10924759441c3 in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:33:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:36:31 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 16 Apr 2024 06:36:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:36:31 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:36:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 16 Apr 2024 06:36:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:36:48 GMT
ENV LEIN_ROOT=1
# Tue, 16 Apr 2024 06:36:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 16 Apr 2024 06:36:50 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c70dc33680c6cbcc872c11af38e2d83af8622a965f0d2d3c904c999ffaa3062`  
		Last Modified: Tue, 16 Apr 2024 06:52:48 GMT  
		Size: 142.0 MB (142006343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2918067f56ae5c051c535c631e717b116e32205b1f8b6f70c5a13d5e7f7fadf1`  
		Last Modified: Tue, 16 Apr 2024 06:54:00 GMT  
		Size: 16.3 MB (16342561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8e8fb4a7347be15a295f1359839b7aef35641ae05b90828eab5a651f86592a`  
		Last Modified: Tue, 16 Apr 2024 06:53:59 GMT  
		Size: 4.4 MB (4399157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
