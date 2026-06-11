## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:3813c331b6b24b1c7b9879bd001fa89a879ce6cc7080944b279da4e1563d5ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:92023b43a6b7d9d901856c3b05e9c179f6b0081dc86823145ff02a40ce442997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105950061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79919800b37a3c8621815f3ce511186477aeac53a78a2f3b8fd15562fcfbcab`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:16:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:16:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:16:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:16:01 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:16:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:16:01 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:16:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:16:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:16:22 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:16:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:16:23 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe6547f42a64279074ac2ff0a6bdfb75cc700d15c0212ef99de77ce645184e`  
		Last Modified: Thu, 11 Jun 2026 01:16:37 GMT  
		Size: 55.2 MB (55198725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9086a20039066a2aba4bf3f2a85c49365383426b23752fde80bfb4486083bad`  
		Last Modified: Thu, 11 Jun 2026 01:16:36 GMT  
		Size: 16.4 MB (16448174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa4153efeec8cab44cd47113f1182c27cdc90e1a09f80163688c4710e980fc3`  
		Last Modified: Thu, 11 Jun 2026 01:16:35 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bcebe8f5e0f5a2355edc0e7bf93436d957905469df5bba0eb3ebb41b7ba35af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830774df4d3c492df1b7b20ef46879c73786c71c324c6b253f77adb72aa3c526`

```dockerfile
```

-	Layers:
	-	`sha256:d34c12247d388d680a75ce6c372ad4779a262cf89b2d2fdb9f51e008d3e9c3e6`  
		Last Modified: Thu, 11 Jun 2026 01:16:35 GMT  
		Size: 2.5 MB (2485819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72686b2be996f0ed11d2c2af87d46b5ef5edd740d2f0f27c072a1db5389f2fb2`  
		Last Modified: Thu, 11 Jun 2026 01:16:35 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:28c831467968060730ec7cb7d63c13f65f65c005a55a6cbe42d90133db303020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105353437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef5f41620f9266026c968135a0d8ab7240fee886f4aa042845610627eea95e9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:02 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:20:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:20:02 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:20:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:20:19 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:20:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:20:21 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f46937d4c333cac54de2b567124c6611ca0cd80e3e0875d3a5b27805ea807`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f385ed67a443d64f32255fd99b7220ff2f0e53be250ad5cd82eb3700c65797`  
		Last Modified: Thu, 11 Jun 2026 01:20:33 GMT  
		Size: 16.4 MB (16414197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3342c4b03b094ae44f61f04762621bb7e5ce42d76e01a884606e4b6f1436074`  
		Last Modified: Thu, 11 Jun 2026 01:20:32 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:91e8e65d9ef07d6664c0b48e51fea75362ac7fe7d5485e440ddc43f25c245fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4c5e058085e71fa718476a8fe94bec9963db55fa9fcf10015e86f7da7e5d2a`

```dockerfile
```

-	Layers:
	-	`sha256:b9cac2f812cecaa4629015607afad1f6f17ece3cdc0cb152cd19e79106eb2836`  
		Last Modified: Thu, 11 Jun 2026 01:20:32 GMT  
		Size: 2.5 MB (2486129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df0ce8656650829828347a6c15feeef9d507092d8d9b6693b0b28c4da3779b6`  
		Last Modified: Thu, 11 Jun 2026 01:20:32 GMT  
		Size: 16.7 KB (16657 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:02368729b7b559d9c8cb371449e52f100f1a3239006011d8d2b4c38261ea2cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107273397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd24fb9f7f034ebbcf314cc0bf0d0d126b9c9e04a6879cfe1dda859b580a8037`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:44:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:44:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:44:26 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:44:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:44:26 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:44:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:44:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:44:55 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:45:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:45:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c11b5f3a4a015128bca89c0e32301100f65c70ad718542cfa4e67c2e91aa807`  
		Last Modified: Wed, 20 May 2026 05:45:25 GMT  
		Size: 52.7 MB (52669123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dab618c4bb14005cb5841ee017715ed17a26f612ad8caa98f5686d2724f9c73`  
		Last Modified: Wed, 20 May 2026 05:45:24 GMT  
		Size: 16.5 MB (16486022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e986400444a8818caeeba69db526eba9668e94ddb2a600d0572bf0eb95a64d`  
		Last Modified: Wed, 20 May 2026 05:45:23 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:534f532d88b53ba1ce12d91d8efe99fbbc5e2e6d12ccfd07930942c7651f0b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8129e85e46a987cdf648a62e66f9b49cc4d758f20eca8023201189f3ba87d9a7`

```dockerfile
```

-	Layers:
	-	`sha256:fe7a4d1b0f1e344688bc0044fc37c4ac1d7f3d19deb370ae8e794db18c0a1ba9`  
		Last Modified: Wed, 20 May 2026 05:45:23 GMT  
		Size: 2.5 MB (2487394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dd6044de36861d2eff1f3ce836cd2e13139651398bffe228d35d5276b0096f8`  
		Last Modified: Wed, 20 May 2026 05:45:23 GMT  
		Size: 16.6 KB (16580 bytes)  
		MIME: application/vnd.in-toto+json
