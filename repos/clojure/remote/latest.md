## `clojure:latest`

```console
$ docker pull clojure@sha256:f0bc76fb87a67c31a4d0ead9521eddc468909a412a17821adb4b9dd42e0939a6
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:3d2f8eb9a4232f334d89c40cd82c17f15a1f066a270d041deab3969705dfe91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240482307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dc5e2f73dd659216dc820fee88e8c9c152020b0a3d796d12f477b2090f6f20`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:13:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:13:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:13:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:13:29 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:13:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:13:29 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:13:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:13:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:13:43 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:13:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:13:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:13:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:13:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:13:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:13:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:13:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:13:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dde5154ff6f9404dc9f4dae1959727a8df5f7feb8cccab0852a55758b8db37c`  
		Last Modified: Fri, 08 May 2026 20:14:24 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d38283795261d15afbb8a001c441ab4b1ee32ba0db5123689c94d7ab327813`  
		Last Modified: Fri, 08 May 2026 20:14:20 GMT  
		Size: 19.8 MB (19806500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be459086f6bb14d4b8ea705fd94f30b31742ea7627589557c415d4c72267033`  
		Last Modified: Fri, 08 May 2026 20:14:19 GMT  
		Size: 4.5 MB (4517699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a998316166df8df16724736fd7bb251af941e0fc6c1dda536d414cd7f8fc923e`  
		Last Modified: Fri, 08 May 2026 20:14:24 GMT  
		Size: 75.1 MB (75093759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0780801d656dd0428a9b100f266be63e3320fffd9b6fc6b77a75b9af4ee729a`  
		Last Modified: Fri, 08 May 2026 20:14:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8ad62c1e6f56aa892fb35c7de26c72bae43aa50489df15f3c8328e8fe18a5e`  
		Last Modified: Fri, 08 May 2026 20:14:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:741c70416ee19a3b128a809aa0036050347bd677c512c7d83187bcefb4ee4055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7465257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeb03a63dddc611706758c281f9838402fc3a89928ddcbc52700cfb4b63c946`

```dockerfile
```

-	Layers:
	-	`sha256:6521cdafcc0315ee92bde9356545b4fe966ffdb15f8c9b025ce3332adab532e5`  
		Last Modified: Fri, 08 May 2026 20:14:19 GMT  
		Size: 7.4 MB (7439494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b47ecf195862266b55eb7c7bbda451ebd53dca3fb2f47ddd249e6417f4b56b25`  
		Last Modified: Fri, 08 May 2026 20:14:18 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:392c9efd70937b7599b1555ee20e0e4bb812c8969f9cc21df42482dfa3d3f9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239322388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991889cbca512bcfc9bf0b2586e8ba517cd818b1cde07062244de451c8b706d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:17:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:45 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:17:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:17:45 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:17:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:17:59 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:18:01 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:18:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:18:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b6b4fb26512e7dd289501c7d2f89f88e159b255cbdc4b27eee306610fb9f3`  
		Last Modified: Fri, 08 May 2026 20:18:36 GMT  
		Size: 91.5 MB (91542295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55eb5dfe04194ab7ce232d777fa4e8fa8c3b888478998705448dfb8dcd87aa7`  
		Last Modified: Fri, 08 May 2026 20:18:33 GMT  
		Size: 19.6 MB (19637032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173f6ac006b3788630736f4dab9e86f6771639515ac049b6aa3703f9b5e0ebbf`  
		Last Modified: Fri, 08 May 2026 20:18:32 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca92cf8459b4bc0d86bb958f5f401cc418d064c1d94abeec48498c9acdfcbda3`  
		Last Modified: Fri, 08 May 2026 20:18:36 GMT  
		Size: 75.3 MB (75251118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fd3d24dcf9512bb38de249164a65095ac8b3116605e13277ec3452f2e968ff`  
		Last Modified: Fri, 08 May 2026 20:18:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2fb6b71eb0cc76dc304bffde751cb853c6cbcbc774f9a9241da8bb621ee4c1`  
		Last Modified: Fri, 08 May 2026 20:18:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:bb309993ed7721680f20aa370893aeaf8ac5d522f41e98ff90ba6f415719682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7471117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1be6c1ccf10b2b01fa80a91c09496985ade8a9d29e9124fb432a70978e465b`

```dockerfile
```

-	Layers:
	-	`sha256:eb3607a24d647a2e9b9240e3057243015d9accb93027f808b171b5f05d85bb85`  
		Last Modified: Fri, 08 May 2026 20:18:33 GMT  
		Size: 7.4 MB (7445230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8578f0481e2ebb2397979dc5634fd54a2b9c7d169235e155f252c5ec73a9f16c`  
		Last Modified: Fri, 08 May 2026 20:18:32 GMT  
		Size: 25.9 KB (25887 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:bac74d9beb15912ea15cedaa5273b8201fc6d0ec8a10e72c1eac894f18b29760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249493758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce986f60b2ccc277b9d228a4fdb94a4dbb0e0f4c90c3f8042b4e673d281c9534`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:18:51 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:18:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:18:51 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:19:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:19:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:19:17 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:19:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:19:21 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:19:22 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:19:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:19:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:19:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:19:50 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:19:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de956b7a11284f1a158aa4d174299365ba072baa5eadc5c41d537c7ba7509c`  
		Last Modified: Sat, 09 May 2026 02:20:31 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7c27935ce89344c9f2063adaf35463730e2c3db3cda2b4435240ccf8a48f5f`  
		Last Modified: Sat, 09 May 2026 02:20:28 GMT  
		Size: 20.0 MB (20030513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8435cb421dfc3e57ae86315bbfd20609e9a621d5a198bd965880b6dcdf4018b5`  
		Last Modified: Sat, 09 May 2026 02:20:27 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5dbea45c4d4d827dcba45069427d81ddd84913a406f73f5e40e64971549b4`  
		Last Modified: Sat, 09 May 2026 02:20:31 GMT  
		Size: 80.7 MB (80693612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58491fb8ae988a9157e5dd0210c05d27b78931e804a0006443302cb8e6c3ff8`  
		Last Modified: Sat, 09 May 2026 02:20:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f825b6dfc22e7edf2ace3a77b03b36d5898140bc3c439f12ebfa1025e182b8`  
		Last Modified: Sat, 09 May 2026 02:20:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:91ec5b368ab460c1e0fd5388490f915b345a8ae57ccb966ec5b0db81779ed13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025596a2243574b637b025ce9878f141535b0e52e38b01bef76518aafd699df1`

```dockerfile
```

-	Layers:
	-	`sha256:4da794caf26bd2aa36d18655f561ad22433f6c2d38195c0d53ca66d83a4a11ea`  
		Last Modified: Sat, 09 May 2026 02:20:27 GMT  
		Size: 7.4 MB (7428010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b222ebad68a5c3e6089ea13f53d6f99735e874c0a14475dc8f9613f1ef488795`  
		Last Modified: Sat, 09 May 2026 02:20:26 GMT  
		Size: 25.8 KB (25803 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:fca7fe821fbec8e78f78265e689b5fe0e892c9ae5a7a116020e603ea8932f0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233794223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2526d80c3bcbefadc9e9dfdfc20aa437dbc777c8cc6ae404cf82764765d0f8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:12:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:12:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:12:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:12:41 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:12:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:12:41 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:12:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:12:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:12:52 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:12:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:12:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:12:55 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:13:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:13:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:13:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:13:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:13:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a188a913daf22f341771db62166f6bc3f7d8f891104f744dec07784a901e7ce`  
		Last Modified: Fri, 08 May 2026 22:13:43 GMT  
		Size: 88.4 MB (88420321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c733194e0e799c2d764ce0d3324ff52913e41da44cadaa52465ce4b5e3a48d07`  
		Last Modified: Fri, 08 May 2026 22:13:41 GMT  
		Size: 19.5 MB (19466774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b715cf92e86d57654fdb72c5429f6d5c3378402893f9eca8a1f6b31bfe815fb`  
		Last Modified: Fri, 08 May 2026 22:13:41 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455d701c02321988aba691a157af1f504b0d55c0057496c1d0e1623422181a8`  
		Last Modified: Fri, 08 May 2026 22:13:43 GMT  
		Size: 74.2 MB (74240290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3ed661c85209ac9d92d8ba4997e2cda58a42535106fb9313f503c04a418f6e`  
		Last Modified: Fri, 08 May 2026 22:13:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82314db1d4803737b240cf293b9c0c665db1ea038dade0ebcb05bac33edb163c`  
		Last Modified: Fri, 08 May 2026 22:13:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:e971b1490ea54cab5377d036d6b461965c9a253607b4f6dc58bfca7fb033a5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68b90517caf2bc7f04f85f826972f86fb6ac095c05054e927544839ef55a40d`

```dockerfile
```

-	Layers:
	-	`sha256:1fd6af8e3ba0c1c1af295d3aec425ea4bb8fcc0b39defa26594ee83fef09aa00`  
		Last Modified: Fri, 08 May 2026 22:13:41 GMT  
		Size: 7.4 MB (7415375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:083e6637acd0e6ed26d8b2e3f428ab399c67a969d757b496a6d969cb49a3f404`  
		Last Modified: Fri, 08 May 2026 22:13:40 GMT  
		Size: 25.8 KB (25763 bytes)  
		MIME: application/vnd.in-toto+json
