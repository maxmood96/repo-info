## `clojure:openjdk-19-lein-2.9.8-slim-bullseye`

```console
$ docker pull clojure@sha256:3dd0d3f78d59e738c2c7835afbf8d86efc67055acdd245c7586f4048a79cd905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-lein-2.9.8-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:420baa5a59080ae82a38cf958f243567b4762e812d67f22d3d801e71c5e979b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242609929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244f51abe8d924bfab61926a08920143f4d7d42626d5166fbbc0bc3eeea8d0e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:52:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 29 Mar 2022 00:52:15 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:52:15 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:52:16 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:52:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='ac2dedbf7805d85112f20815eb381e1fec51c9d1057f6c0eaf1185ca9c1b2c5e'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/15/GPL/openjdk-19-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='039c2cdec816ea3afe5430f2b9bc74749b10b3372894a9d4098eabef60492a3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:52:29 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:51:32 GMT
ENV LEIN_VERSION=2.9.8
# Tue, 29 Mar 2022 23:51:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:51:32 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:51:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 29 Mar 2022 23:51:42 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:51:42 GMT
ENV LEIN_ROOT=1
# Tue, 29 Mar 2022 23:51:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 29 Mar 2022 23:51:46 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:51:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:51:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dc05f270bad654ee17f1143c48586c188a72929a128d61fd8ae15905d7b00`  
		Last Modified: Tue, 29 Mar 2022 01:04:32 GMT  
		Size: 1.6 MB (1582122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d100fc3e7b0dc5fbbf4534f7688cb06df0e07a6a9cdc51f10e7689f324fb53`  
		Last Modified: Tue, 29 Mar 2022 01:04:47 GMT  
		Size: 193.6 MB (193580462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7435cf11385fdd852b8d05fa42e91dc389ae828c8875efb0da3798b55e68793`  
		Last Modified: Wed, 30 Mar 2022 00:11:54 GMT  
		Size: 11.9 MB (11861312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93d1dbee748338645b11da8aa607c512b1d3b01180bb31e7bac1e0a99b63eea`  
		Last Modified: Wed, 30 Mar 2022 00:11:53 GMT  
		Size: 4.2 MB (4207171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b78aeb31ec425eeda7360ec8d2d30677793f513b8b0c17d1af0013ffa2a040`  
		Last Modified: Wed, 30 Mar 2022 00:11:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-lein-2.9.8-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43e32b3a929ec078ae9d5cf1c994385700eec1ced844d43f45a4f22b88b791ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239559575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7185741e1de387142c5493533440d6a92bd5d3988edc442a2f6d8612ef8ccb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 23:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:20:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 17 Mar 2022 23:20:25 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:20:26 GMT
ENV LANG=C.UTF-8
# Tue, 22 Mar 2022 10:03:48 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 10:04:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Mar 2022 10:04:03 GMT
CMD ["jshell"]
# Tue, 22 Mar 2022 11:48:55 GMT
ENV LEIN_VERSION=2.9.8
# Tue, 22 Mar 2022 11:48:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 22 Mar 2022 11:48:57 GMT
WORKDIR /tmp
# Tue, 22 Mar 2022 11:49:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 22 Mar 2022 11:49:08 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 22 Mar 2022 11:49:09 GMT
ENV LEIN_ROOT=1
# Tue, 22 Mar 2022 11:49:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 22 Mar 2022 11:49:15 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 22 Mar 2022 11:49:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 22 Mar 2022 11:49:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494f7f18e3d8fbed7417515196913f39c7c8b9fb93a63ebaa040b02f90ecde75`  
		Last Modified: Thu, 17 Mar 2022 23:47:05 GMT  
		Size: 1.4 MB (1361288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba04e38b91c9e0766a938bb44f843272845eee156dad1883f818fbc428967dc4`  
		Last Modified: Tue, 22 Mar 2022 10:18:49 GMT  
		Size: 192.3 MB (192282584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0170cbf2aad09bf1d8f006aa55429e9ebbef77962feb10ea054bfe33e73e1d29`  
		Last Modified: Tue, 22 Mar 2022 11:59:21 GMT  
		Size: 11.6 MB (11645194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a159ced07bdc48915ce856363eb5d947881f10e181cee5fcca22e229a691b73`  
		Last Modified: Tue, 22 Mar 2022 11:59:21 GMT  
		Size: 4.2 MB (4207092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62fc8c963b00797a4c907ce77dcf8fd5379582888d21658ade60a02d277b668`  
		Last Modified: Tue, 22 Mar 2022 11:59:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
