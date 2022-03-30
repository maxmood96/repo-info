## `clojure:openjdk-11-boot-slim-buster`

```console
$ docker pull clojure@sha256:ae3557e0ad3e9426e2912bb89248267bfd0a6e7de5fc298405e649c868b22395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-11-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:8411d2568aaa924a11bd0e8a11e99b63b7026ea906e4d59eaf9dad6f23123eb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293060530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aed01eae69b96afb9a502f979c388af6b09ca764b97b9358acdfa53cc93dc1e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 00:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 00:56:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 29 Mar 2022 00:56:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 29 Mar 2022 00:56:05 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:56:05 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 00:56:05 GMT
ENV JAVA_VERSION=11.0.14.1
# Tue, 29 Mar 2022 00:56:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:56:24 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:37:57 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 29 Mar 2022 23:37:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:37:57 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:38:02 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 29 Mar 2022 23:38:02 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:38:02 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 29 Mar 2022 23:38:45 GMT
RUN boot
# Tue, 29 Mar 2022 23:38:45 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a93b586a56127b277f2e371624af9ed70508966a2ca124e827d47b841391445`  
		Last Modified: Tue, 29 Mar 2022 01:05:57 GMT  
		Size: 3.3 MB (3273249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d51428d051968b1c99c379fe964adac3daa39cc473f48886ded32132df46dbd`  
		Last Modified: Tue, 29 Mar 2022 01:11:58 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56100c81830fad7644854e7121c88af397084788a639b44b7c35132545eb09c`  
		Last Modified: Tue, 29 Mar 2022 01:12:13 GMT  
		Size: 203.5 MB (203531498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff31142eb936e8d10330a24a875340774fedf87ff0f820a377ce0645034811b`  
		Last Modified: Tue, 29 Mar 2022 23:59:51 GMT  
		Size: 282.8 KB (282759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b953c0baaf8c744ca1c1932caae1d105b8acc3b8227619328952389ae1c98363`  
		Last Modified: Tue, 29 Mar 2022 23:59:54 GMT  
		Size: 58.8 MB (58820845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-11-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d681314a3e4423bc781caeaf901e71d2f1858ca196e571d1504bf868e2b90871
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288870454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a218aa3582c433b2637ddcd529a07af5df6b2810bc6bc111f758238b1af5f102`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 23:23:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:30:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 17 Mar 2022 23:30:40 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 17 Mar 2022 23:30:41 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:30:42 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 23:30:43 GMT
ENV JAVA_VERSION=11.0.14.1
# Thu, 17 Mar 2022 23:31:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 17 Mar 2022 23:31:48 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 08:55:36 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 19 Mar 2022 08:55:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 19 Mar 2022 08:55:38 GMT
WORKDIR /tmp
# Sat, 19 Mar 2022 08:55:43 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 19 Mar 2022 08:55:44 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 19 Mar 2022 08:55:45 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 19 Mar 2022 08:55:58 GMT
RUN boot
# Sat, 19 Mar 2022 08:55:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae7314079173e0b84736e3e2bd8ab0ecb4a61a7e8edf7f35305c0176b6d73a7`  
		Last Modified: Thu, 17 Mar 2022 23:48:51 GMT  
		Size: 3.1 MB (3118894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe97e620b69fa6ef163eac56725db0a450f05bf580f70d45cc5e35dd602ea5ec`  
		Last Modified: Thu, 17 Mar 2022 23:58:27 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e0044eb13f83ad06a760b7244c13c5a520adbf97488716954e4bff550dd68`  
		Last Modified: Thu, 17 Mar 2022 23:58:44 GMT  
		Size: 200.9 MB (200942219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e46416d2e9db60d87a2eeb3db556c0438da142a397f5ac63a0841dbcff4832`  
		Last Modified: Sat, 19 Mar 2022 09:23:14 GMT  
		Size: 70.4 KB (70386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2ed38cd1e877114c37bb5c603260dd5804bfe82e8356530414f2c2efbb9063`  
		Last Modified: Sat, 19 Mar 2022 09:23:17 GMT  
		Size: 58.8 MB (58815513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
