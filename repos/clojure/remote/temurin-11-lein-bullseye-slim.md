## `clojure:temurin-11-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:6f166c907a3c0587f5c9a413f0a8aafb790ef841f875b1f338b623b0e61366ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9b0f8ac4ded515f8f0f6410415ab3f60b843074068f0d81ac1ae2cde79098086
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196401816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfa997113855ef172852573047c69b0270090196118fa44964adcc5a3009dc0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:32:55 GMT
COPY dir:cf3bf634873a2f76d010dec9a72ea70ddc69381f0d8d3cb32fb43e16f4a2fabd in /opt/java/openjdk 
# Thu, 02 May 2024 05:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:32:57 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:32:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:32:57 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:33:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:33:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:33:13 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:33:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:33:15 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081ca8515cf2999fc67475b477aa76fcb7134cbdf2209d9be8b6fe4d25804cb2`  
		Last Modified: Thu, 02 May 2024 05:47:27 GMT  
		Size: 145.5 MB (145504611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfaaa85d0b9be0df77760c2d2e39848fdabdd330cdb6e804ee7572ad6bf6efa`  
		Last Modified: Thu, 02 May 2024 05:47:16 GMT  
		Size: 15.1 MB (15064796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f890d151ed1f92a0bfdb50ee65c773125ee89a732b5cbe64311597b967e43d4e`  
		Last Modified: Thu, 02 May 2024 05:47:16 GMT  
		Size: 4.4 MB (4398146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:124018a8c4b29e7790b195c3d3becde6675f32385d515c2a99c5ac4642e4eeea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191842466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27a166d945c43c8fcf260e2a32a0ccf2c6097b446b4a46596b2e7883f0d3269`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:31:09 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Thu, 02 May 2024 05:31:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:31:13 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:31:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:31:13 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:31:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:31:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:31:27 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:31:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:31:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47454ded192101c0d37473879a630a0b06f8c38619c60da0859950d1987b84e`  
		Last Modified: Thu, 02 May 2024 05:43:02 GMT  
		Size: 142.3 MB (142304375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f86ae64ff8f840662ef5181484ecc7c003ca41ffcf93e570dc29042f2d93da`  
		Last Modified: Thu, 02 May 2024 05:42:54 GMT  
		Size: 15.1 MB (15052590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02778fd2e03e25e07789cf30dd56129e808e5f65355237b513ec81bd2d7fed41`  
		Last Modified: Thu, 02 May 2024 05:42:54 GMT  
		Size: 4.4 MB (4398165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
