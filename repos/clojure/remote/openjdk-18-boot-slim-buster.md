## `clojure:openjdk-18-boot-slim-buster`

```console
$ docker pull clojure@sha256:c7423474fe58bdd2fe293967c12bd052a690c72f12b049f7586401d9bcbbcb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:b338eecb1dfea58f3e94088cc02797026be2d261348e7d34f38245ff15bc40b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278535812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ffed8730e5958dff5b028125ffac9e56fe7911df0be670b63fa653076205f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:23:04 GMT
ADD file:bd5c9e0e0145fe33beee9d73615cc89b5c5459bb84ea164cb1bbd8c999f0c2e4 in / 
# Tue, 21 Dec 2021 01:23:04 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 22:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 22:59:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 22:59:58 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 22:59:59 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 22:59:59 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 23:00:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 23:00:14 GMT
CMD ["jshell"]
# Wed, 22 Dec 2021 13:41:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 22 Dec 2021 13:41:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 22 Dec 2021 13:41:06 GMT
WORKDIR /tmp
# Wed, 22 Dec 2021 13:41:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 22 Dec 2021 13:41:11 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Dec 2021 13:41:11 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 22 Dec 2021 13:41:33 GMT
RUN boot
# Wed, 22 Dec 2021 13:41:33 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 22 Dec 2021 13:41:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Dec 2021 13:41:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72a69066d2febc34d8f3dbcb645f7b851a57e9681322ece7ad8007503b783c19`  
		Last Modified: Tue, 21 Dec 2021 01:28:32 GMT  
		Size: 27.2 MB (27153723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c983bcc370920d99695dc288c345343be841987206e4ce762a4e7599f28c96`  
		Last Modified: Tue, 21 Dec 2021 23:16:09 GMT  
		Size: 3.3 MB (3269567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f54dcb284410f41e55cf4f4ca250e28e480947f47fd02d4a206df1320d7be4d`  
		Last Modified: Tue, 21 Dec 2021 23:19:07 GMT  
		Size: 189.0 MB (189011832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30b0cf21ef4e234beccdc95446ab2beb7dadb2da58336e844d188866eb9bf0d`  
		Last Modified: Wed, 22 Dec 2021 13:59:57 GMT  
		Size: 279.8 KB (279768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8416f62fc1ff12cad9ed3f38af6bcacb037d1342786e726b8d466dfa19bb053`  
		Last Modified: Wed, 22 Dec 2021 14:00:00 GMT  
		Size: 58.8 MB (58820515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfde9c9b5a3217e162a4fab042bdc05237959bf13fbaeefaad614d58ec3fc65b`  
		Last Modified: Wed, 22 Dec 2021 13:59:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e54905880d69933c04c3e690241e79c2620b4a6db56d41912f07ca99cde8795b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275666214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615f0140b5334257a8bde9606972d0c918f159806ae70f26ee9177587f6901f1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:48 GMT
ADD file:9810440ab841e71bd153282c21cfcd46d3f40bd5099e60c332e05bf066e390ac in / 
# Tue, 21 Dec 2021 01:42:49 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:56:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Tue, 21 Dec 2021 02:56:42 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Dec 2021 02:56:43 GMT
ENV LANG=C.UTF-8
# Tue, 21 Dec 2021 02:56:44 GMT
ENV JAVA_VERSION=18-ea+28
# Tue, 21 Dec 2021 02:57:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='7e5f0e54c799f8c155a934e61d88f4fef3a70a641c1636c925158622c7bd9341'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/28/GPL/openjdk-18-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='e29aa39763ebcfe5f037cc4fe47c6b9eb34cbe482f6ea57e93de89070255e22b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Dec 2021 02:57:05 GMT
CMD ["jshell"]
# Tue, 21 Dec 2021 22:12:04 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 21 Dec 2021 22:12:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 21 Dec 2021 22:12:06 GMT
WORKDIR /tmp
# Tue, 21 Dec 2021 22:12:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 21 Dec 2021 22:12:12 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 21 Dec 2021 22:12:13 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 21 Dec 2021 22:12:28 GMT
RUN boot
# Tue, 21 Dec 2021 22:12:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 21 Dec 2021 22:12:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Dec 2021 22:12:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:753408153c81560bc4244b14524c404cbf483c8afa8ac924272545400536a9d8`  
		Last Modified: Tue, 21 Dec 2021 01:49:44 GMT  
		Size: 25.9 MB (25923149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c74145b5f237a66007b7c0d55f2ffe3d54c07bf5e09c19bebd4ec94b00005e`  
		Last Modified: Tue, 21 Dec 2021 03:17:41 GMT  
		Size: 3.1 MB (3118854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db36813e8b0fa893cb2f9a2ceeede667700fac83259dcbda4848cedbd57cba07`  
		Last Modified: Tue, 21 Dec 2021 03:21:18 GMT  
		Size: 187.7 MB (187740640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1505c4c1557c445ece76356ed5a283672a455d9e0fa85b71113728ecce62695a`  
		Last Modified: Tue, 21 Dec 2021 22:34:55 GMT  
		Size: 67.5 KB (67494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fb1a2e8bab24ba969e4b963a7849b83489fcb9fe054f05ceb58b88e4b3d37f`  
		Last Modified: Tue, 21 Dec 2021 22:35:01 GMT  
		Size: 58.8 MB (58815671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6db5da2070219f047e3f605391a9d38c563af8cdecd28f8801221b825c1d42`  
		Last Modified: Tue, 21 Dec 2021 22:34:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
