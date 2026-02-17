## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:e8c8b310181f49196cfb4c430149033333fe9816528a13c322a2cba8ea73aa7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:680eae6377bc08dcc9918ea71f12e0708afc09e81645fd3cfaf139b35fe09fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220510813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f06c77dd396d571082859df79ca317adc058157ffeee7a15e54d009e267c81e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:42:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:42:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:42:51 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:43:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:43:07 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:43:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:43:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf076687ae5e7ab92becd8d00c84ac632cac1bea6c415e63e7365efb2c4e80b8`  
		Last Modified: Tue, 17 Feb 2026 21:43:31 GMT  
		Size: 145.6 MB (145628776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a428bf1892482283776f3594155b36d35474012b3ee83213f6bb368351f93a4`  
		Last Modified: Tue, 17 Feb 2026 21:43:29 GMT  
		Size: 16.6 MB (16607600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3ff538e7f04153c7e5a84cb6d1598caf3ff42a60c8c5d61e65361e87244a74`  
		Last Modified: Tue, 17 Feb 2026 21:43:28 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c1e6b4a1a87f64d1b45d18f6bd6227c92fce44515c5666198688f0dbf062c4`  
		Last Modified: Tue, 17 Feb 2026 21:43:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8660913de1f50ac69a10b84d94cc9b69b703df5c46605ae0817151aa21e3f4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a673c1c2a92c33f419bd1e8ea2fbc501c03ed936802e346e7529ae95124912ba`

```dockerfile
```

-	Layers:
	-	`sha256:6131c5cfb7719786f73b1cbf460f983ecf37f11a027b9bf52e333ec6d11520e3`  
		Last Modified: Tue, 17 Feb 2026 21:43:28 GMT  
		Size: 4.5 MB (4477442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3458cb147907276c46e9aeb3bdbfd0c8c04595b56ab3c59c18fcf138583a330d`  
		Last Modified: Tue, 17 Feb 2026 21:43:28 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7b17bb8fc07521e9e70119aa94965d16501a51eca3aca02558ebffdf4da61d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217807704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69325e8a63f2c57ed0358bdff3383778965b37ae33db3403f791e96196bf930`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:42:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:42:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:42:39 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:42:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:42:53 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:42:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:42:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:42:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:42:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95401d40f15d8d3edf48a2e9d820584f4380abf10574c70253b2c8e83dcd4d4d`  
		Last Modified: Tue, 17 Feb 2026 21:43:16 GMT  
		Size: 144.4 MB (144436241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59b0a02d5dba76a24181e54b00e318f30e7d34cef6fb5e36e4db9483f04b918`  
		Last Modified: Tue, 17 Feb 2026 21:43:13 GMT  
		Size: 16.6 MB (16595001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d514e90111c0d6b5e986d78a74f919b688f3e8abc98349403183faba712a36`  
		Last Modified: Tue, 17 Feb 2026 21:43:12 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635ec378101d28c38323b8e808f442a989042c44ec818e08a79fbdf14086989a`  
		Last Modified: Tue, 17 Feb 2026 21:43:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2a43faca9bae1d92061273923e385d039aa92459b4fbfe1c59a7b040d42af6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fa842570a4de9c4eecc2e42e759eebe695c187fab771f4f80c924ff2d3af68`

```dockerfile
```

-	Layers:
	-	`sha256:3e1ac8327d2932d525f4a359abeb7091e38814d72364b4c856f4004aaa53e2ee`  
		Last Modified: Tue, 17 Feb 2026 21:43:12 GMT  
		Size: 4.5 MB (4476416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a3bf9362d74ab643d9fe74376e9ba0a7a6d815c065248b34e080eabc8ff0cd`  
		Last Modified: Tue, 17 Feb 2026 21:43:12 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
