## `tomcat:8-jre11-openjdk`

```console
$ docker pull tomcat@sha256:2287d28ff30bfaeca6be2291d69c618fa28086b12d41491bc3214ead9527d7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre11-openjdk` - linux; amd64

```console
$ docker pull tomcat@sha256:dd46901e29fc2e8b3745f1f7ad988a9c834c42e8a63ec524116c4cfed1960411
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (135047454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d9b3bd7dc24cee29b6b6a5fcf16ff9fb34393d8aafeb2ecb869edebbea690d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:30 GMT
ADD file:aea313ae50ce6474a3df142b34d4dcba4e7e0186ea6fe55389cb2ea903b9ebbb in / 
# Tue, 12 Oct 2021 01:20:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:42:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 16:34:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:34:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 12 Oct 2021 16:34:27 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 12 Oct 2021 16:34:28 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 16:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:45:12 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 21 Oct 2021 23:45:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 22 Oct 2021 00:17:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Oct 2021 00:17:00 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Oct 2021 00:17:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Oct 2021 00:17:01 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Oct 2021 00:17:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Oct 2021 00:17:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Oct 2021 00:44:49 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 22 Oct 2021 00:44:49 GMT
ENV TOMCAT_MAJOR=8
# Fri, 22 Oct 2021 00:44:50 GMT
ENV TOMCAT_VERSION=8.5.72
# Fri, 22 Oct 2021 00:44:50 GMT
ENV TOMCAT_SHA512=41d7eb83120f210d238d8653d729bfb2be32f3666e6c04e73607c05f066c4136b0719f8107cf66673333548c82dc5b9c0357e91fc0ac845e64f055b598f27049
# Fri, 22 Oct 2021 00:44:50 GMT
COPY dir:55d0954fdbbc35ba1c04b04e693ab05ced087a0c613541dcb71a38b3f7e031ab in /usr/local/tomcat 
# Fri, 22 Oct 2021 00:44:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Oct 2021 00:44:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Oct 2021 00:44:57 GMT
EXPOSE 8080
# Fri, 22 Oct 2021 00:44:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bb7d5a84853b217ac05783963f12b034243070c1c9c8d2e60ada47444f3cce04`  
		Last Modified: Tue, 12 Oct 2021 01:25:37 GMT  
		Size: 54.9 MB (54917520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b617c6a8c415a175f44d7e2c5d3b521059f2a6112c5f022e005a44a759f2d`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 5.2 MB (5153273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32e17419b7ee61bbd89c2f0d2833a99cf45e594257d15cb567e4cf7771ce34a`  
		Last Modified: Tue, 12 Oct 2021 15:52:48 GMT  
		Size: 10.9 MB (10871935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab18cfab55f9b2e1184b3f5b90de6574c96bdf1c4c782f4e1879437c38541af9`  
		Last Modified: Tue, 12 Oct 2021 16:53:01 GMT  
		Size: 5.7 MB (5653928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456af490083536571b21f8d4e36b4389643d52bad004931fbe8f9a848d1deea1`  
		Last Modified: Tue, 12 Oct 2021 16:53:00 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc1853977f802fc2193d1f8015605d449463b98d290a0c9cca3447bc9c95c3f`  
		Last Modified: Fri, 22 Oct 2021 00:00:57 GMT  
		Size: 46.8 MB (46831678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002f792d6978910dda3343b6bd8836a8ce423686e87d24e2aef23e9f93e3c65c`  
		Last Modified: Fri, 22 Oct 2021 01:04:57 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c3539dbce9136e712fe5f430968c11a12b1f2a090fef74beec4f7f18b49b8f`  
		Last Modified: Fri, 22 Oct 2021 01:24:38 GMT  
		Size: 11.2 MB (11158992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d270bf504bbc55e24e99d5a2d59c5f728c5606e8151a7f9dc6e4d1d2ddcea076`  
		Last Modified: Fri, 22 Oct 2021 01:24:36 GMT  
		Size: 459.6 KB (459615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbdf7cfc8ce5b8e1acae6d2445b3f3d08ca861288f6d1768f63a35fa29aef8d`  
		Last Modified: Fri, 22 Oct 2021 01:24:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-openjdk` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:85cfa4a48f0f09b124328640888d9bf433f36b5a17516eefd1ac5aa5b7b42b89
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132168556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b59b6c58dbd819a1c4eda828faab8e923651addb3774c611b40617ef0747df4`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:59 GMT
ADD file:eb667e18226da8a1ca5a41beacddc65cd1efec01c3d01e50845c5e89e91ea17c in / 
# Wed, 17 Nov 2021 02:40:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:26:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:26:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 21:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 21:58:35 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 17 Nov 2021 21:58:36 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 17 Nov 2021 21:58:37 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:58:38 GMT
ENV LANG=C.UTF-8
# Wed, 17 Nov 2021 21:58:39 GMT
ENV JAVA_VERSION=11.0.13
# Wed, 17 Nov 2021 21:58:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_linux_11.0.13_8.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 18 Nov 2021 06:41:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 18 Nov 2021 06:41:42 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 06:41:43 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 18 Nov 2021 06:41:44 GMT
WORKDIR /usr/local/tomcat
# Thu, 18 Nov 2021 06:41:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 18 Nov 2021 06:41:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 18 Nov 2021 07:06:07 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 18 Nov 2021 07:06:08 GMT
ENV TOMCAT_MAJOR=8
# Thu, 18 Nov 2021 07:06:09 GMT
ENV TOMCAT_VERSION=8.5.73
# Thu, 18 Nov 2021 07:06:10 GMT
ENV TOMCAT_SHA512=4d33760d007acc5271ba0f946d2be96f6146d4632e411c9b72d351fc49d08355e8b84b051713a2f580e0f633cbe4409b7e9bb0e62f3af8d1094c6e4b3fdb96f0
# Thu, 18 Nov 2021 07:06:12 GMT
COPY dir:f56cb8f116e1343f900a288506fd7ee75e9427a71fee853b6dbe73ced5ce7e9c in /usr/local/tomcat 
# Thu, 18 Nov 2021 07:06:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 07:06:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 18 Nov 2021 07:06:18 GMT
EXPOSE 8080
# Thu, 18 Nov 2021 07:06:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ce18cd0ba11c2dfa8c1a2d2b325e1e019b14d4ae25ffdeffb0f9686c5496bf5c`  
		Last Modified: Wed, 17 Nov 2021 02:46:45 GMT  
		Size: 53.6 MB (53619024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f138a340a2373acc72dcc4ea9ef08bdf5648aabc5fe08f7e8d25222ca63b7ee`  
		Last Modified: Wed, 17 Nov 2021 13:36:26 GMT  
		Size: 4.9 MB (4937639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34c030205ccb8656e30a58f96bb1edbe7c59bf17f3329ae3c442ec897f2b270`  
		Last Modified: Wed, 17 Nov 2021 13:36:27 GMT  
		Size: 10.7 MB (10655878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cda574254477c28979f32127ceea6240baf5deb81f044ae6047d126443eaf8f`  
		Last Modified: Wed, 17 Nov 2021 22:14:32 GMT  
		Size: 5.6 MB (5647104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56fb01b48224eff4625f5159ad31b2bff2cb66466a52f42cec76ce6ea42a55e`  
		Last Modified: Wed, 17 Nov 2021 22:14:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c4a31c6d6f6e128f7b52e6d130dd84ec6b89a7f822374f9dbe1f85e7c34c3c`  
		Last Modified: Wed, 17 Nov 2021 22:14:39 GMT  
		Size: 45.9 MB (45919494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444ff59d3a36b7dd4bbf6ec6deb495f1f28d41cce6f5272aae2819368c24bd80`  
		Last Modified: Thu, 18 Nov 2021 07:37:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c13a07f3c9009f3c9b96a7916c3851fb5dbfa39ab5dbb38b3e62dd1f3d4f04`  
		Last Modified: Thu, 18 Nov 2021 07:54:23 GMT  
		Size: 11.2 MB (11172087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683e8777107a0f5d5013c7f1b517b0387cb13b7c1c045c38e1ea1f5db1f939c0`  
		Last Modified: Thu, 18 Nov 2021 07:54:22 GMT  
		Size: 217.0 KB (216981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
