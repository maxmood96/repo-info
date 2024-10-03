## `clojure:temurin-23-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:def77d26a2c6f5dd06dfb8ddc8934ad78b8b3f182779ab77a116385b774d7a26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3be9bba1a5d5aab5d4a24a393d73cec32a1d74db750873a365a91ea6e0280c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277646225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d535a28061469c6d0e31f2703bd32da4968abdd7b966deb4f525dc6bcd3f526`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3db4d59d2a2df73287e0e0b04e19843e5f2a6aaa0003aa906b71abee72553b`  
		Last Modified: Thu, 03 Oct 2024 19:00:44 GMT  
		Size: 165.3 MB (165267612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb012331f2807788c4d1e1385b4103d9b1c5ec98c9b456a75eba1293b20ce0`  
		Last Modified: Thu, 03 Oct 2024 19:00:42 GMT  
		Size: 52.8 MB (52782653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7649f0817824102d525c52b92b1b292d74b9e8f53d2c5a571b4f019cd8732df8`  
		Last Modified: Thu, 03 Oct 2024 19:00:41 GMT  
		Size: 4.5 MB (4514139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6dea93e52733944ae0752c81b86843c9b903f6c8eb7be424edabff37e522d2`  
		Last Modified: Thu, 03 Oct 2024 19:00:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:332d7f30b41c350ad2eb7fe8303625a94a20f0ec7f7796a8df6a66810aa8731e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6629313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225959d9059c1ca06d2b745a3afff86742dce77c8dfd41859ac1010683bac4f6`

```dockerfile
```

-	Layers:
	-	`sha256:924a18ea0d41cf1eb533d4ee3486aba17ed5af0d5254c19769a3eb7534805bc6`  
		Last Modified: Thu, 03 Oct 2024 19:00:41 GMT  
		Size: 6.6 MB (6611267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f82cf224f6f2279e8bad8e1f3f9bcdd82f0e036bcacaa2a4d8a5254dd75708f`  
		Last Modified: Thu, 03 Oct 2024 19:00:41 GMT  
		Size: 18.0 KB (18046 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dcc3aea4ad932393e8464a6f3be69027d57efbc55b446e044737e5a5a3e83b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274322106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ffcc90d24ba16e36592929bbb33c660681e298e147afafd09b0bf37d34c44f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd21f2c0c517dbf21f8221774b130094c4842babef9809f4ca92c71e1a4db8e5`  
		Last Modified: Thu, 03 Oct 2024 19:03:12 GMT  
		Size: 163.3 MB (163252821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fd749502a71ab0e6a5fe944e903978dc42b3ca39cb94a498ff1f21cb80ef43`  
		Last Modified: Thu, 03 Oct 2024 19:03:09 GMT  
		Size: 52.8 MB (52820792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f46941bd5ac8dc73b5f814915bf7505b746ab174cfe4a72c36de4bcd2c874ae`  
		Last Modified: Thu, 03 Oct 2024 19:03:07 GMT  
		Size: 4.5 MB (4514200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f58056021233bdddfbc91e1dd2abb8b04be8394ebcb1460607112957fe42f1`  
		Last Modified: Thu, 03 Oct 2024 19:03:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:36f44e7c524eac1463a928caf2280c52a910f6e2e5f156a54a35875f8c4a194c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6633834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f99c04c2f8c8b3d100ca61f64f96ef833ef344d865c9207773022d31356c636`

```dockerfile
```

-	Layers:
	-	`sha256:0266156bb76131d0e9ca41efd068f2df03e314cef755bb2511802e344310437e`  
		Last Modified: Thu, 03 Oct 2024 19:03:08 GMT  
		Size: 6.6 MB (6615680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:948da41ca01cf270e194f14ae507f2eaba92e35b190a62535c65ab73a0e44649`  
		Last Modified: Thu, 03 Oct 2024 19:03:07 GMT  
		Size: 18.2 KB (18154 bytes)  
		MIME: application/vnd.in-toto+json
