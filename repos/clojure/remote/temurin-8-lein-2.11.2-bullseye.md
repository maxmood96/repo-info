## `clojure:temurin-8-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:6acaa0a466312b5389076fbc1fa1d39e7c52db5493f71a3664297353eccd09fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:99534a06fc83684cf7c44ac783d8f7305091ef2aa64e1389b9f03b4bbfe74a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215741282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd6645537c574f7a89693520aab0ea585daf367c9e7b8f436b0fe6406bc523d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d32ef89b433f016fb9c4de3363df1b579b23fd2725455872dc865da253571`  
		Last Modified: Fri, 23 Aug 2024 20:01:57 GMT  
		Size: 103.6 MB (103611881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b3bed5e30fabd13731a21d37f6c427348ac9b010d9c8503ecf215d868ef0ef`  
		Last Modified: Fri, 23 Aug 2024 20:01:59 GMT  
		Size: 52.6 MB (52646634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84eaa6e817bec400f19dee5ba93e464a383e3fdd803d14d0485a2bb824b0bec6`  
		Last Modified: Fri, 23 Aug 2024 20:01:58 GMT  
		Size: 4.4 MB (4398060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ca8e6d10644af67cf26dfde041f17b098ac3bae6b120881fca73dd7c01076abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f75fb0e5ce6fe0d7c7783fe49cca2eb06c3415c74e186e43c6d79e8e36acce`

```dockerfile
```

-	Layers:
	-	`sha256:49002a3f062e19301696a125ab0cae1f1913a59552bb153d0bf3d0ed1030a1c7`  
		Last Modified: Fri, 23 Aug 2024 20:01:58 GMT  
		Size: 6.5 MB (6480982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd1afa3ca41ecc4b181d0c19b3539b0e7c997666a9bf80924195147f2996e39`  
		Last Modified: Fri, 23 Aug 2024 20:01:58 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:581c5ab45e16ef0464c928554733666e5c4635cdfb23e92728fbc001e9b3ac0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213518544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec66061b2e1f31a2819cf64bf3ed7521c1c8ae978f7907b030e304be36805ac`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5737429281d133cda0b984ae6835507307684f383e03361e715daae49e451af9`  
		Last Modified: Sat, 17 Aug 2024 05:52:41 GMT  
		Size: 102.7 MB (102729249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd666edebf08a8ced26040d4d4a7d7d0f5e15d1aa6ccc7b17475df43bbdda6e`  
		Last Modified: Sat, 17 Aug 2024 05:52:40 GMT  
		Size: 52.7 MB (52661279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8802ac5b305f301431c62ddd18f24523ae5d7d6f2117fa155073c95427ee62e`  
		Last Modified: Sat, 17 Aug 2024 05:52:39 GMT  
		Size: 4.4 MB (4398063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ee337dfba7be5a2f0e73c860098253ca74422976b7fe1e0e21a4f5d6e073d9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6502364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de92f7b5654a765ff5abf6f7b2586fae94bbdccffee5fdbabf4c3103b13b175b`

```dockerfile
```

-	Layers:
	-	`sha256:7146b0ab7fb1aa5ef05cec8247b6cfc04302d6b52bab9d24cac4ac73644ec4d9`  
		Last Modified: Fri, 23 Aug 2024 20:43:43 GMT  
		Size: 6.5 MB (6486636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e888ce63d0596318a68cfacdffe026621122ae8a587fbaab3fb2854e9ef919`  
		Last Modified: Fri, 23 Aug 2024 20:43:43 GMT  
		Size: 15.7 KB (15728 bytes)  
		MIME: application/vnd.in-toto+json
