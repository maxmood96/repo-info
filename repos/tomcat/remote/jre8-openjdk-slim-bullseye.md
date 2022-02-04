## `tomcat:jre8-openjdk-slim-bullseye`

```console
$ docker pull tomcat@sha256:98172bf9927a87109abb6c4f54c4858297639951844257569347223c894a562b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-slim-bullseye` - linux; amd64

```console
$ docker pull tomcat@sha256:33b15612505ac992624657bf1b237fcc35d2b776826d9834bf0e484423b771af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87490895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf24b0679b7eeeaef5749820836cbbcf7dfecf1639c7dae7f57fe15b9d34b02`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:30:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 09:31:01 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:31:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:31:01 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:47:07 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:50:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 04 Feb 2022 01:44:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Feb 2022 01:44:25 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 01:44:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Feb 2022 01:44:27 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Feb 2022 01:44:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:44:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:44:27 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 04 Feb 2022 01:44:28 GMT
ENV TOMCAT_MAJOR=10
# Fri, 04 Feb 2022 01:44:28 GMT
ENV TOMCAT_VERSION=10.0.16
# Fri, 04 Feb 2022 01:44:28 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Fri, 04 Feb 2022 01:44:29 GMT
COPY dir:ea3e56c7668817807e4624e0be1fad87b7e0694ae873b714599e0d360cca121d in /usr/local/tomcat 
# Fri, 04 Feb 2022 01:44:34 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Feb 2022 01:44:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Feb 2022 01:44:38 GMT
EXPOSE 8080
# Fri, 04 Feb 2022 01:44:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e1acf77ba577f7a2387683fc9edb2fd1038983f5445ceccea6183c38dc4fe9`  
		Last Modified: Wed, 26 Jan 2022 09:56:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15194df179bf8ed84393f81809fbbfe4f20aaf17452c94db7cc3bcdf5c441dcd`  
		Last Modified: Thu, 03 Feb 2022 21:05:00 GMT  
		Size: 41.7 MB (41660506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512c977b0ae31c547a935da86d196cf2ee48b29a80ecbc9cd769b4afcf5d6e26`  
		Last Modified: Fri, 04 Feb 2022 02:26:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c9cdb932d1f0c3d8d9558ae53e076a3761fc7ee1f5d524729628dee004b8f4`  
		Last Modified: Fri, 04 Feb 2022 02:26:21 GMT  
		Size: 12.5 MB (12485341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7906f2d00ddbf1d64faa97e6446891e782368447238c2b5ec6ea1236e18d6bb9`  
		Last Modified: Fri, 04 Feb 2022 02:26:20 GMT  
		Size: 396.2 KB (396230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6efeb4e16476736d9604c864349fa54ddfd42eb6d64c689a27eee2e450f376`  
		Last Modified: Fri, 04 Feb 2022 02:26:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:499e4f3e32615a5aba79734f383b3ba744d9e5267e603c947ac3314796930e34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85011803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a305fc706ecbccf2ecaa30d73806a14b54244ce39aa80fe75f8fa584a594f9d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 06:01:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 26 Jan 2022 06:01:09 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 06:01:10 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 06:01:11 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:58:09 GMT
ENV JAVA_VERSION=8u322
# Thu, 03 Feb 2022 20:59:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 04 Feb 2022 00:59:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Feb 2022 00:59:08 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 00:59:09 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Feb 2022 00:59:10 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Feb 2022 00:59:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 00:59:12 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 00:59:13 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 04 Feb 2022 00:59:14 GMT
ENV TOMCAT_MAJOR=10
# Fri, 04 Feb 2022 00:59:15 GMT
ENV TOMCAT_VERSION=10.0.16
# Fri, 04 Feb 2022 00:59:16 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Fri, 04 Feb 2022 00:59:18 GMT
COPY dir:2e38a990a47897da449bb52cb91dbd60eeceee78701a5810fbbc46200395f7f2 in /usr/local/tomcat 
# Fri, 04 Feb 2022 00:59:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Feb 2022 00:59:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Feb 2022 00:59:24 GMT
EXPOSE 8080
# Fri, 04 Feb 2022 00:59:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abf67e3e34eccefabf68f15c7d753f1a4c8e241beb1818f97e276186d54124e`  
		Last Modified: Wed, 26 Jan 2022 06:13:02 GMT  
		Size: 1.6 MB (1565889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5975e457ab95bc20b0e54adead2544099c10756d14ec5aa738495bad98a1fb`  
		Last Modified: Wed, 26 Jan 2022 06:28:47 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dc67b6e5d912842e1a958777d4b08e4295a5777c488af058b6b8f31bde685a`  
		Last Modified: Thu, 03 Feb 2022 21:20:33 GMT  
		Size: 40.7 MB (40711113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1c36e014f7671daaafa8168651cfa198be3af70fa0467212242ea9cd3c6ed`  
		Last Modified: Fri, 04 Feb 2022 01:56:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6557fed9d62faa0831e74cb1ac40b3d43ce5d49c58af46c82ed0160113f57fc1`  
		Last Modified: Fri, 04 Feb 2022 01:56:23 GMT  
		Size: 12.5 MB (12497807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc1ce0a78ff52cf8739e6ad5b8ab632e4fa3edf11c419ec39f02ee770090ffa`  
		Last Modified: Fri, 04 Feb 2022 01:56:22 GMT  
		Size: 179.9 KB (179870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
