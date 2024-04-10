## `clojure:temurin-22-lein`

```console
$ docker pull clojure@sha256:251c36d0e5dd0423d29ed8f5cae1e6e952a903e963de4f2b7312ffce5730db62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-22-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:850c07583e2b38c48925c7c36be7883161cc8b99029f10a0b79360a5fb541934
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229195156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28655e3a4a8db3a2850b6abac9c6f106e20f55dc21dec459ae56e80ec562254d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 18:10:09 GMT
COPY dir:804c07f15e876d329ef9551fe4e0597856a4396e905a8f833a1110ebfd35dfdc in /opt/java/openjdk 
# Wed, 10 Apr 2024 18:10:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 18:10:13 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 10 Apr 2024 18:10:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 18:10:13 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 18:10:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 10 Apr 2024 18:10:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 18:10:28 GMT
ENV LEIN_ROOT=1
# Wed, 10 Apr 2024 18:10:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 10 Apr 2024 18:10:30 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 18:10:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 18:10:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e20f77b40f5a086765f08c1ca4e0e612a1b4d6fddca45dd0e70a414f94c8eab`  
		Last Modified: Wed, 10 Apr 2024 18:24:42 GMT  
		Size: 155.9 MB (155861784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c459dbd514b5b56b928a7dfb249c45c1374a4287c5ed92500ac38d3a58c1b029`  
		Last Modified: Wed, 10 Apr 2024 18:24:33 GMT  
		Size: 19.3 MB (19337498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ae73890d32a5b59a507f918459baa053be9c37a2ea6e088dc1789ee389a213`  
		Last Modified: Wed, 10 Apr 2024 18:24:32 GMT  
		Size: 4.4 MB (4399206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e1d3ce1c42b95be261412accde62ab83bf28d627dfc2916e54877338c668d9`  
		Last Modified: Wed, 10 Apr 2024 18:24:31 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
