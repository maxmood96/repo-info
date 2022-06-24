## `tomcat:9-jre8-openjdk-slim-bullseye`

```console
$ docker pull tomcat@sha256:2b010463432442d91b735916166f2b679d8f44d952a61c27e0ffb70036e34ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre8-openjdk-slim-bullseye` - linux; amd64

```console
$ docker pull tomcat@sha256:3b06aa8dcc825c96d2fb2891546e25694cc7034112fbd3c13b4d0b8a4b95281c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87212038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b543cbededa92c7b17c8f604d6b293d16b6452cf1cf4a4682cf077d096428168`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:00:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:00:37 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:00:37 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:00:37 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:00:37 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:01:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Jun 2022 22:46:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:46:09 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:46:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:46:10 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:46:10 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:46:10 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:52:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 23 Jun 2022 22:52:06 GMT
ENV TOMCAT_MAJOR=9
# Thu, 23 Jun 2022 22:52:06 GMT
ENV TOMCAT_VERSION=9.0.64
# Thu, 23 Jun 2022 22:52:06 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Thu, 23 Jun 2022 22:52:06 GMT
COPY dir:da6e561ebf837f306d29c5e0c12324d6f84a1f9c9329a24c4faf24655d59fe2f in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:52:10 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:52:11 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:52:11 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:52:11 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4dc029a36926590a5070a9a58443942497e3b2d48cff116b8b15004d386a40`  
		Last Modified: Thu, 23 Jun 2022 05:07:14 GMT  
		Size: 1.6 MB (1582249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336e04eeb91a4371c25329796317d1b09a60bacf789ea0952f690c5680fc3cf4`  
		Last Modified: Thu, 23 Jun 2022 05:20:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba945e1408ccd99f81b8a3b5741ad91ef403ac4b97efc3a34175dc79d1dc3eae`  
		Last Modified: Thu, 23 Jun 2022 05:21:52 GMT  
		Size: 41.7 MB (41697352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22878f33e97a17ad713697f81fceb0da94ab4829be3b309e5e61167f31da4124`  
		Last Modified: Thu, 23 Jun 2022 23:14:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c82b953679ce2d79349c2051f5f63771eb1ecac6be23388f11c0e13dbf67ff`  
		Last Modified: Thu, 23 Jun 2022 23:20:27 GMT  
		Size: 12.2 MB (12156254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2334f2cb0fff020b1b263d92b4d90bf7464e255ad6e4804845c1c4f0162e74ec`  
		Last Modified: Thu, 23 Jun 2022 23:20:26 GMT  
		Size: 396.3 KB (396266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e29c34ad5071e4e7196b7608e5cd5f66be49c106ee8ff2938a0a13af2028c4`  
		Last Modified: Thu, 23 Jun 2022 23:20:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-openjdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:33af47d91367b1b133291aed0e5b79fbf305fe301b03058d40fe553d4ea632fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84494804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f004f4686139f11d7af076018cdd7f1c002d9e4fda127c294577a2fedfd2ee02`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:37:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:43:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 01:43:17 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 01:43:18 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 01:43:19 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 01:43:20 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 01:44:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 28 May 2022 20:16:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 28 May 2022 20:16:33 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 20:16:34 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 28 May 2022 20:16:35 GMT
WORKDIR /usr/local/tomcat
# Sat, 28 May 2022 20:16:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:16:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:26:36 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 28 May 2022 20:26:36 GMT
ENV TOMCAT_MAJOR=9
# Fri, 10 Jun 2022 01:30:55 GMT
ENV TOMCAT_VERSION=9.0.64
# Fri, 10 Jun 2022 01:30:56 GMT
ENV TOMCAT_SHA512=38392b651fabe706fb0524c52849601299494178010bb8077af383232c20bbbda1aec4ab8898adb2cc37c07583ff0e9d3c7038ce55a22bc68c3641641b47fd1a
# Fri, 10 Jun 2022 01:30:58 GMT
COPY dir:42313f7e05c4cc5d70f84588b851b75cec1dda454b9008a825565ad3dd629862 in /usr/local/tomcat 
# Fri, 10 Jun 2022 01:31:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Jun 2022 01:31:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 10 Jun 2022 01:31:04 GMT
EXPOSE 8080
# Fri, 10 Jun 2022 01:31:05 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c8727eedfb1755681add8fcb3c2c35d3b41f8231849edcec84588c6404f3b3`  
		Last Modified: Sat, 28 May 2022 01:54:41 GMT  
		Size: 1.4 MB (1361240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24fcebfd56bd1fcbbf2c66cc19bdd396c029b55d0cd5580710f92f55d2e1fdb`  
		Last Modified: Sat, 28 May 2022 02:03:03 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6381faf654a80974c203d58fbd374d009882efc2993a12f6c2feb4cf138dea2`  
		Last Modified: Sat, 28 May 2022 02:04:21 GMT  
		Size: 40.7 MB (40720830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66327cd8721fb40a718cbdd05e1df0066feb423e009ad50c468af7d2ba74df`  
		Last Modified: Sat, 28 May 2022 21:03:48 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f6b21c504b99eacb9a82397416b191adf348b6b94979decf525d1172756034`  
		Last Modified: Fri, 10 Jun 2022 02:05:51 GMT  
		Size: 12.2 MB (12166700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194e936764c615003aa2ddd5e8eeed0b28f03cee476670cc916fa11a91a225b2`  
		Last Modified: Fri, 10 Jun 2022 02:05:50 GMT  
		Size: 180.0 KB (179958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
