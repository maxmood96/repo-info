## `tomee:plus`

```console
$ docker pull tomee@sha256:0ba9a97df3d7efd3510b3a72c582f70fedade5bd210a362d4230e51033015cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomee:plus` - linux; amd64

```console
$ docker pull tomee@sha256:2957ea0ec7256312411e8790a1f2a722eb5ace3ed7a57d497f6ce2b4a6425054
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193948181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279c15b7e0176f52af118c4a28c9531fad7aac21a2f7c5aa0c2e395a84b7a7b3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 28 May 2022 01:20:12 GMT
ADD file:dd3d4b31d7f1d4062ad0eb2d85dba064cea067b1eb4a8b89a0b593ea90001cdf in / 
# Sat, 28 May 2022 01:20:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:40:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 19:38:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 19:38:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 May 2022 19:38:32 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 19:38:32 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 19:38:32 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 19:38:33 GMT
ENV JAVA_VERSION=11.0.15
# Sat, 28 May 2022 19:38:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 28 May 2022 22:48:08 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 22:48:09 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 28 May 2022 22:48:09 GMT
WORKDIR /usr/local/tomee
# Sat, 28 May 2022 22:48:18 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 May 2022 22:48:18 GMT
ENV TOMEE_VER=8.0.11
# Sat, 28 May 2022 22:49:10 GMT
ENV TOMEE_BUILD=plus
# Sat, 28 May 2022 22:49:17 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Sat, 28 May 2022 22:49:17 GMT
EXPOSE 8080
# Sat, 28 May 2022 22:49:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e756f3fdd6a378aa16205b0f75d178b7532b110e86be7659004fc6a21183226c`  
		Last Modified: Sat, 28 May 2022 01:24:51 GMT  
		Size: 55.0 MB (55009253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf168a6748997eb97b48cc86234b7ff7d8bc907645b9be99013158b3f146b272`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 5.2 MB (5156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604223835ccf02d097187b5a58ca73e8598cadbb16a36202ca1943e97f56f1f`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 10.9 MB (10875008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b879d05afe7d1ed6ac0f5b2d9537450b8058210d5c1ba04e3dbdfd0ea7f44da0`  
		Last Modified: Sat, 28 May 2022 19:48:32 GMT  
		Size: 5.7 MB (5657595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67409f01891c54bb4d7cf58512ec5cef2762ae616c2ab81d132c671c585f27b4`  
		Last Modified: Sat, 28 May 2022 19:48:31 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777f3575eb5979e51c7805e2bf9b825868bbd06f981240a48991e55828c1f206`  
		Last Modified: Sat, 28 May 2022 19:48:38 GMT  
		Size: 47.2 MB (47197487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f82acc8703998790493535118cda90e2ca9ba4efa71953fc44671eb1e1f86a`  
		Last Modified: Sat, 28 May 2022 23:10:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a7996941bbd4d7b78bf1b434e2dcf4b62c31a3b53a98138dbe3a5139d78f50`  
		Last Modified: Sat, 28 May 2022 23:10:16 GMT  
		Size: 62.9 KB (62922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b859f3a7f2890abeeea9f96731da568304f4acac9ec0fa6d0a89b0ff739694`  
		Last Modified: Sat, 28 May 2022 23:16:33 GMT  
		Size: 70.0 MB (69989498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:cab6eb00a1857e235662d12dc0c91e317c4b4b3c562df6a4e85ab43c310bcb36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191493793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abeb713a5dad88ee8dfd30bcb25017d3e04477951c6b249e7a8233e47be393ae`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 28 May 2022 00:40:23 GMT
ADD file:a78273677555ebe8bac187f491203093eec62fa1c4f65f00ba2cf0cc2230992f in / 
# Sat, 28 May 2022 00:40:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:05:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 16:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 16:50:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Sat, 28 May 2022 16:50:25 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 16:50:26 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 16:50:27 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 16:50:28 GMT
ENV JAVA_VERSION=11.0.15
# Sat, 28 May 2022 16:50:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_linux_11.0.15_10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_aarch64_linux_11.0.15_10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Sat, 28 May 2022 18:36:49 GMT
ENV PATH=/usr/local/tomee/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 18:36:50 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 28 May 2022 18:36:51 GMT
WORKDIR /usr/local/tomee
# Sat, 28 May 2022 18:37:01 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 May 2022 18:37:01 GMT
ENV TOMEE_VER=8.0.11
# Sat, 28 May 2022 18:38:42 GMT
ENV TOMEE_BUILD=plus
# Sat, 28 May 2022 18:38:49 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Sat, 28 May 2022 18:38:50 GMT
EXPOSE 8080
# Sat, 28 May 2022 18:38:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d794814721d57f8aaec06ab3652e90212cc3beccf5ff5c87f6ecf8375784bcc8`  
		Last Modified: Sat, 28 May 2022 00:47:04 GMT  
		Size: 53.7 MB (53696947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62ee63325dbbad699d6845f68c2391db3bf158f60373849c2d1cb6bb479788`  
		Last Modified: Sat, 28 May 2022 11:17:05 GMT  
		Size: 4.9 MB (4938744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e37b4c58dd1db7ead6f3c2cdf757f490b4e29c958d2a70559c313e9a03a5ef`  
		Last Modified: Sat, 28 May 2022 11:17:06 GMT  
		Size: 10.7 MB (10657073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29312e2f0b2d2423a19b1e65da0020d22da272698007d994eb022cafc68c98dc`  
		Last Modified: Sat, 28 May 2022 17:06:29 GMT  
		Size: 5.6 MB (5649779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd89bea478de23120f9e854c805b853218e7d1c2b55ab2f0d9fa8a312c41bf12`  
		Last Modified: Sat, 28 May 2022 17:06:29 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ea084fee99e1a8783492e9519624f9d393b283f712e81f1af19c68ce1ce2a`  
		Last Modified: Sat, 28 May 2022 17:06:36 GMT  
		Size: 46.5 MB (46498872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e75e38aff0dee34f498461883797ca6c601a05b13a0e9871e4032743a7a381`  
		Last Modified: Sat, 28 May 2022 19:14:57 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598098ec4120c9b8dbaf8bda3ec2a6a5cc45ccf09ea9339fbf2a6d826100fe6e`  
		Last Modified: Sat, 28 May 2022 19:14:57 GMT  
		Size: 62.9 KB (62858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebd7bd03313325bca704a15bb889efaec21bfd50dd1ca11ac466ed15fa568fd`  
		Last Modified: Sat, 28 May 2022 19:22:30 GMT  
		Size: 70.0 MB (69989171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
