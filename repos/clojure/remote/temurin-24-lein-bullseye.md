## `clojure:temurin-24-lein-bullseye`

```console
$ docker pull clojure@sha256:e16a170475d8ab4291e095cfc40cedec93d084a1d0240ef71738603058f4c0b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:be05f80670216f97fa2e9ad8ee8b15fb269314ef7da78a7e8c7ab2b5bd611179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201015127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f28908893ab7a4809ba9d3a60bebe4f3d98c0fc119c7328a8119b3259de6f86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a862a741c4a8c9476b3f8169f085a59370e44326dbe38a1854b138cfc335db04`  
		Last Modified: Wed, 02 Jul 2025 04:17:38 GMT  
		Size: 90.0 MB (89952014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fba4b27f4b21f7845ab758388bc67469fcc2579470611db06834106090d3eed`  
		Last Modified: Wed, 02 Jul 2025 04:17:29 GMT  
		Size: 52.8 MB (52793667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b655dd2be8230f27e9cec4f311982c7bf5a3572091a502e8e5c3aa5bca9f8b72`  
		Last Modified: Wed, 02 Jul 2025 04:17:23 GMT  
		Size: 4.5 MB (4514196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32d4133b631644fe24c53b97fef064462d067b3cfe985e115d914d8e7306396`  
		Last Modified: Wed, 02 Jul 2025 04:17:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:65ae7a8c11ee3e21b8232f8b3cc17685a1e6a9e7bd00f7992e7d467e1656b7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6752622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759e8772fcffcff4588c2b95f015ca1bcffeafcf7d8435653994ebbfc4258fae`

```dockerfile
```

-	Layers:
	-	`sha256:6daca201a814d92511519a721468befb51727ff189b3876967661bcbcf48b630`  
		Last Modified: Wed, 02 Jul 2025 06:41:30 GMT  
		Size: 6.7 MB (6734206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0551a4515eeff8ae2578c7f3cfb892968a6bfa71698006ea234240376a769c1`  
		Last Modified: Wed, 02 Jul 2025 06:41:31 GMT  
		Size: 18.4 KB (18416 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d4e9bbef963100c13d844c6ecc4a1f494d8147caac1cc4cc0b53cf056a91d904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198691259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b9e1efbad20b3606b7da42ef79aed64d0c0d983f55d964f18934f292224b6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8ac54386d4a9338c8561508d35cc624efee0d661ad8cdd0ddcca4d5714029e`  
		Last Modified: Wed, 02 Jul 2025 12:56:57 GMT  
		Size: 89.1 MB (89091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a23102081de8b243709f9b258c2fad52f27f41274fa18a1fcac94ae17eaea`  
		Last Modified: Wed, 02 Jul 2025 12:56:54 GMT  
		Size: 52.8 MB (52833153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4902899ac0a8d69fcb84327e027e81be6aa55235afc199d5f3eb8d617d4cac3c`  
		Last Modified: Wed, 02 Jul 2025 12:56:49 GMT  
		Size: 4.5 MB (4514190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd034db55d4e01b631f935c6f6641f6d6c62d6d222e33572ec66786e0e1937`  
		Last Modified: Wed, 02 Jul 2025 12:56:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e47ec207423fd2f17f26c3215587ebaac9066b64c6fc0b8d8106fc3ad37adcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6757771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2269e9328f37ff89390325a867ce1b8630acf83aae6247e6e512057492d5e450`

```dockerfile
```

-	Layers:
	-	`sha256:6a49b4299954281394071a307c46308279490d46b1dca6f0af3c65f5abf8cd38`  
		Last Modified: Wed, 02 Jul 2025 15:42:32 GMT  
		Size: 6.7 MB (6739234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fbe15293faf826eb0aeb285d048b9d589ee8d6c772550745c4926ca0c0b88ef`  
		Last Modified: Wed, 02 Jul 2025 15:42:32 GMT  
		Size: 18.5 KB (18537 bytes)  
		MIME: application/vnd.in-toto+json
