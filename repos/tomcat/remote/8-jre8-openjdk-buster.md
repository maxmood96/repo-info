## `tomcat:8-jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:c8cad0fb41b6c67765a370ab70e0b3c4fec020b7a710f90ae073f1a94b6b70f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:6e1d5fea6766b289d03083b85320a19a42f3904140b80d716c08a5aa85ef8186
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126854923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c5b8c956ea90882e634d49b8c7974c827e2f3bf16bc6c95805d19903dac43e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 16:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:37:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 12 Oct 2021 16:37:25 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Oct 2021 16:37:25 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 16:37:25 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:48:15 GMT
ENV JAVA_VERSION=8u312
# Thu, 21 Oct 2021 23:48:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 22 Oct 2021 00:28:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Oct 2021 00:28:04 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Oct 2021 00:28:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Oct 2021 00:28:05 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Oct 2021 00:28:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Oct 2021 00:28:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Oct 2021 00:50:20 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 22 Oct 2021 00:50:20 GMT
ENV TOMCAT_MAJOR=8
# Fri, 22 Oct 2021 00:50:21 GMT
ENV TOMCAT_VERSION=8.5.72
# Fri, 22 Oct 2021 00:50:21 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Fri, 22 Oct 2021 00:50:21 GMT
COPY dir:5363effac558b747bb1144e894edf233a32b2597a20347ff805708415e51aa3b in /usr/local/tomcat 
# Fri, 22 Oct 2021 00:50:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Oct 2021 00:50:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Oct 2021 00:50:28 GMT
EXPOSE 8080
# Fri, 22 Oct 2021 00:50:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926071273d78abc57f0ee894a7c609a97b18a29335e5a856a83535ab4eab675b`  
		Last Modified: Tue, 12 Oct 2021 16:53:48 GMT  
		Size: 5.5 MB (5531169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5418360573ae7b218a03404e088e2d78eb71a34c55088b9395dd155960241d39`  
		Last Modified: Tue, 12 Oct 2021 16:56:54 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f293130c16dc743b962fb1aa0110f93a9745e35e5aec1db31a7a48e5680683f0`  
		Last Modified: Fri, 22 Oct 2021 00:05:40 GMT  
		Size: 41.4 MB (41378116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635f1d4e7cb7a9b0e1d94541413811effc24967f3913b600b05cc2e67e53cb57`  
		Last Modified: Fri, 22 Oct 2021 01:13:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced8f1dfe1fc3ff92bc1b911bf853ce7d68c6e44e4b04e86b93a9b27dcaf1c1`  
		Last Modified: Fri, 22 Oct 2021 01:28:25 GMT  
		Size: 11.2 MB (11216448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff45d74a92a06fc3b4b09cd4d0e44809d7de8e752b81fd69a8963ebcb812080b`  
		Last Modified: Fri, 22 Oct 2021 01:28:24 GMT  
		Size: 460.9 KB (460919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d44c2bc2a6112cb2eff1504fef0f735b5f96c523f028772b2413e1d1f4634`  
		Last Modified: Fri, 22 Oct 2021 01:28:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:463581620f0f0a7ce49824f3b1b0021598e338574e563e03c811b63581c4faff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124276290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febffc24c129b01e9b01ea8ee60211b0c5039d816ff8acfb5c5282bee6fa5db8`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 21:59:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:01:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 17 Nov 2021 22:01:07 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 17 Nov 2021 22:01:07 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 22:01:08 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 22:01:09 GMT
ENV JAVA_VERSION=8u312
# Wed, 17 Nov 2021 22:01:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_8u312b07.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 18 Nov 2021 06:50:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 18 Nov 2021 06:50:43 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 06:50:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 18 Nov 2021 06:50:45 GMT
WORKDIR /usr/local/tomcat
# Thu, 18 Nov 2021 06:50:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 18 Nov 2021 06:50:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 18 Nov 2021 07:13:40 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 18 Nov 2021 07:13:41 GMT
ENV TOMCAT_MAJOR=8
# Thu, 18 Nov 2021 07:13:42 GMT
ENV TOMCAT_VERSION=8.5.73
# Thu, 18 Nov 2021 07:13:43 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Thu, 18 Nov 2021 07:13:45 GMT
COPY dir:d2203eada75d018a7f70e3891b0f77d471b54eee1819824e950d14e2dca27b70 in /usr/local/tomcat 
# Thu, 18 Nov 2021 07:13:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 07:13:52 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 18 Nov 2021 07:13:53 GMT
EXPOSE 8080
# Thu, 18 Nov 2021 07:13:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68bc1b9fc908d2ecc7d041954a367dcb743ea85f5b79ff3ae93ac0871355ebf`  
		Last Modified: Wed, 17 Nov 2021 22:14:57 GMT  
		Size: 5.5 MB (5505361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee54ccba463ffb26806c54540c1188e492a17dedc1f4db4e48cbfdce1f255142`  
		Last Modified: Wed, 17 Nov 2021 22:16:51 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febd88e1e693e703e43551bce2f2859c52ef72c6346f9fe9a16f414f16420467`  
		Last Modified: Wed, 17 Nov 2021 22:16:57 GMT  
		Size: 40.6 MB (40632007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadcfe5515588d27d9e0388d3279772ea0cd1aa35fbae628c45f168899b6880e`  
		Last Modified: Thu, 18 Nov 2021 07:44:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085ad64ebb0db1adeb3cc738fcb401636cd79954a3c55baaf01c558784788d01`  
		Last Modified: Thu, 18 Nov 2021 07:59:20 GMT  
		Size: 11.2 MB (11235125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cb43af1671f8d2d627c5883968eed84ba2d15d679c6572d0b2327c63232d0c`  
		Last Modified: Thu, 18 Nov 2021 07:59:19 GMT  
		Size: 218.2 KB (218162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
