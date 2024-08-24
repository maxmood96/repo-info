## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:b969bc0fee8a8964f91f2a6c7084657d27b6afeb451f33ec6a02c42828232d0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:168670c8b35c8e9af18627d3697fadc0e5cf72ee02516f6581e9a5f21d8b6b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261301860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a11f280725e705211ae7586e6ea5b1ddb9bbe57fcd3d326ff3d0266109554b8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d9a1e9ba960be3642dab4c44ddde6ef81047c14d106d47315ac3ea8938982`  
		Last Modified: Fri, 23 Aug 2024 20:02:09 GMT  
		Size: 145.6 MB (145550029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6a23918b7f60e075f3254e55b220632bc9c8ba813ec2ad19d715af7f466f90`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 61.8 MB (61799685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a757e5f939e23aa607e43d945cf93e05916da99c4aa0dd411b9b2c9287b8a058`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 4.4 MB (4398034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:390046add716dc7bf3b59e11083cd0c8f9809070ae0111b6e1af44ed5e1ba4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6379059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2ea0a083216f199f37ad76c77da8638ffdb6367719303faaccaec2ea48f41c`

```dockerfile
```

-	Layers:
	-	`sha256:8896c9e3ceb4fb89a0f01a5b5ae35aec302e57d78274b5afc00ddd7aad50d928`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 6.4 MB (6363013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8257c4da770f60994e2cc37301965913f0401555535fa19b015f78fd6bfec897`  
		Last Modified: Fri, 23 Aug 2024 20:02:06 GMT  
		Size: 16.0 KB (16046 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20f6378001106ce404c14044da2658f816920cb580582184427eb9ff464c2c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258015872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4d0e96b61ca225f6ac92c2f568c1fb94055695ae2555e4469e61a674471a8b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c7e107b4736e704c136824cd4b625750da0fdc9e8e5ad885340c116db3e802`  
		Last Modified: Sat, 17 Aug 2024 06:01:13 GMT  
		Size: 142.4 MB (142354796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84607c60dc13faca0826c669353f4c9b0ceddc10e274e8fb512f0874a40e535e`  
		Last Modified: Sat, 17 Aug 2024 06:01:11 GMT  
		Size: 61.7 MB (61674421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afb06021b18dfdddc5e70a9a3a4888857bb589973059ed80424762a8fb6c974`  
		Last Modified: Sat, 17 Aug 2024 06:01:10 GMT  
		Size: 4.4 MB (4398031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:178d816c5e55d1feaae5947ae2eccbabac7281196a2086f4057e4588fab1f28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e3930ae7f7f18ce8c2f0ab6d5fd9a4ee1b842c21342e1b3f8164a3451e6b34`

```dockerfile
```

-	Layers:
	-	`sha256:9ecfd8e4737b4a5158427ec4693a263f88780b22a84463fff2f158281ab4b473`  
		Last Modified: Fri, 23 Aug 2024 23:50:18 GMT  
		Size: 6.4 MB (6369331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f729f75f952c62449fb9253e7a5d2f19cdb27cd4442202dcbca074d1c708dd7a`  
		Last Modified: Fri, 23 Aug 2024 23:50:17 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
