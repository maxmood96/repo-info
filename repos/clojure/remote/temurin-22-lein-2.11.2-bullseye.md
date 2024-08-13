## `clojure:temurin-22-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:d39dae4d48cdc46193d69ccae61f0438299ec3ec4ae02b914842b0ee798cfddb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:42c715c1ccc96663889405d01fd35bab649139b538cffaed436651e6977be4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268611283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f01ae975f84a591a57d2fc4611ae985352a6f804904e46ee55af627f4baad2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa80d10354fa56b380ae225a693e38a2e035b914320914975b9ecaf5bde3281`  
		Last Modified: Tue, 13 Aug 2024 01:11:47 GMT  
		Size: 156.5 MB (156481595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954fb8a4a54c39d0ad187c9a0027426553e1891bc22772984c3caa14ac6f7e53`  
		Last Modified: Tue, 13 Aug 2024 01:11:45 GMT  
		Size: 52.6 MB (52646509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93aee7facb0f154f91adc186c53e74ceb14d608a2d64d9d432d0fcdf82df9878`  
		Last Modified: Tue, 13 Aug 2024 01:11:44 GMT  
		Size: 4.4 MB (4398076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9a90a33ade1c4f01813f58906c395e159ee319aa6f3609fe53928804c524f5`  
		Last Modified: Tue, 13 Aug 2024 01:11:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c15c6d7f953f463e1e0b5b86b48528eb2e01624063e6d477540ad0d411a31ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5284b0754195aa5ac2dbd08039be53aaddd3c6f498b7415d3992523fce9138`

```dockerfile
```

-	Layers:
	-	`sha256:e2763203d94697843ff59ab3b184ec38f9bfa632506f088cab68f5f8a2094849`  
		Last Modified: Tue, 13 Aug 2024 01:11:44 GMT  
		Size: 6.5 MB (6455483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6933bc879767bf6b03a3e89621f57cb1ff486be1ab7077a74628a46d1abf9a9b`  
		Last Modified: Tue, 13 Aug 2024 01:11:44 GMT  
		Size: 18.0 KB (18042 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e9d105158e07c4dedf9fa22a98deea64c3e56d34a0b95539ee88e65e6382474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265293563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee160a770b183b1b2f8c09319e7e8e9dd9020bbb5301fefbaaba7963b246b46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_ROOT=1
# Thu, 25 Jul 2024 20:19:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b26f305860c4ff586a0338632919bd31b49a3b9bb89c8ebda5d6c0f4a1b3e7`  
		Last Modified: Thu, 25 Jul 2024 21:29:10 GMT  
		Size: 154.5 MB (154503721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c398d5dfe98fdc54ff379bfd13108727d7af21ca33f0275343fe5ed911fe22a6`  
		Last Modified: Thu, 25 Jul 2024 21:29:08 GMT  
		Size: 52.7 MB (52661371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701d3deebc96456a35a23c9cab0d00bb517aa70825f99e14b08fa0f49c8de7c`  
		Last Modified: Thu, 25 Jul 2024 21:29:07 GMT  
		Size: 4.4 MB (4398055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75fc93d2da9b47184b1344fdbe5d854c11d8f9eb758e0af2c3a5cc74ede18e`  
		Last Modified: Thu, 25 Jul 2024 21:29:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6ad3e5a6ede335d8280ad1e00cea0fabdf2cd8e27018bcc8fae65f3ada36de08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef850f724c8eb9c36faeac7eda37d21ac36ee3a78b678a8bf8a96db1e79db54`

```dockerfile
```

-	Layers:
	-	`sha256:7474f32f8e0be618c38de7463031a447db70b7c09b63e9c7635570281acf6faf`  
		Last Modified: Thu, 25 Jul 2024 21:29:07 GMT  
		Size: 6.5 MB (6461147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f2065d6e24d299cda4ce9e3cfba36d4ef6a1dc7ff75f154191d81c9db94b1d8`  
		Last Modified: Thu, 25 Jul 2024 21:29:06 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json
