## `clojure:temurin-24-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:881043c1c05c1bc500a8472506c47bdf3d3cb8b09c6db8eab64488de9532983a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:76401ffa6c9809e3cb7f21932476ce2a7c822526d20f667488e40f91956a366f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205018447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca552e49eafa44c41d08b10707721179ce6e0c6f065ca25d7937b6ab69eaf457`
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
	-	`sha256:c3c8c748893555c1bc371efa5596270bbbff72274f809e4ebafb34b015f153f4`  
		Last Modified: Wed, 09 Apr 2025 02:19:22 GMT  
		Size: 89.9 MB (89949051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f91f11f79014174cad26493c06d632faeb7567cbbecda02354d0ea059fc19e`  
		Last Modified: Wed, 09 Apr 2025 02:19:21 GMT  
		Size: 62.1 MB (62064264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0516be94995ccd9ebb86b00eae0425b105d97c3323cc3978a9e4456340c9e065`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 4.5 MB (4514161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a4b4af72115d0c7479beec61c676cdbaeb21b6b2cde37a916e8979df8a7ac7`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:58c9141435534aa9af1a964087080e3edb4b3c2b22516ce27ccfcd03e3d11e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6505991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a93bad84d3f688f5c8eff7c48cfd6ec7b7bb34cad2b24cfa0cbc2989ec2706f`

```dockerfile
```

-	Layers:
	-	`sha256:40c16fe2b2cbc0e58fbc0ba1fc42a486cd982fa49ba1fef689d9dbb9e79efccd`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 6.5 MB (6486925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70e7d7d2bc40b2442a662b2c0f4cc291b6ab6794792f4d24c9ae47d63494a3f`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 19.1 KB (19066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:57e5c0c3b8d81ce3e0334beff24c6c65fe2dfd907d56c4bfad5f5361f55b5041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.0 MB (203971753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5181fad215f306c4c7936f33dbf279b112dac40ea84d481bf984e5c9ab20d5`
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
	-	`sha256:e663ce4f306cc9c264ec0b57d4f93f02ea679e43515d91dd37eeedeef5a0293b`  
		Last Modified: Wed, 09 Apr 2025 17:47:39 GMT  
		Size: 89.1 MB (89092703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7561963140d562b5ecf6ec0fc75dae4962ea9d632e53f0d875ace60d9a60ef`  
		Last Modified: Wed, 09 Apr 2025 17:47:39 GMT  
		Size: 62.0 MB (62036973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4711ec4adc42d52d492426a806bab19c4bba85a600ec90049e89fc05966c49ed`  
		Last Modified: Wed, 09 Apr 2025 17:47:37 GMT  
		Size: 4.5 MB (4514179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a90e06361ef439828c66771072935c0901ebb87f4163732da9d72ca44766191`  
		Last Modified: Wed, 09 Apr 2025 17:47:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ce97911740a19a587eaa999c714ec4df7e6fbf351068a894f576d2e394fbe7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6511851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0dc35cefd68eb278c2aaef82106bf0568d4b626eb0396b4034f50815485bbff`

```dockerfile
```

-	Layers:
	-	`sha256:4775833b61cdcd79e24ad9812d971c1ce98502041c095c825006c283898a5a0a`  
		Last Modified: Wed, 09 Apr 2025 17:47:37 GMT  
		Size: 6.5 MB (6492640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855d9df4a0098459b3e101c9187452d5ecdbecfeb2b8be5c3b68ad24428a165a`  
		Last Modified: Wed, 09 Apr 2025 17:47:37 GMT  
		Size: 19.2 KB (19211 bytes)  
		MIME: application/vnd.in-toto+json
