## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:e5ef7035f92c445e66d1b1a39d397c8dc920414db5ff513e655346233a5d8e57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:77025d37fd0266a6e1024dfedc2c2ee57983f37b0cae08704656c09a4b2426ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259603861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19175ac8dcd4dccae8450f11519a428b7608f2c2a85d832c795769a8eb8a9e8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_ROOT=1
# Mon, 06 Jan 2025 23:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8242f423d75ebf7f76848baef3eeece481a8be52508eaf61d0e6ad887cdea4ad`  
		Last Modified: Tue, 14 Jan 2025 02:44:25 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a57641fb51225b309623be986a74b3fa3455ab3bf2a8cb3801fd61133300cd3`  
		Last Modified: Tue, 14 Jan 2025 02:44:32 GMT  
		Size: 62.1 MB (62072602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c664b42bf4706c66d373fca7584bedd550628062ed3072d4d6d812bcdcc7fd`  
		Last Modified: Tue, 14 Jan 2025 02:44:30 GMT  
		Size: 4.5 MB (4514154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ac083ccd0f5a5a5ac4afa49ad50762c73e0ae780cb324edfabd1b34274f5c7`  
		Last Modified: Tue, 14 Jan 2025 23:16:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c2609786fb2e8da38811101ca1e53ae19627a928e12cfff3c1be09eeec8b9c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6552670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e150005938a9d8ed3b1442a9714b36cd2593311ca908547c24231fc6c20ea2`

```dockerfile
```

-	Layers:
	-	`sha256:4f3e68bd094f4eb2dce2bae0bd1e39ee7542b00b99842fc8b8bef0b8427b81a2`  
		Last Modified: Tue, 14 Jan 2025 02:44:30 GMT  
		Size: 6.5 MB (6534247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e290ed4b009cd891aed4c107a4e592d59a995cdd4462158094772a1ffaa56884`  
		Last Modified: Tue, 14 Jan 2025 02:44:29 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d0576678386bb8a7933a78526376eb9f0b2297a3e2c622128e957bae036ed667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258226276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a40a83a49c6773361e29710c63a0a83c156d9a39fcc2fa31475b3d4665f058`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 06 Jan 2025 23:07:46 GMT
ENV LEIN_ROOT=1
# Mon, 06 Jan 2025 23:07:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947bf59c3a98883a7ccfecb5a4185a268dc485dd6f84c20120ee1b840a307dbc`  
		Last Modified: Tue, 14 Jan 2025 12:26:54 GMT  
		Size: 143.4 MB (143360983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9fd1c334d13c550f31b48b9d5a8ebe502a08a8a5854a8274db4b82a3e01a47`  
		Last Modified: Tue, 14 Jan 2025 12:26:52 GMT  
		Size: 62.0 MB (62043829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0254484304ae15c8ab55f76e2722258afe4d6d2ea0df5bacf85f692787429c5b`  
		Last Modified: Tue, 14 Jan 2025 12:26:51 GMT  
		Size: 4.5 MB (4514140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c6bdb79236a6a7c81445cc166219b6aae5d8c4b637393959b436cdbbaa912b`  
		Last Modified: Tue, 14 Jan 2025 12:26:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:418f440458f6388d18ff7927836aadf6916ab9cc589213240e05cbcc1d01a999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6558484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96007625495c9c891e1827e972fca2e5e19cc7b985e42bf045ce83c1c9392c3e`

```dockerfile
```

-	Layers:
	-	`sha256:1d5523aec1d285d6ebe442f23d50a692216771a06b5f420ab2fa20d8685bd4dc`  
		Last Modified: Tue, 14 Jan 2025 12:26:51 GMT  
		Size: 6.5 MB (6539941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a7988fd08a58826a62e196fd026860a6241c79c1af11b1eecf6930b94041c0a`  
		Last Modified: Tue, 14 Jan 2025 12:26:50 GMT  
		Size: 18.5 KB (18543 bytes)  
		MIME: application/vnd.in-toto+json
