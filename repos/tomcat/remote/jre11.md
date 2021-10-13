## `tomcat:jre11`

```console
$ docker pull tomcat@sha256:3bac3e6e1af33b3119c976b5c3277e3a34e21158c065c88540590c833d97d2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre11` - linux; amd64

```console
$ docker pull tomcat@sha256:ff1d7e09d40a2f683d9c1560e608bb8d77c8500c2aa41a2bcaf1166d87264964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136389809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6d4114b8aeb9729909b0e2b8c95cc7c63d57fea9fe7239d5f2598a50d2a260`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:25 GMT
ADD file:d05a14b1e57f9cc8eeb316a843403bbb35176d6222d60d6ddbb34faba977e316 in / 
# Tue, 28 Sep 2021 01:22:25 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:49:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 01:50:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 28 Sep 2021 09:22:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:22:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 28 Sep 2021 09:22:47 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 28 Sep 2021 09:22:48 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 09:22:48 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 09:22:48 GMT
ENV JAVA_VERSION=11.0.12
# Tue, 28 Sep 2021 09:23:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 29 Sep 2021 11:14:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 29 Sep 2021 11:14:31 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 11:14:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 29 Sep 2021 11:14:32 GMT
WORKDIR /usr/local/tomcat
# Wed, 29 Sep 2021 11:14:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 11:14:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 11:14:33 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 29 Sep 2021 11:14:33 GMT
ENV TOMCAT_MAJOR=10
# Wed, 06 Oct 2021 19:11:09 GMT
ENV TOMCAT_VERSION=10.0.12
# Wed, 06 Oct 2021 19:11:09 GMT
ENV TOMCAT_SHA512=e084fc0cc243c0a9ac7de85ffd4b96d00b40b5493ed7ef276d91373fe8036bc953406cd3c48db6b5ae116f2af162fd1bfb13ecdddf5d64523fdd69a9463de8a3
# Wed, 06 Oct 2021 19:11:09 GMT
COPY dir:83ab0aa093519444bdef1253bde7e93d1f3c5c241a7cf03e0cf73454fc161150 in /usr/local/tomcat 
# Wed, 06 Oct 2021 19:11:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 19:11:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Oct 2021 19:11:16 GMT
EXPOSE 8080
# Wed, 06 Oct 2021 19:11:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:df5590a8898bedd76f02205dc8caa5cc9863267dbcd8aac038bcd212688c1cc7`  
		Last Modified: Tue, 28 Sep 2021 01:28:33 GMT  
		Size: 54.9 MB (54927682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705bb4cb554eb7751fd21a994f6f32aee582fbe5ea43037db6c43d321763992b`  
		Last Modified: Tue, 28 Sep 2021 01:57:51 GMT  
		Size: 5.2 MB (5153152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519df5fceacdeaadeec563397b1d9f4d7c29c9f6eff879739cab6f0c144f49e1`  
		Last Modified: Tue, 28 Sep 2021 01:57:51 GMT  
		Size: 10.9 MB (10871798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc850b11e97cfdecca53799a94b78db748c40ae0a76694dbc10af9cd746c1229`  
		Last Modified: Tue, 28 Sep 2021 09:45:06 GMT  
		Size: 5.7 MB (5653948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7b60a356cdce9314bde5a6d6241e05e624f74c375fb2e3429522af7d177585`  
		Last Modified: Tue, 28 Sep 2021 09:45:05 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4852932383b995dd06cd3a26725cff2a5aa9211bf381867863db4f932333b1`  
		Last Modified: Tue, 28 Sep 2021 09:45:13 GMT  
		Size: 46.9 MB (46853910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3361dc5090a6a5d6047d9d14d6ae1872106f35726df6af42015bb62eb2de7b73`  
		Last Modified: Wed, 29 Sep 2021 12:23:23 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a2525465c46bf19058148aa2bd8fb4d7f0e60f2d2ab02bcfce7a994be71d76`  
		Last Modified: Wed, 06 Oct 2021 20:01:38 GMT  
		Size: 12.5 MB (12469347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a302736e19fac90b98b79dc51d6d3219b8138d1737d241f9c626fa1e59f0d2ac`  
		Last Modified: Wed, 06 Oct 2021 20:01:37 GMT  
		Size: 459.5 KB (459459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f5f6853777db26a5c25ed15a51e4da4b36ae551925a5e6cc29378c034a3abd`  
		Last Modified: Wed, 06 Oct 2021 20:01:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre11` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:c09b4d3f46891e840b39e954c7cd416e64f26a4e0c75400f0174273990bdb328
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133888828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48bb7d87a3154d081a3b4c20898e1450b271070adf99f6b97871bd2b6e04ad6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:04 GMT
ADD file:1529ae12e334fd992892d3fb97c103297cff7e0115b0475bec4c093939a2bff7 in / 
# Tue, 12 Oct 2021 01:41:04 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:10:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 02:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 06:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 06:11:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 13 Oct 2021 06:11:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 13 Oct 2021 06:11:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 06:11:33 GMT
ENV LANG=C.UTF-8
# Wed, 13 Oct 2021 06:11:34 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 13 Oct 2021 06:11:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 13 Oct 2021 08:37:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 13 Oct 2021 08:37:54 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 08:37:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 13 Oct 2021 08:37:56 GMT
WORKDIR /usr/local/tomcat
# Wed, 13 Oct 2021 08:37:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:37:58 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 13 Oct 2021 08:37:59 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 13 Oct 2021 08:38:00 GMT
ENV TOMCAT_MAJOR=10
# Wed, 13 Oct 2021 08:51:55 GMT
ENV TOMCAT_VERSION=10.0.12
# Wed, 13 Oct 2021 08:51:56 GMT
ENV TOMCAT_SHA512=e084fc0cc243c0a9ac7de85ffd4b96d00b40b5493ed7ef276d91373fe8036bc953406cd3c48db6b5ae116f2af162fd1bfb13ecdddf5d64523fdd69a9463de8a3
# Wed, 13 Oct 2021 08:51:58 GMT
COPY dir:d0f55ca777cc37b5a74a9c34cf50afd4e20127c92048d59d86f4f17680635b5b in /usr/local/tomcat 
# Wed, 13 Oct 2021 08:52:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 08:52:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Oct 2021 08:52:03 GMT
EXPOSE 8080
# Wed, 13 Oct 2021 08:52:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1c47a423366578e5ce665d03788914bf0459485a627a27896fa9c5663ce55cdf`  
		Last Modified: Tue, 12 Oct 2021 01:47:41 GMT  
		Size: 53.6 MB (53603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580c36351f836fd83ee4aee909834823b15f90ce0ec580f869717dc3679a020b`  
		Last Modified: Tue, 12 Oct 2021 02:18:53 GMT  
		Size: 5.1 MB (5142731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b655be758028f8234aab1f828dc2f79ee5abf3ce0a85560430b5f7c806367d1`  
		Last Modified: Tue, 12 Oct 2021 02:18:53 GMT  
		Size: 10.9 MB (10872848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e801adad0b6a144db48e53949b8f0c2e7eb8cd8e802e8e667ccfe21d8df8d`  
		Last Modified: Wed, 13 Oct 2021 06:41:02 GMT  
		Size: 5.6 MB (5647116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcb5c4bb6a744f5bc0b0da7fe0a235b50bf7a358ebba0d09048976f8552b68f`  
		Last Modified: Wed, 13 Oct 2021 06:41:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f420e94ad080c512407bfa2bde2c8362b24753c4274421a27aed3cb8f1ed7d`  
		Last Modified: Wed, 13 Oct 2021 06:41:08 GMT  
		Size: 45.9 MB (45925278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f73c0847a6f876980e65dcf9ef714321174153dd5e8be49e89b40cecf8fe131`  
		Last Modified: Wed, 13 Oct 2021 10:18:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dff31ee9ac061a38033b775088768a268a7faad7e89ebbf520f3cccd6019b6`  
		Last Modified: Wed, 13 Oct 2021 10:28:57 GMT  
		Size: 12.5 MB (12480450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639338c584f7d0b5d65fbb9717567eb088737d04890588f8feb2ece46347cfff`  
		Last Modified: Wed, 13 Oct 2021 10:28:56 GMT  
		Size: 217.0 KB (217038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
