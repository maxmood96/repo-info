## `clojure:temurin-8-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:3e971e2ca3e505b8cb36a282fa3c9eb314c89409bbbd6374428c7aacd02557a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ceea974296636e2c4bd0bbb7cfdc8c4e0951e32f818da5e87a7dd2d300278ab8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154498359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a6d4b3f130fda0267722736547de870cc8e7be32fe7fc5b0c2f93a7058c2eb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:15:01 GMT
COPY dir:54f5f76f9b290ecbafc047cf196165b69f1cb32e49c8748c35e250f5e316fcc0 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:15:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:15:02 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:15:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:15:02 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:15:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:15:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:15:19 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:15:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:15:21 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eec355dced25396607810d8a074f4df2b1edf41d31600fd54b82c499259aded`  
		Last Modified: Wed, 24 Apr 2024 21:40:54 GMT  
		Size: 103.6 MB (103600133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00a88cbf5e58070a2360c9379aaced980da4c29dabd86d3e4a2c5802f232343`  
		Last Modified: Wed, 24 Apr 2024 21:40:46 GMT  
		Size: 15.1 MB (15064734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a4548d7023fd1760092b358efce17f67ddca3b8e36bcb8915291c2be2a0e83`  
		Last Modified: Wed, 24 Apr 2024 21:40:46 GMT  
		Size: 4.4 MB (4399229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b476ab8b67bd2363f55d376628ffbe0a3886114a483c0bc3d3180cd4d0246f87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152239227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5d5ffdb032ef8cb69e2f5cbfe00647216ce2ce595b622b4660cd1f2d6bf5d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:00:52 GMT
COPY dir:f816a852ac21a5e29532918ac40e44b27f618ca8c5c539e334f114f460fe4b51 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:00:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:00:54 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:00:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:00:54 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:01:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:01:09 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:01:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:01:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1d3aa9544a8fa97e0e443515a329cf4c529fc91820fd3aa9ee9f1b352ffa51`  
		Last Modified: Wed, 24 Apr 2024 19:22:09 GMT  
		Size: 102.7 MB (102700111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592bab82ee443ad65bb624a2b50df32e29eb03df0d8539d6d1de8e7a059cb9ed`  
		Last Modified: Wed, 24 Apr 2024 19:22:03 GMT  
		Size: 15.1 MB (15052568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c330a9a33c9f5d1e08c2ea6c9e99cabb7cb827a6af94ea461cc1b8ed001f60de`  
		Last Modified: Wed, 24 Apr 2024 19:22:02 GMT  
		Size: 4.4 MB (4399212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
