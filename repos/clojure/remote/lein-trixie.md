## `clojure:lein-trixie`

```console
$ docker pull clojure@sha256:ee7ec581f8b4410ca27b1b0a0ded5227ad3230f826602bc141342e4d4f6d2152
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

### `clojure:lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:64115677c98c0cee5b5796ffc7f58f0297083e3911d60ee9def6ebcd88ba5084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164992749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5d9424518c6a010c4a80f0117496534ce74a4208c23633c97b5a0dd6e43011`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:00:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:47 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:00:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:00:47 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:01:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:01:03 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:01:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:01:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d24d871fc8bf96d43663799f4f296f97196700667aa90a933fbe208a0b5a84`  
		Last Modified: Wed, 20 May 2026 00:01:37 GMT  
		Size: 92.6 MB (92574574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e0d1a2150d8b54cd50e5d78c93247239ce9e9b1d7bc0cd2d3b0e307f8ee177`  
		Last Modified: Wed, 20 May 2026 00:01:35 GMT  
		Size: 18.6 MB (18589412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44b307d0a6bd49704baa7b2e0a39ab28ac9ac1489d56b3ee27266e3e4420b85`  
		Last Modified: Wed, 20 May 2026 00:01:35 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22684ed83e7dbd72a7676699ca67bfeb68fb2fc6b18e48aa69324a12ef2fe391`  
		Last Modified: Wed, 20 May 2026 00:01:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:42bbc07d04c2d0c349ee042abf0166d4ef7a36652f9f948bdbeb5f37976cc54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b352377784b637e10972c157b9e6bde3257ef4c2236ea771a105bc670f16e073`

```dockerfile
```

-	Layers:
	-	`sha256:49478dad5c668627d4571f8d28d589bef783d85227b4647f9abd26095bad31e4`  
		Last Modified: Wed, 20 May 2026 00:01:35 GMT  
		Size: 3.8 MB (3784224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2beb86fc370b1d264e9cb5bf02edb91058b5a14f51ef1477cf98111e7004e6a4`  
		Last Modified: Wed, 20 May 2026 00:01:34 GMT  
		Size: 19.1 KB (19132 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8c84f6360d8294313d5c6f616c3c5ac2c06120775bc3014ad3c76b2612f90884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164280079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cda97af24d2d9e783f708002c1f47bbb74d9d7a633cf7b80be3d7972c411828`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:08:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:08:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:08:02 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:08:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:08:02 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:08:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:08:17 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:08:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:08:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f5f0158da6c1e07ce4cfe2f77b744223c4693b467d6de9945a7aa64bfac6a2`  
		Last Modified: Wed, 20 May 2026 00:08:38 GMT  
		Size: 91.5 MB (91542245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184b6b1a6c4ccf0272d0fa72fb7ce80009f21d99bab842786734cae42aad594f`  
		Last Modified: Wed, 20 May 2026 00:08:36 GMT  
		Size: 18.5 MB (18547429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edec91048558f68e59c58101f30cab7586c8d92cf46dbca55d96e3267222285`  
		Last Modified: Wed, 20 May 2026 00:08:36 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fa38b9b1da5f7006331de3a689d00e98ba0a3775c5b4816fd33be1a4a54611`  
		Last Modified: Wed, 20 May 2026 00:08:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7f3f560b074dba5246ebb33d9d198cca6d80aee254dc308db23c22ecac2a077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ff420a06a86e12a68177d62c355867306c7aebd9533ed53060e3e6e1b51911`

```dockerfile
```

-	Layers:
	-	`sha256:9f89a3112ec77025749b125cc77ae02ce265a02f5791a0d1b77bc39ac7fb581b`  
		Last Modified: Wed, 20 May 2026 00:08:36 GMT  
		Size: 3.8 MB (3784485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2bfae8a2dbb3921ec69c85f1acb250ed03c695ddd7a982dcbfe77c3daf19954`  
		Last Modified: Wed, 20 May 2026 00:08:35 GMT  
		Size: 19.3 KB (19278 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:844acab2a4447a53f735c2b0ee961957284f333367592bd7a40797edd1234696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.2 MB (168209178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdb97191990a5be2d5ad63b80c52f1f1bbc43fb1177e94c665857bf8a4042bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:05:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:05:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:05:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:05:58 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:05:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:05:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:06:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:06:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:06:35 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:06:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:06:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec19a238e74deea8797932477dbefdee56677e4d3a52ffe0c521942846410b8`  
		Last Modified: Wed, 20 May 2026 06:07:13 GMT  
		Size: 91.9 MB (91914019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135f69c042fab34199990adc50bee60749486a1e3da6f331dd15c6f2c547c347`  
		Last Modified: Wed, 20 May 2026 06:07:11 GMT  
		Size: 18.6 MB (18644786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e994daf65831ad119a5946a367b4aa43ef9caf86482153d6b5eeac12ce9eaf`  
		Last Modified: Wed, 20 May 2026 06:07:10 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9602a3689cedc52880f00c9ab09eb3c6d7625bfb0efb5a610a1f5e23b5f29`  
		Last Modified: Wed, 20 May 2026 06:07:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ff219bf58b4a0c02f048f86b7ba33746a0a068ba432e3e568085780e318385ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3787736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4213b2255d66a7568c954d4c2972d671e1d65607c53cd60748f6cbd1ccd0de`

```dockerfile
```

-	Layers:
	-	`sha256:6ea4959c3ddcb28314caa929758b64076c64743873f82fe300f486b8db804c07`  
		Last Modified: Wed, 20 May 2026 06:07:10 GMT  
		Size: 3.8 MB (3768548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee158af642de5a66dcfa5338d341af53b3843242ce3efeaef1413d4e5602bf9d`  
		Last Modified: Wed, 20 May 2026 06:07:10 GMT  
		Size: 19.2 KB (19188 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:beb19d4faaa0c1dcbda1403a44aacbe482bda73f9b11a7ad208529319074f8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160948872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d1b053382a727bda779af0b7b34a1a2cb09f642022472c3e82a6b2c3313438`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:47:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:47:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:47:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:47:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:47:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:47:23 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:47:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:47:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:47:36 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:47:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:47:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:47:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:47:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77a591861f1b273c45555677bf026cf5bd1c028b177d75ed2f6b38f41fd6977`  
		Last Modified: Wed, 20 May 2026 01:48:03 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f1ae3c6cf0a8618a246c85e1c6d89bd8bf1c684ce139f05606b3e9dc9b0f00`  
		Last Modified: Wed, 20 May 2026 01:48:01 GMT  
		Size: 18.6 MB (18630598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee390993eb833dfe5ffc195e5d42a539962222ccc140219cc4ca9e1d5f7cb69`  
		Last Modified: Wed, 20 May 2026 01:48:00 GMT  
		Size: 4.5 MB (4517730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc75e60971d9d3ddf99156e47c0e2125fb6e7bc99cf4ed77b4a721f2c6187ed0`  
		Last Modified: Wed, 20 May 2026 01:48:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:67ec40687e2910d222203feb548f59af6676b2395d22b174bc6084a0c55f349f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7061755afe49167a5df2fec7ce3f204dc7844ecd6d535a0992561d3116f0927e`

```dockerfile
```

-	Layers:
	-	`sha256:1349263accb584abb112c2dc31f5cbe2d8b527f5b90409c6eaf08ae9b2ff7702`  
		Last Modified: Wed, 20 May 2026 01:48:00 GMT  
		Size: 3.8 MB (3765213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3605551ead74114ec8ef93f47ed7e4eee72189b7550f2800056117e24d27314`  
		Last Modified: Wed, 20 May 2026 01:48:00 GMT  
		Size: 19.1 KB (19132 bytes)  
		MIME: application/vnd.in-toto+json
