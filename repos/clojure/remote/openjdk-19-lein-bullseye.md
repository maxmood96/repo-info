## `clojure:openjdk-19-lein-bullseye`

```console
$ docker pull clojure@sha256:7d46b263cef2b3c7672e2db7a275160b1ee8cf323998edf022c1137ffd91e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6d2eb5536706a5bc9a1dff6b70d23b55087ebd35ce742834db181091a89454d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349579614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405788ecfea135ed8b15ce7bfc2bea93274111144fb7aa116f57be85ba272d40`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:26:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:20:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:20:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 14:20:32 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 14:20:32 GMT
ENV LANG=C.UTF-8
# Mon, 14 Mar 2022 20:14:38 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 20:14:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 20:14:49 GMT
CMD ["jshell"]
# Mon, 14 Mar 2022 20:44:45 GMT
ENV LEIN_VERSION=2.9.8
# Mon, 14 Mar 2022 20:44:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 14 Mar 2022 20:44:45 GMT
WORKDIR /tmp
# Mon, 14 Mar 2022 20:44:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg
# Mon, 14 Mar 2022 20:44:52 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Mar 2022 20:44:52 GMT
ENV LEIN_ROOT=1
# Mon, 14 Mar 2022 20:44:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Mon, 14 Mar 2022 20:44:55 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Mon, 14 Mar 2022 20:44:55 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Mar 2022 20:44:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12de8c754e45686ace9e25d11bee372b070eed5b5ab20aa3b4fab8c936496d02`  
		Last Modified: Tue, 01 Mar 2022 06:36:38 GMT  
		Size: 54.6 MB (54575903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00199018d51876dde0db2a50f86b4db2ce5eaebcf284907dca80a8af67765bda`  
		Last Modified: Tue, 01 Mar 2022 14:40:10 GMT  
		Size: 14.1 MB (14071739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1ed8c70503e06348b37925dfbb45f52bfbee048d716f08cd6f53587b1ffffe`  
		Last Modified: Mon, 14 Mar 2022 20:23:00 GMT  
		Size: 193.2 MB (193188186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072efa9cd653d58f91d2dad9efc4ae09671bbad5f39a9e17e441c1606fae2c93`  
		Last Modified: Mon, 14 Mar 2022 20:51:29 GMT  
		Size: 12.6 MB (12594176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127c14dfbfe7abc70f3c4c0e4c5b928de7394b6e36dcf8c579cecc247691006`  
		Last Modified: Mon, 14 Mar 2022 20:51:29 GMT  
		Size: 4.2 MB (4207224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da39c583b509680b043996d7183566d4771633030d0991a2984bf685232c1697`  
		Last Modified: Mon, 14 Mar 2022 20:51:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8918b6ac284936c5b6e9b795b396145e2ea7e636e6ddbeb558002f8da91a612b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348391528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66816c8f5718411badadab0785d2df95a7a5ec9284c8ec5d5a4e806aa0f184f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:12 GMT
ADD file:9d66afa8fc90803d689e087b38b38a3bd58d0434b495ca4165ca520e73bccf55 in / 
# Tue, 01 Mar 2022 02:11:14 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:34:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 10:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:47:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:47:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:47:34 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:47:35 GMT
ENV LANG=C.UTF-8
# Mon, 14 Mar 2022 19:05:38 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 19:05:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 19:05:48 GMT
CMD ["jshell"]
# Mon, 14 Mar 2022 19:57:22 GMT
ENV LEIN_VERSION=2.9.8
# Mon, 14 Mar 2022 19:57:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 14 Mar 2022 19:57:24 GMT
WORKDIR /tmp
# Mon, 14 Mar 2022 19:57:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "9952cba539cc6454c3b7385ebce57577087bf2b9001c3ab5c55d668d0aeff6e9 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg
# Mon, 14 Mar 2022 19:57:32 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Mar 2022 19:57:32 GMT
ENV LEIN_ROOT=1
# Mon, 14 Mar 2022 19:57:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.3"]])' > project.clj   && lein deps && rm project.clj
# Mon, 14 Mar 2022 19:57:37 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Mon, 14 Mar 2022 19:57:37 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Mar 2022 19:57:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c7869242ae9abf6340558e18846f64a05eb06f2eaf66c6bfa2dc66ff2c997976`  
		Last Modified: Tue, 01 Mar 2022 02:17:52 GMT  
		Size: 53.6 MB (53608753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9880592b351f34fa791bd7749a127063cd6a76b1190bd059c168696d700f6b04`  
		Last Modified: Tue, 01 Mar 2022 10:44:26 GMT  
		Size: 5.1 MB (5141642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd9934a374f1ba93d2da0983d2aac86c9b4bf6ca063aa108519d2588e0212ac`  
		Last Modified: Tue, 01 Mar 2022 10:44:26 GMT  
		Size: 10.7 MB (10655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37be3698694527b9e5af78494bbcb68f6b045af5247de8c988b24ef7dcd877e`  
		Last Modified: Tue, 01 Mar 2022 10:44:48 GMT  
		Size: 54.7 MB (54671139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5dc6dcc457fec75c4796decb43a2b4f5f0bfce35e577de9171e96fb39eeee4`  
		Last Modified: Tue, 01 Mar 2022 14:12:17 GMT  
		Size: 15.5 MB (15524992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8721790ef34835374c8cbfae43b79fcc71b5cba1dc6a16102e46ea0b431c5c`  
		Last Modified: Mon, 14 Mar 2022 19:20:01 GMT  
		Size: 192.2 MB (192228567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2025e4bfbc65f33902ee9b90c994ace18d69ff6442cec1f22f98befb419d0cfb`  
		Last Modified: Mon, 14 Mar 2022 20:07:48 GMT  
		Size: 12.4 MB (12353049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac24d8250a9dcda32bff9ef972ddd3a341a88d352c55764c999b76269859f2`  
		Last Modified: Mon, 14 Mar 2022 20:07:48 GMT  
		Size: 4.2 MB (4207118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96d20fe6a0d9c2162d6168be0e879ed4c1369756571b52b84b194db62d59f4e`  
		Last Modified: Mon, 14 Mar 2022 20:07:47 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
