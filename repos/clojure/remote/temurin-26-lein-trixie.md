## `clojure:temurin-26-lein-trixie`

```console
$ docker pull clojure@sha256:43a9994d50d4f7d519886cf07feed65974a1b39e0b7382b221de384b69d9e435
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

### `clojure:temurin-26-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:29f272211bfba7e21ae3ba8c678c53b51fde1146fe03eaf1831ef034643714af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170360822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad918d4bb9d52f48f8c17cc2955fee5bf3176e1f6df326600e6cde25c6cf4c54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:07:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:07:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:07:39 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:56 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:07:56 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:07:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:07:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d9040ad847014a29036aa84a29bc2948b1a39c1550b58b8d008e374f7151fd`  
		Last Modified: Wed, 15 Apr 2026 22:08:17 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad61eba24603b66c49d1d98fd20b4e32dddff7b8e72cb9f544e41d3653d0670`  
		Last Modified: Wed, 15 Apr 2026 22:08:16 GMT  
		Size: 22.1 MB (22089123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8a1c53d3f925689ebd56d06a34cc1d380fdbe67464ce3b678df9d50c640db9`  
		Last Modified: Wed, 15 Apr 2026 22:08:15 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4e7fc6bb0b4f465a6c998bba9861a9058986bb5bfc6aaba13ea2354ffde134`  
		Last Modified: Wed, 15 Apr 2026 22:08:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:676ccd10df3a646885a3ffc63dbfe89bdcb78f8818a6d1a900f66d67d8f92f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7c8601b8808c08683852843ea29ceb27c1de1ff0b5a0cd6294112891d713df`

```dockerfile
```

-	Layers:
	-	`sha256:648b1089c9a1e256730b1f489135ef1bd78bd8d35d98f9aa11faea9a50b4c764`  
		Last Modified: Wed, 15 Apr 2026 22:08:15 GMT  
		Size: 3.8 MB (3781031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4ab22d620d4816e85a933fbefb16ca15b553c03fcd4f3de5326dbcfd839006`  
		Last Modified: Wed, 15 Apr 2026 22:08:15 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0c402ebaa1716936e4add963785e027ba5bd5e52e591b9f3eb7ec2073a103a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170002864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972102b4ff7be20b3ecf471a35108a5b20992980b0cf06d465f8fa5ef51119bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:36:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:55 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:36:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:36:55 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:37:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:37:12 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:37:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:37:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde9acb7de012f45afbfad53e522261ea1f2ecfa79f30fc1f092b6badc13493`  
		Last Modified: Thu, 09 Apr 2026 23:37:33 GMT  
		Size: 93.4 MB (93395164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a8dc5272cd1e348b92ebef74ca65ce72f0af2936f14f0fb6686abbc98c0334`  
		Last Modified: Thu, 09 Apr 2026 23:37:32 GMT  
		Size: 22.4 MB (22424276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9266ba1d17ed799a6b5eda40a35270cfeecf77c0378dbc07eacf2e343af539`  
		Last Modified: Thu, 09 Apr 2026 23:37:31 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9905d8633c3501b93fb6bebb6ecedac10ad00fc0dc66811caaa38f4f0dcf30c`  
		Last Modified: Thu, 09 Apr 2026 23:37:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6773faf08aa3c0fb46717cc8f380882fdde553124ed6f39d7ed00490e5be026b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff5ab89670f3ba9a0ddfdf97c912df5dd6564e3555e9e32a5a03770b41e7aa0`

```dockerfile
```

-	Layers:
	-	`sha256:aa95b3e97c91eddba6b72c7850fc84e15e3e239d85678e24b7db9915582715e4`  
		Last Modified: Thu, 09 Apr 2026 23:37:30 GMT  
		Size: 3.8 MB (3781905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:549e7159eea0deed58068f1f5d37efd1e61e529068d3f3fa5b7b9ef81beaa080`  
		Last Modified: Thu, 09 Apr 2026 23:37:30 GMT  
		Size: 18.5 KB (18466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b34e0c191c4b869b889212586712f9df0b8f0a032979a06df8fa1f366e73b588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173809975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5e5e907f2cbad4f1e604cd875e6203b1c4c80a37634e185943c9f0ce725954`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:52:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:52:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 10 Apr 2026 00:52:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 10 Apr 2026 00:53:00 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:53:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 10 Apr 2026 00:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 10 Apr 2026 00:53:41 GMT
ENV LEIN_ROOT=1
# Fri, 10 Apr 2026 00:53:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 10 Apr 2026 00:53:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:53:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:53:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfcead13693a6857ab51b621e372876765c71adf46e88c3448e530a15832886`  
		Last Modified: Fri, 10 Apr 2026 00:54:22 GMT  
		Size: 93.8 MB (93781469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939f9b59dcc310bae2886a3e5b887d515998e62f1a67fc9485867652470543d7`  
		Last Modified: Fri, 10 Apr 2026 00:54:20 GMT  
		Size: 22.4 MB (22391662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0880bb9273b3389fbaca34c3c3adafdeb8f78b6f06f93cb5c2e28b9544746`  
		Last Modified: Fri, 10 Apr 2026 00:54:19 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7ed19e2a8c8930045aed379951930b0d583eeca80929513eb43ef936e60997`  
		Last Modified: Fri, 10 Apr 2026 00:54:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b8b6152cd97e2f5e3721864def283f760cf702d51bac877282633fe34c08cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681d7e7ec96508188344480fd45e483d209c0039c1c30bbd01a8eef433fd4b87`

```dockerfile
```

-	Layers:
	-	`sha256:b215aa3f859a8f1df366394dd4f9bf8535c0754f77f52c023dbf3a612142d3c0`  
		Last Modified: Fri, 10 Apr 2026 00:54:19 GMT  
		Size: 3.8 MB (3765967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d8701b0d35b6b103f1d50cc7ef85d59e76b5de417b4888a9691e5214a70810`  
		Last Modified: Fri, 10 Apr 2026 00:54:18 GMT  
		Size: 18.4 KB (18388 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:faa0be72236dd022eaf7effce761edb2943280de5bb48c68ae98d8f8fd5f10d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167015066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cf2e35ad2188df968ae74079da7bb39c4ef4d07ff12d9f907fa57aa03f3365`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:49:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:49:16 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 12 Apr 2026 18:49:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 12 Apr 2026 18:49:16 GMT
WORKDIR /tmp
# Sun, 12 Apr 2026 18:50:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 12 Apr 2026 18:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 12 Apr 2026 18:50:52 GMT
ENV LEIN_ROOT=1
# Sun, 12 Apr 2026 18:51:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 12 Apr 2026 18:51:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 12 Apr 2026 18:51:09 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 12 Apr 2026 18:51:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90d8e4f2f94de58856173d1d55466c632c6602bdea8fc895ac0398eaddfdb2e`  
		Last Modified: Sun, 12 Apr 2026 18:55:02 GMT  
		Size: 93.0 MB (93008107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b3a94d1a516a768805de850d5d241b15b6eada228fc5d8c522dee91190b6d5`  
		Last Modified: Sun, 12 Apr 2026 18:54:51 GMT  
		Size: 21.7 MB (21696122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd1a929c001304dfe0b6707d24bb5e036bb7f33422a691f09b411abc1e0761`  
		Last Modified: Sun, 12 Apr 2026 18:54:46 GMT  
		Size: 4.5 MB (4517781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f1760391701a8960ed3c9970d25194c45217c2d95b05c29c94a409994bca6b`  
		Last Modified: Sun, 12 Apr 2026 18:54:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bb54a16e99dd58084a4fc68c9bcb1a76fe0ee470b88696a2e73963865184cab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3772532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cb391e9819af19d37b7512084922cdf47b1796f8877d1dfcda63ea900d8198`

```dockerfile
```

-	Layers:
	-	`sha256:bd4dda56697f6059c393b02570b7eff2b07094ada348c70674e7246f32089f3a`  
		Last Modified: Sun, 12 Apr 2026 18:54:45 GMT  
		Size: 3.8 MB (3754143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c11a38502021216aed16b5c47602ec51ea10f0de0ddb417c256382dfeb88fcd7`  
		Last Modified: Sun, 12 Apr 2026 18:54:44 GMT  
		Size: 18.4 KB (18389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:168ca716c3848d3287e2b25677fc96915337bd46e92af41e8318f10f7ba31af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166213208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12db328236e8004aaec428b29f7b91ad13d59c56fd93c7c4b9b95b85195336b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:44:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:44:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:44:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:44:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:44:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:44:06 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:44:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:44:19 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:44:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:44:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:44:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:44:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e10aa2a41f6d7f1d361656c178853889e3348a51d3a809aed5aeaabd70ff55`  
		Last Modified: Thu, 09 Apr 2026 23:44:48 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002a835553d257ad36383051fdc666a663ce06347df27ad0bd20d70f58af40b`  
		Last Modified: Thu, 09 Apr 2026 23:44:47 GMT  
		Size: 21.8 MB (21782250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db2c551e286858f51f8e9b7945d30b3bab5e1e1a67ac6800004a30ec5ed9e3c`  
		Last Modified: Thu, 09 Apr 2026 23:44:47 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7922f910b6838b0cbe8f35f1203acff61de1fbeb75859a6d5b570b6e47d43af5`  
		Last Modified: Thu, 09 Apr 2026 23:44:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:810b92284b6d9bfbe2390325684f4c06cfcb63133b32a8a60cbd312a0d6c8cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0c64796fe5b13028c1b4315333edc2f77311bcd391139ea973edc2d3d97049`

```dockerfile
```

-	Layers:
	-	`sha256:7916d76560dcba11fe1bfefacbbfb777131a4e5628e5430f91d12970f2b49d63`  
		Last Modified: Thu, 09 Apr 2026 23:44:46 GMT  
		Size: 3.8 MB (3762644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7970446dcb35e76630c42550b2a1742145b5fd16e20abe363397da86338aa4`  
		Last Modified: Thu, 09 Apr 2026 23:44:46 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json
