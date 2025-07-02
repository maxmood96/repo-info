## `clojure:temurin-24-lein`

```console
$ docker pull clojure@sha256:831fd603969750a1a1946e2f9dc1f985dbeb1490d16366c4e247b0d4e14564ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-lein` - linux; amd64

```console
$ docker pull clojure@sha256:03737bda9253256cf440c6851cb38cab7fa4aa52d152dd0a952452f292f6b3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205033055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c53b3965922bdfd01e2d66abeda911b735369a7534cb0b2a710c150f7a97989`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a862a741c4a8c9476b3f8169f085a59370e44326dbe38a1854b138cfc335db04`  
		Last Modified: Wed, 02 Jul 2025 04:17:38 GMT  
		Size: 90.0 MB (89952014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea01056e650c19e50f7c6ea684f1d330f465cdf718caf344661bbf162f8977`  
		Last Modified: Wed, 02 Jul 2025 04:17:34 GMT  
		Size: 62.1 MB (62072193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4176aa4addb3e5e05d410f6d1754bf26f545ff1c48f8b7b47669197180f6af14`  
		Last Modified: Wed, 02 Jul 2025 04:17:28 GMT  
		Size: 4.5 MB (4514135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c77bfe522852b67b5669425c72b53d17444c7104f89cf93683628375d2ca4b`  
		Last Modified: Wed, 02 Jul 2025 04:17:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:3135b4ea4cdb53059f2d078956b9f562785d86a3ddd8115a579b159a06161fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c63698a84fb03e4a461cc238f607697b9b885d2c83be815171056ec53258ff7`

```dockerfile
```

-	Layers:
	-	`sha256:9818ff975600e469bbf114d6c587bda91ba70f3ff1b8075fceb1450705ec9a25`  
		Last Modified: Wed, 02 Jul 2025 06:41:17 GMT  
		Size: 6.7 MB (6654017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0199fd791b9b30ec258c5d60cf83cc0770e729778713170fa7fd0c51f82defbd`  
		Last Modified: Wed, 02 Jul 2025 06:41:18 GMT  
		Size: 19.1 KB (19066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfb26912d1b8ab30f18803be7bd7e6f617da670698b7b1b4718a6ef059fac02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (204002629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd23d87364d4a1b37e9c53a7999c7f03b3fe502450e085fcf2893096d76fe62b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed4c8912abb05c9d16227b79bd4d0c95ee19d89d3b3075be39be91242157b3`  
		Last Modified: Wed, 02 Jul 2025 15:43:39 GMT  
		Size: 89.1 MB (89091225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654c13fd1821c7dcc2bef08a176f67be22a68c792fc0fa03d3e4a232977a0b30`  
		Last Modified: Wed, 02 Jul 2025 15:43:39 GMT  
		Size: 62.1 MB (62058028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dcd3f3a5d47b69f315e8bed9ede6cd1c8cb90b6928e9e433b3573ae7a4b83b`  
		Last Modified: Wed, 02 Jul 2025 15:43:36 GMT  
		Size: 4.5 MB (4514162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f4234c97eb2843cc50c5c9a0af79ba1aec7588b639bf89743585dea975ec27`  
		Last Modified: Wed, 02 Jul 2025 12:58:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:2af1b9469753d4b5abe8983ea5312399edac76b08c3c490b28572c0cd6719af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6678941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb107f08f54381b846dff54a93e45ccec5ec7548a1ee878179bf4f1076e952a`

```dockerfile
```

-	Layers:
	-	`sha256:434b47490c7b092a06e199a5185f4edd46ee60b1eab89e4ec79ff8a15d83409e`  
		Last Modified: Wed, 02 Jul 2025 15:42:13 GMT  
		Size: 6.7 MB (6659732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66209f03c408633a735d2616cfce9fb8d4df39c2f7a42cbe92a742e76dc52fc`  
		Last Modified: Wed, 02 Jul 2025 15:42:14 GMT  
		Size: 19.2 KB (19209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:4db91296f2be809c3ee1d50df44e7c40ad4c8f4de83de052ec3077088f9f6ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214087554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd11f12b86352fd788965a0c559fec29b4c69c81e1cad97deb21c4351b4836`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19b842940b208b4f06e0b58568d49e75601533443c8580a39697d58f645f300`  
		Last Modified: Wed, 02 Jul 2025 14:02:05 GMT  
		Size: 89.9 MB (89920275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2212f273c7d33fc1e2fb77e48186d83b91e6a2d06435258619533abee2bc85`  
		Last Modified: Wed, 02 Jul 2025 14:02:03 GMT  
		Size: 67.3 MB (67315405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d975222e40770d45d3b36eb416358215da6f516e0bd730681005147e768c371e`  
		Last Modified: Wed, 02 Jul 2025 14:01:58 GMT  
		Size: 4.5 MB (4514201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bdfc4757f8d53e930a66e1988da9681dd01425065bdb172fb381cc6175e578`  
		Last Modified: Wed, 02 Jul 2025 14:02:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:31e88dbb85a41e8f42bf550e24f2269f3c078aa1cc05df7141e55d440ec969c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6215762f5dbb88ecc3ce631dbfd8d5a157a664ef547786f86f4964d2e4be337a`

```dockerfile
```

-	Layers:
	-	`sha256:529e4c9a6d48a7709f375e1a2740b935a7b6d09c73e073ccd197912b728da523`  
		Last Modified: Wed, 02 Jul 2025 15:42:20 GMT  
		Size: 6.7 MB (6660196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f99e8b291f4dfc09d19a281cd20011aac5bbdb10c334cdeaf8e49fc6c82cb59a`  
		Last Modified: Wed, 02 Jul 2025 15:42:21 GMT  
		Size: 19.1 KB (19122 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein` - linux; s390x

```console
$ docker pull clojure@sha256:ca8713a6981fe4e8b5a36ccd8837c1025304a1d765e56aa10e30aab584d0d78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197981733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991ca24b9264c2682d902158dfa707c60096d9fcad3be33137c478e734af3c5a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5a54602bfb697ba4ba032fdb5bd7dd65566e4d748c05b7a6ab9306169bfb7`  
		Last Modified: Wed, 02 Jul 2025 06:56:10 GMT  
		Size: 85.2 MB (85216779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0993c14ea27f7f2b627899065e9190d6d9e7a76b43d3e869516f3c632f7e8dd0`  
		Last Modified: Wed, 02 Jul 2025 06:56:10 GMT  
		Size: 61.1 MB (61101043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de52d053ef1fc5b31253931f1e5549b9eb81a50ba3565def5b860c02ad8da840`  
		Last Modified: Wed, 02 Jul 2025 06:56:01 GMT  
		Size: 4.5 MB (4514196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f85a4bec8075969290155d1453f6efbf4e0d7c9de53d1f9d0c3bf6ad70163a`  
		Last Modified: Wed, 02 Jul 2025 06:56:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:3274912c90bff33b48a136ec7bb2d46cdd1faa52e6b3a2448542432c73fe436f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d6247194623993a7fe340c3ca264790aa4b54c774ce4f43c9177d4f410ba89`

```dockerfile
```

-	Layers:
	-	`sha256:30032eb46995bccbd5d7273c41905e6024e399b80501638c7c41816d1cb9c643`  
		Last Modified: Wed, 02 Jul 2025 09:40:43 GMT  
		Size: 6.6 MB (6647941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d61e50a5a3080ccab5ca5d539a4dd9088969af70d8b9490b32a9ddb2416eb9`  
		Last Modified: Wed, 02 Jul 2025 09:40:44 GMT  
		Size: 19.1 KB (19066 bytes)  
		MIME: application/vnd.in-toto+json
