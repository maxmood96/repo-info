## `clojure:latest`

```console
$ docker pull clojure@sha256:4b384ec08bad773b8d7ab4b0aea7dee8480a8c2d3d6c5aff9716259b27444f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:a6a43bca25a1a92d7c007dc0c056d307744b427498ab9989eb2bd1307facd404
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343198538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e93cc2aee65ec1c677ddb9ef27fba8de3b8867acb3630fd386908b4e901ab48`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:54:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 17 Aug 2021 06:54:45 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 17 Aug 2021 06:54:45 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:54:45 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:54:45 GMT
ENV JAVA_VERSION=11.0.12
# Tue, 17 Aug 2021 06:55:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 Aug 2021 06:55:08 GMT
CMD ["jshell"]
# Tue, 17 Aug 2021 18:29:33 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 17 Aug 2021 18:29:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 17 Aug 2021 18:29:33 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 18:29:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 17 Aug 2021 18:29:41 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Aug 2021 18:29:41 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 17 Aug 2021 18:30:29 GMT
RUN boot
# Tue, 17 Aug 2021 18:30:30 GMT
ENV LEIN_VERSION=2.9.6
# Tue, 17 Aug 2021 18:30:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Aug 2021 18:30:30 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 18:31:00 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 17 Aug 2021 18:31:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/:/usr/local/bin/
# Tue, 17 Aug 2021 18:31:00 GMT
ENV LEIN_ROOT=1
# Tue, 17 Aug 2021 18:31:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 17 Aug 2021 18:31:07 GMT
ENV CLOJURE_VERSION=1.10.3.943
# Tue, 17 Aug 2021 18:31:07 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 18:31:34 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "f1fdb786fa8b9ef3a08d0b331a51861cd5a6eea277e93bbad64bf37774df17c6 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 17 Aug 2021 18:31:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427b7134c0c7b2e1d9cc703e20a84b850cbbf34ef654cfa0db710678a99da78b`  
		Last Modified: Tue, 17 Aug 2021 07:00:00 GMT  
		Size: 3.3 MB (3268768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea848f5155d0f648fc7fd258de1ce56d16d1ab42c2745a55e8adf26f997b45b`  
		Last Modified: Tue, 17 Aug 2021 07:02:46 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0a59079bf8f55f7ca770b4e060d8f49a02723cde1616cdc7ea122832e46095`  
		Last Modified: Tue, 17 Aug 2021 07:03:02 GMT  
		Size: 203.4 MB (203396055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad8272c58b180735791c06527df99cf6fb8f427951544287a3f49150d52e84`  
		Last Modified: Tue, 17 Aug 2021 18:41:41 GMT  
		Size: 282.9 KB (282890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5552ccd928b241655b4a5c3b2f29a0ea7a497d97efdcb84516d170c9bc1bd1`  
		Last Modified: Tue, 17 Aug 2021 18:41:47 GMT  
		Size: 58.8 MB (58820839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61005ccba939ccdb7dafacee2423b3699cafe72822f051abceb85e6692c0b44`  
		Last Modified: Tue, 17 Aug 2021 18:41:43 GMT  
		Size: 11.8 MB (11799220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ed95c2963d0e587eb58f2c1e98d2cbaab8950c848e93bb9ae3cf1de1422548`  
		Last Modified: Tue, 17 Aug 2021 18:41:42 GMT  
		Size: 4.2 MB (4193900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f193673772b4b37c539891279c07fc9f5189b176fd4490810e19729f9c1207bc`  
		Last Modified: Tue, 17 Aug 2021 18:41:49 GMT  
		Size: 34.3 MB (34290669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ead44ad88430074903c62ac982b3edd22c81e315c5b0cc4174f968aaf04c9a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338907122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d53e44429d6eb21061fb8ef5824abc600d2f8377a280db569859f1457c1d406`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:04:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:06:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 17 Aug 2021 06:06:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 17 Aug 2021 06:06:39 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:06:40 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:06:40 GMT
ENV JAVA_VERSION=11.0.12
# Tue, 17 Aug 2021 06:07:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jdk_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 Aug 2021 06:07:10 GMT
CMD ["jshell"]
# Tue, 17 Aug 2021 15:08:07 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 17 Aug 2021 15:08:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 17 Aug 2021 15:08:07 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 15:08:12 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 17 Aug 2021 15:08:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Aug 2021 15:08:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 17 Aug 2021 15:08:54 GMT
RUN boot
# Tue, 17 Aug 2021 15:08:54 GMT
ENV LEIN_VERSION=2.9.6
# Tue, 17 Aug 2021 15:08:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Aug 2021 15:08:55 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 15:09:05 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 17 Aug 2021 15:09:05 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/:/usr/local/bin/
# Tue, 17 Aug 2021 15:09:05 GMT
ENV LEIN_ROOT=1
# Tue, 17 Aug 2021 15:09:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 17 Aug 2021 15:09:09 GMT
ENV CLOJURE_VERSION=1.10.3.943
# Tue, 17 Aug 2021 15:09:09 GMT
WORKDIR /tmp
# Tue, 17 Aug 2021 15:09:25 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "f1fdb786fa8b9ef3a08d0b331a51861cd5a6eea277e93bbad64bf37774df17c6 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 17 Aug 2021 15:09:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82a27af984eefbe6b82ccb775aead56e92f82cf16d079218087ebe132125cf5`  
		Last Modified: Tue, 17 Aug 2021 06:15:41 GMT  
		Size: 3.1 MB (3118861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d1ea50abf433035bb7f308b855f144aefbbe47ce996fb9e38d8db45df6f75a`  
		Last Modified: Tue, 17 Aug 2021 06:19:18 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5a1a4cff5dcebe7a1a147545a882689f77e5c9b229ad8dd0ad4ee9a302840c`  
		Last Modified: Tue, 17 Aug 2021 06:19:39 GMT  
		Size: 201.0 MB (200994727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817217c8c4e0bff742e611352aeb4ec69f0569e4baee7159795575336d0394f0`  
		Last Modified: Tue, 17 Aug 2021 15:19:37 GMT  
		Size: 282.6 KB (282642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3899c9ee5f86f56e790f1e180a58a92f1276afc82169e2220f6661a99e719fc4`  
		Last Modified: Tue, 17 Aug 2021 15:19:42 GMT  
		Size: 58.8 MB (58820866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362b8c8c86c64b0dc3e8a7ac4d0a4f8823f449e907d4eb1465ccb670d98a5d2a`  
		Last Modified: Tue, 17 Aug 2021 15:19:38 GMT  
		Size: 11.8 MB (11798975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42bb6ead2618685164543572afec8e257bf74c2fdff18341695fcba6f9ffe20`  
		Last Modified: Tue, 17 Aug 2021 15:19:38 GMT  
		Size: 4.2 MB (4193903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d2ebbfb674c57c4cee9c2b979feb9d3442767cd1a0a2570a34968e34af0786`  
		Last Modified: Tue, 17 Aug 2021 15:19:43 GMT  
		Size: 33.8 MB (33781865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
