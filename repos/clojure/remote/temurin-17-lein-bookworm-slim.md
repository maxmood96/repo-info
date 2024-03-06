## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:f6512206840f7f090a943da8fa18bf462cb6950da75fb2bc92594c58759eb40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c0ab167bd00fa323445aa318121cec1c1ba29116634eba67dfac038b3805182d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195901820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbda7520f848cfc641a4465bc683f6727d46fd7feaaa2be321ecd17f4a4b7a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:10:35 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:10:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:13:42 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 06 Mar 2024 14:13:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:13:42 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:13:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 06 Mar 2024 14:13:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:13:58 GMT
ENV LEIN_ROOT=1
# Wed, 06 Mar 2024 14:14:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 06 Mar 2024 14:14:00 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:14:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:14:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44496d713a839fdd0b47c7b0973155ed9bb317b54231c21b7337e12eb724bb83`  
		Last Modified: Wed, 06 Mar 2024 14:28:32 GMT  
		Size: 144.9 MB (144893104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467c65338b3eb6a7cef48b71526b9743018e2a9dfd5f3b671aff2e5f3d8a7500`  
		Last Modified: Wed, 06 Mar 2024 14:30:06 GMT  
		Size: 17.5 MB (17484999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffc96acf745ee42ae9ed1af2b26c8b4eb03c36f60367890b5b045bf9ac5c57e`  
		Last Modified: Wed, 06 Mar 2024 14:30:04 GMT  
		Size: 4.4 MB (4399227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d906e71fe239cc401bae5c6344bc4a1fd05fd904f915bde178d19527ef32c47`  
		Last Modified: Wed, 06 Mar 2024 14:30:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:55c279a9aed0bc76d6ea28d510acde6ee2aa0c80f5bda96b1dfb9840d3d3f84c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194585993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff61313e319fbb411769314ea3a728e5966b22a61347b59de73c24d91eff9f88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:23:20 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:23:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:26:11 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 06 Mar 2024 13:26:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:26:11 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:26:26 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 06 Mar 2024 13:26:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:26:26 GMT
ENV LEIN_ROOT=1
# Wed, 06 Mar 2024 13:26:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 06 Mar 2024 13:26:28 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:26:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:26:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8baf922fb4d908d3a3587a0482690306454d53960171f76f1db75d33164d944b`  
		Last Modified: Wed, 06 Mar 2024 13:38:15 GMT  
		Size: 143.7 MB (143720843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5dc0c52af81d79cf0898c248fb39f39179eb98903f330c28218b4d018e5684`  
		Last Modified: Wed, 06 Mar 2024 13:39:36 GMT  
		Size: 17.3 MB (17309163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6915f7d47e400c4ed519e3002681a532efb4875da63b14d8257039eae1fa0ac1`  
		Last Modified: Wed, 06 Mar 2024 13:39:36 GMT  
		Size: 4.4 MB (4399223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2ed83600e1256e4a4b8564fc6cecac46611008213068d77312179f30d17c7d`  
		Last Modified: Wed, 06 Mar 2024 13:39:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
