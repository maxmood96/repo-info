## `clojure:lein-bookworm-slim`

```console
$ docker pull clojure@sha256:c0833df6c003c4721386be1330222ffdd2c410f3652f33d62f9bd0b7f1c9cc58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:666b0bc04c9305005a19693742a93da9e0553d988582f180061d12d1af351c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209511187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c4bc50714ce3c018ddad076df4a26d7f1752d10e7e8b56a8f22cae8d68fd7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4df991dccd20ba9d65b13413906da9d835edb65ab6820acc607282fa0e1f7b`  
		Last Modified: Tue, 02 Jul 2024 03:03:00 GMT  
		Size: 158.5 MB (158497942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef99a1de1edaaba690d783b6964588d249249815cbce60c4fa324bfe948ebfe`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 17.5 MB (17488448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc69132dcccdcaeb2f2ebe809dd53fc08054b6a7c371adbf28d568618e63e22f`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 4.4 MB (4398090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ec71412d5de523685555575066312e203a4ad0b98191661134ba018f987022`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73aff8c2a43fbdce1ad3707415ca9652723f6b993710add9070712557c59500c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2417855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac800517138bde2fea2631a01ce8a7d25098e4363f314be599c0854a18e6950`

```dockerfile
```

-	Layers:
	-	`sha256:9b470ee1740fa875002a3c6bab9f14ebc96f54a06ad1f912c80cf2238cc287f4`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 2.4 MB (2399114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d19df8a4fc2c792df1490b2700f210eb9a9df1af1375c8472be4878b5c53fd`  
		Last Modified: Tue, 02 Jul 2024 03:02:56 GMT  
		Size: 18.7 KB (18741 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:649ef73d37d4575739ee0a997e0887b5ba3130313aa059a5d4004e0a3da4ab5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207360064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a029cc8c03f6568c4343f20acebc9da27bc69282c2670380778606cd14d1a656`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c24c7a7b86f218dc61de558ffed50d5992f39df50505edf3204888486fe1b7`  
		Last Modified: Thu, 13 Jun 2024 11:53:39 GMT  
		Size: 156.7 MB (156665644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2634ea7acec2a5da4fde2c53a0fca1459ff06f1099a6326c4fedf3a823c5082`  
		Last Modified: Thu, 13 Jun 2024 11:53:37 GMT  
		Size: 17.1 MB (17116232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f98cb04bb95cb118168a6d4111262b1eecefe85efa6532b9ba392ea0fea280`  
		Last Modified: Thu, 13 Jun 2024 11:53:35 GMT  
		Size: 4.4 MB (4398091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043814f80f2568e9d7dc8c115939f1f23df62b7a4b3827ff2e78dc7d9e6e4268`  
		Last Modified: Thu, 13 Jun 2024 11:53:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ebb7bd5865ee4e48949fe142a8236bde23144b5eb00d86f52493354b91e9ae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f894794ea3b5dd007882143b6b0e8b8bd98abfd57b56c5666ba7026b1fd7ef48`

```dockerfile
```

-	Layers:
	-	`sha256:f2d727e49f391f70e8125a47f9fadc348ef1ff0b2686ecead9b216a40a95aecb`  
		Last Modified: Thu, 13 Jun 2024 11:53:35 GMT  
		Size: 2.4 MB (2399341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fffc124fcd4216da6527c0417c206b5abf884cf7657186dfaaae375b4c01dc1`  
		Last Modified: Thu, 13 Jun 2024 11:53:34 GMT  
		Size: 19.3 KB (19294 bytes)  
		MIME: application/vnd.in-toto+json
