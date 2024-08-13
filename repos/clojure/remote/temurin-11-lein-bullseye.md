## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:ac09b47ef65f70ecb0437d33923fef21cad981924344a9675287223a64d66181
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c18ccd52995d8e6ab5274320cb1b9c09ea2b487516cfc95d9ee59e8e3faeae86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257679680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98894bb4bf6cdf1fc94b41401a7ae457643d3317eabb612c5fdeda9ff031a193`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7eb4f5e777d02a0db4859cf52675838e0782b4dedad7990cb7215a4927475b`  
		Last Modified: Tue, 13 Aug 2024 01:11:20 GMT  
		Size: 145.6 MB (145550363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7a689509d4647a376996f0f554b77523169454d351bdfc065973c2c30e12a7`  
		Last Modified: Tue, 13 Aug 2024 01:11:19 GMT  
		Size: 52.6 MB (52646576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2741b781357ba9be5d1e939521fd2b7a403a60c32e589f9c54d7bb15a42a6e6`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 4.4 MB (4398034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:74efcdfa2181f28ed59874704f1e15cb10d50694962b3e88f6fdea88ec3642f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e182e8a3227bf8386d2fe989e9aa0b66ae10fd1b3e2ccf47b7a9494e72cbaa`

```dockerfile
```

-	Layers:
	-	`sha256:3f3618a1e6c5b57997e7500bedd5b7350511e988b23fdbdd8f179c1c842975cc`  
		Last Modified: Tue, 13 Aug 2024 01:11:19 GMT  
		Size: 6.5 MB (6455489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bd7a7de85b1caf9a7603364b8f2bba57d26453e5e2fe7125e581af23f58f42`  
		Last Modified: Tue, 13 Aug 2024 01:11:19 GMT  
		Size: 16.0 KB (16046 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c4b7d202fd42ad7e5a0eb890350127c713ea4c3e36624c7433252b142540e39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253145756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cede5055b324d98bfbd6c00ec98e6add3e46b5be0c6a9274302a81f2c416eb62`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_ROOT=1
# Sat, 20 Jul 2024 21:06:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307167e2f9dddf5502bcdb4ac15623d90fce4e4de6bbc372aa9e0100e67e9221`  
		Last Modified: Wed, 24 Jul 2024 11:26:54 GMT  
		Size: 142.4 MB (142356360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9423c5f7c18d4bc15b9dee4f6c6b251c700c1c92603b1791cba340e412c89063`  
		Last Modified: Thu, 25 Jul 2024 19:20:43 GMT  
		Size: 52.7 MB (52661297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d9211fd1895adf323b9c33034867da1901ea573d329c951baa39c857d13574`  
		Last Modified: Thu, 25 Jul 2024 19:20:42 GMT  
		Size: 4.4 MB (4398080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1ea4be1e670f2305ee50d347d9cf6676c6b432d6a2315440f118185c5aff68b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6477712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f97a538a1735671c897e9e46ccafc019a01c8548113cc167fa03c13897eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:9e01761b02596cd4e4a3644a03eddf8cbfb50020a5de7d69ba39e2e611f35e72`  
		Last Modified: Thu, 25 Jul 2024 19:20:42 GMT  
		Size: 6.5 MB (6461143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9f3d6a0a4f3e1ba2c203f6d4914677e4ef0a996f18a878512f1e4213ea5b3c`  
		Last Modified: Thu, 25 Jul 2024 19:20:41 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
