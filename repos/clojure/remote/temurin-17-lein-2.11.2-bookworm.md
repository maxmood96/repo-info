## `clojure:temurin-17-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:101b4822fa61c6f1ac1c16e967c0682be362cf023d0c7963b50e064915fa2d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:770e46e6fdc18f2278fcba90eb01fc542d25f94be9f2ec628f61509cc04fdace
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 MB (218589579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72140a7c4ef7fc7f7c2b8719e806d126b0c22608b8e2feae55ba7024c0f6e23`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:24:17 GMT
COPY dir:61bea833528044db01491107d8c3fb583322243082c7798fd60ade98f7eb7613 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:24:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:24:19 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:24:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:24:19 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:24:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:24:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:24:35 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:24:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:24:38 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:24:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:24:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46193795e372883da3b4657b2893b9eba1f1bb03039ac6400ad2fb37f30b611`  
		Last Modified: Wed, 24 Apr 2024 21:48:00 GMT  
		Size: 145.1 MB (145095353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f657fead754c3f01e1f90f3f6e2fe4cebfadc6cb2a9c07552b66a01e1883038`  
		Last Modified: Wed, 24 Apr 2024 21:47:50 GMT  
		Size: 19.5 MB (19518381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e101873d0c487fc4fb02591a025025b9886bd2dc833da88c4c837cb8e880a7`  
		Last Modified: Wed, 24 Apr 2024 21:47:49 GMT  
		Size: 4.4 MB (4399161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34072b8c51861503e8f80b04fe4b7cd4aa6e61e591a820265662a0aaba8b6854`  
		Last Modified: Wed, 24 Apr 2024 21:47:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cf862c305b9b56a0776bcb74a101d2beb83594a6f07af0ce4108f6b9da3e9c04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217244575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f354e8299cfc9313527812aec8e8d337357e2505cda95ee010ede63cd2eb91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:08:43 GMT
COPY dir:894420f494a8d73ff0a7e5986ef0142218654b95343c81b2b9fc9a9d3ea0c174 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:08:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:08:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:08:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:08:47 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:09:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:09:01 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:09:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:09:03 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:09:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:09:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fefe737023ec01887dd5a91b2358786392594133742c3e42b86e75cce6fa4c5`  
		Last Modified: Wed, 24 Apr 2024 19:28:15 GMT  
		Size: 143.9 MB (143891869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9954693a55290f9f25da1b33a8aaa7a6a2b1bc76304f123608b04bcdcd9f89`  
		Last Modified: Wed, 24 Apr 2024 19:28:07 GMT  
		Size: 19.3 MB (19339751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02e4485101a17058b1003ca7b1550a092e7524e2d13fd59b15d8fbb7350d09c`  
		Last Modified: Wed, 24 Apr 2024 19:28:06 GMT  
		Size: 4.4 MB (4399212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa0118af70e51901329ee44d20cbfd8567201ebd2b1733cf02faf81b0e5652`  
		Last Modified: Wed, 24 Apr 2024 19:28:05 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
