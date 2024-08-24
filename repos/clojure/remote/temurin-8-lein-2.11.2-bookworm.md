## `clojure:temurin-8-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:e0d57e4fdc70323ae80b8f2ab1388d0ccccddfdf4e8b0b9f5e0ff7b767e5d16d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1e7d5a430889b6e4bf7bedbcaef388c34f25b3b10eed6f2fa194e2678066d23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219363609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5b501d5e0c941d6ec6992a8204c0b9c57ec6803eff1fc3fc8033e845252882`
-	Default Command: `["lein","repl"]`

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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d32ef89b433f016fb9c4de3363df1b579b23fd2725455872dc865da253571`  
		Last Modified: Fri, 23 Aug 2024 20:01:57 GMT  
		Size: 103.6 MB (103611881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b37d192996a74acfce8d88ea79cd68488a93525b17c26c89c5556e5186aa25`  
		Last Modified: Fri, 23 Aug 2024 20:02:00 GMT  
		Size: 61.8 MB (61799584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd428a1284a30918ef550532de08232b3b81bb5bb47e0e4ec06f0ef549ace68`  
		Last Modified: Fri, 23 Aug 2024 20:01:59 GMT  
		Size: 4.4 MB (4398032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a711433fbd8d8ff7fb1baaa69dd6d278259cd3c3b341be41fa8163689410bae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6404542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac1de6e6f629126f3c45c4f8acaf286c11aeddd53ebf84e0a261f3cb89ece3a`

```dockerfile
```

-	Layers:
	-	`sha256:f11a8565bc1434c47adb9159399f84ed48508e80cf5778314f10d24e6e228a0f`  
		Last Modified: Fri, 23 Aug 2024 20:01:59 GMT  
		Size: 6.4 MB (6388506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975189aa47cc054d6b71dfd5e63eb01e5045ffff3710c5526ba49ef58def8751`  
		Last Modified: Fri, 23 Aug 2024 20:01:59 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2676c6838210a03ec3988ad4cd7c41ecfaeac59bdf7885f3988f18dbd22898ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218390133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25d531b27ea3bce4fb08e762be948945e9f5cb8b9ed7354345b10acc1a83e35`
-	Default Command: `["lein","repl"]`

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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df82fcaf825bfd95bf3f6a60bf33b338e56c6f56d64178e49f0cba774c6851aa`  
		Last Modified: Sat, 17 Aug 2024 05:50:41 GMT  
		Size: 102.7 MB (102729249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a605bd49da84077705528f8f356851acd65ba491dad7c86d3614f2efdc7f04`  
		Last Modified: Sat, 17 Aug 2024 05:50:40 GMT  
		Size: 61.7 MB (61674170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4ef3555978b1534f29b7bbcc8600750a6651f46abd97140ebe3c91fbd579b5`  
		Last Modified: Sat, 17 Aug 2024 05:50:39 GMT  
		Size: 4.4 MB (4398090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3fbc97382cfea748319acd1674573b34e32c54a9a62fe5f3abfe95a00efb83bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6411382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fdbb80c0fbee1b190922406f50acc65515d6e28a39be4888c4c23a9ccda284`

```dockerfile
```

-	Layers:
	-	`sha256:143b8c725b7182dd73b6afe37764f13e7387f385f5f094a08d5e5569db5d4a3f`  
		Last Modified: Fri, 23 Aug 2024 20:42:42 GMT  
		Size: 6.4 MB (6394824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ad4a91871c4451097fec2d5e6c22a3039a07fb94438b9fa1ee1cdc32e08558`  
		Last Modified: Fri, 23 Aug 2024 20:42:41 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json
