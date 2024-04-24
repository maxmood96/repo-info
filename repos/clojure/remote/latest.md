## `clojure:latest`

```console
$ docker pull clojure@sha256:f1b060e1745e601e177ba5bd013abed1b0dbda5ad1c39e250b6250f3ea6ac9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:16255123448e48fec80a5bde88c6a23d040f3f71264f754c1ceb052938035c7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302914811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8567737c14c0cd2ac5a6777902747ca9fd862659fbd8268840de6dedd7d3f871`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:12:37 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:12:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:12:38 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:12:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:12:39 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:12:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:12:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:12:57 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:13:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:13:00 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:13:00 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:13:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:13:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:13:19 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:13:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:13:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c6c7005a90bce817446a105fdd2251e1a61cd5b2920bd66991722c9ddab1a8`  
		Last Modified: Wed, 24 Apr 2024 21:39:39 GMT  
		Size: 158.5 MB (158498251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841d9606697b1061f61802562d767bee3df7f3df1f99f4d8c09ec209f6278738`  
		Last Modified: Wed, 24 Apr 2024 21:39:26 GMT  
		Size: 19.5 MB (19518377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3177cb3016dbe72b8b8592c3a5aabbc2fd6de0b37a659050b0276d2969420bd`  
		Last Modified: Wed, 24 Apr 2024 21:39:25 GMT  
		Size: 4.4 MB (4399174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1d218be7b6327c09a3c7eb6647a018f003b4beed9528b0ebfc9fee2c01a491`  
		Last Modified: Wed, 24 Apr 2024 21:39:33 GMT  
		Size: 70.9 MB (70921708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a681c02dd06bfd648744056c7374ed8d208826453644d412106c4fc1d10f4db`  
		Last Modified: Wed, 24 Apr 2024 21:39:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b294fd70d949a117302240bc1a54fe9cff2692bfb3f567664a1f76dcffa5b9`  
		Last Modified: Wed, 24 Apr 2024 21:39:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3397febd7aeb28d28252b374b4df3da98a5edd3a15804ae6d17f9d64127bed7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300861231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb92246b27fef457a1db94183e5df43d4751fd887f7a72d636fa0d6587a85c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 18:58:54 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Wed, 24 Apr 2024 18:58:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 18:58:58 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 18:58:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 18:58:58 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 18:59:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 18:59:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 18:59:15 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 18:59:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 18:59:18 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 18:59:18 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 18:59:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 18:59:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 18:59:36 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 18:59:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 18:59:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169aa930d721e94ed3fa0e531f2c9589622a5daf25bd20ce451e14411686e427`  
		Last Modified: Wed, 24 Apr 2024 19:21:10 GMT  
		Size: 156.7 MB (156665540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2e40001948583c24f4993cc7168a5bb1a62e6ffcd961e297741ccbc70c9faa`  
		Last Modified: Wed, 24 Apr 2024 19:20:59 GMT  
		Size: 19.3 MB (19339742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde8b0e8afd63715375def5cf44972a46d9952592686f642b7f551a72e3b65fd`  
		Last Modified: Wed, 24 Apr 2024 19:20:58 GMT  
		Size: 4.4 MB (4399172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a2b9839744cad849ff81705d27ce75fe9b6942ae2004c275b15a40db334ee4`  
		Last Modified: Wed, 24 Apr 2024 19:21:06 GMT  
		Size: 70.8 MB (70842418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268b96c56394a6094536b70dc5d08a722f5ecc4316b03ce63767b904c5e555dc`  
		Last Modified: Wed, 24 Apr 2024 19:20:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25c260f3d2a4d71ad7c0f0b5f1467e68ff2ff5ca7202943e2962e3c708a48c`  
		Last Modified: Wed, 24 Apr 2024 19:20:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
