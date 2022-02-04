## `tomcat:8-jre11-openjdk-bullseye`

```console
$ docker pull tomcat@sha256:6f88d6c2cb5ad65e055579682b7adf7ac5dcff7f8024b5e980a07e70d0e2ed54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:8-jre11-openjdk-bullseye` - linux; amd64

```console
$ docker pull tomcat@sha256:4f332c26be9cb39840359545a6d36c525e72cd7ffae19298fc5ab02363602642
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135105944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d47cbde39ad874721d697225990a84c8e2b58fa141fee49ee745401884de27`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:22 GMT
ADD file:9cca7f8e4abcd8309501cad216ff33a28932386ded66461a7591c0fdf2c859d3 in / 
# Wed, 26 Jan 2022 01:40:23 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:11:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:12:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 09:28:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:28:19 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Jan 2022 09:28:20 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 09:28:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:28:21 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:40:17 GMT
ENV JAVA_VERSION=11.0.14
# Thu, 03 Feb 2022 20:41:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_11.0.14_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_11.0.14_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 04 Feb 2022 01:32:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Feb 2022 01:32:44 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 01:32:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Feb 2022 01:32:45 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Feb 2022 01:32:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:32:45 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:57:19 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 04 Feb 2022 01:57:19 GMT
ENV TOMCAT_MAJOR=8
# Fri, 04 Feb 2022 01:57:19 GMT
ENV TOMCAT_VERSION=8.5.75
# Fri, 04 Feb 2022 01:57:19 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Fri, 04 Feb 2022 01:57:20 GMT
COPY dir:752533259056412dbc4413e982c9d9d8d7ddd413fdef29ae579aac03be1c0332 in /usr/local/tomcat 
# Fri, 04 Feb 2022 01:57:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Feb 2022 01:57:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Feb 2022 01:57:28 GMT
EXPOSE 8080
# Fri, 04 Feb 2022 01:57:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:0c6b8ff8c37e92eb1ca65ed8917e818927d5bf318b6f18896049b5d9afc28343`  
		Last Modified: Wed, 26 Jan 2022 01:46:07 GMT  
		Size: 54.9 MB (54917164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412caad352a3ecbb29c080379407ae0761e7b9b454f7239cbfd1d1da25e06b29`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 5.2 MB (5152685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d3e61f7a504fa66d7275123969e9917570188650eb84b2280a726b996040f6`  
		Last Modified: Wed, 26 Jan 2022 02:22:09 GMT  
		Size: 10.9 MB (10871783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd32ce0efa70eec9871a7cd5114ec448a2e5a97856007ca63d35543654aaa644`  
		Last Modified: Wed, 26 Jan 2022 09:54:06 GMT  
		Size: 5.7 MB (5653867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121319d3ac5169400ac10eb302063eb2a5920dbe134656057055ab8c364fb467`  
		Last Modified: Wed, 26 Jan 2022 09:54:05 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856a383ccf5d6c87dddf3cd2b97acaecc78eed45f4b954de53d85f6595ea2d16`  
		Last Modified: Thu, 03 Feb 2022 21:00:38 GMT  
		Size: 46.9 MB (46879610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acc28f6e8b54f89b5c3548485917fd5369b946d31b315c3c7a75419b678901a`  
		Last Modified: Fri, 04 Feb 2022 02:17:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a7660e3bbd0bea58cd7ac84fb56269f52b5fb0cda841a641bd3db48e70d96e`  
		Last Modified: Fri, 04 Feb 2022 04:14:31 GMT  
		Size: 11.2 MB (11170803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429331478d8dc153174c13b5dd6ae2ed365c6a4a4b3fcb00ef010891240edd`  
		Last Modified: Fri, 04 Feb 2022 04:14:31 GMT  
		Size: 459.5 KB (459519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa20061dfe9d8e8a0c6cb9d67e02e3f7bd425b9f09c9c80a814d202e515a1cc4`  
		Last Modified: Fri, 04 Feb 2022 04:14:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre11-openjdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7dd64e0d32be1962ecd528941ef0f32a2e5229b1e4d3b5a3cec05f94eda2185a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132428422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15047e624772ee6c8058142dc71e4a73bd75233e870c06f1a9c986166ce12d6`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:15 GMT
ADD file:b6338a9c3c2f8d7ba1a23dcb7a1389c7d0eab75a7489ef66f21c773be56aa9ed in / 
# Wed, 26 Jan 2022 01:42:16 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:13:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:13:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 05:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:59:17 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 26 Jan 2022 05:59:18 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 26 Jan 2022 05:59:19 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:59:20 GMT
ENV LANG=C.UTF-8
# Thu, 03 Feb 2022 20:54:08 GMT
ENV JAVA_VERSION=11.0.14
# Thu, 03 Feb 2022 20:54:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_x64_linux_11.0.14_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14%2B9/OpenJDK11U-jre_aarch64_linux_11.0.14_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 04 Feb 2022 00:40:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 04 Feb 2022 00:40:35 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 00:40:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 04 Feb 2022 00:40:37 GMT
WORKDIR /usr/local/tomcat
# Fri, 04 Feb 2022 00:40:38 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 00:40:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 04 Feb 2022 01:17:17 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 04 Feb 2022 01:17:18 GMT
ENV TOMCAT_MAJOR=8
# Fri, 04 Feb 2022 01:17:19 GMT
ENV TOMCAT_VERSION=8.5.75
# Fri, 04 Feb 2022 01:17:20 GMT
ENV TOMCAT_SHA512=b86d191506f8a647e3f4505bb7cc095068abb26bb4283562924913606514ce15930a467bd5d20c09b11d785827bf1914ed869b48dfb1c95e9f826e4c8b4e8aaa
# Fri, 04 Feb 2022 01:17:22 GMT
COPY dir:58247f0fb5c417008a0ce77ee2b49cc817872b8d2fd0669f9f15d7a02dae7042 in /usr/local/tomcat 
# Fri, 04 Feb 2022 01:17:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Feb 2022 01:17:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 04 Feb 2022 01:17:28 GMT
EXPOSE 8080
# Fri, 04 Feb 2022 01:17:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:39ab78bc09e79a21f719ced771689354d1948f4afd57e86afed8dac6ffb47826`  
		Last Modified: Wed, 26 Jan 2022 01:48:34 GMT  
		Size: 53.6 MB (53608848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf88d09fc28807e643d4f619b2e0c559aaeddc7d7b8176e1144b065d63fa160`  
		Last Modified: Wed, 26 Jan 2022 02:23:47 GMT  
		Size: 5.1 MB (5141567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e019dd0368ba992803442a16cc7792c1bd5a3d06c3a1ae6fae17cb838822fb4c`  
		Last Modified: Wed, 26 Jan 2022 02:23:48 GMT  
		Size: 10.7 MB (10655902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b269ee9fd3f44b0f3ecdfc14a0700e33d5979b928afd56bb96d2be690a462a6c`  
		Last Modified: Wed, 26 Jan 2022 06:26:28 GMT  
		Size: 5.6 MB (5647129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923c665ffc496868d8ddeca0d40be1c28ea915e551c54914665c4810b858632a`  
		Last Modified: Wed, 26 Jan 2022 06:26:27 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9588007194eb5a54c0210525a39a8869a915762a952d43ac44e60fec800935`  
		Last Modified: Thu, 03 Feb 2022 21:15:38 GMT  
		Size: 46.0 MB (45973394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13caea802c56926bf0aea7bcdb9ad5a4e6ec2a88ebf29182e45af9995264871`  
		Last Modified: Fri, 04 Feb 2022 01:45:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c28fd97313e9568228dbce4807a40ddc092f58c50f1090da2f1eade58f9da1`  
		Last Modified: Fri, 04 Feb 2022 02:07:10 GMT  
		Size: 11.2 MB (11184196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2d5486f96904dbfb9b5aa2ca6d4c067f797c8f1cab084bdc5590ee0a7899e6`  
		Last Modified: Fri, 04 Feb 2022 02:07:08 GMT  
		Size: 217.0 KB (217037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
