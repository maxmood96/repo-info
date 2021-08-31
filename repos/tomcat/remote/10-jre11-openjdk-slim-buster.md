## `tomcat:10-jre11-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:b61ebe2601a21d3c6090ca569b5df78c861c45f39d8ff3413717b75592242c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomcat:10-jre11-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:e15572412bc9da96c99dc77d0b0107b4f269d5e1e8e9ccae8cab667fcbd47513
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92334246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b42dc118486b8ac3748fdce8d1735aea2eaa0a1b180d311582c01dfea766e2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:54:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 17 Aug 2021 06:54:45 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 17 Aug 2021 06:54:45 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:54:45 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:54:45 GMT
ENV JAVA_VERSION=11.0.12
# Tue, 17 Aug 2021 06:55:30 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Tue, 31 Aug 2021 20:27:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 31 Aug 2021 20:27:24 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 20:27:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 31 Aug 2021 20:27:26 GMT
WORKDIR /usr/local/tomcat
# Tue, 31 Aug 2021 20:27:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 31 Aug 2021 20:27:27 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 31 Aug 2021 20:27:27 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 31 Aug 2021 20:27:27 GMT
ENV TOMCAT_MAJOR=10
# Tue, 31 Aug 2021 20:37:50 GMT
ENV TOMCAT_VERSION=10.0.10
# Tue, 31 Aug 2021 20:37:51 GMT
ENV TOMCAT_SHA512=3f6d5d292ab67348b3134c1013044c948caf5a4bf142b4e856b5ee63693a6e80994b0b4dbb3404d0fd3542fd6f7f52b4cbe404fc5a0f716ac98d68db879b7112
# Tue, 31 Aug 2021 20:37:51 GMT
COPY dir:192a5f5f807b77d3f08b2967a800935f1da29b4bbe82bbef37e012743dfd7367 in /usr/local/tomcat 
# Tue, 31 Aug 2021 20:37:56 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 20:37:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 31 Aug 2021 20:37:58 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 20:37:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427b7134c0c7b2e1d9cc703e20a84b850cbbf34ef654cfa0db710678a99da78b`  
		Last Modified: Tue, 17 Aug 2021 07:00:00 GMT  
		Size: 3.3 MB (3268768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea848f5155d0f648fc7fd258de1ce56d16d1ab42c2745a55e8adf26f997b45b`  
		Last Modified: Tue, 17 Aug 2021 07:02:46 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663bffc94428db61042052aaa00b98a379ea871642fce53bdc8ac9e06754493b`  
		Last Modified: Tue, 17 Aug 2021 07:03:45 GMT  
		Size: 47.1 MB (47137229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd20e69b9378f2da4b977d0d55f29a6aacf553a02052364a4d3842cf50fa8a8`  
		Last Modified: Tue, 31 Aug 2021 21:33:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67092265a5c81e939b5146cdca47a4e34dbbf322c4a2ea812edd47db0f49e8d`  
		Last Modified: Tue, 31 Aug 2021 21:39:36 GMT  
		Size: 12.5 MB (12505405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442b1b49f8596e201c5714d27906474a7d60b6dde1319347f2b41100735863d3`  
		Last Modified: Tue, 31 Aug 2021 21:39:35 GMT  
		Size: 2.3 MB (2276346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d325d3e7da880224a996765e85eb8f34c4d86eadb1f3e982d87a46ca2fb9407`  
		Last Modified: Tue, 31 Aug 2021 21:39:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
