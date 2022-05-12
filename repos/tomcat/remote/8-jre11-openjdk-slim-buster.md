## `tomcat:8-jre11-openjdk-slim-buster`

```console
$ docker pull tomcat@sha256:2cf4b44bfb65450f28f21035b8af07a7e42b764c0b5464e599e0e281d9078e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre11-openjdk-slim-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:2bbd431b8c0368252a3b76645b0d7c765f64107a986ebb25850d2d619a9179f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89500420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e59b25adb3f7f9e45a3134f55345a731fe701b7937df4987a2877f35534e45`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:50:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 11 May 2022 05:50:53 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 11 May 2022 05:50:53 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 05:50:53 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:50:53 GMT
ENV JAVA_VERSION=11.0.15
# Wed, 11 May 2022 05:52:25 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Wed, 11 May 2022 23:51:59 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 11 May 2022 23:51:59 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 23:52:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 11 May 2022 23:52:00 GMT
WORKDIR /usr/local/tomcat
# Wed, 11 May 2022 23:52:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 11 May 2022 23:52:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 12 May 2022 00:07:14 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 12 May 2022 00:07:14 GMT
ENV TOMCAT_MAJOR=8
# Thu, 12 May 2022 00:07:14 GMT
ENV TOMCAT_VERSION=8.5.78
# Thu, 12 May 2022 00:07:14 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Thu, 12 May 2022 00:07:15 GMT
COPY dir:2057ecb3cb1944f132ac163ab46d08428e32bb9e7f2171545344640441ea7116 in /usr/local/tomcat 
# Thu, 12 May 2022 00:07:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 00:07:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 12 May 2022 00:07:20 GMT
EXPOSE 8080
# Thu, 12 May 2022 00:07:20 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9930d1f61e9a044df90a13c9456f95b2e6b31da0c5f483757324dfe0a5fc33`  
		Last Modified: Wed, 11 May 2022 05:59:57 GMT  
		Size: 3.3 MB (3273265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e180b549d0140dd3a0f09953f26fcabcef901117b88f37992b70eac1d0b2ee3`  
		Last Modified: Wed, 11 May 2022 06:05:49 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88a38edf3851da662417ca2a0b02b9e7ef6cb78b69b8a3fe3e937fb3cb9cca6`  
		Last Modified: Wed, 11 May 2022 06:07:34 GMT  
		Size: 47.5 MB (47481995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4e9639ae4783cefe928e59225199272771f23597f3fd8566b1d493d9beee87`  
		Last Modified: Thu, 12 May 2022 00:20:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065dd6af29c05a096fc9e09b17a3187c2c50d4ca6bd04b8e68a53fdb4e58c3a6`  
		Last Modified: Thu, 12 May 2022 00:36:29 GMT  
		Size: 11.2 MB (11216253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0064210d39de4e80734c6abd24d4d3cbecfd81cc56a37f970104861d9def7f4`  
		Last Modified: Thu, 12 May 2022 00:36:28 GMT  
		Size: 387.7 KB (387673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7063cf8393813730c27b29acca744264f581384bdc86bc48ef224e64706e2c3b`  
		Last Modified: Thu, 12 May 2022 00:36:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-openjdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:14dd89e2fc1aed01fbd543704008a43f7daaabfa3751e95e0c0b080ee3d60bbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87005386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d985a997c24b672c0414e409dde71c3a1a52927131ded2d293b9d7f54a547f5d`
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
# Mon, 25 Apr 2022 18:46:36 GMT
ENV JAVA_VERSION=11.0.15
# Mon, 25 Apr 2022 18:47:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 25 Apr 2022 23:22:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Apr 2022 23:22:20 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Apr 2022 23:22:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Apr 2022 23:22:22 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Apr 2022 23:22:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Apr 2022 23:22:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Apr 2022 23:40:04 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 25 Apr 2022 23:40:05 GMT
ENV TOMCAT_MAJOR=8
# Mon, 25 Apr 2022 23:40:06 GMT
ENV TOMCAT_VERSION=8.5.78
# Mon, 25 Apr 2022 23:40:07 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Mon, 25 Apr 2022 23:40:09 GMT
COPY dir:b923ee6ab57f5f95f0d4cacaa9025c424696beda728905a4168a5f377457a112 in /usr/local/tomcat 
# Mon, 25 Apr 2022 23:40:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Apr 2022 23:40:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Apr 2022 23:40:15 GMT
EXPOSE 8080
# Mon, 25 Apr 2022 23:40:16 GMT
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
	-	`sha256:af8dab8e0d8e1687dff848d5de31b7847170c34cb2dec670652b60bf63bf1381`  
		Last Modified: Mon, 25 Apr 2022 19:09:24 GMT  
		Size: 46.6 MB (46566824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec38df88037f674bc63b8a35ec0ab28168fb69331947aad481b4808f956b906`  
		Last Modified: Tue, 26 Apr 2022 00:02:34 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c4466f66fc2e863401f2e038806edc1de9594e377fb74e61d9c261de798d62`  
		Last Modified: Tue, 26 Apr 2022 00:16:57 GMT  
		Size: 11.2 MB (11230523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7c701cae93f255a7869399a1dcb076a5b357ec77181400eaa4714b0e889b89`  
		Last Modified: Tue, 26 Apr 2022 00:16:56 GMT  
		Size: 173.7 KB (173658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
