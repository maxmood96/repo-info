## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:ca3fddd22baf95d90a50db7cc15c549191861f3cb49ad4766d00da1c82d1b01d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e1e6ab9afb00983339eb70c25da80641e5926b40eff4a00092f15ac643b16d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270709032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a537460d169f5ff377320a057151df3d80dcb68e0bc6b42152dd078aa3e5ba6`
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
	-	`sha256:b226db74a5e02bcf09cc9447d521aca790d20b4e5c339614557b678e991f04d5`  
		Last Modified: Tue, 13 Aug 2024 01:11:29 GMT  
		Size: 158.6 MB (158579313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1993b1d60c65acd18f1e32be445adbfa668ff86fb5d57ec5be5621132667a97`  
		Last Modified: Tue, 13 Aug 2024 01:11:28 GMT  
		Size: 52.6 MB (52646585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23550680b299dde1688bec504691c16f7f77a461f17309018e8bc5140061e13b`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 4.4 MB (4398031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cc668dea2f055e128309e84ba52bd8cad885bf6c43988d09b64abbdaf35e03`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:176d84ef3ca859964588e954f15d0f284aad13f19e9e428f37994ec52b95cde6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6474825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4facfed3bd7d2a9915e075cb58356cd055a0f9383c9fd6755fca54287d3e19a8`

```dockerfile
```

-	Layers:
	-	`sha256:54e48b2f366d44734a59647fb1b5f20541f132abf44c79f1239e5a1386fbf7e6`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 6.5 MB (6456141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf62d8b03b874897549fc687610a51c2608afcf0374b51bcc34b5e339d2aaef`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 18.7 KB (18684 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f038f68dbfc85ba0281c113d38b595bf5a63de688e2b2f1d96d6866e2665f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267535998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5378a56f9ee8c103f997d0777c870a306f4ef4ef0cb0688a87106073808832`
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
	-	`sha256:2430d84b3203c6622dea811cc35b3f4c6b527003ba6199fff9466c03919a6664`  
		Last Modified: Thu, 25 Jul 2024 21:17:29 GMT  
		Size: 156.7 MB (156746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15bd4b99298632b7ee0d19341720e6f920e89f1265f16eace22c4e4cc0adf6`  
		Last Modified: Thu, 25 Jul 2024 21:17:27 GMT  
		Size: 52.7 MB (52661310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f425b224d988593d3eb7c1f152d1074d849aab56a36308a545461bebf115c81`  
		Last Modified: Thu, 25 Jul 2024 21:17:25 GMT  
		Size: 4.4 MB (4398087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c94477ddd56e1d779e08a02c59814c0b1562c0440bb6db4303854466e2e8f9`  
		Last Modified: Thu, 25 Jul 2024 21:17:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7b8095d7ec9a443377bb81dc3fe3e3e95f82bcd32e6a21310aecfb222a4dfb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c667144f70dfcb05e121991ebe63dc520da406caa8a5851fb58e1c72aaabe7`

```dockerfile
```

-	Layers:
	-	`sha256:215ec0c776da6e215e497843f56337d8d25691556fe3610171e1da133c3b3ad7`  
		Last Modified: Thu, 25 Jul 2024 21:17:25 GMT  
		Size: 6.5 MB (6461819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f105d5b2cf2daa426725e87aa1aca794c02c2b3de00d39a03a880dce327a0f5`  
		Last Modified: Thu, 25 Jul 2024 21:17:25 GMT  
		Size: 19.2 KB (19232 bytes)  
		MIME: application/vnd.in-toto+json
