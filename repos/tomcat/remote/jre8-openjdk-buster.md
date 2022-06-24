## `tomcat:jre8-openjdk-buster`

```console
$ docker pull tomcat@sha256:5cd43815e7854c301ec2289e2c50eaa1002be9e93ec3af4dc37e85484cf6cb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-buster` - linux; amd64

```console
$ docker pull tomcat@sha256:03b760408bdcfe34884fac333c78a0aa90994051b2f8909d48c0d6fc1404f212
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128289538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f963b80d7584abab84a6d1e93c974b52bb6b353280e0f905349a6864e716063a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 04:59:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 05:01:45 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 23 Jun 2022 05:01:45 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 23 Jun 2022 05:01:46 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 05:01:46 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 05:01:46 GMT
ENV JAVA_VERSION=8u332
# Thu, 23 Jun 2022 05:01:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 23 Jun 2022 22:45:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 23 Jun 2022 22:45:18 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 22:45:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 23 Jun 2022 22:45:19 GMT
WORKDIR /usr/local/tomcat
# Thu, 23 Jun 2022 22:45:19 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:45:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 23 Jun 2022 22:45:19 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Thu, 23 Jun 2022 22:45:19 GMT
ENV TOMCAT_MAJOR=10
# Thu, 23 Jun 2022 22:45:19 GMT
ENV TOMCAT_VERSION=10.0.22
# Thu, 23 Jun 2022 22:45:20 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Thu, 23 Jun 2022 22:45:20 GMT
COPY dir:11c37c99e09bc545bca1590c55099e1f42e74a966db04567e19808386e8176b6 in /usr/local/tomcat 
# Thu, 23 Jun 2022 22:45:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 22:45:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 23 Jun 2022 22:45:26 GMT
EXPOSE 8080
# Thu, 23 Jun 2022 22:45:26 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a014c92148934973210d840dc7cfed53e0afba38d839afaa48ed5150eae19af`  
		Last Modified: Thu, 23 Jun 2022 00:59:51 GMT  
		Size: 7.9 MB (7856631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ff1be7001d642a624409e2d5f90e7708ef7e6f1a75f4eb7362a9296e18d20`  
		Last Modified: Thu, 23 Jun 2022 00:59:50 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9250eef0f01e9551fef0eaea0e242501ab3d09c6a7e72c66f5083b55a6daa18d`  
		Last Modified: Thu, 23 Jun 2022 05:19:07 GMT  
		Size: 5.5 MB (5532608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706a76fd54c3779c8650b52578c425ee9ea28faf52393424f3a137a9974627bc`  
		Last Modified: Thu, 23 Jun 2022 05:22:11 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99571f7ac24e01dd83ae457173630a53f6e3ef10ce6926ffcc4b23cff6a7c9c7`  
		Last Modified: Thu, 23 Jun 2022 05:22:16 GMT  
		Size: 41.4 MB (41432122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a683662b013655f930c6abe898746300080619143558b33246960906c92cbf23`  
		Last Modified: Thu, 23 Jun 2022 23:14:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4a2162aa2a4c3ab47877e52272a029ba22f7e52999d55f8aaf2555837c46b5`  
		Last Modified: Thu, 23 Jun 2022 23:14:08 GMT  
		Size: 12.6 MB (12568674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a0928bd0e52b17e8345d2ca110a5d7c092a5a97565f0def2b91408a8588396`  
		Last Modified: Thu, 23 Jun 2022 23:14:07 GMT  
		Size: 460.9 KB (460949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6574ab80e9574a22c3db96b6730117cf6e7e264267af1a374a930f942f8d8248`  
		Last Modified: Thu, 23 Jun 2022 23:14:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-buster` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:1ae6767c1bf92dd5a4295bc26c80921b676aa83f0db2a28690b72455d92be765
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125694072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb0473ee6761e07813c879080459483d4d09689fc34013ccbac837501bb4fb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 28 May 2022 00:40:49 GMT
ADD file:af879be34a7eccc177a3000eb8c45d5207bfbec108caf9be9d11c1a6620c376c in / 
# Sat, 28 May 2022 00:40:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:07:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:07:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 16:50:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 16:52:48 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Sat, 28 May 2022 16:52:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Sat, 28 May 2022 16:52:49 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 16:52:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 16:52:51 GMT
ENV JAVA_VERSION=8u332
# Sat, 28 May 2022 16:52:56 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_8u332b09.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Sat, 28 May 2022 20:15:11 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 28 May 2022 20:15:12 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 20:15:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 28 May 2022 20:15:14 GMT
WORKDIR /usr/local/tomcat
# Sat, 28 May 2022 20:15:15 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:15:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 28 May 2022 20:15:17 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 28 May 2022 20:15:18 GMT
ENV TOMCAT_MAJOR=10
# Mon, 13 Jun 2022 21:07:58 GMT
ENV TOMCAT_VERSION=10.0.22
# Mon, 13 Jun 2022 21:07:59 GMT
ENV TOMCAT_SHA512=fe46db8794f066882b30e7a94bd8d3dbcf29e8e8ffaf67c1355846755745a7c9eafd124819283f218bcf410921a485b44b57b56fd6251fb99d67d95f3dd36826
# Mon, 13 Jun 2022 21:08:01 GMT
COPY dir:b1ae41c227d679a7c724694a4ee1dd9a312ca3a9f0478f60aadfca54ca499bb5 in /usr/local/tomcat 
# Mon, 13 Jun 2022 21:08:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 13 Jun 2022 21:08:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 13 Jun 2022 21:08:07 GMT
EXPOSE 8080
# Mon, 13 Jun 2022 21:08:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fadbed17b01e84815ca3018d3dc42670c3add65c67e7cc74d6bc477ae8425934`  
		Last Modified: Sat, 28 May 2022 00:47:58 GMT  
		Size: 49.2 MB (49229054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5795076bf6e9bf96da71f2e31cbe91d3c49a17f211c5b0d33e032e095c5564a5`  
		Last Modified: Sat, 28 May 2022 11:18:22 GMT  
		Size: 7.7 MB (7719823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1eda3e266fa432ba8ae8ba25a5ad2fa4c5349ef2aa244612c89f990704c5b25`  
		Last Modified: Sat, 28 May 2022 11:18:22 GMT  
		Size: 9.8 MB (9767307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ee2604901b84270e3319485b241bd7323e97383ddc6b24f2c63ac7f32138d0`  
		Last Modified: Sat, 28 May 2022 17:06:56 GMT  
		Size: 5.5 MB (5506814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2881af960401022aec5e19177c045d2957038165297b420c0bb4b04a6c772aec`  
		Last Modified: Sat, 28 May 2022 17:08:52 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba2da4ee4e36569a74a469f5b609db7a06437f79de57777095fa2ead0b61c4d`  
		Last Modified: Sat, 28 May 2022 17:08:57 GMT  
		Size: 40.7 MB (40672255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ab95e01a34abbaaf022f51f32b2133d8ad405ae0cb0563cee2c16ae12fdd84`  
		Last Modified: Sat, 28 May 2022 21:02:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664f8d36fc5e10c9515f2c62864dff7a03a02e9f21515a6c6e9f8b558f5b8466`  
		Last Modified: Mon, 13 Jun 2022 21:51:40 GMT  
		Size: 12.6 MB (12580208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3ae5b39317cd44ee18934e933893e8788fe781248a24624b499380b7109607`  
		Last Modified: Mon, 13 Jun 2022 21:51:39 GMT  
		Size: 218.3 KB (218262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
