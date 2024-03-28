## `clojure:temurin-11-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:a4f6a131f5e3f9fc94701d7bedeb62848b9fd10fa9547ed39a15782411705fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f3b0d5691deb243792808ed9446d91ec0a9be28359c8dff8b60f4906c992b10a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196279506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8d43ca86e91f50b471b4fd6ee52e9072e93bf0eddffb7edcf95edf0964d9d4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:58:35 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:58:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:02:00 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 03:02:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:02:00 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:02:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 03:02:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:02:15 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 03:02:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 03:02:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49a6ac31b34979fe9ad3cbc392d1e9236c7163db662ad2db2662f3d8c2227e1`  
		Last Modified: Thu, 28 Mar 2024 03:19:31 GMT  
		Size: 145.3 MB (145271203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569405743bb47d5bb4ffeb4925705cdbd26f99d5b41a7d69590edc181bb65b68`  
		Last Modified: Thu, 28 Mar 2024 03:21:13 GMT  
		Size: 17.5 MB (17484957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3a4b2ee78f7eae05827b77e3732a974fe13c67c813ea5f5fbb083642e4953d`  
		Last Modified: Thu, 28 Mar 2024 03:21:12 GMT  
		Size: 4.4 MB (4399165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dca2371cd514062e1d5c2d0d7e3d5cc08bd8ce94a61b46e875ae25f50fe596fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192871066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6fd7da955a7bf998d32ee26f4a41df5e4edb0d2b37af514e3c055596c1459e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:32:45 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:32:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:35:30 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 02:35:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:35:30 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:35:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 02:35:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:35:44 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 02:35:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 02:35:47 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7819794f44d5487fb5284f90132fb8e3a770cac3a81ff8a43630aa0ffcd999db`  
		Last Modified: Thu, 28 Mar 2024 02:49:43 GMT  
		Size: 142.0 MB (142006296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b97dddf24936ddd4f17ba1ccf51f385ebea0dba042521d670ec20a9ab7e6553`  
		Last Modified: Thu, 28 Mar 2024 02:51:04 GMT  
		Size: 17.3 MB (17309167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2616cb80472927dc547c82e168bbfef6ce586a41271a9eb37baf1596853e68`  
		Last Modified: Thu, 28 Mar 2024 02:51:03 GMT  
		Size: 4.4 MB (4399169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
