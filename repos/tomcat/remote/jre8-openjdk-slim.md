## `tomcat:jre8-openjdk-slim`

```console
$ docker pull tomcat@sha256:37f6bab4de167e2b284771447f673abbc23f77e582d66737bacaa8c6c09db19f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomcat:jre8-openjdk-slim` - linux; amd64

```console
$ docker pull tomcat@sha256:7b99121c602a43f816f1982a92625efc4002fed1e55d95a01c5137eb8441744e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87475510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1988c0e77b1d29eee15427e37267f07a3c4bae4c1082f6c6628826bdb7558`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:40 GMT
ADD file:3c520ad50b13b922356e0a5e4f7c12b202e09584acf332a65d5603dacd4a9380 in / 
# Tue, 28 Sep 2021 01:22:41 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 09:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 09:25:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 28 Sep 2021 09:25:12 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 28 Sep 2021 09:25:13 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 09:25:13 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 09:25:13 GMT
ENV JAVA_VERSION=8u302
# Tue, 28 Sep 2021 09:27:35 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 29 Sep 2021 11:29:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 29 Sep 2021 11:29:40 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 11:29:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 29 Sep 2021 11:29:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 29 Sep 2021 11:29:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 11:29:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 11:29:42 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 29 Sep 2021 11:29:42 GMT
ENV TOMCAT_MAJOR=10
# Wed, 29 Sep 2021 11:29:42 GMT
ENV TOMCAT_VERSION=10.0.11
# Wed, 29 Sep 2021 11:29:43 GMT
ENV TOMCAT_SHA512=16e1879490bb0e5843059e3a475558f1990b03f897a7d5cce5788d6983598ec30cbf3749e30c18fb799f5068cab8407d04e9e6e9705700b152f90a3dc8bc0cb5
# Wed, 29 Sep 2021 11:29:43 GMT
COPY dir:fceb71c7a6fed7b9b3f98c6cc5b3fc996c28e7659f4ee43dc481561deef7019e in /usr/local/tomcat 
# Wed, 29 Sep 2021 11:29:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 Sep 2021 11:29:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 29 Sep 2021 11:29:49 GMT
EXPOSE 8080
# Wed, 29 Sep 2021 11:29:49 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:bd897bb914af2ec64f1cff5856aefa1ae99b072e38db0b7d801f9679b04aad74`  
		Last Modified: Tue, 28 Sep 2021 01:29:00 GMT  
		Size: 31.4 MB (31368912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc7fec72146c7ce5a6ca7ee0750b1c72d0554380437767653dcb8dc27d303e4`  
		Last Modified: Tue, 28 Sep 2021 09:34:00 GMT  
		Size: 1.6 MB (1582018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdb783f109fe5199148a46daa8c799d3bde27b23584ee8db6f225a1a7aa6469`  
		Last Modified: Tue, 28 Sep 2021 09:47:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3705cbf1f04f3608cd822990596ecf48b0426e399f32ba9149e56113e13b2453`  
		Last Modified: Tue, 28 Sep 2021 09:49:05 GMT  
		Size: 41.6 MB (41632902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83cc0b501a0e7f1d1e77138b6a31ded5e0318b29503122326bbc506c0b90535`  
		Last Modified: Wed, 29 Sep 2021 12:34:58 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cbd8addc7cb8be3e9d81503a72719de8a3fe5115f0fb6600025cad7dbca6d8`  
		Last Modified: Wed, 29 Sep 2021 12:34:59 GMT  
		Size: 12.5 MB (12494971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad745bcae0b11a8348f29a9607f434fd251cf6910898e44a91301095b59095f`  
		Last Modified: Wed, 29 Sep 2021 12:34:58 GMT  
		Size: 396.2 KB (396198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7201a21b2712f2d9a5e32102eb9d7aee011364758481c5b1c6f0ed595b7383f5`  
		Last Modified: Wed, 29 Sep 2021 12:34:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-openjdk-slim` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:cdcb0c189aec02e91c642411cdf2796526f1dd4fb5a1b0288cf2f15d948a6883
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85413928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14f6aa1a2c30869afc6cfc578e699da18678bcb51c85aff61371496e24086e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:43 GMT
ADD file:6472ab63529e688735f77634402740e08fdbd5bfa788c150915027993df7e8ec in / 
# Tue, 28 Sep 2021 01:40:44 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 05:42:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 05:52:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Tue, 28 Sep 2021 05:52:34 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Tue, 28 Sep 2021 05:52:34 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 05:52:35 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 05:52:35 GMT
ENV JAVA_VERSION=8u302
# Tue, 28 Sep 2021 05:54:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_x64_linux_8u302b08.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jre_aarch64_linux_8u302b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Wed, 29 Sep 2021 04:12:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 29 Sep 2021 04:12:00 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 04:12:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 29 Sep 2021 04:12:01 GMT
WORKDIR /usr/local/tomcat
# Wed, 29 Sep 2021 04:12:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 04:12:02 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 29 Sep 2021 04:12:02 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 29 Sep 2021 04:12:02 GMT
ENV TOMCAT_MAJOR=10
# Wed, 29 Sep 2021 04:12:02 GMT
ENV TOMCAT_VERSION=10.0.11
# Wed, 29 Sep 2021 04:12:02 GMT
ENV TOMCAT_SHA512=16e1879490bb0e5843059e3a475558f1990b03f897a7d5cce5788d6983598ec30cbf3749e30c18fb799f5068cab8407d04e9e6e9705700b152f90a3dc8bc0cb5
# Wed, 29 Sep 2021 04:12:03 GMT
COPY dir:75f23f6d64a2d6897b06cf26e7103fa1bf7f022d72dbe565a90216599dfc7bb5 in /usr/local/tomcat 
# Wed, 29 Sep 2021 04:12:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 29 Sep 2021 04:12:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 29 Sep 2021 04:12:09 GMT
EXPOSE 8080
# Wed, 29 Sep 2021 04:12:09 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:2f8871a8654eb1158cb626f8dc69992dba7e4bd8796fae6aa7cf967f951f5fe9`  
		Last Modified: Tue, 28 Sep 2021 01:48:25 GMT  
		Size: 30.1 MB (30055408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc69e286af9edc8fb3518a0692316edc953730d4b65004457f37972b70873fe1`  
		Last Modified: Tue, 28 Sep 2021 06:04:25 GMT  
		Size: 1.6 MB (1566191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf168ad06bb1f054ea1fbfa1190fea3dc5a597f5601ddc404305c7b029488d7`  
		Last Modified: Tue, 28 Sep 2021 06:18:55 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150dca295858012152ae1a986c6cee49c3db29d1cb65be521a0b34c8ad7c7282`  
		Last Modified: Tue, 28 Sep 2021 06:20:58 GMT  
		Size: 40.9 MB (40889179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d280bb92733fba480cf9bcfd993ef09a9b3538fa4956fca5d3df94967e2e8eb`  
		Last Modified: Wed, 29 Sep 2021 05:34:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6bd780ac3ebaea45288fa7a016dce781aba8107607775a83d5f14746a103d3`  
		Last Modified: Wed, 29 Sep 2021 05:34:54 GMT  
		Size: 12.5 MB (12507864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf354565115f52ede3bc98e9dba5e7d320f89c86cf43fcedd44433b52ad67e0`  
		Last Modified: Wed, 29 Sep 2021 05:34:53 GMT  
		Size: 394.8 KB (394772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d476330208df9efca3b1a2da35f65ba0d47c9a7b157d39af2c4f2aa145b5a4`  
		Last Modified: Wed, 29 Sep 2021 05:34:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
