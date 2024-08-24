## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:b76f06bf4a985be299c94b069761752b3fff5583783de6d7c612801f3db157f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1af3124b6f79b0e489dbe5a1f528341d1d042713575659c00ac13bbe88c8e20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229912158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5642b0acc2438d0ab2d55a92910c842ec5bf1d202385ae47365e9033299ca5c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab073e97ac8da7b00bb6a6d5f9c2f4620ff702cf5d6c1ad2ce10e2fe7717dd`  
		Last Modified: Fri, 23 Aug 2024 20:02:24 GMT  
		Size: 145.2 MB (145166504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33bfb31ca8e63ee0ab3b14ea16ddf396763dfc5e26d3233df8fd1fc0084ba4b`  
		Last Modified: Fri, 23 Aug 2024 20:02:24 GMT  
		Size: 51.2 MB (51220915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b354f9f79491aa6608225ba74646d22f7a2257c047e28815798ae8634dbab`  
		Last Modified: Fri, 23 Aug 2024 20:02:23 GMT  
		Size: 4.4 MB (4398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953144f9559c5fcfd8d5084be5504e31a03abda6668717896aa5d65d77ca1f31`  
		Last Modified: Fri, 23 Aug 2024 20:02:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:682abd45404e5640620573763b41cb829b8e45100505148e093aed21569f9de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232767f6dc758addcdd585d39b5444cfd2df7c8e208a76f86eea37653cee8f86`

```dockerfile
```

-	Layers:
	-	`sha256:ab0aa03d4c5ecc7e444a13d073e88362b667a37b3c5e17bfd190d723e0fcb282`  
		Last Modified: Fri, 23 Aug 2024 20:02:23 GMT  
		Size: 4.2 MB (4153009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1c3342ae44f2e0480084e0832ba58026e457d006ff8b2241374a6b1528eb368`  
		Last Modified: Fri, 23 Aug 2024 20:02:23 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e2824b033105b9824d78c9997442ba1e52d893f2b677c7177ec7d58dec8c695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228609853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b1c593b7479736d0617180cb8b72e2b8059f46d7f672de93c801d793e6ee2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0215db3e3aa771746614fc4e3673f71f09461c4bbce29be5c787da057a5ee10`  
		Last Modified: Sat, 17 Aug 2024 06:12:19 GMT  
		Size: 144.0 MB (143959503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2eafa2d4adfbd49f525a76ed4b1cc09a461fb45960a7b38dbfbc016642af5b`  
		Last Modified: Sat, 17 Aug 2024 06:12:17 GMT  
		Size: 51.1 MB (51095355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27992bb018f53c0e70c7a4d74c506aa821d15acf412682fc1d593371d43fa2fe`  
		Last Modified: Sat, 17 Aug 2024 06:12:16 GMT  
		Size: 4.4 MB (4398037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856889e1a7b54795194f7151b3282e250a5321826429f3ada1ed49abccb70910`  
		Last Modified: Sat, 17 Aug 2024 06:12:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d55f24652c39fd31008534edee7b1045b73932e29ef88bc740f66d068536404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120309780121337ec4f283a42defd4de3bcd44bae875c4ab1468b2c9bd07bcdc`

```dockerfile
```

-	Layers:
	-	`sha256:ccc92cef2aeb36aaa19eea10825503728db63fd4c5b17d0281feebb043a526a0`  
		Last Modified: Sat, 17 Aug 2024 06:12:16 GMT  
		Size: 4.2 MB (4159325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd163fab9d7d49906bf8138336ff1ecde581fe6a1b06c4a84bbcef75422f5ef`  
		Last Modified: Sat, 17 Aug 2024 06:12:15 GMT  
		Size: 18.6 KB (18621 bytes)  
		MIME: application/vnd.in-toto+json
