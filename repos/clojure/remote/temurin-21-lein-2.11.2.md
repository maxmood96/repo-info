## `clojure:temurin-21-lein-2.11.2`

```console
$ docker pull clojure@sha256:d24de1f98eede7a92de8982e42692f180dab4dd4f0b8f351f5be774d535d0445
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-lein-2.11.2` - linux; amd64

```console
$ docker pull clojure@sha256:3ac0277c2ec90d37716f553a3e01a61c09321fa02db606246630131fdbeb94b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272898049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d1badb3f139a0318d470c369a3be8379be6d2cbe3b51d955d72e9f041fe6be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_ROOT=1
# Tue, 26 Aug 2025 17:11:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec333d20f51b88d7aedec2020b836e427b1241ed51491d08348a870e7df768f`  
		Last Modified: Tue, 02 Sep 2025 04:03:48 GMT  
		Size: 157.8 MB (157804794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03065ba0a01327436813bc2723fb4a815c7bbb15a682570ef95d7fdfb0ab70f6`  
		Last Modified: Tue, 02 Sep 2025 01:55:51 GMT  
		Size: 62.1 MB (62084151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a5f39781cc51a908f36ca464c8acc39edcc772e2daada76fc43f8d7235ff2e`  
		Last Modified: Tue, 02 Sep 2025 01:55:40 GMT  
		Size: 4.5 MB (4514162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3083097ad4931397dcee1fc51362a5fb3110a08c116bdcce152875dcd89f9d6`  
		Last Modified: Tue, 02 Sep 2025 01:55:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2` - unknown; unknown

```console
$ docker pull clojure@sha256:0828f2467d31ce03418b58dc078074ade88e769eda67e88344c3a98d9e8daec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290d4105b6e73edb25a8ffb2c2e8138d4dcf12cbac1defdbef38faa11d2dda34`

```dockerfile
```

-	Layers:
	-	`sha256:22e1a69ea7a37253bf6dabb38dfa56c486764834cd14642e951d4376653f8f8d`  
		Last Modified: Tue, 02 Sep 2025 03:34:31 GMT  
		Size: 6.7 MB (6707721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a598435069f143d088907ba7bf7a2e19bfda763bd4eee5eab97a102bde578a7`  
		Last Modified: Tue, 02 Sep 2025 03:34:32 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.11.2` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bcbb984c51fe56780026d05960427c5af8c4ec1cf571390cb46033e6354855aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.0 MB (271007160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f2132a0d224c771780b4ff7c45f8059e73b2fe7a16c034c094a4071af06f6a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e753482983ad3d2a629b620956b3cd49a7214c4f84f167fd737158d8332d4c`  
		Last Modified: Wed, 13 Aug 2025 16:01:51 GMT  
		Size: 156.1 MB (156081215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8856aa3623c50daafdf1e8b737756bc9da09490027bb0823fee5cd877cd0f06`  
		Last Modified: Wed, 13 Aug 2025 14:31:29 GMT  
		Size: 62.1 MB (62068867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b10260051706e4b966b73975284e30faabb1cdef55ffd270a0c5497e3895d35`  
		Last Modified: Wed, 13 Aug 2025 14:31:07 GMT  
		Size: 4.5 MB (4514200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be061af1c6a3f0ae1c87d86e2dfe9cbd3ff3dac652f6f030ad68a67272d75e69`  
		Last Modified: Wed, 13 Aug 2025 14:31:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2` - unknown; unknown

```console
$ docker pull clojure@sha256:af44421eb48aeba4dd66f4044499753f1b539611e0babbd2e43f51888e6e46d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6734001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c1ab48b7ffa03a3441be4b50d300008a73a02ed63e2bcff29891ea52fa927c`

```dockerfile
```

-	Layers:
	-	`sha256:86f68690a265622e5ace61f3684afaf922cbf93822adfe4794ac6e80daa6ca88`  
		Last Modified: Wed, 13 Aug 2025 15:34:25 GMT  
		Size: 6.7 MB (6713487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07433d01f716d55c6d310662f3992291111a780d0b7cc152e7dc1d9049551d7b`  
		Last Modified: Wed, 13 Aug 2025 15:34:26 GMT  
		Size: 20.5 KB (20514 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.11.2` - linux; ppc64le

```console
$ docker pull clojure@sha256:0bcbf60dfe710a24a01919a29c9a5232fc543b036fd1c35f8f851ea0d6b0fb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282135606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e219b04dde8636b891fe74ac0082bddb7cbb0823868853700aab1901c6698`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21178e342602edd12ca410499981adb42800eb941f19d77cad58cb797945aa34`  
		Last Modified: Wed, 13 Aug 2025 22:01:26 GMT  
		Size: 158.0 MB (157963474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975d0422b476bf5542b98f3b3e328e5e540e7906eba26423df4a5cd04720e57e`  
		Last Modified: Wed, 13 Aug 2025 19:15:44 GMT  
		Size: 67.3 MB (67319468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008a029848fe2d651f9dfe299da6b09f98362369ef2e0b35cc2fe8ac9359417d`  
		Last Modified: Wed, 13 Aug 2025 19:15:39 GMT  
		Size: 4.5 MB (4514158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dd2b401f1304c54e5d774c8c6c26cf25f090585ac724cb288466f6319a2396`  
		Last Modified: Wed, 13 Aug 2025 20:01:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2` - unknown; unknown

```console
$ docker pull clojure@sha256:e116ded3f34e29e6d2fc38856df34d10059ca7ec53e1437bfc93b8193db7f83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6733027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d55f80e5677b94d772f90c210b6ec55b69628a357dc4144a02ff1a220fcc86b`

```dockerfile
```

-	Layers:
	-	`sha256:e129730de12de444855878cc2968e8852b1865db0e26242e1ca62abdf3005a44`  
		Last Modified: Wed, 13 Aug 2025 21:34:37 GMT  
		Size: 6.7 MB (6712626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a05a4f6758904dda60e0ed17a09e45fffd6d83bee012f097ab609d12fd98001e`  
		Last Modified: Wed, 13 Aug 2025 21:34:38 GMT  
		Size: 20.4 KB (20401 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.11.2` - linux; s390x

```console
$ docker pull clojure@sha256:c5da87482c9f158dbc00b5d9343b066f74fa4a1d590288754000213d74048418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.8 MB (259795119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a6c1e8f0191cca1596e4f1b7a5bd789b374acfb057586d9f119125a52d292c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_ROOT=1
# Tue, 26 Aug 2025 17:11:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c854f0bb2062cb8e3203dbffc406ec501de420643779bca54d79fdb8235d74`  
		Last Modified: Tue, 02 Sep 2025 03:34:47 GMT  
		Size: 147.0 MB (147026994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfa6e41ff4ddd14e0c205a8635504a0e121ebdc4246eeeced3a7ca86ad51cff`  
		Last Modified: Tue, 02 Sep 2025 01:43:04 GMT  
		Size: 61.1 MB (61103640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb9551b91f7825b89a424cae6ab68cbc4e5c14a5dd1bffe0fe5d1e7a2913d18`  
		Last Modified: Tue, 02 Sep 2025 01:42:58 GMT  
		Size: 4.5 MB (4514189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72b61d9af8c2642a0d58c92b3bc382d15fa8f2dcc31e40b4d7d346560a3d332`  
		Last Modified: Tue, 02 Sep 2025 02:08:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2` - unknown; unknown

```console
$ docker pull clojure@sha256:fd58adb96f2d692a97922575a3dae70431c2c340a941a0a95a3f74354db6ccec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6719418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf377e491d334fe90547e4100c5172f660de6c2df32f6545d2b1d1aacc2b85af`

```dockerfile
```

-	Layers:
	-	`sha256:ec325e00a71b3c6abd100e4fb07b42d5916ce3aae46b3b55f436a9b6e8d33641`  
		Last Modified: Tue, 02 Sep 2025 03:34:48 GMT  
		Size: 6.7 MB (6699097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f834b42bcbcb2d40c3286bfd51683e8f2074fdfcdb719ad11c26e347146dd610`  
		Last Modified: Tue, 02 Sep 2025 03:34:49 GMT  
		Size: 20.3 KB (20321 bytes)  
		MIME: application/vnd.in-toto+json
