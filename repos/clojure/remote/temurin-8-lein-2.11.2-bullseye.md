## `clojure:temurin-8-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:b43705a0ce0c6913d912860c478994d17fa860e9d7ae10fc937bf697509f632a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:223af5d189c4b7df43f8306be2986bdae66d7ec0f6511b9cff9f6d4c66310b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165770209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2314680d5ee360b81d7adef8783674c4d1538ec13fa2f3f6de4400aeac0f68d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030ffa542227a0427269b511e6b4e898d12fd65c8ba96cf48a3029baa38a894a`  
		Last Modified: Mon, 05 May 2025 17:06:45 GMT  
		Size: 54.7 MB (54716188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a676b0d9adbbad8180222c98d058686651cd6bf7a486d08ec7e0641f2b158299`  
		Last Modified: Mon, 05 May 2025 17:06:46 GMT  
		Size: 52.8 MB (52792112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b2c2ff9cc3814063d77cc09eb8ffad6f7dcd2f4adaf5e7d0205cacea07b09`  
		Last Modified: Mon, 05 May 2025 17:06:46 GMT  
		Size: 4.5 MB (4514137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:54f8da33ffe7b11ffc7ac0f56922182f5de2fd02050ee441a8490bcfe28d9270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6759788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4f4f8b83cea7a6b69ba93482d69d33d0abdf7f38941f357602ef028bbdcd83`

```dockerfile
```

-	Layers:
	-	`sha256:de54cc8253cc09d5fd2e266465ea68e85863d46a9bbd2dea41b269fe16a5915a`  
		Last Modified: Mon, 05 May 2025 17:06:46 GMT  
		Size: 6.7 MB (6743368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c63bfcc6d041eed8ee879e470279880aa22e6cd21c5742677d30d4a9aade43`  
		Last Modified: Mon, 05 May 2025 17:06:46 GMT  
		Size: 16.4 KB (16420 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b40a990427b70e247fc565f1816ccc26130afb4e16f579742ae247622db206a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163422459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53bdd7e0af299b3e4a87d1b9597751b1f70c7d228af92335bf39726e58cfd82`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb2f48618bca1674b7b6aa07975908acb6ec1fe86ee6887bac65ee97038b811`  
		Last Modified: Wed, 30 Apr 2025 01:00:11 GMT  
		Size: 53.8 MB (53830504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642550aa72c186d7a52a6f246e433ff9a33f916e49348f84eafd775516b3aa7d`  
		Last Modified: Wed, 30 Apr 2025 01:00:12 GMT  
		Size: 52.8 MB (52831751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df09f0ce099b679c6ebd9f0687dceed4daab72963822e9f8eb73743fdc8f764a`  
		Last Modified: Wed, 30 Apr 2025 01:00:10 GMT  
		Size: 4.5 MB (4514193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2f6443614df65f1c77cffbcf9ba34b9409379be13a77784483f405903d25039a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6765639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f5b6dd35541058c5af1b23d34263e54779677df4717827ccbccefaf4818947`

```dockerfile
```

-	Layers:
	-	`sha256:0023c1b2419a6e1f6e7a454dfe75d3216f9034a5ba95383118981e7406183246`  
		Last Modified: Tue, 06 May 2025 00:17:19 GMT  
		Size: 6.7 MB (6749097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c140dbd79006f6dc2954e5e345a647ba8f8866e4dc9541a6fab645b5db004247`  
		Last Modified: Tue, 06 May 2025 00:17:19 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json
