## `clojure:temurin-17-lein-2.10.0-bullseye`

```console
$ docker pull clojure@sha256:c9adf6555afeeb9bc452ca0b9783a4ba68dc52904e2573f9007886267383f972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.10.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4ab07440e805a3ce137da1d1b21d493964a2129a63b88841d8dbfe0d7e43ec8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265890120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902013c12ded8da51df567054de409f7564375e79f12fe7df915d5b053da3427`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:00 GMT
ADD file:150a6453ab2258061c1a1549ab119df752bdc2c2c84028fa0e83a0663cd8cedf in / 
# Tue, 23 May 2023 01:20:01 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 08:09:51 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 08:09:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:10:56 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 23 May 2023 08:10:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 23 May 2023 08:10:56 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:11:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 23 May 2023 08:11:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 23 May 2023 08:11:11 GMT
ENV LEIN_ROOT=1
# Tue, 23 May 2023 08:11:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 23 May 2023 08:11:14 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 08:11:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 08:11:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bd73737482dd5575526c7207872963479808d979ab2741c321706b8553918474`  
		Last Modified: Tue, 23 May 2023 01:23:46 GMT  
		Size: 55.0 MB (55049027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62e3a1941399287928e0b128fbf9c001cd1f164f2cd9d5b0f242162cb22481`  
		Last Modified: Tue, 23 May 2023 08:18:28 GMT  
		Size: 192.6 MB (192580373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85633cc3aa909d1547ac4072a20cdee4a4e1d32d41da5c00ab30f8aff666f44a`  
		Last Modified: Tue, 23 May 2023 08:18:54 GMT  
		Size: 13.9 MB (13861056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b05512cf71f6d623c3946a4e5f61ccb004510606201d5571ffb95fde1b29ef2`  
		Last Modified: Tue, 23 May 2023 08:18:53 GMT  
		Size: 4.4 MB (4399264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba686ce40d00e753ec4f5f3036358db1a31589c7ca39877bb8e70fd74509610`  
		Last Modified: Tue, 23 May 2023 08:18:52 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.10.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6a30dac380beb616024c47c93db42be706e6193c9666e50a9eaad088a518297b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263329265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0461a84ab2d38293458760ed78fe65332731e46f8c6262df54d1a83fdb3912d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:08 GMT
ADD file:a823391455122220a061ff349b66ee33413e968447ec5ba4bd544d9182fa2fbe in / 
# Tue, 23 May 2023 00:43:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:18:37 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:20:10 GMT
ENV LEIN_VERSION=2.10.0
# Fri, 02 Jun 2023 01:20:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Jun 2023 01:20:11 GMT
WORKDIR /tmp
# Fri, 02 Jun 2023 01:20:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Jun 2023 01:20:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Jun 2023 01:20:25 GMT
ENV LEIN_ROOT=1
# Fri, 02 Jun 2023 01:20:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Jun 2023 01:20:28 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Jun 2023 01:20:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Jun 2023 01:20:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b04fae59f135dd79280e4a6da39408e04c6d703c617cbcb1c524dfe6f2962fe5`  
		Last Modified: Tue, 23 May 2023 00:45:45 GMT  
		Size: 53.7 MB (53692612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f84bb66698dfd6516ae40960a9ff86d5acdff3a75decc6e793b695113145916`  
		Last Modified: Fri, 02 Jun 2023 01:26:57 GMT  
		Size: 191.4 MB (191387660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d88035e03fb038daa8a537a47f428c48df027f23699310301df19074143346e`  
		Last Modified: Fri, 02 Jun 2023 01:27:49 GMT  
		Size: 13.8 MB (13849379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:903346510c2c08cf4de0d3b9737b2ca84224da3d25f8b76b036da1e220d0eaf8`  
		Last Modified: Fri, 02 Jun 2023 01:27:49 GMT  
		Size: 4.4 MB (4399214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ee3457c53167d96425f2e34e00bb51c1cb5a4016ad84a0b671d74c9d967a00`  
		Last Modified: Fri, 02 Jun 2023 01:27:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
