## `maven:3-openjdk-16-slim`

```console
$ docker pull maven@sha256:618b92847cbbf6b6087871cc0c28b91b5919093acb5232a4e2eb0941a6f1aa49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16-slim` - linux; amd64

```console
$ docker pull maven@sha256:71021c52841b8b207f91648e7e79eab1c0d6fb54faab6b6f10847ed4ae6c843d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226060159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503a38f052352fa5cfc4f259bb8cdf43eccf6d17cfb9c09d149b5b5e3768a611`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 08:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 08:58:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 08:58:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Tue, 13 Oct 2020 08:58:54 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 08:58:55 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 06 Nov 2020 19:54:05 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 06 Nov 2020 19:54:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_linux-aarch64_bin.tar.gz; 			downloadSha256=25895e31bc111565483e1b9c33959bc6dc943003066921faee80181a9c087232; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_linux-x64_bin.tar.gz; 			downloadSha256=efed45c4c7fd4de6a27845c6457b8b5a86ea95da655bdcf3b8407fdc978f6fbd; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Nov 2020 19:54:23 GMT
CMD ["jshell"]
# Fri, 06 Nov 2020 21:22:12 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 06 Nov 2020 21:22:12 GMT
ARG USER_HOME_DIR=/root
# Fri, 06 Nov 2020 21:22:12 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 06 Nov 2020 21:22:12 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 06 Nov 2020 21:22:18 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl procps   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 21:22:27 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 06 Nov 2020 21:22:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 06 Nov 2020 21:22:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 06 Nov 2020 21:22:28 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 06 Nov 2020 21:22:28 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 06 Nov 2020 21:22:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 06 Nov 2020 21:22:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00028440d132be6f9dd59a787bc5d1372d575a539c19954651757f12912f2e65`  
		Last Modified: Tue, 13 Oct 2020 09:08:08 GMT  
		Size: 3.2 MB (3248445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d3f9016801bc943373bbb1397fe32a0219af3d56f3a8361ffae543191883ce`  
		Last Modified: Tue, 13 Oct 2020 09:08:07 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9f16ba2f0248362a654874bd633233707d345b9a3252fe611501893521c19e`  
		Last Modified: Fri, 06 Nov 2020 19:59:21 GMT  
		Size: 183.5 MB (183520182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3958aa88aebcc3da6dd85b8641c07df179af87c37567de43aab58948402876b`  
		Last Modified: Fri, 06 Nov 2020 21:24:26 GMT  
		Size: 2.6 MB (2616652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb9ff3da14a39b08010e46f6ac3e08f143ed7185cc14e3ae9099606fc74ccc`  
		Last Modified: Fri, 06 Nov 2020 21:24:26 GMT  
		Size: 9.6 MB (9581223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accc1b75e441564ec0d7f255f049fda44eb0f2288a0e746f4f38da83fd835722`  
		Last Modified: Fri, 06 Nov 2020 21:24:26 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122366773c9bef9dcdf22562fc37fa314094352fd0c596ae2c65762185de8b11`  
		Last Modified: Fri, 06 Nov 2020 21:24:25 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-16-slim` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a76fce4a36332e7ea38e7c894a348aefcf7d5f78d9298c4177ca947df37e1c9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.1 MB (219108663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02405827479af826be2cc0e324b49614226c63bc86729c7efe4f1facd38eac51`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:09 GMT
ADD file:3488b1423094a75be5bb5956e9187827b8dd35d7a1f2b14081f8e74a1629e7d0 in / 
# Tue, 13 Oct 2020 01:41:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 12:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 12:24:15 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 12:24:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-16
# Tue, 13 Oct 2020 12:24:18 GMT
ENV PATH=/usr/local/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 12:24:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 06 Nov 2020 19:47:41 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 06 Nov 2020 19:48:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_linux-aarch64_bin.tar.gz; 			downloadSha256=25895e31bc111565483e1b9c33959bc6dc943003066921faee80181a9c087232; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_linux-x64_bin.tar.gz; 			downloadSha256=efed45c4c7fd4de6a27845c6457b8b5a86ea95da655bdcf3b8407fdc978f6fbd; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$downloadUrl" --progress=dot:giga; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Nov 2020 19:48:09 GMT
CMD ["jshell"]
# Fri, 06 Nov 2020 21:19:22 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 06 Nov 2020 21:19:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 06 Nov 2020 21:19:23 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 06 Nov 2020 21:19:23 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 06 Nov 2020 21:19:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl procps   && rm -rf /var/lib/apt/lists/*
# Fri, 06 Nov 2020 21:19:46 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 06 Nov 2020 21:19:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 06 Nov 2020 21:19:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 06 Nov 2020 21:19:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 06 Nov 2020 21:19:48 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 06 Nov 2020 21:19:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 06 Nov 2020 21:19:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4e6164a63b7b4cf981546947e191644c122214975d40b51ede0536791ebec3d4`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 25.8 MB (25849329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51571e799d6113fa90df1694d3dac0eb7b52f4ce6cdddd495020745912328e3f`  
		Last Modified: Tue, 13 Oct 2020 12:34:16 GMT  
		Size: 3.1 MB (3101485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4a2e9199e352858201dcec814c7b4ffc78c724e418442f0da70247bfc8b752`  
		Last Modified: Tue, 13 Oct 2020 12:34:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3871a1b16614858b0f749be0db0ca6df97d372020f6adb31ac92356fb80910`  
		Last Modified: Fri, 06 Nov 2020 19:52:42 GMT  
		Size: 177.9 MB (177938703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449b5bad9603944e16ee69d3d26ec3d747a59a28b4ad8609c13765ad9aa0f3b5`  
		Last Modified: Fri, 06 Nov 2020 21:22:01 GMT  
		Size: 2.6 MB (2636517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cae53c5e964980253bc8a7b86223d3c460ff3a9d6cdc61119d39950483c754`  
		Last Modified: Fri, 06 Nov 2020 21:22:02 GMT  
		Size: 9.6 MB (9581199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1425cd2b8c25590bc62c204d5bf77fe57101e157bb56ea533169df445da6266d`  
		Last Modified: Fri, 06 Nov 2020 21:22:01 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099e97cc7e92ec2c0719ed6da35556243f14abe6a8dd0e0f8aa25ab84a4879f1`  
		Last Modified: Fri, 06 Nov 2020 21:22:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
