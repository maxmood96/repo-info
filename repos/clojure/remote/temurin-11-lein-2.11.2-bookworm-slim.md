## `clojure:temurin-11-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:32304f3f1e38fd4da0921e5134f68b79a692355a3df149863952d03efda6de80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:883d0f63a29e608efd899586927d0790ad110c4b3331431df59ecd75a575bbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230295228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d609b4d1bacee216a8351b490ed4764f39bd794cc74db165f762d3150d116bd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abacd3e95e1ed2b074beb8524ce33773b638742ca561659381f460db5068e4e`  
		Last Modified: Fri, 23 Aug 2024 20:02:06 GMT  
		Size: 145.6 MB (145550028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd513ec11c337d704db14c10057a522949e21360ccda1b9870df6019c7d11dd5`  
		Last Modified: Fri, 23 Aug 2024 20:02:05 GMT  
		Size: 51.2 MB (51220907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6286898d890cfb59bdbceb62a44764e30538c6730117dc46666dde9c215d3ff9`  
		Last Modified: Fri, 23 Aug 2024 20:02:04 GMT  
		Size: 4.4 MB (4398029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a846272c91212fe42c9a163a53a35603ec588064f5da277892604ebcd1312745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba42e7b1ce0e95dde4329ec7d9588b35c4871bd47ae1a286d1e4c42e1f157d16`

```dockerfile
```

-	Layers:
	-	`sha256:bca73e6d61321214595c33b3f3a47b8556fc99353ccb513a573a7921fca80e7a`  
		Last Modified: Fri, 23 Aug 2024 20:02:04 GMT  
		Size: 4.2 MB (4153009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bffbc7878ffb3d45d8ef9ce28d3fa7c92bcc04ce07db537a17276b3c97a9fd3`  
		Last Modified: Fri, 23 Aug 2024 20:02:04 GMT  
		Size: 16.1 KB (16091 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebe7a3ea2f062d2a9cd4822a0d202d09726ca1708e89c9b9875aacca16f671ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (227004867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f284af8611208583f6ba43731c5616a9edb4f2c279bf04c354a3e48c7b3e5c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab21e04edf6f0707618ded0c1ff6a94764c25f714abaa1345780da846e579ad9`  
		Last Modified: Sat, 17 Aug 2024 06:02:09 GMT  
		Size: 142.4 MB (142354842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49902e26e7f167f3b6248c3da15f9b5577f901b561d26bd8392e137d45e380d`  
		Last Modified: Sat, 17 Aug 2024 06:02:07 GMT  
		Size: 51.1 MB (51095383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1672c6f6b9d06c277d1adc3b84de7c500f7002f6230826f16fddc8d75a1e8c0e`  
		Last Modified: Sat, 17 Aug 2024 06:02:06 GMT  
		Size: 4.4 MB (4398082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:540b00b3396ed10868108b1b622101fa7b272a0a8266c46e005c094cdeaee428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4175114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2593bb1862cebbc16768d5b0e55d7ee0aec375be744fc1ed2cb7c47c7c3fc081`

```dockerfile
```

-	Layers:
	-	`sha256:704e082878e353b2913779c349c19a28eb8250f39329011919002d9d4c635df5`  
		Last Modified: Fri, 23 Aug 2024 23:50:49 GMT  
		Size: 4.2 MB (4159325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72b20684412a183d1324208f70e450cc66f5d9cf5e19d009c6c69ebff2f69a09`  
		Last Modified: Fri, 23 Aug 2024 23:50:48 GMT  
		Size: 15.8 KB (15789 bytes)  
		MIME: application/vnd.in-toto+json
