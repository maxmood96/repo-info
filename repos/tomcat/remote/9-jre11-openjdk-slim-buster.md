## `tomcat:9-jre11-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:55d053dbb4b46c390185b265f8a4c0b6c7179ccbf59e36d331fa4248db50b799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre11-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:91ff53511c775120742a3c32b176ffdd7111c8df405c7ffb35812b1f5d4b3ed6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90153728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7d388283dd7fe3132594a3e562722cfb89c99d1d4edf687cd792189124555b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 28 Sep 2021 01:23:09 GMT
ADD file:99db7cfe7952a1c7a7959cc3457af37c1d6facdd43a946bd72313d8b5ede0029 in / 
# Tue, 28 Sep 2021 01:23:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:21:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 28 Sep 2021 09:21:51 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 28 Sep 2021 09:21:51 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 09:21:52 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 09:21:52 GMT
ENV JAVA_VERSION=11.0.12
# Tue, 28 Sep 2021 09:24:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 29 Sep 2021 11:17:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 29 Sep 2021 11:17:35 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 11:17:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 29 Sep 2021 11:17:36 GMT
WORKDIR /usr/local/tomcat
# Wed, 29 Sep 2021 11:17:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 11:17:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 11:41:55 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 29 Sep 2021 11:41:56 GMT
ENV TOMCAT_MAJOR=9
# Wed, 29 Sep 2021 11:41:56 GMT
ENV TOMCAT_VERSION=9.0.53
# Wed, 29 Sep 2021 11:41:56 GMT
ENV TOMCAT_SHA512=ee731b2d0c3ab7e14fa924dcb8d598707cedf714c9ce1f2c2d907a1fd51e26f7eec1343c3dc39e240ff64dac2e0213f154d23e5f94a430f429165b5df51f786f
# Wed, 29 Sep 2021 11:41:57 GMT
COPY dir:0b8cece38ef7e6f09fda7913af63ec0293b17e238d438e03e04ccd90dcf820d9 in /usr/local/tomcat 
# Wed, 29 Sep 2021 11:42:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 Sep 2021 11:42:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 29 Sep 2021 11:42:03 GMT
EXPOSE 8080
# Wed, 29 Sep 2021 11:42:03 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:07aded7c29c6011dfdf02fc98e087c941d3c2661c4e73d134c6491e25231d16c`  
		Last Modified: Tue, 28 Sep 2021 01:29:45 GMT  
		Size: 27.1 MB (27145994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49190af1e362ddee7f9a92cbf321a9b1444ccbc631019b5ebcc582e4ef2ec3e9`  
		Last Modified: Tue, 28 Sep 2021 09:35:40 GMT  
		Size: 3.3 MB (3269563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebbc8ce5650e52dc785a2c8e731a1c51a69f6d5379475fae0561ab343141d41`  
		Last Modified: Tue, 28 Sep 2021 09:44:22 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c069a075a3304def269353f9a74f31bb6dc233522d35bcd64488cd6700e1dfe8`  
		Last Modified: Tue, 28 Sep 2021 09:46:27 GMT  
		Size: 47.1 MB (47137210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d138e66ece2290004ad6b432cb985b9edb7260eff7db883ca91c6672c46e88`  
		Last Modified: Wed, 29 Sep 2021 12:25:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bb9868721ef59bcffa95b2fab2a4c4945163cf8277b0e3bd0ec95a714f8e08`  
		Last Modified: Wed, 29 Sep 2021 12:41:27 GMT  
		Size: 12.2 MB (12212733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12838776d08189e531f8049d8f2c8a27c9e04af91a127e2ba31f1c921b1a920`  
		Last Modified: Wed, 29 Sep 2021 12:41:26 GMT  
		Size: 387.7 KB (387720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fd92e6c904f024d3b15ceb16c8cb1d903a4b66f71413261741084b7eb50371`  
		Last Modified: Wed, 29 Sep 2021 12:41:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:9a9fa1020da35e006d0f94b1b694a33301ed5599afc1963c22bb43ee80bfc712
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87851683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bccddda696be9e27d8e2f84e49060c77abd4dcd3af098e05cdaed4b21ba77a0b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 28 Sep 2021 01:41:13 GMT
ADD file:3e2426765cfe2b896fc847bcb435624930753c72ac00b87d2c73f4a81c813fd4 in / 
# Tue, 28 Sep 2021 01:41:13 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 05:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 05:49:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 28 Sep 2021 05:49:34 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 28 Sep 2021 05:49:34 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 05:49:34 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 05:49:34 GMT
ENV JAVA_VERSION=11.0.12
# Tue, 28 Sep 2021 05:51:48 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 29 Sep 2021 03:58:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 29 Sep 2021 03:58:10 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 03:58:11 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 29 Sep 2021 03:58:11 GMT
WORKDIR /usr/local/tomcat
# Wed, 29 Sep 2021 03:58:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 03:58:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 04:24:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 29 Sep 2021 04:24:44 GMT
ENV TOMCAT_MAJOR=9
# Wed, 29 Sep 2021 04:24:45 GMT
ENV TOMCAT_VERSION=9.0.53
# Wed, 29 Sep 2021 04:24:45 GMT
ENV TOMCAT_SHA512=ee731b2d0c3ab7e14fa924dcb8d598707cedf714c9ce1f2c2d907a1fd51e26f7eec1343c3dc39e240ff64dac2e0213f154d23e5f94a430f429165b5df51f786f
# Wed, 29 Sep 2021 04:24:45 GMT
COPY dir:06132ad3e67ae84d3b91d14daf41ad3d3402577369c5dfe073743bdc287925c8 in /usr/local/tomcat 
# Wed, 29 Sep 2021 04:24:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 Sep 2021 04:24:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 29 Sep 2021 04:24:51 GMT
EXPOSE 8080
# Wed, 29 Sep 2021 04:24:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:896f18f54b28590b15a0f3354b13e8ea2f88a05f13de4117720f88cef30206ee`  
		Last Modified: Tue, 28 Sep 2021 01:49:22 GMT  
		Size: 25.9 MB (25915039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f844c3c3d3fdf0c62ff77a82ed24a2a010ad55e3206255c75275457b868825`  
		Last Modified: Tue, 28 Sep 2021 06:06:17 GMT  
		Size: 3.1 MB (3119080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06eb9ef87ee8e52c71593bb38565b2d668a18f4b3f9bf2871a329550364803a`  
		Last Modified: Tue, 28 Sep 2021 06:15:45 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66c50d59d3844dbb62117ae6d41b5eaadaf62182294aa889c6b8318e1000ea5`  
		Last Modified: Tue, 28 Sep 2021 06:18:01 GMT  
		Size: 46.2 MB (46203736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a157e3bc6f77befc7c4494adf43a185ad79216ba09f080f076d65c5260be83`  
		Last Modified: Wed, 29 Sep 2021 05:22:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb827f8563ff05f3bdb993293ee2db23630942dd3cc6f3fdb3179d63f7b476f`  
		Last Modified: Wed, 29 Sep 2021 05:42:58 GMT  
		Size: 12.2 MB (12227108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19cd56dde8ab0b42d883d61fd7b330d8506bdd1457e420c75c17a23ce4357ac`  
		Last Modified: Wed, 29 Sep 2021 05:42:57 GMT  
		Size: 386.2 KB (386207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcf132ed2c12a158b1552be32b3f50927d22ec03139699396dd9c318949e0da`  
		Last Modified: Wed, 29 Sep 2021 05:42:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
