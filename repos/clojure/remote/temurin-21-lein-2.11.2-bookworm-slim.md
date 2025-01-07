## `clojure:temurin-21-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:4e7a42a2b94a769cb9cb98aa2d0d36f111a7bef86c24fd01d1b06561b8bd5c4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c843c5ea526da3512e057cfc975e1fa7bbeef5573bc5dbe40a50548b52197db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241579105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94968f4cbf60b0b48c1cc8c6741adcb7276740b3a2a838b2b30c2fa9301fb0b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e9cc3782817ba7dcb0fbcb9dab1a6508d54c72983a093a0bd886d430569c2c`  
		Last Modified: Tue, 24 Dec 2024 22:38:18 GMT  
		Size: 157.6 MB (157568694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23feb4db385867d1fa5430422b713bc2438d1662bd5968ff6ca5a7498e913ad`  
		Last Modified: Tue, 24 Dec 2024 22:38:16 GMT  
		Size: 51.3 MB (51264204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a9cc305ca6367e58ea0bb7fec0562db23792f3a72a742144ea7417d3be44eb`  
		Last Modified: Tue, 24 Dec 2024 22:38:16 GMT  
		Size: 4.5 MB (4514198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c7003ed2171ee53c62b1486e15fc1e0ea6eca43ca45a3be8a1b42de3e45fe4`  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f0afcffdbd6a73c47631828470f8c1a247a78420be5098b948ddf0404b47de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f825b8658f8b156e88c9d19e49a8cb7a24b04faa9789a1214d9bcb65d3dddb`

```dockerfile
```

-	Layers:
	-	`sha256:05ad5fa3ec3d1ef24cfa6b70487e7be64883238a7b27c46ecc10b77225854f1e`  
		Last Modified: Tue, 24 Dec 2024 22:38:16 GMT  
		Size: 4.3 MB (4324193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1a2071a6c99cdcb8e3e2d5db43de861a9d77c042d43639d7c9aec3f6c57eefe`  
		Last Modified: Tue, 24 Dec 2024 22:38:16 GMT  
		Size: 19.1 KB (19120 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5eb1407981e9238fc7348b2592c25ebad8e421936f22acd6124c108449b0d040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239600000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e94307919defa43a39f5794d80f787731c336c1a2bdd01f0d4ca9e1c1da455`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260e6f636d1eb05d00e219fab56e3c7bcc3684217f5d55e0e62a3009ee3468f9`  
		Last Modified: Wed, 25 Dec 2024 07:31:19 GMT  
		Size: 155.8 MB (155793090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd67887429f959966c7a3d9eecb8085ad2118c0c7ddc5f0cab412312fb6f9282`  
		Last Modified: Wed, 25 Dec 2024 07:31:17 GMT  
		Size: 51.2 MB (51233578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf06777b6d537e536c28144724e8bb1d04617cd4f4d1db468df51eece79542a`  
		Last Modified: Wed, 25 Dec 2024 07:31:16 GMT  
		Size: 4.5 MB (4514182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabc29a419291e96922dc847e69e5587771449dd078fc97b37f3a06c917d2bc5`  
		Last Modified: Wed, 25 Dec 2024 07:31:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c562fab54a8cf3ebd57c4a5bf176b706ffb707b6d929f13092b7c600551b827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4349174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200634534acd13dfdf5c76ac39700be4f643ce00938ae447cb570beebd67b6c7`

```dockerfile
```

-	Layers:
	-	`sha256:052f0142cc5a3bd430bfc275fc76a625dc63640ad2930bf79bc24c673f60874d`  
		Last Modified: Wed, 25 Dec 2024 07:31:16 GMT  
		Size: 4.3 MB (4329909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad6d8104d87063d5877ecaee2bcb748dc673ef9b48d8b1bbf2f3d1a3d788f4c`  
		Last Modified: Wed, 25 Dec 2024 07:31:15 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json
