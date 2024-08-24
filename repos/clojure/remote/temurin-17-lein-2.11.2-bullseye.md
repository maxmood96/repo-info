## `clojure:temurin-17-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:e3ef9433fa0a21502bccbe92b8b64bf700d68a0070e379c39f796812cdd0f34e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:90633ca20a13e3d9aa110de9c89275ffb69e1f84e0f0b078799c76bdc6c7aa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257296322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97690a68aab189fb53366eeb21d4334a98ff621e9d64bf52507d545f42c07b3`
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
	-	`sha256:07abb79a89876f8ba1079409aa46960fedd2958bebbfe9ba0e1c70e37e37c2c9`  
		Last Modified: Fri, 23 Aug 2024 20:02:25 GMT  
		Size: 145.2 MB (145166526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4924adec296401731460a5a85fdccda7375bfffd9fd687ce494de97fa50be13`  
		Last Modified: Fri, 23 Aug 2024 20:02:23 GMT  
		Size: 52.6 MB (52646658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bbe1c14cb48d3ef0e3e61a876330ef2245470e0b2b5058b53df0d2457ae2c4f`  
		Last Modified: Fri, 23 Aug 2024 20:02:22 GMT  
		Size: 4.4 MB (4398033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e412232cd2eb3cfcba5372bc58b7c705839faecf7f2b1b773906883c78ffe5ea`  
		Last Modified: Fri, 23 Aug 2024 20:02:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4b7a4ece6b0cf0207c78c51922ccdabcb64db60e33eead35559ea52443f21443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414c7b0e299bfbc2afc11c819c76d8f93c3f7531775a493e8945c53cff62344b`

```dockerfile
```

-	Layers:
	-	`sha256:421e32f7888d83857302dc834ea33da7173e62cf0a82db70b215407506718d8e`  
		Last Modified: Fri, 23 Aug 2024 20:02:22 GMT  
		Size: 6.5 MB (6455489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d147572dd633c23ad649058375bcd90f30960b7f43f68f41fd72640bc535498`  
		Last Modified: Fri, 23 Aug 2024 20:02:22 GMT  
		Size: 18.0 KB (18042 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8fd72250a7e2826c13aa15e49b5fd7bf30c525275697d6373f1e904f6dff6c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254749234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdf37aefa00cdaeb4be5b64a6464f75128c7d32c2961e703eb26dc53aae52e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d3fde3d3d17b93a446a4eecbcfa1ebd2d2f9f07d55e44c654e037142ffeade`  
		Last Modified: Sat, 17 Aug 2024 06:13:14 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed0f59ecfdb12bf4add86de762b80916ce7f248db2b5b310e4ddb21962c9121`  
		Last Modified: Sat, 17 Aug 2024 06:13:12 GMT  
		Size: 52.7 MB (52661376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f194b91f6f02f01bc2e9c7552072d3ea487818f197af6a2a6c4402574a924796`  
		Last Modified: Sat, 17 Aug 2024 06:13:11 GMT  
		Size: 4.4 MB (4398037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528469f23794b932e4ae11bb3a2ce28e9f6df049ea67a35eb5648a003cab7f45`  
		Last Modified: Sat, 17 Aug 2024 06:13:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:267eceb8fe3603c4daea64aa65db0654025d0eda3a9ff6e3ea0cb93825e01635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cc93419432ee550a0450590579afa9da907237bb291ae242bc808e9f23b1c2`

```dockerfile
```

-	Layers:
	-	`sha256:be6158b592c493dd4e4a6a9bfa3abddb307af04e10b2885a5d23cd14d4703c23`  
		Last Modified: Sat, 17 Aug 2024 06:13:11 GMT  
		Size: 6.5 MB (6461143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:052bba141dc7c7c77ce473a67468467748cee603dd684bc2432d7500df182a83`  
		Last Modified: Sat, 17 Aug 2024 06:13:10 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json
