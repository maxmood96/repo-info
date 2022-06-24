## `tomcat:jre8-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:ea5724547e1f96fd8a63f8389448d6fb46b908afa27f62e288dd82d3b13c29b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:49d847d72a1eb8c97ac03b3aad3f68f910327044e8c1abc45a373f79c531a599
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85074348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85baa8193850d4647d194c9f8c0a7716f7348ba22a1f212aa85985d882a92dfb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:01:05 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:01:05 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:01:05 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:01:05 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:01:05 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:02:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Jun 2022 22:46:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:46:54 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:46:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:46:55 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:46:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:46:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:46:55 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 23 Jun 2022 22:46:55 GMT
ENV TOMCAT_MAJOR=10
# Thu, 23 Jun 2022 22:46:56 GMT
ENV TOMCAT_VERSION=10.0.22
# Thu, 23 Jun 2022 22:46:56 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Thu, 23 Jun 2022 22:46:56 GMT
COPY dir:b55e684a7f634e413c139a808e791952f05b4dea29b131457bffb896c99b30a7 in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:47:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:47:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:47:02 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:47:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420fab7e4cce528d853465a0775f91b15783a53a42b906820fb3f70f0f731667`  
		Last Modified: Thu, 23 Jun 2022 05:08:38 GMT  
		Size: 3.3 MB (3273402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cc1e3d6d3732acee702c68bf93504ebe4e5c55920790e28b99c6849e782b35`  
		Last Modified: Thu, 23 Jun 2022 05:21:08 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157ed8b1255f39df56128dba009619425842ec5ccbdbcc3c877a494f33a08f7b`  
		Last Modified: Thu, 23 Jun 2022 05:22:31 GMT  
		Size: 41.7 MB (41703996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf6d852829687247cbc55eb901d61eafafafa2ffb29239142c02848509f69a8`  
		Last Modified: Thu, 23 Jun 2022 23:15:35 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b9a7f7591d5e6a0d14e7d6517f51c25d077c33c6e973c6a699e1bac6dfc65`  
		Last Modified: Thu, 23 Jun 2022 23:15:36 GMT  
		Size: 12.6 MB (12568684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15eb5515da489cbc2645ec304226b268d7fa018898fdf93ce601a3c1e8fc9d4`  
		Last Modified: Thu, 23 Jun 2022 23:15:36 GMT  
		Size: 387.7 KB (387709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239760876e543c992d75107350f454d80ee998a29443468ffab48cb7c835f7e8`  
		Last Modified: Thu, 23 Jun 2022 23:15:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:6622c9d5d4ac3f77723e67898f83cf90722cccbfa908713f8af368f2d4d66612
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82525370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef6e40bd7804002c2bc78e5190cab6d0e551c18a68ef39ca71a66876b642506`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:38:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:43:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 01:43:53 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 01:43:54 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 01:43:55 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 01:43:56 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 01:45:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 28 May 2022 20:17:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 28 May 2022 20:17:52 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 20:17:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 28 May 2022 20:17:54 GMT
WORKDIR /usr/local/tomcat
# Sat, 28 May 2022 20:17:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:17:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:17:57 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 28 May 2022 20:17:58 GMT
ENV TOMCAT_MAJOR=10
# Mon, 13 Jun 2022 21:09:55 GMT
ENV TOMCAT_VERSION=10.0.22
# Mon, 13 Jun 2022 21:09:56 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Mon, 13 Jun 2022 21:09:58 GMT
COPY dir:ba194fc93f6c1a67391ef602a39c5e2d7ea2fc66f477ae06f04e45e323db497b in /usr/local/tomcat 
# Mon, 13 Jun 2022 21:10:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Jun 2022 21:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 13 Jun 2022 21:10:04 GMT
EXPOSE 8080
# Mon, 13 Jun 2022 21:10:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fd49b058d9314bede6d26981edcf8cfa5f28eebce620889117829184769a12`  
		Last Modified: Sat, 28 May 2022 01:56:24 GMT  
		Size: 3.1 MB (3126023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96556ba78de34115f1382d311d0b34b208450b8f104f03fd8eb7431cae357a7c`  
		Last Modified: Sat, 28 May 2022 02:03:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31280ea80053f61fea6340a16399bdfa29cc468fccbc56fcaa842c64d265393`  
		Last Modified: Sat, 28 May 2022 02:04:44 GMT  
		Size: 40.7 MB (40731085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe2d2e04d060e1114f259974db3af7b39a081fa31d469765b3354e4572b8c29`  
		Last Modified: Sat, 28 May 2022 21:04:39 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5808b3d92401babb956769261a54cf342066ffee2506e0530d8e97a13eb61c`  
		Last Modified: Mon, 13 Jun 2022 21:53:19 GMT  
		Size: 12.6 MB (12580211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0da5a5aa6e77422a29613ac694b3074f359c136ec0763ac1785146b47187d8e`  
		Last Modified: Mon, 13 Jun 2022 21:53:18 GMT  
		Size: 173.7 KB (173671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
