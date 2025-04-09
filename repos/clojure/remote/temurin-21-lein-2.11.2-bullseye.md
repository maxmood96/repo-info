## `clojure:temurin-21-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:cf05b822dd0661e69ceb0a6c1cd08d3570ae78a7f110374a0c5b49f12f937252
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:135e50fcd89c13ffa3e7ee0438838c6dfad4872867c31cf0b0aec7c0391dd345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268640684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55c42a15318191de310c852299649bfbd95f55b92489082fc28e476bd99bcb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece72ba342ff1fa7fada44a40841bfad4158d71f702383dcd956a4bfa7f6e2d8`  
		Last Modified: Wed, 09 Apr 2025 02:19:29 GMT  
		Size: 157.6 MB (157585891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025a552caa2b341f44f89b29d0c4e5899e0801b1f9e5558d7fe5f4694dfd9170`  
		Last Modified: Wed, 09 Apr 2025 02:19:25 GMT  
		Size: 52.8 MB (52791693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89255d483fe67b9676358ffa3a99b8f80b2fc76d4e381d6e4e781abac9404fd0`  
		Last Modified: Wed, 09 Apr 2025 02:19:24 GMT  
		Size: 4.5 MB (4514141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3214e5317a721f8092a30bf32cef286dbb26aef9d0e3fa6d073e9d9a88fc4792`  
		Last Modified: Wed, 09 Apr 2025 02:19:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:27ceae521771712be4a2776a0c60f02e13bcaed663bc97aad7b8cd0036a10ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6644510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce56911af842f9ad565c48761f1a47b3dbdf8ac06ead4ce3d8c24567558da4c3`

```dockerfile
```

-	Layers:
	-	`sha256:e4cee71fbb2642573e23e2aa4833a7ce7cdd1f2882b931b54eb929939e769524`  
		Last Modified: Wed, 09 Apr 2025 02:19:25 GMT  
		Size: 6.6 MB (6625446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a27e951e0f3efae02989e72b20799a20c5075bd5b5353b872121e497032a5f`  
		Last Modified: Wed, 09 Apr 2025 02:19:23 GMT  
		Size: 19.1 KB (19064 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd6c212d2b5180a05c746d278a46e0c33e594ddaae4cd664a7c600527bbecf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265459103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afdb07937b6c74bd20174bfd8a5a0818d1f96ce85a3fbb87822f5dda0466f6fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f215dedabd3f6571b951ada57aeede59411f781d2de563093560f3e7f1cfa37`  
		Last Modified: Wed, 09 Apr 2025 17:40:05 GMT  
		Size: 155.9 MB (155859314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17509300d067306808de372847924f4f2e42b439ec470fa3fb97ca147dcf88d2`  
		Last Modified: Wed, 09 Apr 2025 17:40:03 GMT  
		Size: 52.8 MB (52830998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200d71cd245aa9a0cda683508579b9e2df33f89c6c5697c98062c7ddb148e7d1`  
		Last Modified: Wed, 09 Apr 2025 17:40:01 GMT  
		Size: 4.5 MB (4514140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa971c1ee13a62c10c6a408dcc24dda384a5334b3c5365b799f4ec07995211c1`  
		Last Modified: Wed, 09 Apr 2025 17:40:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:aab9e30a93c17287a81339397873d6db6fc04264414a8f4ef06569bb466bd5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6649709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233059e2a2bacdbff8926374bd60be82bf2d10800d29a2ae38c37c3258dd6917`

```dockerfile
```

-	Layers:
	-	`sha256:d271f7147394f72e9983cd17292258230f78d24d09c3aee145d97101b7c65ef2`  
		Last Modified: Wed, 09 Apr 2025 17:40:01 GMT  
		Size: 6.6 MB (6630501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf00e91aa388a732d3a14bda1ec3e4b3ea68c6cb35d0d3fe67dfaa3402b60eb`  
		Last Modified: Wed, 09 Apr 2025 17:40:01 GMT  
		Size: 19.2 KB (19208 bytes)  
		MIME: application/vnd.in-toto+json
