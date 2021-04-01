## `clojure:openjdk-15-boot-2.8.3-buster`

```console
$ docker pull clojure@sha256:8728323b9d6928f90928181afd057ed7dd69a7f8861d67a3741ab405a1943298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-15-boot-2.8.3-buster` - linux; amd64

```console
$ docker pull clojure@sha256:dccbc8cb2c7e08053b2e232aeae6cf193a673342b565698a366f84ca2c041961
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.8 MB (388758074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbe5057b3ea395c5bc6a9a835e9a149a6aa306126cf656ca02d99d003ad59f4`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:16 GMT
ADD file:c254898ceb4172f05cd40460f8d0b1ca2d39d5178bdddd4e794c7d3fc5a60a03 in / 
# Tue, 30 Mar 2021 21:49:16 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:03:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:03:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:40:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:43:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-15
# Wed, 31 Mar 2021 05:43:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 31 Mar 2021 05:43:05 GMT
ENV PATH=/usr/local/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Mar 2021 05:43:05 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:43:05 GMT
ENV JAVA_VERSION=15.0.2
# Wed, 31 Mar 2021 05:43:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='91ac6fc353b6bf39d995572b700e37a20e119a87034eeb939a6f24356fbcd207'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='3958f01858f9290c48c23e7804a0af3624e8eca6749b085c425df4c4f2f7dcbc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 31 Mar 2021 05:43:24 GMT
CMD ["jshell"]
# Thu, 01 Apr 2021 01:45:05 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Apr 2021 01:45:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Apr 2021 01:45:05 GMT
WORKDIR /tmp
# Thu, 01 Apr 2021 01:45:07 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Thu, 01 Apr 2021 01:45:07 GMT
ENV PATH=/usr/local/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Apr 2021 01:45:08 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Apr 2021 01:45:37 GMT
RUN boot
# Thu, 01 Apr 2021 01:45:37 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:004f1eed87df3f75f5e2a1a649fa7edd7f713d1300532fd0909bb39cd48437d7`  
		Last Modified: Tue, 30 Mar 2021 21:53:41 GMT  
		Size: 50.4 MB (50432842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6f1e8117dbb1c6a57603cb4f321a861a08105a81bcc6b01b0ec2b78c8523a5`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 7.8 MB (7832608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c2faf66abec3dce9f54d6722ff592fce6dd4fb58a0d0b72282936c6598a3b3`  
		Last Modified: Tue, 30 Mar 2021 23:14:05 GMT  
		Size: 10.0 MB (9997208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234b70d0479d7f16d7ee8d04e4ffdacc57d7d14313faf59d332f18b2e9418743`  
		Last Modified: Tue, 30 Mar 2021 23:14:37 GMT  
		Size: 51.8 MB (51840782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba3dff9f19003d9bccdb99aff6591b545b6bfd1c7dd7bd791f8c695f45339ce`  
		Last Modified: Wed, 31 Mar 2021 05:51:50 GMT  
		Size: 13.9 MB (13921332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4bab4375f51030100958789eaea86b3ceb995712705a5f729ccfff9ec3c745`  
		Last Modified: Wed, 31 Mar 2021 05:55:46 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b7ad83a03b6f76bea7ed37bbab65251695408322ec25aba4bd7f6895ef18c`  
		Last Modified: Wed, 31 Mar 2021 05:56:08 GMT  
		Size: 195.9 MB (195905676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d95da107b0065407786bd037c261f80d1a2b77e3605c62f44756651b35bc6ae`  
		Last Modified: Thu, 01 Apr 2021 02:03:55 GMT  
		Size: 6.9 KB (6921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6751fe7417f2d0776cc994c07fae85d161b83ae59e2598fd09fd3190d0ce4d0b`  
		Last Modified: Thu, 01 Apr 2021 02:04:01 GMT  
		Size: 58.8 MB (58820496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-15-boot-2.8.3-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77fd45e2382bc1067822bf7d4667bc91edfd56b855d4b8700e8e15ea7966735a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.5 MB (367542364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59673660016c325a89b502a8a3ba24fbd9ca42ddf3eabe2b4648365c1fd3e211`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 26 Mar 2021 15:41:27 GMT
ADD file:536306ac674764a6a921b71adcbb4440797b916a0583b9270cd1565d62642e4d in / 
# Fri, 26 Mar 2021 15:41:30 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:14:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:14:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 04:15:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 10:40:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 10:42:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-15
# Sat, 27 Mar 2021 10:42:29 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 27 Mar 2021 10:42:29 GMT
ENV PATH=/usr/local/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 27 Mar 2021 10:42:30 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 10:42:31 GMT
ENV JAVA_VERSION=15.0.2
# Sat, 27 Mar 2021 10:42:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='91ac6fc353b6bf39d995572b700e37a20e119a87034eeb939a6f24356fbcd207'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk15.0.2/0d1cfde4252546c6931946de8db48ee2/7/GPL/openjdk-15.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='3958f01858f9290c48c23e7804a0af3624e8eca6749b085c425df4c4f2f7dcbc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 27 Mar 2021 10:42:48 GMT
CMD ["jshell"]
# Sat, 27 Mar 2021 10:58:01 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 27 Mar 2021 10:58:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 27 Mar 2021 10:58:03 GMT
WORKDIR /tmp
# Sat, 27 Mar 2021 10:58:05 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Sat, 27 Mar 2021 10:58:06 GMT
ENV PATH=/usr/local/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 27 Mar 2021 10:58:07 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 27 Mar 2021 10:58:35 GMT
RUN boot
# Sat, 27 Mar 2021 10:58:36 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:383261dafcc4f63ecae5f2d661d1ef8d0a5e1c9f4b1f12285115baca7d101d5a`  
		Last Modified: Fri, 26 Mar 2021 15:48:21 GMT  
		Size: 49.2 MB (49196215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8073d5d993eeeb13d2b5798a56220bed01add2f8e543d1a68cf5bdeb13b3a`  
		Last Modified: Sat, 27 Mar 2021 04:28:03 GMT  
		Size: 7.7 MB (7694449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e04ac5d1463667a0a3b2db65c9975df4dda175b8d5442808d4b141537d5531`  
		Last Modified: Sat, 27 Mar 2021 04:28:03 GMT  
		Size: 10.0 MB (9984376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be813e6ab58661299ea055f3b4c3080523e549d0874073a5c2699c5a33082d44`  
		Last Modified: Sat, 27 Mar 2021 04:28:24 GMT  
		Size: 52.2 MB (52164238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85f50a75c08118e9b37706bdc185926125ed245c576dceff4410e77ce5c4265`  
		Last Modified: Sat, 27 Mar 2021 10:46:52 GMT  
		Size: 14.7 MB (14673571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a022af465ea55e285fb9ac3bc53fb34c36fea0bdeb88a2c9ed38ef9610c4d381`  
		Last Modified: Sat, 27 Mar 2021 10:48:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84ba3e84552b25168dcf500e28f059f3d61a8a8c3abd10c1a426719b33630f0`  
		Last Modified: Sat, 27 Mar 2021 10:48:49 GMT  
		Size: 175.0 MB (175002166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b69641ce19c94e3afd5b92393725d0dda0f6d8c9dac0ef6ff788a93e2c9c6d3`  
		Last Modified: Sat, 27 Mar 2021 11:07:47 GMT  
		Size: 6.9 KB (6920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c724cbec2288ab360494bc29ee1a9934f1283fb7a40a4cba102b94bf611fdd5f`  
		Last Modified: Sat, 27 Mar 2021 11:07:53 GMT  
		Size: 58.8 MB (58820216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
