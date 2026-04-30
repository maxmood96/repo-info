## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:c65c1f2cd75c098b0e71c1e3398877a2c6f0113622f19dfe6a2cf8d4a93a0058
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6a8eb21041d0a0bcffa4943bae1b7ce8e21007985aac0b28e1ca7c21c3c3d5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220796738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1afd49741ecb816b6cfac6af27ca78164069c27cd985f46d173f035d10a9a6`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 29 Apr 2026 23:14:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:41 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:41 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:56 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:57 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d54a736f560651ebad4fb620470067f4f48b3dfedc66232d5ed044459b1a8c`  
		Last Modified: Wed, 29 Apr 2026 23:15:17 GMT  
		Size: 145.9 MB (145886254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbfab26eef9278bb540ba845f5d5b5654ae14e655b84b99e95d55d3fc5c9a27`  
		Last Modified: Wed, 29 Apr 2026 23:15:14 GMT  
		Size: 16.6 MB (16629559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8748e2acedb01a054d8fff7bc91f9e0b736129a7b25cadcde673088e4a9866`  
		Last Modified: Wed, 29 Apr 2026 23:15:13 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0a7c823f3473252984eeae0930c6741772ce973b48118a3f0c9aa150e6442de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f18e9de040aada051b5ec66a924dd939a634bb966feb6aebd7460ab3b1fb423`

```dockerfile
```

-	Layers:
	-	`sha256:e2ac780b0cbf07c7c191683c84606d8386575722be452b370b780049d896e603`  
		Last Modified: Wed, 29 Apr 2026 23:15:14 GMT  
		Size: 4.5 MB (4506005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a8c2bfe5619ff2c90186920866aa1c69111b3596ba29e20c49ba09a30ed2838`  
		Last Modified: Wed, 29 Apr 2026 23:15:14 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b79ef3b4d032cdc3cc35c641eaf39299c738ef5b1899635a410451c33e1337fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215971223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023dc0c1e107b73c0f704a3e26a7f2dd98d8d9b4668c4b969a9b630e73a1a5e9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 29 Apr 2026 23:14:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:11 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:11 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:26 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:28 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06b226354f3fcebcc0fb046fa7687b32e30da6b4cd2dff9b2fc0b1117991f86`  
		Last Modified: Wed, 29 Apr 2026 23:14:50 GMT  
		Size: 142.6 MB (142583969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94b7ceb7f3be9ccab25d25186a81b71eece67bd1d88c9b8045331794229703b`  
		Last Modified: Wed, 29 Apr 2026 23:14:47 GMT  
		Size: 16.6 MB (16616469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7c0a3b06873ee8bd9fe0438afc5879cd5d5270d7b27db8d88767227938b2d4`  
		Last Modified: Wed, 29 Apr 2026 23:14:46 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0903c96672b3dba5172f8f06494ee92fed0d08ab9829723fe24caae38f4bb1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b50229791e86183407065275a5957e43e9bd7b5b8db1923363667001c7af45`

```dockerfile
```

-	Layers:
	-	`sha256:4f167b405fa47c484fff364703b7162da71cf75ff7c524880563c304ce4c950c`  
		Last Modified: Wed, 29 Apr 2026 23:14:46 GMT  
		Size: 4.5 MB (4505597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:596faad3602efb56f4b2132545c828b9115b126914282bcea7538fa3f25d3f38`  
		Last Modified: Wed, 29 Apr 2026 23:14:45 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json
