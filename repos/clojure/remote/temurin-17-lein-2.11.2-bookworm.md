## `clojure:temurin-17-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:6273f309035221e06b2b849f1da5b23eca9d67a18e1ab6ac69b33bbd916b3589
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:abc2c0d138b3f640ad12fc6b40f9554dd16d12d5cdb2e3ed63b15cceb857ff6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260918549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1debe779ed9255b43db97cef460fea6abebf25c0fbc1c800b94c239444271915`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dd6d08e61a9f76a12f27bc903b20119d8470ab41efcad4ed5613ffa25df4b3`  
		Last Modified: Fri, 23 Aug 2024 20:02:36 GMT  
		Size: 145.2 MB (145166508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663650b4d3c7b7663e0d96d58e43c60163434fbfcdd77bb8e96a0132f281b082`  
		Last Modified: Fri, 23 Aug 2024 20:02:32 GMT  
		Size: 61.8 MB (61799499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c58438aec990c161463f0e3bb588504e350ba67659d7cb1bc877492ee692aef`  
		Last Modified: Fri, 23 Aug 2024 20:02:31 GMT  
		Size: 4.4 MB (4398031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5d397f30016129d7d20bbb7865d0164a6d0e8195a9e06ff4055bc4d005ef02`  
		Last Modified: Fri, 23 Aug 2024 20:02:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7d23dd79e89a87bdb79d6eefc17715fe663fdf5f56c0b7d9e38cded7af5bc28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6381055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130b3a40304fcd778cb0a86f71860f365366177fa40c824f1c8202d76ecc80f`

```dockerfile
```

-	Layers:
	-	`sha256:0c2c15783ea062027c93ef4a22463de166670b874ae1ee3f622854914567a053`  
		Last Modified: Fri, 23 Aug 2024 20:02:31 GMT  
		Size: 6.4 MB (6363013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a26a507aca98925dcaf8fa4274a8215116cd03ad813823890556e1908ff98e9`  
		Last Modified: Fri, 23 Aug 2024 20:02:30 GMT  
		Size: 18.0 KB (18042 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:47d940ba0e30469887a92669f00def0480be9c092cabc6d94138e70c8e9b7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259620784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc730794f0e4bb77c1e503fb9a8c2e93281423316c4c1b66b403fc3b0b9a2b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30518595e909e33f4b333ed4f46e0a6bed2642d328f1ab72905e694f16d9876`  
		Last Modified: Sat, 17 Aug 2024 06:11:23 GMT  
		Size: 144.0 MB (143959503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66886bf42dd69a3f15d98bdc750ecfba0966e4c04c9761209d82610e166201`  
		Last Modified: Sat, 17 Aug 2024 06:11:21 GMT  
		Size: 61.7 MB (61674231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8745e857c32dbfa8b95bc5842b8807764fdcde7ef08569549cc9f5895ad65e3d`  
		Last Modified: Sat, 17 Aug 2024 06:11:20 GMT  
		Size: 4.4 MB (4398030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0126138f20736f21c84b1a3ef9e52727c9d60f87b82530264753374c41790e25`  
		Last Modified: Sat, 17 Aug 2024 06:11:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e2b25116d72d3d9fc658d1f962014f2973d5ed01fceb3b7575c5678f8bedcf00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6387896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7a902629dde0a6591366004c39735e4607e49f0e1c6d954ec7762e6bff08c7`

```dockerfile
```

-	Layers:
	-	`sha256:ed923ff00fd78e28f9b269b3df1069d2c0a08c686b5abdb3e5a10a46ba8158ac`  
		Last Modified: Sat, 17 Aug 2024 06:11:20 GMT  
		Size: 6.4 MB (6369331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afb8147be61b0a3aaa32f4ca9837881b675898faef71d84678b27b325866184f`  
		Last Modified: Sat, 17 Aug 2024 06:11:19 GMT  
		Size: 18.6 KB (18565 bytes)  
		MIME: application/vnd.in-toto+json
