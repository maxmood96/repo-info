## `tomcat:8-jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:7404fe8ad78daceb2baba5d5ea2cacc07d636e446d0cd04cc2669e1c035e72ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:5c7dcf05b3f7abb2de4348c99c4f344b8f763391fa8154cc5e3d7886df215645
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126894516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0396419ff31a3c92393867153982ee6636b6072ab49180c4f716eb37e5d1fbd`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:59:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:59:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 10:54:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:56:22 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 20 Apr 2022 10:56:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:56:22 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:56:22 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:56:22 GMT
ENV JAVA_VERSION=8u322
# Wed, 20 Apr 2022 10:56:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 21 Apr 2022 04:33:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 04:33:19 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 04:33:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 04:33:19 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 04:33:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:33:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:49:53 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 21 Apr 2022 04:49:53 GMT
ENV TOMCAT_MAJOR=8
# Thu, 21 Apr 2022 04:49:53 GMT
ENV TOMCAT_VERSION=8.5.78
# Thu, 21 Apr 2022 04:49:53 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Thu, 21 Apr 2022 04:49:53 GMT
COPY dir:96ccc2270bbf6472f981fdafaf81b61b48a55fc29f9a3224f1db5706b8570700 in /usr/local/tomcat 
# Thu, 21 Apr 2022 04:49:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 04:49:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 04:49:58 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 04:49:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdd409f4b2bf3771fac1cbc2df46d1cbb4b800b154cfc33e8e0cd23e67ab3e0`  
		Last Modified: Wed, 20 Apr 2022 07:06:56 GMT  
		Size: 7.9 MB (7856378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3069e6cecf9d5e43ace0a925b53849b2fd189ef41883d45d8f2e12213c2c06`  
		Last Modified: Wed, 20 Apr 2022 07:06:56 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f81393f382611cf77dfb7e0e958aff2c06386dab286300b237441df9a07ef6`  
		Last Modified: Wed, 20 Apr 2022 11:13:16 GMT  
		Size: 5.5 MB (5532533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a53754fb28d2d41f1b5e59821b1d521fae12c802f79efb17560e3cc3a8c9f4d`  
		Last Modified: Wed, 20 Apr 2022 11:16:34 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25da910c8c7162f9e8f9657fc02eac7460d4d20b2bd17402f6cdc25a56548b4`  
		Last Modified: Wed, 20 Apr 2022 11:16:39 GMT  
		Size: 41.4 MB (41395119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e5b5df5ac7e715bf47cb9de6df05ef6cd5991d86c718ebeb6c4618f3d784d1`  
		Last Modified: Thu, 21 Apr 2022 05:11:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9026829048eb157db92fca49cc0458b31fb55d43047fa1c3940c147958c27`  
		Last Modified: Thu, 21 Apr 2022 07:06:14 GMT  
		Size: 11.2 MB (11214835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2071494b7426ba50e12b034d52a9b38b15898ed34c814cde2c97722c7604db`  
		Last Modified: Thu, 21 Apr 2022 07:06:13 GMT  
		Size: 460.9 KB (460924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8640eaca2df3df166c7d8a9b80ede3fa4d16a00d97aa329e06d38adf52f481`  
		Last Modified: Thu, 21 Apr 2022 07:06:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:3c402598094fe9d5eb95286bdc8a589e846274f5b754c3b8921a0d04aa8104f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124329713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4566539c2bfe1b408ea71e3f4fc3241ece5d55fff0782e6fdc4284a21da28e9f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:45:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 10:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:36:59 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 20 Apr 2022 10:37:00 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:37:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:37:02 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:37:03 GMT
ENV JAVA_VERSION=8u322
# Wed, 20 Apr 2022 10:37:08 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_linux_8u322b06.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 21 Apr 2022 06:13:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 06:13:04 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 06:13:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 06:13:06 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 06:13:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:13:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:36:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 21 Apr 2022 06:36:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 21 Apr 2022 06:36:51 GMT
ENV TOMCAT_VERSION=8.5.78
# Thu, 21 Apr 2022 06:36:52 GMT
ENV TOMCAT_SHA512=b50213e64cc1fd3da2847deda1ca13bee4c26663093c11d53c5ecfe4cdec8856e743b4a1d8488e0c0cbe9bf149e755df40a4140f3b155e2195e3bc6335de3512
# Thu, 21 Apr 2022 06:36:54 GMT
COPY dir:8ac53b160dfa020fe41b76e72a5ca635316b11112d4cfd150f2739d0f9377c0d in /usr/local/tomcat 
# Thu, 21 Apr 2022 06:36:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 06:36:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 06:37:00 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 06:37:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80651adb7e52d8ecd27d43b9e69ada9ca277071ea09607121d0076de36480b`  
		Last Modified: Wed, 20 Apr 2022 06:55:25 GMT  
		Size: 7.7 MB (7719745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38ee622cbfb492ebc3bc598771624fba7ef1830b4e0f9737f2bbf4b6ec0ea`  
		Last Modified: Wed, 20 Apr 2022 06:55:26 GMT  
		Size: 9.8 MB (9767312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd9ef6cd611a3f644d8e2dbd9072cca066d10483bb06b4db05027567e857821`  
		Last Modified: Wed, 20 Apr 2022 10:59:18 GMT  
		Size: 5.5 MB (5506710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2b8029f074801977d682a25323a6ee36cd9fb5c5cda266d5fc860005b5e2f8`  
		Last Modified: Wed, 20 Apr 2022 11:02:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a77b8eeb11c11d0863039682856c214aecdaa290b1497d6a2d3bfb8d6b56616`  
		Last Modified: Wed, 20 Apr 2022 11:02:57 GMT  
		Size: 40.7 MB (40659904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ec7086de6cd82e877ddec31736f794e31d2c4fa42b1ad94a2f36beba502c32`  
		Last Modified: Thu, 21 Apr 2022 08:50:47 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da7aa7f5bca0ee56eec4b2e56402819c10d624c5d29248e60455f1f0b74dd6c`  
		Last Modified: Thu, 21 Apr 2022 09:07:51 GMT  
		Size: 11.2 MB (11229727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdecb17226b1cd4b9722118c21c6d16cc6c63b4af810ba4c9332070b7282a5e`  
		Last Modified: Thu, 21 Apr 2022 09:07:50 GMT  
		Size: 218.2 KB (218228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
