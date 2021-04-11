## `maven:3-openjdk-17-slim`

```console
$ docker pull maven@sha256:cbe8f2567ec042b9c63e27be220f9e9fbd783fe38d2f9e2c655d4c6203e33770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-17-slim` - linux; amd64

```console
$ docker pull maven@sha256:093bac26665c4e2ae5873c45affdc06ee948c5e864cfa7d5f812be096fe496bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228983403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1977b5aa174658a8692ca71ed3eba1d66edf7cd597b3d005e54d66d00223e59e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:44:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 12:44:50 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 12:44:51 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:44:51 GMT
ENV JAVA_VERSION=17-ea+17
# Sat, 10 Apr 2021 12:45:06 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/17/GPL/openjdk-17-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='a53ace955971ef1ad745c2e9fef7f76b57b51d57e7076dd3a55243ab65febf87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/17/GPL/openjdk-17-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='ccd8ee7bb908835e697ebae8dbe38d2cf68d9f266e2d9787bdf34d26da30e45b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 10 Apr 2021 12:45:07 GMT
CMD ["jshell"]
# Sun, 11 Apr 2021 01:55:11 GMT
ARG MAVEN_VERSION=3.8.1
# Sun, 11 Apr 2021 01:55:11 GMT
ARG USER_HOME_DIR=/root
# Sun, 11 Apr 2021 01:55:11 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Sun, 11 Apr 2021 01:55:12 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Sun, 11 Apr 2021 01:55:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl procps   && rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 01:55:19 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sun, 11 Apr 2021 01:55:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 11 Apr 2021 01:55:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 11 Apr 2021 01:55:20 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sun, 11 Apr 2021 01:55:20 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sun, 11 Apr 2021 01:55:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 11 Apr 2021 01:55:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf4c47c8c6124c3089f3ed26410da9870ba18dd4bc68331e2b7e853116a6cad`  
		Last Modified: Sat, 10 Apr 2021 12:54:28 GMT  
		Size: 3.3 MB (3268764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b747e468795b0735d06d63736391b020a145f9b53f2c7af4ffff68ee8f8e1925`  
		Last Modified: Sat, 10 Apr 2021 12:54:42 GMT  
		Size: 186.3 MB (186345244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f39fb4e7294be3c751aa356e87b4eeeb56e1769a972192ba8eea0cdb649468`  
		Last Modified: Sun, 11 Apr 2021 01:59:39 GMT  
		Size: 2.6 MB (2617847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370edbf7dd859e47d60a252015ba7863c09ccb4561f2505b55049f4c91f2ed34`  
		Last Modified: Sun, 11 Apr 2021 01:59:40 GMT  
		Size: 9.6 MB (9610956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e264a4d85b33481caae7a158cd106a900f3d30e6b6b54b4d337b1e6976cf44fe`  
		Last Modified: Sun, 11 Apr 2021 01:59:39 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6f73702c9cd3ceb491204124273309bf44a63543a5a8615442402100c11f6f`  
		Last Modified: Sun, 11 Apr 2021 01:59:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-17-slim` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:afa8be755cdc62b7a7a17494df78f6275c0e896259cfd207c2a12f6bb2867727
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223665982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227a15425e4e8221d208869f9e2c5ea40e95f8b49f735a49946714737846be74`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:25 GMT
ADD file:b24da7eb23eeae04e00d0e45da29a89fe8f992e8dcf4ba482afb907b8015b7bf in / 
# Sat, 10 Apr 2021 00:41:28 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:31:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 01:31:15 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 01:31:16 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 01:31:17 GMT
ENV JAVA_VERSION=17-ea+17
# Sat, 10 Apr 2021 01:31:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/17/GPL/openjdk-17-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='a53ace955971ef1ad745c2e9fef7f76b57b51d57e7076dd3a55243ab65febf87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/17/GPL/openjdk-17-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='ccd8ee7bb908835e697ebae8dbe38d2cf68d9f266e2d9787bdf34d26da30e45b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 10 Apr 2021 01:31:43 GMT
CMD ["jshell"]
# Sat, 10 Apr 2021 18:15:58 GMT
ARG MAVEN_VERSION=3.8.1
# Sat, 10 Apr 2021 18:15:59 GMT
ARG USER_HOME_DIR=/root
# Sat, 10 Apr 2021 18:15:59 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Sat, 10 Apr 2021 18:16:00 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Sat, 10 Apr 2021 18:16:14 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl procps   && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:16:18 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 10 Apr 2021 18:16:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 10 Apr 2021 18:16:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 10 Apr 2021 18:16:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 10 Apr 2021 18:16:22 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 10 Apr 2021 18:16:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 10 Apr 2021 18:16:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:15cb40b9c4df1a06940dc2a154c3be46844241235c1a091afa70da0ee2dc811a`  
		Last Modified: Sat, 10 Apr 2021 00:47:53 GMT  
		Size: 25.9 MB (25904582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0ed82b9f1018dd9b8a3d8ed771ba8773bd33481ce655abab47d10bd3034f05`  
		Last Modified: Sat, 10 Apr 2021 01:37:31 GMT  
		Size: 3.1 MB (3118914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda1186efdf3bcd7cc9f4fd0b67fd4035feb0f23ad9570a49556519dbbfedae9`  
		Last Modified: Sat, 10 Apr 2021 01:37:59 GMT  
		Size: 182.4 MB (182393443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53463e76f4a50bf7027f912bdb7eadd94b50805bece68038d605cb8111b4c2d`  
		Last Modified: Sat, 10 Apr 2021 18:18:45 GMT  
		Size: 2.6 MB (2636871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b54142ec23a90b91e26392ccc45b8f6cbd72913655bf829575b1fe39f743fa`  
		Last Modified: Sat, 10 Apr 2021 18:18:46 GMT  
		Size: 9.6 MB (9610957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26952b07706ec6c52e9b7ebd79a04dc0e0060cd4545e4025477ffcfac6ba2768`  
		Last Modified: Sat, 10 Apr 2021 18:18:45 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d706133026286ce8c1ecd8d7a96a343b8617c5dbcdc938c982fe04539f459c`  
		Last Modified: Sat, 10 Apr 2021 18:18:45 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
