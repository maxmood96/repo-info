## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:ed666c3c5d9b3b950cb7178b6f17efd1282971c0a54ee6d21ff067810852e53c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:798f43e2e861a0ae21d8b1ce848cfd78bfd50aad9e2c5a18a38e0c5d91496048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229912212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323b3c12b3938e81fc0cdac794267aa90c61b603014ec12c86f66f96a0d248b6`
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
	-	`sha256:2568119f07ae4748e0dea956e1df3b249fccdc7c7411cbf45c9d9a8c8cbcf75b`  
		Last Modified: Tue, 13 Aug 2024 01:11:19 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffec8a5200404baedcedad1195909887e0e3effab26901db718f900e5760ae2`  
		Last Modified: Tue, 13 Aug 2024 01:11:18 GMT  
		Size: 51.2 MB (51220960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2741b781357ba9be5d1e939521fd2b7a403a60c32e589f9c54d7bb15a42a6e6`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 4.4 MB (4398034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713fb9e6d4819c3a27421699ead5652cd8e1e3898185a3d786260852aebca260`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d549fedb2d5e3d475166bf53edc0af930ab47333c2c73f2777e8ec926e71ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d930bfdf2d0398b082ac698df44de4b81b52495aa57ae77ed8922d12be202134`

```dockerfile
```

-	Layers:
	-	`sha256:3d9cefd062b347f03ae4e31e430b36181302abe7f202768c8422b5097b746bb8`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 4.2 MB (4153009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a50e1b40315a3df8b39211a6d3b5cf949329e205fef5988b3403e574fe3c576`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 18.1 KB (18091 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:915ce50682b031bd4b3bc3ec83bea04077cf4ceca49d129c71dfc19fb214edd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228610000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512cb1bfde6b36b2474ec97a7ac83b6876b49405ea17855e17ec6dc5993d7c96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 20 Jul 2024 21:06:39 GMT
ENV LEIN_ROOT=1
# Sat, 20 Jul 2024 21:06:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228d17b6c8b13f68265397f277085d6d433219f01c8551f3a5272bb6cd9389fe`  
		Last Modified: Thu, 25 Jul 2024 19:30:31 GMT  
		Size: 144.0 MB (143959439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5ac888422617b7376fb8584930de0dc3da42ce0082c13d7ba28d3eb57d1f40`  
		Last Modified: Thu, 25 Jul 2024 19:30:29 GMT  
		Size: 51.1 MB (51095524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bf5af1b8f3c94473933135774b5cafdaaf8e3ed4a6991d23f901284ae72618`  
		Last Modified: Thu, 25 Jul 2024 19:30:28 GMT  
		Size: 4.4 MB (4398037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522c28ce871c1052d381e1487145e00a05b011f1f32b13e714273d96992674d`  
		Last Modified: Thu, 25 Jul 2024 19:30:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:30fe9b3b708705e0a9207a7dfbeb00f75153d8afd915362eb41697f6d50585d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788b29b94327d3e996b22c20804f2058e99af48afedfcc8ff3ca70e9deb71f79`

```dockerfile
```

-	Layers:
	-	`sha256:5c7ff842e0e8cba9f96eedc8921f179353094ad15bf3a30dca21021f85366f75`  
		Last Modified: Thu, 25 Jul 2024 19:30:28 GMT  
		Size: 4.2 MB (4159325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1842fd4806b121f15c6e8ea02a7337c10783295785fc801223a9a7df4d5f6a16`  
		Last Modified: Thu, 25 Jul 2024 19:30:27 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json
