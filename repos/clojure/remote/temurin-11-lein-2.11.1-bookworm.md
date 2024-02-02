## `clojure:temurin-11-lein-2.11.1-bookworm`

```console
$ docker pull clojure@sha256:c6a078bff0bb47b9833a7831e9fe2e880f2290f898f2737608ac4a56abc41dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.1-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6029b247ebb705856902ab9486311c4f6a4c4eae6869fa31d409de9e340f5a50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218771147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6c5e8923074d59726956094fced7b0b89e04c5325c4a0c9e5bc0c91eb98042`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:09:55 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:13:16 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 17:13:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:13:17 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:13:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 17:13:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:13:35 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 17:13:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 17:13:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93311b9f1dccdb9ed4e27ec9e72dff9468583e68756f160ae709603707528b12`  
		Last Modified: Fri, 02 Feb 2024 17:31:02 GMT  
		Size: 145.3 MB (145271022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7609b2b5ecebb85441ab616b6016a0047df5b147da219bdb384c03d9aea271a4`  
		Last Modified: Fri, 02 Feb 2024 17:32:47 GMT  
		Size: 19.5 MB (19517150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def1049c73cd3850628678923f19e93e4206f24155c259b60a240a862e6e43e7`  
		Last Modified: Fri, 02 Feb 2024 17:32:45 GMT  
		Size: 4.4 MB (4399221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad8b11665e3e3f64e0c91c115ec9a14ce9bbba5f8f96baf0b945fc93fcd99cbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215358835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6057a5234983a032da3fc386413e64c836d1ae0932c96953e4bfcbec8784e059`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:19:38 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:19:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:22:53 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 08:22:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:22:53 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:23:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 08:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:23:10 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 08:23:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 08:23:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d300b593857f6a07a4266828dbbe1e03ed64d43a6bf503b48194d30675f3a069`  
		Last Modified: Fri, 02 Feb 2024 08:38:08 GMT  
		Size: 142.0 MB (142006417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8bb08b542d576bb70295639145e7a26117e5df80e934aa883ace924cbc128a1`  
		Last Modified: Fri, 02 Feb 2024 08:39:40 GMT  
		Size: 19.3 MB (19337952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb9044df79bc06259eab34f717f50e28667c34725fadcd1b30309375c7567b9`  
		Last Modified: Fri, 02 Feb 2024 08:39:39 GMT  
		Size: 4.4 MB (4399170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
