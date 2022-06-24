## `tomcat:jre11-openjdk-buster`

```console
$ docker pull tomcat@sha256:e91a184d7cbe6a5d7244daf9affab5b8fed7a0f798a38bda518d735f15ea436f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre11-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:93c917a2360dfe6a92300bbf34657af50954ce5ed1d72f86fabb6402255a9ed4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134064719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e757795ea743d4b15bfbf3ef918e17eedd7ea968b9c61e972b81c82994c8d6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 04:59:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:59:49 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 23 Jun 2022 04:59:49 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 04:59:49 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 04:59:50 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:59:50 GMT
ENV JAVA_VERSION=11.0.15
# Thu, 23 Jun 2022 04:59:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 23 Jun 2022 22:39:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:39:21 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:39:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:39:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:39:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:39:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:39:22 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 23 Jun 2022 22:39:22 GMT
ENV TOMCAT_MAJOR=10
# Thu, 23 Jun 2022 22:42:27 GMT
ENV TOMCAT_VERSION=10.0.22
# Thu, 23 Jun 2022 22:42:27 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Thu, 23 Jun 2022 22:42:27 GMT
COPY dir:588c514223a0155aac3e659f9d86d37cd6f9cd848c5a4c193fdfd688bcfa1cf1 in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:42:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:42:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:42:32 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:42:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a014c92148934973210d840dc7cfed53e0afba38d839afaa48ed5150eae19af`  
		Last Modified: Thu, 23 Jun 2022 00:59:51 GMT  
		Size: 7.9 MB (7856631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ff1be7001d642a624409e2d5f90e7708ef7e6f1a75f4eb7362a9296e18d20`  
		Last Modified: Thu, 23 Jun 2022 00:59:50 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9250eef0f01e9551fef0eaea0e242501ab3d09c6a7e72c66f5083b55a6daa18d`  
		Last Modified: Thu, 23 Jun 2022 05:19:07 GMT  
		Size: 5.5 MB (5532608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3969d4e96be0fe658c00f6470d43bed2ac921be1aa78ec4291152107219803d6`  
		Last Modified: Thu, 23 Jun 2022 05:19:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b052dd935874d534abf3e130c99d2be324d345c7c07b3fa578317369fc087`  
		Last Modified: Thu, 23 Jun 2022 05:19:13 GMT  
		Size: 47.2 MB (47206773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8086d979640f420396f5ac5c0a2533547a54ee79dfd699c69179369e4ec845`  
		Last Modified: Thu, 23 Jun 2022 23:07:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca9f83823cef7a268c8a38ba75df15fd713f501166684f89694de2ff95c6e3d`  
		Last Modified: Thu, 23 Jun 2022 23:10:59 GMT  
		Size: 12.6 MB (12569188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f14d99ec8fb9f0677e751cd58ca9c9fc40f44790fecba24edc8eedc45668f8e`  
		Last Modified: Thu, 23 Jun 2022 23:10:58 GMT  
		Size: 461.0 KB (460966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3c06db8a3e6e68748c280ce022357f6dbae2c4864f4036842293223642d26b`  
		Last Modified: Thu, 23 Jun 2022 23:10:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:ca72701e77fd246b4d2c1fb459c9e268d6a2e69b1bef40b1a7d2f4e179f3d65d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131528201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046bad270f634f84370234f958a843f8cc4d3869056bd6c8b7f4661409ec4c4f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 28 May 2022 00:40:49 GMT
ADD file:af879be34a7eccc177a3000eb8c45d5207bfbec108caf9be9d11c1a6620c376c in / 
# Sat, 28 May 2022 00:40:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:07:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:07:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 16:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 16:50:58 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 May 2022 16:50:59 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 16:51:00 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 16:51:01 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 16:51:02 GMT
ENV JAVA_VERSION=11.0.15
# Sat, 28 May 2022 16:51:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 28 May 2022 20:04:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 28 May 2022 20:04:58 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 20:04:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 28 May 2022 20:05:00 GMT
WORKDIR /usr/local/tomcat
# Sat, 28 May 2022 20:05:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:05:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:05:03 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 28 May 2022 20:05:04 GMT
ENV TOMCAT_MAJOR=10
# Mon, 13 Jun 2022 21:02:43 GMT
ENV TOMCAT_VERSION=10.0.22
# Mon, 13 Jun 2022 21:02:44 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Mon, 13 Jun 2022 21:02:46 GMT
COPY dir:4b7d227583994617e68cc67c68249edf14be92adb704048c6646002f4a1c7df3 in /usr/local/tomcat 
# Mon, 13 Jun 2022 21:02:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Jun 2022 21:02:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 13 Jun 2022 21:02:52 GMT
EXPOSE 8080
# Mon, 13 Jun 2022 21:02:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fadbed17b01e84815ca3018d3dc42670c3add65c67e7cc74d6bc477ae8425934`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 49.2 MB (49229054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5795076bf6e9bf96da71f2e31cbe91d3c49a17f211c5b0d33e032e095c5564a5`  
		Last Modified: Sat, 28 May 2022 11:18:22 GMT  
		Size: 7.7 MB (7719823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1eda3e266fa432ba8ae8ba25a5ad2fa4c5349ef2aa244612c89f990704c5b25`  
		Last Modified: Sat, 28 May 2022 11:18:22 GMT  
		Size: 9.8 MB (9767307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ee2604901b84270e3319485b241bd7323e97383ddc6b24f2c63ac7f32138d0`  
		Last Modified: Sat, 28 May 2022 17:06:56 GMT  
		Size: 5.5 MB (5506814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be344314c9fa8853316307cd3cc5330dfe992882b307ad0bfd077ba68c6a5820`  
		Last Modified: Sat, 28 May 2022 17:06:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e6bc99e8c297918cf689d5e4f53c63f972f5c39d6c613572ff9e7b72b74d6e`  
		Last Modified: Sat, 28 May 2022 17:07:02 GMT  
		Size: 46.5 MB (46505512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22647cf5d41b58dd0f27d06fa6efe009fddb86262748d73b89a7698f71ca314`  
		Last Modified: Sat, 28 May 2022 20:54:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75111dab5ea4442aa64483f4e33254072a4cb4bfb1c4dd687af03fc54cde37b3`  
		Last Modified: Mon, 13 Jun 2022 21:46:37 GMT  
		Size: 12.6 MB (12581052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595da46d1a481531e6344c5adb8de42d74921f4cba522c56077b7e3a93fe6893`  
		Last Modified: Mon, 13 Jun 2022 21:46:36 GMT  
		Size: 218.3 KB (218290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
