## `clojure:temurin-8-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:a47d61359ab15ee19772321ff7520b7801f05f39a6258b6a75129afcab0ed0e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ac226d763a81c175e51fd6991deee7269958a2e9488450e2b4ea1043d81362ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176896145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c2c63527d448167f9bcf138cc870d27897de8ecf5cce2ec0b5c6c23c8c03ac`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3a932e605cdf7ba977d910782dcd5d79ffe17ac6925c06631458c3bd788bc`  
		Last Modified: Wed, 29 May 2024 19:56:45 GMT  
		Size: 103.6 MB (103600229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8390a4ee5b4e0487fd33ff2cb617c27393108a349dc9998e0b5fd18662b7239c`  
		Last Modified: Wed, 29 May 2024 19:56:46 GMT  
		Size: 19.3 MB (19321432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a872bda81c6adab199b66e4eda7dd91f576a98b1c735cef6e186524453113870`  
		Last Modified: Wed, 29 May 2024 19:56:43 GMT  
		Size: 4.4 MB (4398062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:337a6de7b2eec340dc5479c436780bd94f3f7f988ccfe6cb04d20d40e811cf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573578e5aa63a66e0006c8e7b9bdf45f9cb7d2791ada38f628b20177f1b04f5f`

```dockerfile
```

-	Layers:
	-	`sha256:5fe0865902dff2c2c6aae4a2da2c4873ada735cf805395be1273ec6b7e80e761`  
		Last Modified: Wed, 29 May 2024 19:56:43 GMT  
		Size: 4.0 MB (3971166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d3f3e38ec2212c02327158c2a5c89ff5ddf4d637595a162b1cddaab05e1668`  
		Last Modified: Wed, 29 May 2024 19:56:43 GMT  
		Size: 16.0 KB (15978 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b8efa0160d97f2b72b83aa7562797307b7973901bf038d81ea1314658c147815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175854664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7216318db2eb58b55730baa2961321353c7363f6d665e4a31eddd4fb56668d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429513d912c66c681705c8aa16d730a4b71c1cd1e40db844d161cca11cced3a2`  
		Last Modified: Wed, 29 May 2024 20:23:52 GMT  
		Size: 102.7 MB (102700444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa98fd4d245b27104d88e6a7b6a707bc218cf3a12126b83cc659fc468342711`  
		Last Modified: Wed, 29 May 2024 20:23:49 GMT  
		Size: 19.1 MB (19142720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7facce4933084544db5bd15071ed5bd6a8134736ec6180af3bfd437d69d5c8`  
		Last Modified: Wed, 29 May 2024 20:23:49 GMT  
		Size: 4.4 MB (4398080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d464243a7ff3d199b06dc2170885cabc5df8db6e558ac8d4e88427da6b65c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2b16b48f27839699ab8bbf2cd8e6fd716016d5ee8055f803f194083c243a1e`

```dockerfile
```

-	Layers:
	-	`sha256:10597cec2cf0465afe3c1175ec1ce55d14ae482dcb634485425eb0ab46536940`  
		Last Modified: Wed, 29 May 2024 20:23:49 GMT  
		Size: 4.0 MB (3971388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130090ca4730c8f0a8b4fc2fe1b2fd0bd6af649faeefd51a5df6dcc49f5ed3ee`  
		Last Modified: Wed, 29 May 2024 20:23:48 GMT  
		Size: 16.5 KB (16500 bytes)  
		MIME: application/vnd.in-toto+json
