## `tomcat:10-jre11-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:f4bac388b79eb0eba588f25611d5d3c35000b9ee157bd919dcc340321fad6c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jre11-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:c4592a528e8eacf3744e799d08627bf96a13ad5112c91fc36d6bdf94fa848869
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90531931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81006dd555ffc141c573ea471704e2405a2e81047a38b69ea24334da7955f769`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:27:33 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Jan 2022 09:27:34 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:27:34 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:27:34 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:38:55 GMT
ENV JAVA_VERSION=11.0.14
# Thu, 03 Feb 2022 20:44:02 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_11.0.14_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_11.0.14_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 04 Feb 2022 01:36:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Feb 2022 01:36:20 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 01:36:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Feb 2022 01:36:20 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Feb 2022 01:36:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:36:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:36:21 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 04 Feb 2022 01:36:21 GMT
ENV TOMCAT_MAJOR=10
# Fri, 04 Feb 2022 01:41:07 GMT
ENV TOMCAT_VERSION=10.0.16
# Fri, 04 Feb 2022 01:41:07 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Fri, 04 Feb 2022 01:41:08 GMT
COPY dir:f61039fa60ed27200ac9a4ef79f69d3dca8e035c74b3fa633fa15e3d8a74c0be in /usr/local/tomcat 
# Fri, 04 Feb 2022 01:41:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Feb 2022 01:41:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Feb 2022 01:41:15 GMT
EXPOSE 8080
# Fri, 04 Feb 2022 01:41:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa8d0f5eb646a53df0b867301afa43404e868c540fdf170240578844dfd0d6b`  
		Last Modified: Wed, 26 Jan 2022 09:43:10 GMT  
		Size: 3.3 MB (3269688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26703fd9b538d0033bb6b086787138d6495f4c06aa58d045911dbe78a87a299`  
		Last Modified: Wed, 26 Jan 2022 09:53:21 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89bc310d41cf876071cb4d113778c7a0b8f0a542482e1ff2d16f1f77e774374`  
		Last Modified: Thu, 03 Feb 2022 21:01:42 GMT  
		Size: 47.2 MB (47172366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098b483c67294cc61d787281ad7b3357ec2ee0a3dd11091ae9a6e41fcba59b00`  
		Last Modified: Fri, 04 Feb 2022 02:19:24 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20251605372178724e0ef403e184972702cf7b10090ebb7a5e8cc939c3be7dbc`  
		Last Modified: Fri, 04 Feb 2022 02:23:30 GMT  
		Size: 12.5 MB (12547902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf80269a19406534dd18b4e7ef8bf735b56036e163c0128935d3b307085aa407`  
		Last Modified: Fri, 04 Feb 2022 02:23:29 GMT  
		Size: 387.7 KB (387730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2d5fc0903b8f035d480fa639a0c93bf620a1534c4ab204feeba819864de67f`  
		Last Modified: Fri, 04 Feb 2022 02:23:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b4bd88bd914cb988c210ce46e17c0d37dd592908023976e3ba98d22bc412aa4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87827867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac765a625cd0a758f4ef960bc53b5f29842b91be815759c7d0c77d509b5547d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:56 GMT
ADD file:796bc43a948899ba53bddebf7f613769fe96e8ea3a27eb7143d079c7a166ab01 in / 
# Wed, 26 Jan 2022 01:42:57 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:58:38 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Jan 2022 05:58:39 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 05:58:40 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:58:41 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:53:05 GMT
ENV JAVA_VERSION=11.0.14
# Thu, 03 Feb 2022 20:55:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_11.0.14_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_11.0.14_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 04 Feb 2022 00:46:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Feb 2022 00:46:13 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 00:46:14 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Feb 2022 00:46:15 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Feb 2022 00:46:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 00:46:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 00:46:18 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 04 Feb 2022 00:46:19 GMT
ENV TOMCAT_MAJOR=10
# Fri, 04 Feb 2022 00:53:33 GMT
ENV TOMCAT_VERSION=10.0.16
# Fri, 04 Feb 2022 00:53:33 GMT
ENV TOMCAT_SHA512=9b70f4db2c7b2efb5453cd581322b1137df7b6443acd6a8e278eaaf97de89c9ad0c7c7996a2d545ef1e4d965aca43c40d2b2c7d5e46b021695f87093143fbba2
# Fri, 04 Feb 2022 00:53:35 GMT
COPY dir:77080e72ea3b23c0aed7d6dd525570f2d366a7c4ea83717388f36fa43c851901 in /usr/local/tomcat 
# Fri, 04 Feb 2022 00:53:38 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Feb 2022 00:53:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Feb 2022 00:53:41 GMT
EXPOSE 8080
# Fri, 04 Feb 2022 00:53:42 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4c7c9f6f1115fd4f35807a2f6c1375759365a991748aee0111873e55255f150b`  
		Last Modified: Wed, 26 Jan 2022 01:49:55 GMT  
		Size: 25.9 MB (25923216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a5c9716b24a17043a5d8ede1303daffeaaa07ff0393fa14caed54f01154833`  
		Last Modified: Wed, 26 Jan 2022 06:14:50 GMT  
		Size: 3.1 MB (3118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a17aecfab787a677b438c0036f44f4493389f53ef1bd17f65127c02a4dbdbb0`  
		Last Modified: Wed, 26 Jan 2022 06:25:36 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d6f61d7c12a61283904474d7f986e696c164af1d13299640bba8b350ef8ac9`  
		Last Modified: Thu, 03 Feb 2022 21:16:50 GMT  
		Size: 46.1 MB (46050399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccba8e7995d52d8286007448f215c37c620716e63ada5d6a9d24c4f75e1251a`  
		Last Modified: Fri, 04 Feb 2022 01:47:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb344cbd5a3b0e6161d0732f205cfcc5bcc31929bf909bd6ee13a109392d68`  
		Last Modified: Fri, 04 Feb 2022 01:52:32 GMT  
		Size: 12.6 MB (12561414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f9bd8c7e469e280e61270ddeb09d50aff227ba8e6d59537aeb56f26b4c09fb`  
		Last Modified: Fri, 04 Feb 2022 01:52:31 GMT  
		Size: 173.6 KB (173632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
