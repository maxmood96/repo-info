## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:8f88886d10594c5f019e426a050d173855b338d22f85bb4966aa0d286007c77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:73857606e5dfa0839bcd690111385c253e2af791635c0bd071ffdddc422cdecc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209536820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1580b67eb7077127a9c00b8580ad90a9ce0ebc17e10bc3d887d9ea5c0d5cab1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:29:18 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:29:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:29:20 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:29:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:29:20 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:29:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:29:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:29:36 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:29:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:29:39 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:29:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:29:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7462f33b89bb1c152a23b7ab72eed1d7cdb12b31a227633d49c79427162abc`  
		Last Modified: Wed, 24 Apr 2024 21:52:14 GMT  
		Size: 158.5 MB (158498295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a97411286dcd3df3cf10c7f8ca75e31c893584cdbf85833d95412cae394827`  
		Last Modified: Wed, 24 Apr 2024 21:52:03 GMT  
		Size: 17.5 MB (17488464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57bd098834cdad2f5be90c7e6777196b6d20182e4d6100037298bc557893235`  
		Last Modified: Wed, 24 Apr 2024 21:52:02 GMT  
		Size: 4.4 MB (4399180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6f16e3eab2d117882f3439bada1019858ecafda4f33a7754891cb47d3dd187`  
		Last Modified: Wed, 24 Apr 2024 21:52:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7503bf37b1cd1c128b14de92955d073cd6deb65d23e3403c4dbcaafc8deaeb27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207556416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52561c03ea82068d5bd28a08967deffbf317c42f8f25108a401ff2c275778fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:12:51 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:12:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:12:55 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:12:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:12:55 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:13:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:13:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:13:09 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:13:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:13:11 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:13:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:13:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b59b9a60b19751e0df08713db8963a0fd972e4179b83db306f1cc7095416af7`  
		Last Modified: Wed, 24 Apr 2024 19:32:00 GMT  
		Size: 156.7 MB (156665539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91d11b314a01f42a294867601fab9a36383c3c2d737091a17668cdf01700e22`  
		Last Modified: Wed, 24 Apr 2024 19:31:51 GMT  
		Size: 17.3 MB (17311337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f274eb2105b336dfddc45df1ac5ce0012f2511cb64f8d6fd889adcbfb59d5008`  
		Last Modified: Wed, 24 Apr 2024 19:31:50 GMT  
		Size: 4.4 MB (4399204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9e3113ec01a54a6b8dec724b4a68a18c2ea4dcdd5d07de880088ec7e022965`  
		Last Modified: Wed, 24 Apr 2024 19:31:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
