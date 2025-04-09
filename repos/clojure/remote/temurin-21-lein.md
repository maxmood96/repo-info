## `clojure:temurin-21-lein`

```console
$ docker pull clojure@sha256:1a6f641d40454fb44ea549ba19d0277648e7f8816cce39bb06db1e4caf404f40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein` - linux; amd64

```console
$ docker pull clojure@sha256:3f3a3db3576883351a41746ee0b14884e321f07bcc16f601c33ba02aa9d6538e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272655115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1bd6b3d3e0860d8a32d733147178f7453035ea2260aa7ba32842aa4ed051b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fe8c1b1d5462ec6d08a898d34b59f3ad50536f0d0b881f8b443f26316e8f29`  
		Last Modified: Wed, 09 Apr 2025 02:19:12 GMT  
		Size: 157.6 MB (157585893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7d1d01a504527df3d7203cb336dbb55eaaff187c8a58c0635dfc2e5ca63ed0`  
		Last Modified: Wed, 09 Apr 2025 02:19:10 GMT  
		Size: 62.1 MB (62064092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee63db7492f200c01a53936026589886ea4730432d34cd2c281478162343b641`  
		Last Modified: Wed, 09 Apr 2025 02:19:08 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59fb20cb8701ba867375b4717cc458006ebb05ddf60e5a77697f7bde68183`  
		Last Modified: Wed, 09 Apr 2025 02:19:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:20df687f66852b51fe0969a2e169e361ed7697bfdf2b319a56998a4fafbb025f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835c51c78a9f96a83445fdd2f605248e9e2dd553ee67ac910272acaefa94ab9e`

```dockerfile
```

-	Layers:
	-	`sha256:b848b564a0ca2f89c8837fc6bdd56972267a52285cf54a1d548f5e7c9ce4dbf5`  
		Last Modified: Wed, 09 Apr 2025 02:19:08 GMT  
		Size: 6.5 MB (6540643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c80f0b74d877f6fa713846bd8f4f7d41c4eb81be37f4d287a1d37a461c590b`  
		Last Modified: Wed, 09 Apr 2025 02:19:08 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:56297dafad04697fca61426bdca24556809bd0a8c5fece1d16fc118bfa4af2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270738306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e29301ae9445e837998ee8c47544dd17093ec19ee81df6b5afe147bd98546cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c9d1eca0c6f0c11c056bd1a9c0a6fc6af61a9d35f24ad12f42bc4153e746a6`  
		Last Modified: Wed, 09 Apr 2025 17:10:48 GMT  
		Size: 155.9 MB (155859270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6264492c76768d92f30db245176983d512ec4d8912695cb44ab124e30a0269`  
		Last Modified: Wed, 09 Apr 2025 17:10:47 GMT  
		Size: 62.0 MB (62036977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9b17373cb7245bc060c8d6870d10d7a9a9763b218d293161d0abdc860488f8`  
		Last Modified: Wed, 09 Apr 2025 17:10:45 GMT  
		Size: 4.5 MB (4514164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c933f655a089b555865c5582f909c512f0f1486147acf968076b0abb69eb746`  
		Last Modified: Wed, 09 Apr 2025 17:38:14 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:9d30d1bd5b2612857afe7deac713f5cdf945fd7ab51e88927b9f829fa5446b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6566923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99e34d49817fa563827a3eca522b88cd59b8d46d5179c4729747362277c7959`

```dockerfile
```

-	Layers:
	-	`sha256:7711fedef6c5283763e3d36c418c5b7350a813989db2bfc486e47db6ed07b2c4`  
		Last Modified: Wed, 09 Apr 2025 17:38:15 GMT  
		Size: 6.5 MB (6546409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4540178a8e254a43557323d8a9437729a57c3a8107c4b2b9beb5689ccd0c69`  
		Last Modified: Wed, 09 Apr 2025 17:38:14 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json
