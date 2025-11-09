## `clojure:temurin-25-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:c611acd2b1dd0433dcba1d35c25bc0b290a067b0bc69761e0f971e36d3e5b4e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4d1265cd3a1bc16537423b413e8a823111501adce956e1d6981e7a5fd8264255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142140826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab7297614847a17b4a21859d9be3e44734ca4f5574af67b069f984156861fa5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:45:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:33 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:45:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:45:33 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:45:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:45:46 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:45:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90addc3ea016e2265d738502839e9ae3b894f663a6e59090205cf0beb732e475`  
		Last Modified: Sat, 08 Nov 2025 18:46:55 GMT  
		Size: 92.0 MB (92045322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911abad1411ad5f560e755ab1d8a01f66da77ee8d14ecef458fc4c853a7031ac`  
		Last Modified: Sat, 08 Nov 2025 18:46:48 GMT  
		Size: 15.3 MB (15318728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be4e3895d77dd20699564261b3def285402ac2d4341f759b61ca0f5e16b0a76`  
		Last Modified: Sat, 08 Nov 2025 18:46:46 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47adf8d8a48df1abe659793a8f347d21970f4d5fe5314690c0784328f08fb081`  
		Last Modified: Sat, 08 Nov 2025 18:46:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c1f83fe36d5ac8455036498d2c0f57202af3cd2be8eb781ec6214273cdf50917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47a3b7db5df4cf137ac54e199c23ae1027b8382bef50c79ddf5c77eae4bd57d`

```dockerfile
```

-	Layers:
	-	`sha256:7986181bedb9b3688dfb463bfb752d00938ee88545c2bc68e96997816da98133`  
		Last Modified: Sat, 08 Nov 2025 22:35:17 GMT  
		Size: 3.0 MB (2969234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33163c715d7b1d5a631bb0f859b557c66b4a25210c10967e792ec23fcb113c1`  
		Last Modified: Sat, 08 Nov 2025 22:35:18 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce5e0cd0c90afe4e46229b7a45e9be5222137cbd095034f14e6e2e248237e5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139625055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad75c3d11cb63e9bb53206eba62b69e62e39dd738bfa2e1a487669ed56481b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:45:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:09 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:45:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:45:09 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:45:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:45:22 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:45:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:45:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:24 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac796599d4832f5a56e8ffe70fc34f8a07b5ca0f9be875928e0c637e1258b97`  
		Last Modified: Sat, 08 Nov 2025 18:46:08 GMT  
		Size: 91.1 MB (91052503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3cb870a10521286c6a5e55e4210b406c369f67a7e9dc806e57282b73dd25ba`  
		Last Modified: Sat, 08 Nov 2025 18:45:52 GMT  
		Size: 15.3 MB (15305819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f06af60c394adf07d713452ddd0902b38258899ad21fc75a079386e36bacac`  
		Last Modified: Sat, 08 Nov 2025 18:45:52 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a7323c3c26457df7ed040b7605010a3a8e81b883e7640ef46873bc71540525`  
		Last Modified: Sat, 08 Nov 2025 18:45:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72fb3852f0c82fb46822503c316616373663b17cb387b542a8ec9b79430af69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc66d9d153cd22208fa3ae579aefcb80de37c455c1dc4846be2f0634adf75f05`

```dockerfile
```

-	Layers:
	-	`sha256:b71dcd520aee54300e3ec35e29be248c2c60fd043bc727be4e505f0785de6eca`  
		Last Modified: Sat, 08 Nov 2025 22:35:22 GMT  
		Size: 3.0 MB (2968864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2cde4f485707e488fbb63bb98cd7417d07794558181a5456f1653980213c8f`  
		Last Modified: Sat, 08 Nov 2025 22:35:23 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.in-toto+json
