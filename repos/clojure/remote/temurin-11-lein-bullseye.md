## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:a8eefa0c6f667008e8c3b3cad2f3e9ff1da35b9f59ada81dc5f81d1236aa4c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7ef2f8ad64b59d91207bbfb0f100fda08c05f8c251df44d462d55411d57f188a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221356639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8268c886a52a8d432f75cc23773348599de9cc9db4c2f10bb77aed2ec3f0c1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:44:07 GMT
COPY dir:e23ce7557a2e7bee9271385ae1512d655314258ebf585995b794db69e6e3d8aa in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:44:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:44:09 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 26 Apr 2024 04:44:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Apr 2024 04:44:09 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:44:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 26 Apr 2024 04:44:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Apr 2024 04:44:29 GMT
ENV LEIN_ROOT=1
# Fri, 26 Apr 2024 04:44:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 26 Apr 2024 04:44:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4427caf927495e62e89f897690044d4bf78001b43414f226c88d479c035c69a`  
		Last Modified: Fri, 26 Apr 2024 04:58:53 GMT  
		Size: 145.5 MB (145504625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab638ca615c0e26f675009b830d3f71f6e990ca40820a32a49f52be304cd046c`  
		Last Modified: Fri, 26 Apr 2024 04:58:43 GMT  
		Size: 16.4 MB (16355002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaf5120a57edfb58748f743f2afff935e033c46b2863fcd963266e35ba8c0d4`  
		Last Modified: Fri, 26 Apr 2024 04:58:43 GMT  
		Size: 4.4 MB (4398142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22399dae82d1dc3c0a41ae581248c3e6901ae264cdf6af684e7e91f9529fa43c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216788490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d4ffd0e9c1471e5afa2b55b8dac13faf84e69aeeb6974917097b687fca5837`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:26:44 GMT
COPY dir:c78738cfcdd58dc875cb3f022a49b10c7fb9df08ee8a9995710ddf9cd16d96a3 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:26:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:26:47 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 26 Apr 2024 01:26:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Apr 2024 01:26:47 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:27:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 26 Apr 2024 01:27:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Apr 2024 01:27:04 GMT
ENV LEIN_ROOT=1
# Fri, 26 Apr 2024 01:27:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 26 Apr 2024 01:27:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2379b596d29c4a48c7ba2b4784c6d0898b32073be72fa219ab0f0f5637a4815b`  
		Last Modified: Fri, 26 Apr 2024 01:39:07 GMT  
		Size: 142.3 MB (142306371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09678f85b14ebbc58a24ce274cabcaaf8f94027486013747a362fe5c559640e`  
		Last Modified: Fri, 26 Apr 2024 01:38:59 GMT  
		Size: 16.3 MB (16344032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6e8810f265f2bfda0fe4e16ff17a2177933f6ace6e538fad6e35b7fc2a2aeb`  
		Last Modified: Fri, 26 Apr 2024 01:38:58 GMT  
		Size: 4.4 MB (4398128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
