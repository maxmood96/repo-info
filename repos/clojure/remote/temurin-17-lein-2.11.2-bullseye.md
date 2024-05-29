## `clojure:temurin-17-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:d3291e6fad2fdb22b55f2fe0932e4beae7ace89a8b67bd7eb7e12cdaf744f914
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3d84bbe8ec6c76504bd097b87e626f960e750a25dafc48504136c9b9c7c363dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220740552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6aab50a675ad64d9afbcd4d0f496954ab82bb4b065f09daf7729f6b9ff6a23`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90ae77913fabbaebb1417b6f4939fd5e363353749a5277aa4bd91830217142d`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 145.1 MB (145095011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8c283cb658e9fa6a919f7834f8e438d27c60a4c2da32e95c1ea32a8b2142a2`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 16.1 MB (16147672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfbacfe8aa069e8f04a9ae46886083aa69430e3c410ae7ac50ef5b243aaa223`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 4.4 MB (4398038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e43e6b319d7b89f4c4dfea0313e9be2e4c9752704671d332896a49b54a9c4b`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f9244d9b4ec3ba0591fb1eb0db36077cad1a132d708aaf643ad0fd2a54cb756f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f191bfe0e55511659654574602b14b4fac06a680c889aa53f9bb68049c91ba`

```dockerfile
```

-	Layers:
	-	`sha256:432c3726a69df672725605c3cf3b39f6ba7682953cb0880866a974ac33a6a1c0`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 4.2 MB (4151320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c44738516a1c9aa697ed69f9c3dd86018f3fd19e1aa5c71cda885368ac7b0b3`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 18.0 KB (17980 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0e4e65b6099185b814547e4f51add26ceb3cbdd608ab40865867f1c8eaedcc03
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218373339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149ffee49fffa1f5331c7d5596475fb1c25b89e5894e425897d94af836b9e490`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:55:20 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:55:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:55:24 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 19:55:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 19:55:24 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:55:38 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 19:55:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 19:55:38 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 19:55:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 19:55:40 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:55:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:55:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330e78a137a375764261c3ed0e8ed70982d3c4a9101c2e44901d2345409912d5`  
		Last Modified: Tue, 28 May 2024 20:15:11 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e063d5bc1f1e81b8e820f70751a732137319d579c655e728bd502063ba222e1d`  
		Last Modified: Tue, 28 May 2024 20:15:03 GMT  
		Size: 16.3 MB (16343966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc57ab9da6be22f34ad9e7ee6a3a973b4d2f97273de0a9c55913b585620f5bb`  
		Last Modified: Tue, 28 May 2024 20:15:02 GMT  
		Size: 4.4 MB (4398145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd50539be4dda9e85ee17ff766d19840f37d2c7768cb0919f6ef1a3da3730d41`  
		Last Modified: Tue, 28 May 2024 20:15:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
