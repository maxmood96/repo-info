## `tomcat:10-jre11-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:d3c05ae88d666fc19c47e2d463cc3777d55e537ad73dae24ba9718415504ee24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:10-jre11-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:fd39b6f297c91c02f27f590dac08f3d00f84c728d4cd9c8599efd29046c53648
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90521289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb326e2f51d53da287df33b857696b4b04c2d2c395e8a62e0f21036927e107e4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:53:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 20 Apr 2022 10:53:28 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:53:28 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:53:28 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:53:28 GMT
ENV JAVA_VERSION=11.0.14.1
# Wed, 20 Apr 2022 10:54:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 21 Apr 2022 04:27:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 04:27:06 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 04:27:07 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 04:27:07 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 04:27:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:27:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:27:07 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 21 Apr 2022 04:27:07 GMT
ENV TOMCAT_MAJOR=10
# Thu, 21 Apr 2022 04:31:55 GMT
ENV TOMCAT_VERSION=10.0.20
# Thu, 21 Apr 2022 04:31:55 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Thu, 21 Apr 2022 04:31:55 GMT
COPY dir:d116ae9a3c37e6fd8255b0b58e892a4058c35b0da1f44c9cae1a02d278424c5f in /usr/local/tomcat 
# Thu, 21 Apr 2022 04:31:59 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 04:32:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 04:32:00 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 04:32:00 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97724dec0639ffbe1d30e60defc8ff8fc2e27a3844e7c6173e64cb73e25b88`  
		Last Modified: Wed, 20 Apr 2022 11:02:57 GMT  
		Size: 3.3 MB (3273257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b642cc34186e8ecd452dd0c4cca4c6f7e661e0940a6488a160182eced0a84acd`  
		Last Modified: Wed, 20 Apr 2022 11:11:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451843aaecade4f972e1c91382bfcd6c210e5807661cf6211c0c2e15b89d4b4b`  
		Last Modified: Wed, 20 Apr 2022 11:13:45 GMT  
		Size: 47.2 MB (47165105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9522f3e50e4ee592b7ac3f689c801f02d55d3ec396137e61703fa139edfdfb`  
		Last Modified: Thu, 21 Apr 2022 05:03:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f58b99e1e8dba1cac3795daa60e8980693f705d36e510a15f22a742b9334f9`  
		Last Modified: Thu, 21 Apr 2022 05:09:28 GMT  
		Size: 12.6 MB (12554019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1c1fdd18f81905cea5d79b2426ce2b3e1aa396c79b0906f28b981bfe48ffc3`  
		Last Modified: Thu, 21 Apr 2022 05:09:27 GMT  
		Size: 387.7 KB (387732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4f4bf74c56faafac3689e4fc99d177e997374793cd0d2ccc41fb9412c106f0`  
		Last Modified: Thu, 21 Apr 2022 05:09:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:c10b8628195e06f06ffb11e66b63bf25679d3ee1266df3e4c17af7ed53ba1b46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87824707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4498c42284f827d8554309fe38b3fdc458d8f6aaa600bece9f5add8028ec965c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:25:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:32:37 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 20 Apr 2022 10:32:38 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:32:39 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:32:40 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:32:41 GMT
ENV JAVA_VERSION=11.0.14.1
# Wed, 20 Apr 2022 10:34:37 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 21 Apr 2022 06:03:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 06:03:59 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 06:04:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 06:04:01 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 06:04:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:04:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:04:04 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 21 Apr 2022 06:04:05 GMT
ENV TOMCAT_MAJOR=10
# Thu, 21 Apr 2022 06:10:33 GMT
ENV TOMCAT_VERSION=10.0.20
# Thu, 21 Apr 2022 06:10:34 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Thu, 21 Apr 2022 06:10:36 GMT
COPY dir:a01392eddadee9dcc14f9b410c3d1b6a26fd8eaabcff7d9c995d0d87dce51901 in /usr/local/tomcat 
# Thu, 21 Apr 2022 06:10:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 06:10:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 06:10:42 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 06:10:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef4c0391a581a54e4ae08706ac3173bf39e99722f6efe3a9094dbe8916d7bfd`  
		Last Modified: Wed, 20 Apr 2022 10:47:49 GMT  
		Size: 3.1 MB (3125683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98e615f0d4667817d0647ba9f2a1de21a29f09ac4865e1a2884ea98d5a37a97`  
		Last Modified: Wed, 20 Apr 2022 10:57:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3db2c50508fcf9274bc6fdbabdbf1437062173f3eca6ba8b9c3b870acb06e9`  
		Last Modified: Wed, 20 Apr 2022 10:59:49 GMT  
		Size: 46.0 MB (46049839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41248aebfce6697f749da265a7c2e9e7a1c1af3eaabfce02a90c1d09c804ef4`  
		Last Modified: Thu, 21 Apr 2022 08:42:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb63b6a9fb4f63ecfd83f5afc8032692d49e916bdc3e7afa36d2bd42ea75af2`  
		Last Modified: Thu, 21 Apr 2022 08:48:26 GMT  
		Size: 12.6 MB (12566859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdd52fb24b086651a1ebe50e90fd3bac65efba72dc775c98716b853301b908e`  
		Last Modified: Thu, 21 Apr 2022 08:48:25 GMT  
		Size: 173.6 KB (173629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
