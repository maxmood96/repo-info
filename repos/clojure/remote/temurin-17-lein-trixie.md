## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:387d56605942e27c7e874de923d3db7314571ddd36b994fcae1ebe672cf91ae5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:48c0357627297a3c7ae04226009f087ece572ad8a3e9fcc9f2aa47b8aeb4af92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267783293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd1542edeb81d9f7bb7729d44c46c1d24d1b9bf7abf58da5446cfb49edf97ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccab1dcf5bcbf50dba11b2029c18b4b9e7744afa13ed19f66c1a01f2a2e69dd`  
		Last Modified: Tue, 03 Jun 2025 17:51:50 GMT  
		Size: 144.6 MB (144634987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece2c47ab088ec0ff81dd20fceef993239cc7cb9398c75a83c6d4a6d726d5e4e`  
		Last Modified: Tue, 03 Jun 2025 17:51:46 GMT  
		Size: 69.4 MB (69386810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d525cbe8ed350941304812ad4a24923d3e8af3d44dc426775a4e09a363edfa`  
		Last Modified: Tue, 03 Jun 2025 17:51:41 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da3d16d5d37794473de86988ab300233629960129f38989f7d25bff242fb432`  
		Last Modified: Tue, 03 Jun 2025 17:51:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d02db19a70e67550d3c5f7c4c959103dda436785492ccb200528155c2054788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6351607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310ddf8681a6bf2cb0b14db5be0ec42053f0b69810e7312597fb4f2ccecc905a`

```dockerfile
```

-	Layers:
	-	`sha256:cec7f73656458b062d9cc267f310498223b510e22933807e9238a80f81d4f471`  
		Last Modified: Tue, 03 Jun 2025 15:35:59 GMT  
		Size: 6.3 MB (6333204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db354d1d30bde2f4a25497648426b5dbce8134b79d8ac873cbc0a972793e6dc4`  
		Last Modified: Tue, 03 Jun 2025 15:35:59 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:33ea91765015f5c1f39ed8ca646f5bfcd467f5c6684a74345fdebf9b244428af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267436163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f20f86754659eb90f17a2a3818a6f572e820e99b3f47665c0d9a2363d73dc65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0716c0c482281cd83847775856a8d2b5dd899b670a27f613e6c9f63273d5d058`  
		Last Modified: Tue, 03 Jun 2025 12:50:48 GMT  
		Size: 143.5 MB (143512625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb3809d33d3372cbbded903f2b2f795d2303e060833b5a34da7b3054653f6f`  
		Last Modified: Tue, 03 Jun 2025 12:50:46 GMT  
		Size: 69.8 MB (69790626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0275f335cc25aec9472ce4ef00b7b16be02941aa49eb089038525ebb318dee89`  
		Last Modified: Wed, 04 Jun 2025 14:28:04 GMT  
		Size: 4.5 MB (4514189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1186ffbc789f828b7f11639948bde823098895cdeccc7f5001089277bb2a540b`  
		Last Modified: Wed, 04 Jun 2025 14:47:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7a9ff1d330e04d644926c9e864e9caadaff5e6cbb8d049f71a8dd375f58dc693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6358691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fb3e95efc20be822d6882f6e8a7b90859fe5a87a5fb8ecbe5405e051468942`

```dockerfile
```

-	Layers:
	-	`sha256:76cd88148d954ca1e21efbd62edec125c0da420c90ade0ce43a37844a0a58a60`  
		Last Modified: Tue, 03 Jun 2025 15:36:05 GMT  
		Size: 6.3 MB (6340167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1042987d3c8295cfd87cf9e7a8703f7407895c9e4b4f3201e613ba5e8d5d1fed`  
		Last Modified: Tue, 03 Jun 2025 15:36:06 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:868c1214928ed65c69d138f4128bc9cdb6c43971294eb97decf2740c05432901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276592082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41411b74fe26d7251c5aec3191128795622102985699893a20fc064b63a9bcd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fd7f4fc1007a30b1949050f0ba69932c1032b69ee73e8eb4d85a1f11db273`  
		Last Modified: Tue, 03 Jun 2025 08:51:10 GMT  
		Size: 144.3 MB (144280585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa748a12433563c17752df3675dc7ce7b177aa5afd7612701f9a27f4ac799ee`  
		Last Modified: Tue, 03 Jun 2025 08:51:09 GMT  
		Size: 74.7 MB (74716333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8799ad64e9e053422b2a13a5d12d5ff83d04ca13c68d2e88971b90a4af8d9d3`  
		Last Modified: Wed, 04 Jun 2025 19:45:05 GMT  
		Size: 4.5 MB (4514192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af588cf8e4300d97ccc799934fadb27b23922a8893ba7b65d6256c9ece4b943`  
		Last Modified: Wed, 04 Jun 2025 19:47:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c8b8d4d1f830f003f40d208013cbdb6c389261878af388cba882c0bb67aa3eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9956214582f9d47aecd7dbf424bdf3e938ed0dab7853ce683b91541d38d0c3e`

```dockerfile
```

-	Layers:
	-	`sha256:b2a6a9f8691eafe45c0039c4e12f1424d5a1498b2574cbb319a5431efcb917f3`  
		Last Modified: Tue, 03 Jun 2025 15:36:12 GMT  
		Size: 6.3 MB (6337312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64455658dab97de7226adfe06e9dd5d40709fe4545b5982f2280a0b1354fc164`  
		Last Modified: Tue, 03 Jun 2025 15:36:13 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3db3f332f8d995a0a4b81b45eab58bf1bf875410b1b0b868285076811e6d87fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258969944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc46c29a483ccfee7d4c2579de7958eb12d9dd49b496a366db57eb4e5db6b31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23085f00cc2fab5db834062a7c0906b2e2764d3635d1f0a0795de617ce89767`  
		Last Modified: Tue, 03 Jun 2025 08:54:41 GMT  
		Size: 138.5 MB (138492460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbca66ca594781be9094f7a8c8822afa3fd4c9ad7e40bdf9ecce591ad38b7f1`  
		Last Modified: Tue, 03 Jun 2025 08:54:32 GMT  
		Size: 68.2 MB (68231403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab29096fa3de1a33cb406763ba06668bb8fe7c937cecdba2fcfa5003ad8320b`  
		Last Modified: Wed, 04 Jun 2025 19:59:44 GMT  
		Size: 4.5 MB (4514242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aacee64ce617a29d1b70ed0279fb866d82d5a81ca6b5d617f26d7e2e090d213`  
		Last Modified: Wed, 04 Jun 2025 19:46:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:810c4421d39a59353f6c0c797573d91351e13f9acde7b812e766dd847949c742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9812427774be90b51335a381be9296982d6ffc22b06bd2418178518f950ba6ac`

```dockerfile
```

-	Layers:
	-	`sha256:0ab0bc1021abda3b73ea7eaebf17c80eb0c6c9a2b4ccb3ff38ec99607910a558`  
		Last Modified: Tue, 03 Jun 2025 15:36:18 GMT  
		Size: 6.3 MB (6319107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f05bcf23244f7e40ca817ba3b6389346acdc302fefded413ca7ca15eac2e0d`  
		Last Modified: Tue, 03 Jun 2025 15:36:19 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3ee0589d5b903c8b1f59d2781861428dc752b316174f3f5963d0e5d311c41b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258619129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffff18e674fc72791040b099320152bc92ee22c71636cde03e537763347ef73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3774d10487b032eb1a2167ed2afb6c687158159ce2ed561584cd53595528c`  
		Last Modified: Tue, 03 Jun 2025 06:16:20 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f947c729bef8e82bcdd6c95a3e11ed2fe4baea3a590c9d96af4d013e10589`  
		Last Modified: Tue, 03 Jun 2025 06:16:20 GMT  
		Size: 70.1 MB (70108742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53bffbe0fdb44fbec025d29a453adfa3cc6cf9a9a3b177fbfa0b783ce1d828a`  
		Last Modified: Tue, 03 Jun 2025 06:16:18 GMT  
		Size: 4.5 MB (4514183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4cf46c5d66e8ce8ee76c489440d27fef1646cd8bc961fd8aa0b13c75185f30`  
		Last Modified: Tue, 03 Jun 2025 06:16:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:151d80f35eb091fbe732dadc0d12761e591ab48c505a72ed87c85e14992352b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6347583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5117b1ab1fb1233c71c2971152a9d2382d6ddd808ef3e9ad37944c3ef10bb00c`

```dockerfile
```

-	Layers:
	-	`sha256:3e67d4308dd288fc6d9f05130e9fbdd6ada8c215266c939b33c6ad935f2c6d02`  
		Last Modified: Tue, 03 Jun 2025 15:36:26 GMT  
		Size: 6.3 MB (6329181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8038c07de600bc43045153d462d9e46dd3b96bd60f041ed6aca853a2925579d1`  
		Last Modified: Tue, 03 Jun 2025 15:36:27 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
