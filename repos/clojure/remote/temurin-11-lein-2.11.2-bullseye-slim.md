## `clojure:temurin-11-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:19cd6d9382f20618ccda99f5a5e0670380b35ec00cbf6db6984899f4db30bb76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d62f477816535b8881a25e1c4fa43fc5f5e45f0c1e51cd6c18f5a9b565c474aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223648951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b47771bf04bf7a68a27dd776f72c5dcdd76e2f4d85b097abb325e2d18d8657`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6608c62337a8b093644f5c3f04e47b993b5d50a9cf88b11d089a646fd87c46`  
		Last Modified: Wed, 09 Apr 2025 02:18:24 GMT  
		Size: 145.6 MB (145598787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ac467678606202ec63e5e1c60ba652a4121b463530deb559140a96ba3f945`  
		Last Modified: Wed, 09 Apr 2025 02:18:22 GMT  
		Size: 43.3 MB (43278512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619c51747be6e7af6b9a1badea4aae5b42a6c94db76763fe25e7c9aeb0b7950d`  
		Last Modified: Wed, 09 Apr 2025 02:18:21 GMT  
		Size: 4.5 MB (4514201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fddafa4ddeec269cccf22ee1953e61b8915ea267f12ce282aa7f608c21c8fac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f02557aa5cb7e238c4ede7bc610766dd6a76c66ce9435e17483c900938a20c`

```dockerfile
```

-	Layers:
	-	`sha256:d24c6b556ec51a09e1d9cc581782949b57cf25a973d283b44c3c1740e89bf860`  
		Last Modified: Wed, 09 Apr 2025 02:18:21 GMT  
		Size: 4.6 MB (4590256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9676a650931e68a0a9ca67ddc959e333441bbfa9e9963b7796ffadcc4ad42b7b`  
		Last Modified: Wed, 09 Apr 2025 02:18:21 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b3625490bf2d3376304854701b7f99356f89948ab73f5d1a2baa1fb64dfab64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218963388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90d7ceb0bbdaa28a5b457e793ef7a52c42bcdf2d9b104ef7e0ff4a9548cb71f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f86bfeaec95ef5ec2e11f38efc47425f6b274dcf46f09ceb8e0aa91d383d675`  
		Last Modified: Wed, 09 Apr 2025 15:20:58 GMT  
		Size: 142.4 MB (142385515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fd7d4e46b5adeb99e6a74bc484894248df2b1359252415c285d16ec9fa9ddc`  
		Last Modified: Wed, 09 Apr 2025 17:23:07 GMT  
		Size: 43.3 MB (43314188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbffc236d9723475c4e75bc73a804f0d76aa3065291c8a94632bd4e74c2a264`  
		Last Modified: Wed, 09 Apr 2025 17:23:06 GMT  
		Size: 4.5 MB (4514155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09b7a1d6001369f2bf8f63a444f9b56270d65e4ea3375fbc0818fa92608c1f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4613122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c28fbc2668b7e576db1b02b25b88037d3ffa895825edd218dd675c171c86cc2`

```dockerfile
```

-	Layers:
	-	`sha256:668981bd2392b9cd4ef8b272aabfe1427d0ba588308a56541803e8effe85d4b7`  
		Last Modified: Wed, 09 Apr 2025 17:23:06 GMT  
		Size: 4.6 MB (4596538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a52a1698dd1b4e4d9a3fbca422af4ce8dabc70516e728b6512d15e72ea29b9`  
		Last Modified: Wed, 09 Apr 2025 17:23:06 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json
