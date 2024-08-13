## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:12178d6343470371c31aed5d7f70523f92d12b3a07b3e13dd3e7788f2b1a5eec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1a336597562c62e3ea3134624369d362f4f2e3b977d2326abad9d58584a0cf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182576215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d99bb6e10b381f3fc8323f60f11f5abc6adeaa37be5d998a520b027f0c9cff`
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
	-	`sha256:55ef94880f93d849d4c624897b17e27406c732b76867986186f0fb657c19b2ba`  
		Last Modified: Tue, 13 Aug 2024 01:11:10 GMT  
		Size: 103.6 MB (103611899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fd9631efadabeb1f895860e5b822e2ba82a33571349e61a35f9faf1c04f1ff`  
		Last Modified: Tue, 13 Aug 2024 01:11:09 GMT  
		Size: 43.1 MB (43137917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b31868a4cd801235c68d2678f1acd08785bc712167c0047142d81138e0f355`  
		Last Modified: Tue, 13 Aug 2024 01:11:08 GMT  
		Size: 4.4 MB (4398080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fddb640b2d9a8807548e762fe6c50cb68ac367bc1654dbfce655486313d2f1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4442660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8648e9a4314c72d7f206f1552b3a11b4bc175d4e5e4b5e445ddbe282c206b0b`

```dockerfile
```

-	Layers:
	-	`sha256:4fc0308b5d125a82e3ac80826fcb3d5418e1eaeac56026de6f8a57eb0181e916`  
		Last Modified: Tue, 13 Aug 2024 01:11:08 GMT  
		Size: 4.4 MB (4426579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d18c517febc672a011b6a5c74238ca71efb4f8a8bd8a9766e4ea7bf3647fa858`  
		Last Modified: Tue, 13 Aug 2024 01:11:08 GMT  
		Size: 16.1 KB (16081 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3138e24cf64ed9b33bfddc04b600a176e454f3b6c77f86ec66953acf0b7fed8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180360711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f38650c87a92a177f876e477eb04883af617ae3b6194d27d665ceffece956c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_ROOT=1
# Sat, 20 Jul 2024 21:06:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0813be99e5fef18309cedf80ba934aa71a9e9724621b1626f3edd869359e2519`  
		Last Modified: Thu, 25 Jul 2024 19:10:40 GMT  
		Size: 102.7 MB (102729198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab02179a96d31a8d31b212575872c9dc44c9b348f10b9f0286556d06f4a4f574`  
		Last Modified: Thu, 25 Jul 2024 19:10:38 GMT  
		Size: 43.2 MB (43157309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a397b6b1b15ba992e3ec076ae8dc64464954286c4c2d62085882f6126860d80`  
		Last Modified: Thu, 25 Jul 2024 19:10:37 GMT  
		Size: 4.4 MB (4398089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c568e18d3f71d2887af42c23dcb96074f8b074aa66bbf5320d6e4b6a9012608d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4449476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264f9345f224b4613407356d6b845bb1c017ceff962441e7720b393701b1f266`

```dockerfile
```

-	Layers:
	-	`sha256:284ba85665db29d40e21faa3e60ce1ce4a4098f43d6e102bc3c28419616371c3`  
		Last Modified: Thu, 25 Jul 2024 19:10:37 GMT  
		Size: 4.4 MB (4432867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f09de56de3053d797544872c664242049cadd068375356ad1e6a39a1508b48`  
		Last Modified: Thu, 25 Jul 2024 19:10:37 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json
