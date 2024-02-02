## `clojure:temurin-17-lein-2.11.1-bookworm`

```console
$ docker pull clojure@sha256:0581e99539bd34ed483bc54af76f6ff87307ff994159209e5e3133b347962ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.11.1-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:aa6233350bf34b36270677c394cedd6895783c109e2c4f34c08184a5c7b17b12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218393868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbb88f84b172f1c8bb69b7794e8eef0964000e956218498bc9ad7e0c5799471`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:18:01 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:18:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:21:27 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 17:21:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:21:27 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:21:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 17:21:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:21:43 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 17:21:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 17:21:45 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:21:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:21:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e272de56020947d967cc38ae404bdf929ec35fa85009eb7fcaa4a05298c22e`  
		Last Modified: Fri, 02 Feb 2024 17:35:57 GMT  
		Size: 144.9 MB (144893230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d21c531b6a581a7e2d3c857838b299feeaca2e5e58b817288e86d2eeb4eb4d`  
		Last Modified: Fri, 02 Feb 2024 17:37:43 GMT  
		Size: 19.5 MB (19517281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33b6a0e3c342e8d865f66ec337401a14b2419e57adc4c4c68ccae86011c976f`  
		Last Modified: Fri, 02 Feb 2024 17:37:42 GMT  
		Size: 4.4 MB (4399202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7766c9a05e9fa367d0b969611b0c4ceb8159dad7c846f66ca05a0d59ff5dc4`  
		Last Modified: Fri, 02 Feb 2024 17:37:41 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.11.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3584cac756813e841b07c78a259c31ecc8a5cc1920caf503361c62c26de8eb27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217073794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122835c0f01efac1b0f7a624a758868f93bcea40a5fc906af1b2c519de5e073c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:27:01 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:27:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:30:10 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 08:30:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:30:10 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:30:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 08:30:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:30:25 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 08:30:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 08:30:27 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:30:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:30:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2123fb31cbd519f0e5acdcb92c2fd15e1872407955fb24a687b068c997bb7e12`  
		Last Modified: Fri, 02 Feb 2024 08:43:27 GMT  
		Size: 143.7 MB (143720880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97715220392832de31d17d6d1aa59e92d2d3dcc0ee711690f07c2c3a0d9143a`  
		Last Modified: Fri, 02 Feb 2024 08:45:10 GMT  
		Size: 19.3 MB (19337990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2085d1dae89e55fbdbfc8e5d03c2bb280fd07f64b6cb4c4ad5c1996e73dc7fbe`  
		Last Modified: Fri, 02 Feb 2024 08:45:09 GMT  
		Size: 4.4 MB (4399227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d909d2b103b2faf82e664fdbc04493e070ce1ce9aef4b7bb7c1b6ff7dcdfdcb2`  
		Last Modified: Fri, 02 Feb 2024 08:45:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
