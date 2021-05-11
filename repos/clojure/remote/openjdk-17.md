## `clojure:openjdk-17`

```console
$ docker pull clojure@sha256:69102af7e84d9e69a5b7013b8ec0ad924a44bd50e6a546c401cb388ad9d35e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17` - linux; amd64

```console
$ docker pull clojure@sha256:aad9cd469fd95b4902290cb54709affc59995e9490606f8d4a0a3663c4d3b344
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232816443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92f85180d281984227561f66ff3e06d2252a015db464cf3f8c5b06e7938d04d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:44:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 12:44:50 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 12:44:51 GMT
ENV LANG=C.UTF-8
# Tue, 11 May 2021 00:15:34 GMT
ENV JAVA_VERSION=17-ea+21
# Tue, 11 May 2021 00:15:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2a923efe7bd6c682d5550551a16dadfe8057b0106e0b4b4aad2aa56b8bed4c19'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb389fe6915c9e70e639db6ab630342a5ccc275f5a06aaded43321eeea9ba6ee'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 May 2021 00:15:53 GMT
CMD ["jshell"]
# Tue, 11 May 2021 01:28:15 GMT
ENV LEIN_VERSION=2.9.6
# Tue, 11 May 2021 01:28:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 11 May 2021 01:28:16 GMT
WORKDIR /tmp
# Tue, 11 May 2021 01:28:28 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 11 May 2021 01:28:28 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 11 May 2021 01:28:28 GMT
ENV LEIN_ROOT=1
# Tue, 11 May 2021 01:28:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 11 May 2021 01:28:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf4c47c8c6124c3089f3ed26410da9870ba18dd4bc68331e2b7e853116a6cad`  
		Last Modified: Sat, 10 Apr 2021 12:54:28 GMT  
		Size: 3.3 MB (3268764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb80c72a96b420bbf07f0cdaeaaab1859c2f04cec313dc4312e8107eca41433`  
		Last Modified: Tue, 11 May 2021 00:23:07 GMT  
		Size: 186.4 MB (186401638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af4d07660f4909fb6e685ef2c29608248f8473f2410c014575270ab79edf721`  
		Last Modified: Tue, 11 May 2021 01:33:15 GMT  
		Size: 11.8 MB (11802974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b18a5493fd1bbd0eb7989fbf7143913d9cdaf7d16ca51b2412a471254d37d8`  
		Last Modified: Tue, 11 May 2021 01:33:15 GMT  
		Size: 4.2 MB (4203694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7ed51e7e5ab5e13d970692931ad68e181f59ae003aaf92ee74e53f64bc309f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227511974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c10647a79f497e5ea1085974007b03ef0a1536dda6781632b0452e3a38631b1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:25 GMT
ADD file:b24da7eb23eeae04e00d0e45da29a89fe8f992e8dcf4ba482afb907b8015b7bf in / 
# Sat, 10 Apr 2021 00:41:28 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:31:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 01:31:15 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 01:31:16 GMT
ENV LANG=C.UTF-8
# Tue, 11 May 2021 01:46:12 GMT
ENV JAVA_VERSION=17-ea+21
# Tue, 11 May 2021 01:46:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2a923efe7bd6c682d5550551a16dadfe8057b0106e0b4b4aad2aa56b8bed4c19'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb389fe6915c9e70e639db6ab630342a5ccc275f5a06aaded43321eeea9ba6ee'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 May 2021 01:46:41 GMT
CMD ["jshell"]
# Tue, 11 May 2021 02:39:00 GMT
ENV LEIN_VERSION=2.9.6
# Tue, 11 May 2021 02:39:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 11 May 2021 02:39:02 GMT
WORKDIR /tmp
# Tue, 11 May 2021 02:39:22 GMT
RUN apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "094b58e2b13b42156aaf7d443ed5f6665aee27529d9512f8d7282baa3cc01429 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 11 May 2021 02:39:23 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 11 May 2021 02:39:23 GMT
ENV LEIN_ROOT=1
# Tue, 11 May 2021 02:39:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 11 May 2021 02:39:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:15cb40b9c4df1a06940dc2a154c3be46844241235c1a091afa70da0ee2dc811a`  
		Last Modified: Sat, 10 Apr 2021 00:47:53 GMT  
		Size: 25.9 MB (25904582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ed82b9f1018dd9b8a3d8ed771ba8773bd33481ce655abab47d10bd3034f05`  
		Last Modified: Sat, 10 Apr 2021 01:37:31 GMT  
		Size: 3.1 MB (3118914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11d8fd64baec0ee00d154286dee2bd77466e042e6aab4916de26401821337c8`  
		Last Modified: Tue, 11 May 2021 01:53:12 GMT  
		Size: 182.5 MB (182481831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dc224fa88bc0e7f340589028a455c950379a8921f6c547723a480c6cc9b12e`  
		Last Modified: Tue, 11 May 2021 02:44:43 GMT  
		Size: 11.8 MB (11802937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb6fe90d1affadbac5f01d12627ed118cb8c0caeddcea4e87ab409f664c86e`  
		Last Modified: Tue, 11 May 2021 02:44:43 GMT  
		Size: 4.2 MB (4203710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
