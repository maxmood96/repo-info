## `clojure:temurin-11-lein-2.10.0-bullseye`

```console
$ docker pull clojure@sha256:23046d77b73b3ed15e50b54f32e767eb617136552401c82bdd0cb33943f0562b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.10.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:32bd42e68c8ae524265449d91046b08f53cfb213664cd38454b0e035c08ef2b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218148795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76818c4ac7e0d891058ce6b174e145cd10858e36efd37235fa8b6c929e63d1d7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:04:32 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Wed, 16 Aug 2023 18:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 18:06:08 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 16 Aug 2023 18:06:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 18:06:08 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:06:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 16 Aug 2023 18:06:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 18:06:23 GMT
ENV LEIN_ROOT=1
# Wed, 16 Aug 2023 18:06:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 16 Aug 2023 18:06:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802f7c61301eef1eb08be64b58b246c8d0994f99e572b694d6cd34c52442c978`  
		Last Modified: Wed, 16 Aug 2023 18:15:30 GMT  
		Size: 144.8 MB (144831648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a51abd2b932f47eaee6324584737f8c7d1a7a201af6173d73e4f3a22a721f04`  
		Last Modified: Wed, 16 Aug 2023 18:16:12 GMT  
		Size: 13.9 MB (13861297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6298c64169cf0d6e8476b89f82e07471e52dd63412957f69c48f389c0f1bd71b`  
		Last Modified: Wed, 16 Aug 2023 18:16:11 GMT  
		Size: 4.4 MB (4399229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.10.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0d61199033d7fa694cb9f43bc10769c119a1badf6b39f0e21fb342569e23671
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213518731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698626b9a3614fd9f60616f2b554a2de673fd6a148293a2087bdc1c77e44391e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:21:45 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 17:23:20 GMT
ENV LEIN_VERSION=2.10.0
# Wed, 16 Aug 2023 17:23:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 17:23:20 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:23:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 16 Aug 2023 17:23:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 17:23:35 GMT
ENV LEIN_ROOT=1
# Wed, 16 Aug 2023 17:23:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 16 Aug 2023 17:23:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175ec2cb09b3952032a7dbf0cdc9f641b1c5035ea846b712b44240d849a2979f`  
		Last Modified: Wed, 16 Aug 2023 17:31:34 GMT  
		Size: 141.6 MB (141565216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea6e15062adae72d46bbd51749931521be695d32413efc94b0eb702f0608301`  
		Last Modified: Wed, 16 Aug 2023 17:32:23 GMT  
		Size: 13.8 MB (13849505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67625a894100700db9b6e227645d115e68972fbac12d060580319746008ed7`  
		Last Modified: Wed, 16 Aug 2023 17:32:22 GMT  
		Size: 4.4 MB (4399231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
