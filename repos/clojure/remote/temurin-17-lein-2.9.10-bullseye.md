## `clojure:temurin-17-lein-2.9.10-bullseye`

```console
$ docker pull clojure@sha256:129a7d645d0374aca9d569fa16fd12493d67ba59ed92bd81c2743decb321cb46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.9.10-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b3213a495b78af6fc902f807c5bf6e2a375d94ea6e093dbfcaa460051a4e6e0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265849058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430b6052a6183db353d1c89f33e44a74ffcc702d3d63de68fed086d559df8988`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:02 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:56:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:57:47 GMT
ENV LEIN_VERSION=2.9.10
# Thu, 06 Oct 2022 03:57:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 03:57:47 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:58:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 06 Oct 2022 03:58:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 03:58:03 GMT
ENV LEIN_ROOT=1
# Thu, 06 Oct 2022 03:58:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 06 Oct 2022 03:58:07 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 03:58:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 03:58:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9acfce48843835d39fb569ba75ae523857fdae8d21d473e9152a27cb419979f2`  
		Last Modified: Thu, 06 Oct 2022 04:12:08 GMT  
		Size: 192.1 MB (192137601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e3ca94fd3929c9d502fd9048d1641f85bf06879afe14dc275aad42a5295839`  
		Last Modified: Thu, 06 Oct 2022 04:13:29 GMT  
		Size: 14.3 MB (14266112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fee61bd5b0aac2487a358fd0d796d18f59533a8470f28dc6ad7b9cad68b1b9`  
		Last Modified: Thu, 06 Oct 2022 04:13:28 GMT  
		Size: 4.4 MB (4398697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30f4faa861562e76dec968b982c8adfee187842eb6374877d781db80c39d0ed`  
		Last Modified: Thu, 06 Oct 2022 04:13:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7ae18272ea86d7cb46387afaa10560b923ab00870cefe4deff093120e490e85c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263052171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da02da3fcf1cdb7ca5737babb8067ea0a72908892f2de4513910261305ded0cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:38:34 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:38:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:41:09 GMT
ENV LEIN_VERSION=2.9.10
# Thu, 06 Oct 2022 02:41:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:41:11 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:41:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 06 Oct 2022 02:41:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:41:38 GMT
ENV LEIN_ROOT=1
# Thu, 06 Oct 2022 02:41:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 06 Oct 2022 02:41:43 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:41:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:41:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b7798e9e43d2494af502b188de7bd161f67c7162a0b931a6e81e4e8d7c52d5`  
		Last Modified: Thu, 06 Oct 2022 03:01:09 GMT  
		Size: 190.9 MB (190904332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c956d956e7acdc58672ffff760f044ae67d63949cae007700c70a1e8dfba0a2`  
		Last Modified: Thu, 06 Oct 2022 03:02:42 GMT  
		Size: 14.0 MB (14048212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755e8e535b3bf461295e49e146db00c917f48df8cb038e1d647e3722a70a2c9`  
		Last Modified: Thu, 06 Oct 2022 03:02:41 GMT  
		Size: 4.4 MB (4398602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15322cfc3a8af07744c034067e1c0ead13a43a95e544b51bb607dc9c5d03ddb4`  
		Last Modified: Thu, 06 Oct 2022 03:02:41 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
