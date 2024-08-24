## `clojure:temurin-22-lein-bookworm`

```console
$ docker pull clojure@sha256:0ed3c018aefdd7b9dcc553905a7608c2df2f6b2df8fc6bf2181b26d28237a444
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:53a5aa72fdd0c41b5f852664fa7b32788b4f22b655ce72e1c685efcb49dadb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272233716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d49e2b56886a34a3f05854a6d9638d52c733d6aa500b12b1fd7c18ba7fd00e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2622cda60e815645d4a0e8b58ed2b29ff684fdd0b6bba06b31a7f17dd07b90a0`  
		Last Modified: Fri, 23 Aug 2024 20:05:33 GMT  
		Size: 156.5 MB (156481631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1756011097d905d76c0278477fe0d76f4469982fb16e1e3239234f5f2124d34`  
		Last Modified: Fri, 23 Aug 2024 20:05:35 GMT  
		Size: 61.8 MB (61799537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5f44b8cc782ad76376a0f4cd75aa825706f0ca58732cfa9ffc6d5d5cab6e2c`  
		Last Modified: Fri, 23 Aug 2024 20:05:34 GMT  
		Size: 4.4 MB (4398038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21648ea515947c513dc0866c93cc2d44e0b0720a2e8fa09dc5c65f703c2e964e`  
		Last Modified: Fri, 23 Aug 2024 20:05:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a7d4285be51222ec43bfc4080b7f0bf8561bff27c34a8b53f7d3cbbf36914ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6382349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606a3f14e77fa23012753ca58370eb2061e70dd0a99a8aa6908f373217405a4f`

```dockerfile
```

-	Layers:
	-	`sha256:3d11c6c2fa1693680ac310d06a8dc69a36fe2913261c6f31f87e376e767ab91e`  
		Last Modified: Fri, 23 Aug 2024 20:05:34 GMT  
		Size: 6.4 MB (6363657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56623366ec18e4bc2744e113de93456b218f1dc6a4217fa9d66ce1718c5ce3ec`  
		Last Modified: Fri, 23 Aug 2024 20:05:34 GMT  
		Size: 18.7 KB (18692 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4a5a3b9f10abafd5a07a73cef7bda9a00de51ba9c52ed8ccaf667c51d489cda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270165058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250c589b2ac9bea9e157b7627e09cdcd3084441cbd79b0edb5cb12bd356d8b9a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648268b85fd4c094d06e828855a5f546b3a97f5c94583775fd9a0fed4c242a27`  
		Last Modified: Sat, 17 Aug 2024 06:33:14 GMT  
		Size: 154.5 MB (154503694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab563a883606fd29840d4049789082ab55af23254ac1c9b4c8bdc78a7797c430`  
		Last Modified: Sat, 17 Aug 2024 06:33:13 GMT  
		Size: 61.7 MB (61674250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1cfbf48d731583add268aefcaea4e2d035f83961942e06b122752d79a566cf`  
		Last Modified: Sat, 17 Aug 2024 06:33:11 GMT  
		Size: 4.4 MB (4398091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73f0d0d6d1d07a862e64cb444ee99d6c3bba6c02029e1631a2db2c5b9b9c408`  
		Last Modified: Sat, 17 Aug 2024 06:33:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6a51db22e2caf204a89c1d68a8c8f669096cd7005604fe12ac775c8d8e0e963b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfd0b1b34939342d878e895cf64b686ef75ae17101a0515e2e8c379e665db4f`

```dockerfile
```

-	Layers:
	-	`sha256:af6dd914380a478db7423219b64055e15cec4251f57e36a2d67b4053be27fa44`  
		Last Modified: Sat, 17 Aug 2024 06:33:11 GMT  
		Size: 6.4 MB (6369999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59d496cdc9a4afea921dc98dbc9b9160dff01588bd791e1fcc6610e063d6adf`  
		Last Modified: Sat, 17 Aug 2024 06:33:10 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json
