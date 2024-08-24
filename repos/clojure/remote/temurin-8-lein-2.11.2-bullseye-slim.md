## `clojure:temurin-8-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:38db0432116af4e9bb736f765a0a09d74216160a3e5c4ae68389a651b5cbb591
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c9571089a67bdab76d67cd68fc6a1e58da86457d58845edb7fff918cd6b38265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182576193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9752dc03cf6a067921e51b94f36dc9677762aa9a198ade55fef64f440d746eac`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d32ef89b433f016fb9c4de3363df1b579b23fd2725455872dc865da253571`  
		Last Modified: Fri, 23 Aug 2024 20:01:57 GMT  
		Size: 103.6 MB (103611881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf561538ff31cfd47f91dc0829b9b5e49a299312838798e2cfe855614c413e3`  
		Last Modified: Fri, 23 Aug 2024 20:01:57 GMT  
		Size: 43.1 MB (43137915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cfa3d0601dd6c3b432e5e5877aad0d63edc90457e112965861bdb9440c8caa`  
		Last Modified: Fri, 23 Aug 2024 20:01:56 GMT  
		Size: 4.4 MB (4398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:194adbe887c332f93a3791193807c7afb1810fb61aa20c7cb5438c4513b43399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4442659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0d0dea634e7d17f2d9533f38e5e8e0e4d1caaed9e29fa5dfb2faa7767a1669`

```dockerfile
```

-	Layers:
	-	`sha256:07646a98e81fc2739700f6b7809d74660739539afd33bf31dbd02106814aeefd`  
		Last Modified: Fri, 23 Aug 2024 20:01:56 GMT  
		Size: 4.4 MB (4426579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a0b11f48c76bb18f1fb7835bc392cdcb9de3e145cd0b158305ead76114d86af`  
		Last Modified: Fri, 23 Aug 2024 20:01:56 GMT  
		Size: 16.1 KB (16080 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c97bef270c9558222f7a186939b2b77b4b9a85f6e92ea7e62fb6da07621b31ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180360669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b018b4592643b4ba6117b92e44cfd4e0782909ad757746c2ce67bebba0f09758`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb51859b870a1fb12b81d80a40fc8b349baf98ee32dc9205b1701fc6ba1ea395`  
		Last Modified: Sat, 17 Aug 2024 05:53:33 GMT  
		Size: 102.7 MB (102729220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffa0840c1d8e32ad9390ed522cb55fee2a2d94a66605b98f576bfec73f8cc82`  
		Last Modified: Sat, 17 Aug 2024 05:53:31 GMT  
		Size: 43.2 MB (43157287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c5a291381ca3003fa153025eec7208d866ba96224b2dc32beb1d1a53f21ad`  
		Last Modified: Sat, 17 Aug 2024 05:53:30 GMT  
		Size: 4.4 MB (4398043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f563e155065b06d32ca95ca4bcb24aa8cef9e7bc298d8841fb9232dd3c3a42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4448645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108c4ce9d2e4e14b3f3892e19d1437c2dfd3cfdd310a27cca74dd800a239c2d1`

```dockerfile
```

-	Layers:
	-	`sha256:38c3d067b2b2c3b30275f3ee65668b37ba6c54ff848dccad8370c733d447d957`  
		Last Modified: Fri, 23 Aug 2024 20:44:16 GMT  
		Size: 4.4 MB (4432867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2acfa4e41857e354a7d797bc645a904a7c09eadbae4cf8a46626ef02077f625e`  
		Last Modified: Fri, 23 Aug 2024 20:44:15 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
