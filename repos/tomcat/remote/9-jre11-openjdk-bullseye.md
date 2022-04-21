## `tomcat:9-jre11-openjdk-bullseye`

```console
$ docker pull tomcat@sha256:03592ecd4a4f4977c6c17b780f02db644e74fed4a2fc2b8ed4b0c3042a62350b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:9-jre11-openjdk-bullseye` - linux; amd64

```console
$ docker pull tomcat@sha256:6f7339ab63c42db46b9fa960a224ddb9b9d8b5c6aeaa4ae79c643d2a67deede5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136111410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdb3679bbc43de6e38429a57b8fb845a181ab620264b526cbed6edc77903f4e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:15 GMT
ADD file:3a81c181c66f226bd6abd48d0c7ed8a9c599c9f521ec7229286c83161afec8c2 in / 
# Wed, 20 Apr 2022 04:43:16 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:57:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:57:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 10:53:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:53:57 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 20 Apr 2022 10:53:58 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:53:58 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:53:58 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:53:58 GMT
ENV JAVA_VERSION=11.0.14.1
# Wed, 20 Apr 2022 10:54:05 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 21 Apr 2022 04:25:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 04:25:00 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 04:25:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 04:25:00 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 04:25:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:25:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 04:37:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 21 Apr 2022 04:37:53 GMT
ENV TOMCAT_MAJOR=9
# Thu, 21 Apr 2022 04:37:53 GMT
ENV TOMCAT_VERSION=9.0.62
# Thu, 21 Apr 2022 04:37:53 GMT
ENV TOMCAT_SHA512=179af1d50a7d330d0842d3f1cae086bbc1b20e8f6752d66500663f3ac71d80f50113bbd29931e21c8e2eccd982f9f872e193364311316fdd67349130d440c83f
# Thu, 21 Apr 2022 04:37:54 GMT
COPY dir:f0dd1814dbb48cb811da31893ebea358c8c8dc4f61cd09fa1c12894a69e34228 in /usr/local/tomcat 
# Thu, 21 Apr 2022 04:37:57 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 04:37:59 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 04:37:59 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 04:37:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6aefca2dc61dcbcd268b8a9861e552f9cdb69e57242faec64ac120d2355a9c1a`  
		Last Modified: Wed, 20 Apr 2022 04:47:57 GMT  
		Size: 54.9 MB (54941777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967757d5652770cfa81b6cc7577d65e06d336173da116d1fb5b2d349d5d44127`  
		Last Modified: Wed, 20 Apr 2022 07:05:43 GMT  
		Size: 5.2 MB (5155716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c357e2c68cb3bf1e98dcb3eb6ceb16837253db71535921d6993c594588bffe04`  
		Last Modified: Wed, 20 Apr 2022 07:05:45 GMT  
		Size: 10.9 MB (10874928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ccb680c1c472c36a4595e2d4a2b4d1a434c377feb1ec57942b4006051064e6`  
		Last Modified: Wed, 20 Apr 2022 11:12:20 GMT  
		Size: 5.7 MB (5657427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c2d2d2ad823b35ca184fcea252da3e7848e1ed4b31168688a265e4a1ab86b0`  
		Last Modified: Wed, 20 Apr 2022 11:12:19 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adba0a35f28cdd034bef4df08d640578ed8f0c6b971084706a9203183d6387c`  
		Last Modified: Wed, 20 Apr 2022 11:12:26 GMT  
		Size: 46.9 MB (46880152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65019af8900d362d043451a91c27c671e46dfa483af0500921dea6a5ac706470`  
		Last Modified: Thu, 21 Apr 2022 05:01:52 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082f641ba97c9a51568e5d09a553baae7ced3dee66f128e94384197b3c3cfe3c`  
		Last Modified: Thu, 21 Apr 2022 06:55:38 GMT  
		Size: 12.1 MB (12141237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8e79b7b599df64e13118b156d61f91f365b3a19a63ec0c3e6da57c9aa4b41d`  
		Last Modified: Thu, 21 Apr 2022 06:55:37 GMT  
		Size: 459.7 KB (459662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140fa84795cf8c3d7b2ff9249fe68d980245de9580f6faa569bc9aeba5afb1eb`  
		Last Modified: Thu, 21 Apr 2022 06:55:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-openjdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:5c55ceb9f45c6bff1c74c17cc59b5602dda52b4db42a7c287c56c4b0783d5c71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133218906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bba90e6b6b1bc17c6aca9b4da2bab50fcc94679c2e4dff5a8571941eaf8ddc`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 20 Apr 2022 04:28:55 GMT
ADD file:ece192802cbdaf1a141d04f0c2e90cfd3479e5e3e82c6a00206970684494cf48 in / 
# Wed, 20 Apr 2022 04:28:56 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 06:44:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 06:44:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 20 Apr 2022 10:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:33:21 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Wed, 20 Apr 2022 10:33:22 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 20 Apr 2022 10:33:23 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:33:25 GMT
ENV JAVA_VERSION=11.0.14.1
# Wed, 20 Apr 2022 10:33:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 21 Apr 2022 06:00:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 21 Apr 2022 06:00:32 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 06:00:33 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 21 Apr 2022 06:00:34 GMT
WORKDIR /usr/local/tomcat
# Thu, 21 Apr 2022 06:00:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:00:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 21 Apr 2022 06:19:46 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 21 Apr 2022 06:19:47 GMT
ENV TOMCAT_MAJOR=9
# Thu, 21 Apr 2022 06:19:48 GMT
ENV TOMCAT_VERSION=9.0.62
# Thu, 21 Apr 2022 06:19:49 GMT
ENV TOMCAT_SHA512=179af1d50a7d330d0842d3f1cae086bbc1b20e8f6752d66500663f3ac71d80f50113bbd29931e21c8e2eccd982f9f872e193364311316fdd67349130d440c83f
# Thu, 21 Apr 2022 06:19:51 GMT
COPY dir:32b13ed2733a41cf301017fa72164c8480ee339a4717081c81c9abee2e725dbc in /usr/local/tomcat 
# Thu, 21 Apr 2022 06:19:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Apr 2022 06:19:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 21 Apr 2022 06:19:57 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 06:19:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:83d5dcfea08e6927083bc886bf182fc39d87bb04b54b63002ac0c4c0b9aab682`  
		Last Modified: Wed, 20 Apr 2022 04:35:19 GMT  
		Size: 53.6 MB (53633096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cfa86b7b1aca6d694057e4d42ee1440527f41c00b9e577df729244380c9eba`  
		Last Modified: Wed, 20 Apr 2022 06:54:10 GMT  
		Size: 4.9 MB (4938663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c79b19335f27cc78840bf9159e875322f3252ac06113c73756f9d4fba905f9b`  
		Last Modified: Wed, 20 Apr 2022 06:54:10 GMT  
		Size: 10.7 MB (10656971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579ba6ed012bb5067169efabd19955cc8bc89ef5df54b8aac8fa222e892c1e88`  
		Last Modified: Wed, 20 Apr 2022 10:58:19 GMT  
		Size: 5.6 MB (5649495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46016f3a0b390c1ffbf70f7c3608b0562ff1162909dac20f2e3cf144104f0ac4`  
		Last Modified: Wed, 20 Apr 2022 10:58:18 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d6de991e78ab0a1a545ddecf4aabe021bb59242b8dda46c0c3d39f1f857969`  
		Last Modified: Wed, 20 Apr 2022 10:58:25 GMT  
		Size: 46.0 MB (45973128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c0f355e3e6067af42281b47f1c1c4a637726c4050d64057296fd4ca268a617`  
		Last Modified: Thu, 21 Apr 2022 08:39:47 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd694b459ed40aed12801e43971c306c92cf15795ee84381dc0b8c91d45f806d`  
		Last Modified: Thu, 21 Apr 2022 08:55:36 GMT  
		Size: 12.2 MB (12150063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da32b33834d1dbb4f2e8160bb03b461f76ca272d76c7ffe046a56211858321`  
		Last Modified: Thu, 21 Apr 2022 08:55:35 GMT  
		Size: 217.1 KB (217141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
