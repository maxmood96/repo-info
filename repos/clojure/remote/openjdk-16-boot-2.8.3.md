## `clojure:openjdk-16-boot-2.8.3`

```console
$ docker pull clojure@sha256:6da3cb96fa5f5831ed198c877b41f666fd604930267e0a8edbae3e423ccad5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-16-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:42eb189d851b1b6bfeff82247b4e92dc4403d989b8e9b6477640a9c5f859ea50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274595701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcabb39ab6eec9630c8ff2d05914c1f28dbf587002d04ff8233e599cfd877dd`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:49:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Mon, 01 Feb 2021 19:49:22 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:49:23 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:49:23 GMT
ENV JAVA_VERSION=16-ea+34
# Mon, 01 Feb 2021 19:49:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='11fd069e3a17a17268b9bb0c8bfd440016af686acfe8d3a4bfd71381fbce22dc'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='9c294a8b7c440c45968fc16d3aa3261be71b00a7fad22b7aafa2a7b7381e5f2c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:49:44 GMT
CMD ["jshell"]
# Mon, 01 Feb 2021 20:46:34 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 01 Feb 2021 20:46:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 01 Feb 2021 20:46:34 GMT
WORKDIR /tmp
# Mon, 01 Feb 2021 20:46:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 01 Feb 2021 20:46:40 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 01 Feb 2021 20:46:40 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 01 Feb 2021 20:46:58 GMT
RUN boot
# Mon, 01 Feb 2021 20:46:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950c363148faa95e771cc0cd56d8bbfb554665a4cb2a557d8a34fa4f23bedb55`  
		Last Modified: Mon, 01 Feb 2021 20:04:50 GMT  
		Size: 185.1 MB (185139366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16aefafb8f1be8c89a0358f8a0d316a76d9d036cf8716bf0adbbd9d036e7ed4`  
		Last Modified: Mon, 01 Feb 2021 20:53:56 GMT  
		Size: 279.6 KB (279623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4209d9172b337e53ce1497c3055cfda3c1de9eaa9f8e4060b83859fc48f2d7e`  
		Last Modified: Mon, 01 Feb 2021 20:53:59 GMT  
		Size: 58.8 MB (58820085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-16-boot-2.8.3` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6831287b6ba10048bd07c9ac2c4d48fa5965c2a641f7ca1e6aad8577ea8d4e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.6 MB (267581197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a345dd67326954fc35f0b1265cec32ced0367fa46b8f1da4a4fe51e51fe95b7a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:00:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:00:31 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 01:02:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Tue, 12 Jan 2021 01:02:13 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jan 2021 01:02:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 23 Jan 2021 01:48:03 GMT
ENV JAVA_VERSION=16-ea+33
# Sat, 23 Jan 2021 01:48:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_linux-aarch64_bin.tar.gz; 			downloadSha256=1da1b96306a0ede9e1c7b4284772b5de3c9f8f08f895e082f561f5f3c86ea3be; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_linux-x64_bin.tar.gz; 			downloadSha256=ba2ac6ccca898cd63090d768b89a95fba76b6303a55c41e851d75dd0c5afcee8; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 23 Jan 2021 01:48:26 GMT
CMD ["jshell"]
# Sat, 23 Jan 2021 02:19:12 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 23 Jan 2021 02:19:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 23 Jan 2021 02:19:13 GMT
WORKDIR /tmp
# Sat, 23 Jan 2021 02:19:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 23 Jan 2021 02:19:23 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 23 Jan 2021 02:19:24 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 23 Jan 2021 02:20:02 GMT
RUN boot
# Sat, 23 Jan 2021 02:20:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6132c56bf059fe6b3844038ac4ca6b320af5f511b4c60addc956fb470ebfcb8`  
		Last Modified: Tue, 12 Jan 2021 01:11:08 GMT  
		Size: 3.1 MB (3101516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a74a7e0616e4c6b1416ebb635323d67d5fbc93ea9f39d503031d2e52228e6b`  
		Last Modified: Tue, 12 Jan 2021 01:12:23 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec762a6adcd1c2545abff26fa93bf810d362e6fa6a932917c539b86fcc652bd`  
		Last Modified: Sat, 23 Jan 2021 01:56:59 GMT  
		Size: 179.5 MB (179514618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31aaaedd9fa9a1e2a9c00c592957071c43ec2ef6c0f5263f0071e0662420a64a`  
		Last Modified: Sat, 23 Jan 2021 02:24:16 GMT  
		Size: 279.5 KB (279475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d65e4697975243d868cebd9938c13a3c44d4d32f14920c378c7296672a5d12`  
		Last Modified: Sat, 23 Jan 2021 02:24:23 GMT  
		Size: 58.8 MB (58820885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
