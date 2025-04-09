## `clojure:temurin-17-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:572a8eb6487c75c4c77b5ecc95a41d273badf5c3a631d0aecda10e65a65664f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f47f6b1054d991142442c3acedae35535c435ff5efb8d112f3d3df984db9ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228774379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746e34d8899db3570074bf0a9d28dd13901c3b57ed86ba433e78f6c7adb63f82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa76a8e6c8974f2b3517e65004b05603c8c5a8d10ef8ba9fc83699cbecb4f99a`  
		Last Modified: Wed, 09 Apr 2025 02:18:46 GMT  
		Size: 144.6 MB (144566541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dcbe22bfcc63c207e90d9c4e3dc1e391268021e435dd3b60504e70c99a5271`  
		Last Modified: Wed, 09 Apr 2025 02:18:44 GMT  
		Size: 51.5 MB (51465935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e563d9af9272f860d0a8274c3e55a1b42aeba629ba6982452b9f63338c791e`  
		Last Modified: Wed, 09 Apr 2025 02:18:43 GMT  
		Size: 4.5 MB (4514216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb1d4246976dd539d97a2a7e783bbcaafcb57a0bde6fc9b21b29b718cc3d90e`  
		Last Modified: Wed, 09 Apr 2025 02:18:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a518a4bdbbff19b929574edd81c1062f4edc972bc60c250c1c1dcda1966b0cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4340283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d95aa65fe389927f3d32a2253f3120b078e4b37f890b155d5ec2a9aeb4e2126`

```dockerfile
```

-	Layers:
	-	`sha256:9a66239dc73e61e2a856568fc19f0ef80216a2c14856b09d19e529abfdbc5f6b`  
		Last Modified: Wed, 09 Apr 2025 02:18:43 GMT  
		Size: 4.3 MB (4321825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:951ae6596def50ef14516db0a9ce29f1fc19b68425b0b1ef97f3faa6671ad3b0`  
		Last Modified: Wed, 09 Apr 2025 02:18:43 GMT  
		Size: 18.5 KB (18458 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cf38ab3294de248154b73d9c3237fa550509bbe62e7cfab4401933f35ba689e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227464748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9e33dd7bbc887cb6ac085fe4f03625671380a0b38d373fc85238b8b33134f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e330b25eff171b18e5a99f840bc62624233db83e3b75bc7cf704398fb8b1a059`  
		Last Modified: Wed, 09 Apr 2025 17:30:24 GMT  
		Size: 143.5 MB (143454651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0482c9cab3049f51edf13b93118039d032b6c0d425571f9d21565b9f47fc4a3`  
		Last Modified: Wed, 09 Apr 2025 17:30:22 GMT  
		Size: 51.4 MB (51429178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdda2a7cba7592230b7217e13313854d97c27937890cc6b420c2ee72f62fb70`  
		Last Modified: Wed, 09 Apr 2025 17:30:20 GMT  
		Size: 4.5 MB (4514169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc2df28ee907a88d10cba9934ea0263d19f7620db198dded6315ed6ace81324`  
		Last Modified: Wed, 09 Apr 2025 17:30:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ae9ea5821d2894251353c5330ae2981886bd9a5faa2723483efd377a473cabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4346096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1ad872a0c33b12d87d6e94afc4edac95740123b67b7b7a909f8222f102942c`

```dockerfile
```

-	Layers:
	-	`sha256:825fc1a0a53707a42eae25cfe50b9a4feba866238d90243d1d4a3859a03ee1f7`  
		Last Modified: Wed, 09 Apr 2025 17:30:20 GMT  
		Size: 4.3 MB (4327517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:804009c019eec241c384c7681d2ed3a0466cf19b261be5a28443af352a966d9c`  
		Last Modified: Wed, 09 Apr 2025 17:30:20 GMT  
		Size: 18.6 KB (18579 bytes)  
		MIME: application/vnd.in-toto+json
