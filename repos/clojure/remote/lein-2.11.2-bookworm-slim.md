## `clojure:lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:713a85f4c5da851b080ab8b9bda2ef5af26de261bdfdf46a3bc249e11c5ebc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:030011ec50f32fd9458927b7fde1eed438188714d3dd405557524204ccac807d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210598852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ec2f6a6f777840d98c910ce60f6ed1b63a64c19605c0c9045269d5c2553598`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:34:12 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:34:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:34:14 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 10 Apr 2024 06:34:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:34:14 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:34:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 10 Apr 2024 06:34:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:34:29 GMT
ENV LEIN_ROOT=1
# Wed, 10 Apr 2024 06:34:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 10 Apr 2024 06:34:31 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:34:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:34:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60ce6f3f5cc5f9f734b801978be67d2f134eb8358976fd04daf3f15c7c16228`  
		Last Modified: Wed, 10 Apr 2024 06:49:21 GMT  
		Size: 159.6 MB (159582870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f93ad5f816e3936a08bb6d572a9b96d0276466a38933a874f204dec3e0216f7`  
		Last Modified: Wed, 10 Apr 2024 06:49:10 GMT  
		Size: 17.5 MB (17485030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cdd41f3699849461a676bc6f0a67c19f365966c783fffedeb446d58dd95739`  
		Last Modified: Wed, 10 Apr 2024 06:49:09 GMT  
		Size: 4.4 MB (4399193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9a31c622684b53c542f2b11b46128123463624d1aa3fa1ce631008ad8b32b2`  
		Last Modified: Wed, 10 Apr 2024 06:49:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6cbcccc669481a2a72db8eea1e3cdc1cfe73d74e9ce38a073b0e0315bb0acccc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208655680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8637838cd1b3cdc917eaf09533160a4d6248b2a06d938e74a01ee8c2525b1368`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:53:16 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:53:20 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 10 Apr 2024 04:53:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:53:20 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:53:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 10 Apr 2024 04:53:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:53:34 GMT
ENV LEIN_ROOT=1
# Wed, 10 Apr 2024 04:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 10 Apr 2024 04:53:36 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a58fe06d24a9c9973da82863c842560b8b11ab8de0f315e299af1d20774048a`  
		Last Modified: Wed, 10 Apr 2024 05:07:52 GMT  
		Size: 157.8 MB (157784670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98db9fd1820d82a09cf305e903810f6013e7c4b4fed2855f2388e2d71b06ff68`  
		Last Modified: Wed, 10 Apr 2024 05:07:44 GMT  
		Size: 17.3 MB (17309258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef1192d0ccdac12a155993750b6efba9007905da341a5dfa0c82ab20a30baab`  
		Last Modified: Wed, 10 Apr 2024 05:07:44 GMT  
		Size: 4.4 MB (4399194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce22e9252f96d92280f053f7b40343769f263548bf62d340a18d558528616b5`  
		Last Modified: Wed, 10 Apr 2024 05:07:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
