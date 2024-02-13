## `clojure:temurin-11-lein-2.11.1-bookworm`

```console
$ docker pull clojure@sha256:f3625ca98bdba5df0ed10bcdd675e1397c3173145979dd47d51701f99a50826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.1-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:33dba57dd6bf01ae7e0b5a282a4cca67e25b395f016560f2d69a9a40375af107
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218737059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15abfc75e3ccb58ceb0c5e0b365860c92539cf6a662d3628ed6030747d96cb91`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:52:46 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:52:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:55:09 GMT
ENV LEIN_VERSION=2.11.1
# Tue, 13 Feb 2024 01:55:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 01:55:09 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:55:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 13 Feb 2024 01:55:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 01:55:25 GMT
ENV LEIN_ROOT=1
# Tue, 13 Feb 2024 01:55:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 13 Feb 2024 01:55:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3470e538d4e3cfd65043bfc65a4966ed42ab558a0d02d70086e803479fa66`  
		Last Modified: Tue, 13 Feb 2024 02:12:52 GMT  
		Size: 145.3 MB (145271036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5abd77d98f34b105f274abb958a90f2648067729b86d952dca4669954d0328`  
		Last Modified: Tue, 13 Feb 2024 02:14:09 GMT  
		Size: 19.5 MB (19514188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e2e64d9401b02078dabad52efa5d5c92f60143dd72faf8d481366c02e7130b`  
		Last Modified: Tue, 13 Feb 2024 02:14:08 GMT  
		Size: 4.4 MB (4399230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:db3f6c54ed4dbffc1c33ebf45b50a219759230332bca6504633fd46bb5d14965
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215332288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3d97d80105735263cc6adbe8cc723fb03d09274fa2a908b304cb44a0eaa330`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:59:30 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:01:45 GMT
ENV LEIN_VERSION=2.11.1
# Tue, 13 Feb 2024 02:01:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:01:45 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:01:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 13 Feb 2024 02:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:01:59 GMT
ENV LEIN_ROOT=1
# Tue, 13 Feb 2024 02:02:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 13 Feb 2024 02:02:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb18bf1feb8a022b56cb764ff4154c937334b989bb90ffde840254ce27e971b`  
		Last Modified: Tue, 13 Feb 2024 02:17:04 GMT  
		Size: 142.0 MB (142006386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3e83cabc168631a68a155775b6b9ec8cd2503be175a952c91cffb81d4674da`  
		Last Modified: Tue, 13 Feb 2024 02:18:22 GMT  
		Size: 19.3 MB (19335782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605b44c7ea2d0869bf07a52394f492958fa653a211b1e9ac8e52cfcb2f3d90b0`  
		Last Modified: Tue, 13 Feb 2024 02:18:20 GMT  
		Size: 4.4 MB (4399155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
