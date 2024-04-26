## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:de1f60ab0d7403ab684b9e7ef52b4bc9014ef8d46c44f10ac796957dc8832c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d3fca86e2ec6e9cb7022c9cadc72594ee12386cf9749585fbc568dbd46bfae7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196541687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04138f95138bb1e25c1ecce8c72993bd2f95e397262a81d01e6de8f9c220b213`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 04:43:38 GMT
COPY dir:e23ce7557a2e7bee9271385ae1512d655314258ebf585995b794db69e6e3d8aa in /opt/java/openjdk 
# Fri, 26 Apr 2024 04:43:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 04:43:40 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 26 Apr 2024 04:43:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Apr 2024 04:43:40 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 04:43:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 26 Apr 2024 04:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Apr 2024 04:43:56 GMT
ENV LEIN_ROOT=1
# Fri, 26 Apr 2024 04:43:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 26 Apr 2024 04:43:59 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5451d23c265a96976235198bef5cb1f30dc90f569b030d0d6e4cb30487b180e9`  
		Last Modified: Fri, 26 Apr 2024 04:58:35 GMT  
		Size: 145.5 MB (145504637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3736e3427a47d6959a1ab892bd9182f436bd634f12a1b3f3979aca6990d6bd4e`  
		Last Modified: Fri, 26 Apr 2024 04:58:25 GMT  
		Size: 17.5 MB (17488440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee653e888dc01644524ab9cc57353cb5232735f9741ba7e29e94265118e8cc0`  
		Last Modified: Fri, 26 Apr 2024 04:58:24 GMT  
		Size: 4.4 MB (4398131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6aec200b133c063a9f49850da02b9ffda91999bb5e566a2f7870aa44c8e52dd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193195670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94576229de381604fa6b2bfae42fffd1fe8b2b259a7bbf42d25e06ce6220030d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Apr 2024 01:26:20 GMT
COPY dir:c78738cfcdd58dc875cb3f022a49b10c7fb9df08ee8a9995710ddf9cd16d96a3 in /opt/java/openjdk 
# Fri, 26 Apr 2024 01:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 01:26:24 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 26 Apr 2024 01:26:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 26 Apr 2024 01:26:24 GMT
WORKDIR /tmp
# Fri, 26 Apr 2024 01:26:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 26 Apr 2024 01:26:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 26 Apr 2024 01:26:39 GMT
ENV LEIN_ROOT=1
# Fri, 26 Apr 2024 01:26:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Fri, 26 Apr 2024 01:26:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbd4062cc19d042c5390eac83fc5731b06f530a4ec708b9f72724f47c221d38`  
		Last Modified: Fri, 26 Apr 2024 01:38:50 GMT  
		Size: 142.3 MB (142306320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0515f557a81958311eee9ae49ece9c7557b2f4013348875a600194bb47760756`  
		Last Modified: Fri, 26 Apr 2024 01:38:41 GMT  
		Size: 17.3 MB (17311294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a75425ddea94431075246ca5f2cdd5d5ecc390fb56218b3fe460394ac0d6089`  
		Last Modified: Fri, 26 Apr 2024 01:38:41 GMT  
		Size: 4.4 MB (4398121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
