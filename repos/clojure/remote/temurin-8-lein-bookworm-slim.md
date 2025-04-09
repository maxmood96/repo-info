## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:6d7c972dbfac61797f6a4687ea1333d47673fc5442c8695978214f770ef3026e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b6018a5fe635db8986c3ce0f4672a4dc87895eef5c9da8b7eeadc56e26cf542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138928665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0805c34d58182cd0443303d12a3066780fdb9cd7558f0b04c05f5af8f31ca9f9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263cd050ec5c581f103821a6e72683b3533adb8bfae343280063241277e689dc`  
		Last Modified: Wed, 09 Apr 2025 02:18:07 GMT  
		Size: 54.7 MB (54721244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f349aa42dc2f376d1de01c15f09065ecd46a3d88a4fae9dbd19aaad4674fd127`  
		Last Modified: Wed, 09 Apr 2025 02:18:08 GMT  
		Size: 51.5 MB (51465974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f02f9dd6b08604e5544a1a2b3af9ff9b6f471197e33cf2e31fa1504657dcdc6`  
		Last Modified: Wed, 09 Apr 2025 02:18:07 GMT  
		Size: 4.5 MB (4514156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cdd450f3e1dda7834a329abaa5910279cfb7ca63328bd31e6668c2ffbb0edda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4459888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b3b9c2dbf0f17c5e1b5534ce13b612e366ff209238a11260b701dfce21e40f`

```dockerfile
```

-	Layers:
	-	`sha256:f038acbf8cee3a656491b4c45512c645e92c90b16dd336f04a501d128ebac453`  
		Last Modified: Wed, 09 Apr 2025 02:18:07 GMT  
		Size: 4.4 MB (4443437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b7095b9f787d21c31b6439b1943f0ce84c627d3735e67dfce4fa9762c97caa`  
		Last Modified: Wed, 09 Apr 2025 02:18:06 GMT  
		Size: 16.5 KB (16451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7ae3c4ba04f22d7f85d11ea1b487e4ef761f9522270bb4a6be8d962434b3b3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137832353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146ceeb133a254f5f65800434a1870b9dfe78a57bd27d4383f5682735e3784d0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e816d872a5165a56e55df8bea6933fd7114deda268519e3d3e5ba5725dbdc956`  
		Last Modified: Wed, 09 Apr 2025 17:12:23 GMT  
		Size: 53.8 MB (53822736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433250da6022972be2445accc6c6e6d317c68004dc2281996ad09ed02f096da5`  
		Last Modified: Wed, 09 Apr 2025 17:12:23 GMT  
		Size: 51.4 MB (51429118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e076df39087cab99c2641b3d6019bcd466d13d506eaa3874389e944c101ebe`  
		Last Modified: Wed, 09 Apr 2025 17:12:22 GMT  
		Size: 4.5 MB (4514147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b39043e6ecacf8531e04b83bb23aa366e83f4975151d31bd2f456438ea3f604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4466399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a807d8c5c65b0cd3aaa59d82407e306271978d9f2dfd3ad2d31c1ad7c1a129`

```dockerfile
```

-	Layers:
	-	`sha256:30645d969ca6a0bedf402fe9dfcdb63aa7fa9d717aaa17df29bae348dcc1f627`  
		Last Modified: Wed, 09 Apr 2025 17:12:22 GMT  
		Size: 4.4 MB (4449827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84bb8df7edf4d7cbec8d1414fae451733d4febc50ed072fbd276feaae7777fb3`  
		Last Modified: Wed, 09 Apr 2025 17:12:21 GMT  
		Size: 16.6 KB (16572 bytes)  
		MIME: application/vnd.in-toto+json
