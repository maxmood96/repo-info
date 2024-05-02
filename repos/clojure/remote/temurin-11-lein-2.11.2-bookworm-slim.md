## `clojure:temurin-11-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:783d26c9445f0ed7a4c3ca906226a11876ffc1846a94ea5738163c485cd0ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4635836e0ca51fcda4e488ed59bfb8752582a154dc085c9660927c27c7458f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196541685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60cbd6d01bbfe675b4a197e1e19a90650e2e20ee48fff0f1ec0aa42d9b229dd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:31:57 GMT
COPY dir:cf3bf634873a2f76d010dec9a72ea70ddc69381f0d8d3cb32fb43e16f4a2fabd in /opt/java/openjdk 
# Thu, 02 May 2024 05:31:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:31:59 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:31:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:31:59 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:32:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:32:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:32:15 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:32:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:32:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6999d802e184a3444400e20c51ed4b411a4c877911267d08e51549eb1da69ca1`  
		Last Modified: Thu, 02 May 2024 05:46:48 GMT  
		Size: 145.5 MB (145504632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b658cd5a79a491deddefb291a0dd735ba6eab2fdbf5d9ffc6b0cdc671d2d0282`  
		Last Modified: Thu, 02 May 2024 05:46:38 GMT  
		Size: 17.5 MB (17488468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ae4dcc2df9eef5c745625894b0e71f1cb75db23621817811f5c93b3eb7655a`  
		Last Modified: Thu, 02 May 2024 05:46:37 GMT  
		Size: 4.4 MB (4398106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2100dc9d623c9f800ec195aa08a966498fbe608d3dae9c5186fa2eaa198b611d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193193732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e38cc55eb185589196fb9fdaf8508c6ca597c42a515edd066f504e97a4747`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:30:18 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Thu, 02 May 2024 05:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:30:21 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:30:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:30:22 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:30:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:30:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:30:36 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:30:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:30:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0987a6f1fe0e0791144fed7d417846c016ee438e9987dc82e4c3e9513f7360`  
		Last Modified: Thu, 02 May 2024 05:42:28 GMT  
		Size: 142.3 MB (142304377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94943ac6f4daa355f0735157fcf73779128fc1188466857b586a744ad45f6eda`  
		Last Modified: Thu, 02 May 2024 05:42:20 GMT  
		Size: 17.3 MB (17311282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed6184d185adacbcf0f313081081c358a9f7b59726fdc3c679fdc76581ccc95`  
		Last Modified: Thu, 02 May 2024 05:42:19 GMT  
		Size: 4.4 MB (4398138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
