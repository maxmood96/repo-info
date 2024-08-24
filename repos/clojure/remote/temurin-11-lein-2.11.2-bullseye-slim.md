## `clojure:temurin-11-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:73b8b45fed8f78095470bf7ed937cf53e891860d5d9c44df91e11bc5c7abffda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:46f2403682092cf67d4d1c4d003bc1aa7e02ccddbd75636a99d307c0d30e6e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224514365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1849395d8084ba5e244f7480be05242193d8b6052fd482bb8a7ac5e23e89a658`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5e9418ea24af63486036286053445e840008f79a066bd89121dd8b3b35d21c`  
		Last Modified: Fri, 23 Aug 2024 20:02:10 GMT  
		Size: 145.6 MB (145550054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6f642f9a6f8d1d195810e41cb32635b89ee7d9e361c53b4bcadca111fd6406`  
		Last Modified: Fri, 23 Aug 2024 20:02:08 GMT  
		Size: 43.1 MB (43137961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5d704407c7655dca963102aad94b0a959c42ea11a6a1f212e01b7ec42ad4f3`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 4.4 MB (4398031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:87f7f8fe3f196053f43fd56d871e2676ec7979b9d74333786356b6a01f48a50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4417177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46bc4ead4eee8fdab1150bd336eeacd388fa8b12f9fb0b9a77dbbc5a67f42c3f`

```dockerfile
```

-	Layers:
	-	`sha256:1b042c47c507226fd8eb211a28e0fdf1a5cd1d37539f7b6af7384eb209596d50`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 4.4 MB (4401086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a2f7edc587a01ec16887884afee2c2f8b20abcb5c4536860f7270efd606a77`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 16.1 KB (16091 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e0bce367ec8d08c2d5caad0a2a567621bc4e9bb6d4cb92109fa4738ae1b00d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (219986238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6387d32f69b2c0cfbe09e77306300eac7a5198f28182ecf619dec4e3a8f114d5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97190d565d6e988e1267474ec2deb103d496585fb03fad3f32525640389e705a`  
		Last Modified: Sat, 17 Aug 2024 06:04:04 GMT  
		Size: 142.4 MB (142354792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de352bc532b58fb7884c3c5867a6574acb3b40c6819ae58b565be760195bb83d`  
		Last Modified: Sat, 17 Aug 2024 06:04:02 GMT  
		Size: 43.2 MB (43157286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b6ba77c3f2077002e8da0a8be59e0b8ed94b1c673b5b7f190190415f298a61`  
		Last Modified: Sat, 17 Aug 2024 06:04:01 GMT  
		Size: 4.4 MB (4398041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5bc06fca96d6e80c3d5287e9ddfdeef5947cb08276d4b3f45bb7c5eaac6d9c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4423163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdf81addcce0bb3887d01a260bba1665a8947d9b771d0eafe44d81a742287a8`

```dockerfile
```

-	Layers:
	-	`sha256:85322836eb4b29bb124d12594a5cb64a2c2f0db0d6289401e2976072ae9954c2`  
		Last Modified: Fri, 23 Aug 2024 23:51:53 GMT  
		Size: 4.4 MB (4407374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a23d223262cbd0851c629e86ff70894af1736b686df911bbfbaaa1e6f50e252`  
		Last Modified: Fri, 23 Aug 2024 23:51:53 GMT  
		Size: 15.8 KB (15789 bytes)  
		MIME: application/vnd.in-toto+json
