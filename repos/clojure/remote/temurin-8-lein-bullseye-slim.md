## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:ac60bc10eaf7820f4706854cd4e6e79662dc1f0677c25b86c2befe2dab22ff37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ea3adb511a9d1ede054b0b6f5818ddae33f46232c3849d00b097e65e435f506a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132766215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57363f4bde884188b722d4186f70e5bdf4acecab0fa3bddb11e8d9517f7386c4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14953474ffe927c7bb8162dc553c921274e8cb5c56b9f8a1bc5370c4a39df951`  
		Last Modified: Wed, 21 May 2025 23:31:18 GMT  
		Size: 54.7 MB (54716178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739605b38326140cecbf6cb0cf02125dba851992ff2f5f42f4ae3f3788ac840b`  
		Last Modified: Wed, 21 May 2025 23:31:18 GMT  
		Size: 43.3 MB (43279889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3681f28df426ac1d61cc278ae5ab2e1826fd5117303fefde6b219011dbb8a9f9`  
		Last Modified: Wed, 21 May 2025 23:31:17 GMT  
		Size: 4.5 MB (4514176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b33f8faf048bdd04c6f20301592aec617322e2150d752001503fd0406ede54bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4754017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d723b10fa7362efaff5933dff6249531c6ee6b49dd07abe96f96df8c1f75de`

```dockerfile
```

-	Layers:
	-	`sha256:e232ef2e35ed782abcf5447d324f6cc3330b1dafc2448b7fa7bdead34a47ddc9`  
		Last Modified: Wed, 21 May 2025 23:31:17 GMT  
		Size: 4.7 MB (4737566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a502d94fdb7effd1d0ef1c33d2617b427acf770bd2ed1356714a8d58b8a7b44c`  
		Last Modified: Wed, 21 May 2025 23:31:17 GMT  
		Size: 16.5 KB (16451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4f101599d48a63712e33722c7e65c0f2d6a5acf56ab74685794c5fa97a99f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130403582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a48b6a6a2822138e977eda66df037b0c7dd16449b571adb3f5ae0612b7f7c0`
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9362c53d1c14ecfefba9cf38dd0fa524f1f96fc993f360367b03a91b556103f`  
		Last Modified: Wed, 30 Apr 2025 01:00:56 GMT  
		Size: 53.8 MB (53830503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16647b195a79f5df3c31d47307e1ba62ce6ed3f9140b26bd142fb211bd92465`  
		Last Modified: Wed, 30 Apr 2025 01:00:55 GMT  
		Size: 43.3 MB (43314249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf124332b124fc50940b674782e651bf9bc99874132df67aed6a8dfe010bc022`  
		Last Modified: Wed, 30 Apr 2025 01:00:54 GMT  
		Size: 4.5 MB (4514153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2beb70a8ee33dd32eb0b19428fac8be9c0f73cf93aa72e0afbc681dbc5c6fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4714715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef3a6c87264eba3ceaf97e3c9fa648923c4f185cdb861b6bed1c492ac6c9bf9`

```dockerfile
```

-	Layers:
	-	`sha256:469c9c85e36091d0e85b88d79000061a29965009bf1792da92b6743d31c862c7`  
		Last Modified: Tue, 06 May 2025 00:17:42 GMT  
		Size: 4.7 MB (4698143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca91b8a9bf1fd1ea73c792f2c043b9038a6cb1f0f6aa234a9e14de3a8f5372b`  
		Last Modified: Tue, 06 May 2025 00:17:42 GMT  
		Size: 16.6 KB (16572 bytes)  
		MIME: application/vnd.in-toto+json
