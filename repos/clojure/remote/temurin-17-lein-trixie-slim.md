## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:ae35ba3f62da37aacf1d653d9a12790ba744f3da2a2852e2d5290b6146ff2baa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b27353cb6dc83a2a9cfced8d6cc9f7426def2bafb2d2e33bc6a01af7c03948b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196375066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4257c404a7e1bc3177f8732cb171f5647f0a51a995380f722044f3db91811d4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:18:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:15 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:18:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:18:15 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:18:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:18:31 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:18:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:18:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:18:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:18:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f376a9301a511d6611c24705a0d1d19a49ecb2569622e95d15447f009bd25a`  
		Last Modified: Wed, 22 Apr 2026 02:18:51 GMT  
		Size: 145.6 MB (145628747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b4be6a2b0639531cec7151710ca012be1abf743b85da3a6a2e6d0cb7c0190`  
		Last Modified: Wed, 22 Apr 2026 02:18:49 GMT  
		Size: 16.4 MB (16448001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec6be33c32ccf24bd211c6c535c9426453397f8460373e205a3a82d4603da42`  
		Last Modified: Wed, 22 Apr 2026 02:18:48 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c21047f9d4a06a3467f599bb3ad380f1e659dd12753c86eb2c1225d4be427fc`  
		Last Modified: Wed, 22 Apr 2026 02:18:48 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49adc5ed4bd0d76b4ae56659ac0c64b6e0a4f6f4b6dbaae19045ea0eb3efb529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9954ccfe54443b8a3eaa90117be00aec79f39a9d3e9988313342f253f9a0efc8`

```dockerfile
```

-	Layers:
	-	`sha256:88c131be3e916043f92fbe9f7f1dc2569fa31f954deafa27c1915a486adc4c56`  
		Last Modified: Wed, 22 Apr 2026 02:18:48 GMT  
		Size: 2.4 MB (2364788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b214ecd96f1c0edc0751f31fa36dee0f69d4bd484cd5bcabe2d9c5a2df21a35`  
		Last Modified: Wed, 22 Apr 2026 02:18:48 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b39c9a292f5d10922bfcd2858b9b65636877499df2e3130fc87a69a0a965d6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195511953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2b23511e19422ebb823845194488f60588ec8554445704529def43dfbb3f67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:21:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:42 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:42 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:58 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:58 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477f06212b35e7c8240654dcf2ddc43667ad7c3e02ab33bb3114bb74e937ce57`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 144.4 MB (144436253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc7e4f643bc7c5755543d4c202c4945a5b7a471f3f7cf5293461713e5a7f01a`  
		Last Modified: Wed, 22 Apr 2026 02:22:16 GMT  
		Size: 16.4 MB (16413951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185380fe009f4ae03530486cfed801e1892dfd35bc2d19d16c036a04a6cd98b3`  
		Last Modified: Wed, 22 Apr 2026 02:22:15 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eab3768e24ee160e6895bfc30c4cdfd189d2c19a31be74def0d878bfc2ee2`  
		Last Modified: Wed, 22 Apr 2026 02:22:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1062d5ef139a6a3b15301c752725bce901dc7972cd50a6163e669db085789ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2405687034e30671f94a37cb3f5157bd92dc060a3920a4dedcdd670ebef2bc`

```dockerfile
```

-	Layers:
	-	`sha256:da849fc32214864beb708f33254233c001cd2ddfcc557da2c5835eead58ef7ea`  
		Last Modified: Wed, 22 Apr 2026 02:22:15 GMT  
		Size: 2.4 MB (2364406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9577d879fa857da5441cea5b020dbd1c58f4790601f5f9a836e3d1bee2473a1`  
		Last Modified: Wed, 22 Apr 2026 02:22:15 GMT  
		Size: 18.5 KB (18507 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:50817a10e371dfd42394ea5abc5593380b5c7bae5e018d3065d3fedbb2cf36fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203235867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68a9465226e9109ee412895af6b0e304eb5257eb423938133f38895e84ef850`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:51:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:51:45 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:51:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:51:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:52:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:52:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:52:28 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:52:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:52:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:52:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:52:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d63fa71f8a08634b0312e1df11dd8fc3363471d8c3e45af52999c7c3ba56e4`  
		Last Modified: Thu, 16 Apr 2026 02:53:12 GMT  
		Size: 145.4 MB (145438287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023b39aa86c3de3ef5fae001df93273c4fd154460a53e12496bd4cdfcc54ed47`  
		Last Modified: Thu, 16 Apr 2026 02:53:09 GMT  
		Size: 19.7 MB (19686394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d236a281e99791b0e1535d92a57fad4556a0bdbbaaedc34381ca343af6aa97e5`  
		Last Modified: Thu, 16 Apr 2026 02:53:08 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697e62791846a729ebee72e4bf5a111d45bf520c7033772f1f7878a0e0a8ef62`  
		Last Modified: Thu, 16 Apr 2026 02:53:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e9647dcd9da6a2cc02b95cc312c3650b3997c9cf1fe9cea06f53a2c0e53ab9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c3f768c89446865ebab4118f4d67556ac21e6f4c0d86662f8e5c882e19c7f9`

```dockerfile
```

-	Layers:
	-	`sha256:876957575813370f6e16cf0930433c8076029adffb6b3b71330084fb50a441b3`  
		Last Modified: Thu, 16 Apr 2026 02:53:08 GMT  
		Size: 2.4 MB (2365768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84efd601c4e2d94c3df6a8bd31427b1881b8931cea5fd7e9564594bf946d18a0`  
		Last Modified: Thu, 16 Apr 2026 02:53:08 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:ab8f8eae14631506452d9cc9a01e53626176b9257d55bed7ccae044699142009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194475094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0109c8eb9021f12d61a1999ea38a1b2d55785497967170a5e9a3663610c8a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 18 Apr 2026 04:12:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 18 Apr 2026 04:12:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 18 Apr 2026 04:12:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Apr 2026 04:12:57 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 18 Apr 2026 04:12:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 18 Apr 2026 04:12:57 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 04:14:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 18 Apr 2026 04:14:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 18 Apr 2026 04:14:34 GMT
ENV LEIN_ROOT=1
# Sat, 18 Apr 2026 04:14:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 18 Apr 2026 04:14:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 04:14:50 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 04:14:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6098747780e1520a3d6d899270f72a03303fffbfe05521aef71b5a82c3ec10`  
		Last Modified: Sat, 18 Apr 2026 04:18:43 GMT  
		Size: 142.7 MB (142662942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1460b7a4c85c9fb92cbe4b159e8a7d0ccf93175e0d2f05daa2b271eb001c31ec`  
		Last Modified: Sat, 18 Apr 2026 04:18:25 GMT  
		Size: 19.0 MB (19018151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25ae74d911e0e31d5b5f0405efe3fb3574a684142af619686f233b84502877d`  
		Last Modified: Sat, 18 Apr 2026 04:18:21 GMT  
		Size: 4.5 MB (4517792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4864652acca166e4875f0aee4dd45f4ddc3af3d815ac9abf147a0dc8d1cf7a2f`  
		Last Modified: Sat, 18 Apr 2026 04:18:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a2bc23ed41f148fbf7770b3fc84644751ecb22374191cbdbeafe858ffbda7857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ceca28f71f21a3ef57935dbc1cb99ccd077e64cc59b3e32c4a4a4d4128e2cf`

```dockerfile
```

-	Layers:
	-	`sha256:8b887b447970878a156ad21cdcf8b2911974d1e703840e41dbe28a537e4e229a`  
		Last Modified: Sat, 18 Apr 2026 04:18:19 GMT  
		Size: 2.4 MB (2354917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4febc278377dc43b1e801830c3b7a5ac31fa00bd930b663db6fd3ba5d8cdf98`  
		Last Modified: Sat, 18 Apr 2026 04:18:19 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8e6b726f2bbba52d6168795ad49bee40d413699977e5320682b24cbc257c05b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189070756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8871aa6f383faa8d17350cffc41615a9628cbff695c1fa7dd0e380f70a46cc81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:39:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:39:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:39:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:39:01 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:39:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:39:01 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:39:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:39:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:39:14 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:39:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:39:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:39:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:39:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d36a84cb6d079cf792c9c396290b7bd92a15b0e0062e4db42501798b36b6fb`  
		Last Modified: Thu, 16 Apr 2026 00:39:42 GMT  
		Size: 135.6 MB (135627010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308be1ca3c877039d5e8d64a0efaa2df6fce97540555c3592cf5bf62e6bff241`  
		Last Modified: Thu, 16 Apr 2026 00:39:40 GMT  
		Size: 19.1 MB (19090142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b999c1055ca6af25c06c3082fae790f04174b1111f771b4be7a367ba36182ef`  
		Last Modified: Thu, 16 Apr 2026 00:39:39 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b2b7e855ac308662a68ff4226dd8067ef5781ffdb417214d37c2295d0451bb`  
		Last Modified: Thu, 16 Apr 2026 00:39:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0fc9c510989d3ea26eae2f863282ab5ad29e1271a49f5e95a7d7f90716f92055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9a2d09309956f04abdf95ff62f72330cc47814faf7abe7e0e1f8be75955c06`

```dockerfile
```

-	Layers:
	-	`sha256:99feccf4bedb6e75363415313593c181e38d5c8c24955d5ea1e5567af3359ff3`  
		Last Modified: Thu, 16 Apr 2026 00:39:39 GMT  
		Size: 2.4 MB (2361215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776afb745e8710584b86153e85d70c6af491c69cbecb1ba2fdff1a3b05000de1`  
		Last Modified: Thu, 16 Apr 2026 00:39:39 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
