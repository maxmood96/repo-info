## `maven:3-openjdk-17`

```console
$ docker pull maven@sha256:1ad2f7f5295d6d469a4b4d64a983d2c304b90ef80a8f0e7feecd35e84b6ff524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-17` - linux; amd64

```console
$ docker pull maven@sha256:e7ea60175de7e8c9d8f6a0306b024a81938c5b6360a7f8e0994a5b17d4f89d0a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397095453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ec80cbd57ecbf600b127214dc852259046e259e22dc57045ce84e596b3b341`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 17 Apr 2021 01:21:29 GMT
ADD file:9c532b9932419aab70115bea018132ac9096e9eebb25f230bda99cb66245fab2 in / 
# Sat, 17 Apr 2021 01:21:29 GMT
CMD ["/bin/bash"]
# Sat, 17 Apr 2021 01:38:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 17 Apr 2021 01:38:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Sat, 17 Apr 2021 01:38:22 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Apr 2021 01:38:22 GMT
ENV LANG=C.UTF-8
# Mon, 26 Apr 2021 23:21:08 GMT
ENV JAVA_VERSION=17-ea+19
# Mon, 26 Apr 2021 23:21:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/19/GPL/openjdk-17-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='76ee253e411ed65c8166b48d36a9db9e77eea45ef61db577530faee399e0d441'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/19/GPL/openjdk-17-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='313ee29d3a5620edab331814ee4fb9dd7090945cc0afeaf73a3e2e43c907afb8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 26 Apr 2021 23:21:19 GMT
CMD ["jshell"]
# Tue, 27 Apr 2021 00:11:21 GMT
ARG MAVEN_VERSION=3.8.1
# Tue, 27 Apr 2021 00:11:22 GMT
ARG USER_HOME_DIR=/root
# Tue, 27 Apr 2021 00:11:22 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Tue, 27 Apr 2021 00:11:22 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Tue, 27 Apr 2021 00:11:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN microdnf install findutils git
# Tue, 27 Apr 2021 00:11:47 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 27 Apr 2021 00:11:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 27 Apr 2021 00:11:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 27 Apr 2021 00:11:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 27 Apr 2021 00:11:48 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 27 Apr 2021 00:11:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 27 Apr 2021 00:11:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9509c6b41a37fbf5dbb93aedded1aff0dc6ed45ab2d334440e10a5c8d112531c`  
		Last Modified: Sat, 17 Apr 2021 01:22:39 GMT  
		Size: 42.1 MB (42063762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0005db77786a07e4e5d56adc224c9dc85320b46354f9110eb174ce7df9df04`  
		Last Modified: Sat, 17 Apr 2021 01:43:53 GMT  
		Size: 13.3 MB (13272982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75edf53743b43218fbb35d138d72e7d8c27572327b5f6fc74c5423b1867c1cf6`  
		Last Modified: Mon, 26 Apr 2021 23:26:42 GMT  
		Size: 186.0 MB (185989171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc3126e3f68c86fce1eeae3dfd72ed46a93e2bb401bab0a6a4418ed5f2a0d2e`  
		Last Modified: Tue, 27 Apr 2021 00:14:57 GMT  
		Size: 146.2 MB (146157365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62782989efaa2821d35a6bc7a499d3ab06b79b9d55bb8b04c73c92111530dca4`  
		Last Modified: Tue, 27 Apr 2021 00:14:46 GMT  
		Size: 9.6 MB (9610957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff9a3edd9f6ff1d9978e8308d8b8cf42b44e31df63c7143134382c77504ac09`  
		Last Modified: Tue, 27 Apr 2021 00:14:46 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8b5d2e1ca5cbf68e20477ab46ce9a340d39447887e6b164000e224277ae46c`  
		Last Modified: Tue, 27 Apr 2021 00:14:45 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bccdbc05cb2148be2c4a6f6b75a948feda6620bf5e2759092af47b95221e9069
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.3 MB (376270570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6ee40b382d819aa265404865df05dae49431bbfbff310ac6bee4559593860`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 17 Apr 2021 00:43:47 GMT
ADD file:2afad2b68d4889be2ef517aea246957975145f8ad99a3e9e6a01baf79f67d5e2 in / 
# Sat, 17 Apr 2021 00:43:51 GMT
CMD ["/bin/bash"]
# Sat, 17 Apr 2021 01:01:42 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 17 Apr 2021 01:01:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Sat, 17 Apr 2021 01:01:44 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Apr 2021 01:01:45 GMT
ENV LANG=C.UTF-8
# Mon, 26 Apr 2021 23:44:39 GMT
ENV JAVA_VERSION=17-ea+19
# Mon, 26 Apr 2021 23:45:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/19/GPL/openjdk-17-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='76ee253e411ed65c8166b48d36a9db9e77eea45ef61db577530faee399e0d441'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/19/GPL/openjdk-17-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='313ee29d3a5620edab331814ee4fb9dd7090945cc0afeaf73a3e2e43c907afb8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 26 Apr 2021 23:45:02 GMT
CMD ["jshell"]
# Tue, 27 Apr 2021 00:39:16 GMT
ARG MAVEN_VERSION=3.8.1
# Tue, 27 Apr 2021 00:39:18 GMT
ARG USER_HOME_DIR=/root
# Tue, 27 Apr 2021 00:39:19 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Tue, 27 Apr 2021 00:39:20 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Tue, 27 Apr 2021 00:40:19 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN microdnf install findutils git
# Tue, 27 Apr 2021 00:40:26 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 27 Apr 2021 00:40:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 27 Apr 2021 00:40:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 27 Apr 2021 00:40:30 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 27 Apr 2021 00:40:31 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 27 Apr 2021 00:40:32 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 27 Apr 2021 00:40:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4b26d50a92155f32c82c580c6abd80083d4fff230a35ef647094df38f4475f9f`  
		Last Modified: Sat, 17 Apr 2021 00:45:12 GMT  
		Size: 42.0 MB (41996718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc97fa408166ea1b3901653a092a35a895b8718e00810a9bf87dd8f1d0430f3`  
		Last Modified: Sat, 17 Apr 2021 01:07:39 GMT  
		Size: 14.0 MB (14034435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f045285d629d274ef21d033602052381027b6b0b10d5bf5a17df1e4cb1d85d`  
		Last Modified: Mon, 26 Apr 2021 23:50:55 GMT  
		Size: 182.1 MB (182062906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1ac1a69a1b1816660f2348aa0f9330970084d27e36513d9364ed771610bb3`  
		Last Modified: Tue, 27 Apr 2021 00:44:06 GMT  
		Size: 128.6 MB (128564313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179db102c08a6f954f01e49e0def6961b3018da32c8790a7a73184e779d72df`  
		Last Modified: Tue, 27 Apr 2021 00:43:41 GMT  
		Size: 9.6 MB (9610981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec8e2c547806531dbea596e1f37ea4df900d23038f5926e12c32af4c260b007`  
		Last Modified: Tue, 27 Apr 2021 00:43:40 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b7604f6a596edfc8b870aa325490468dd39a7a0ce2301b0db94b13ea23ad51`  
		Last Modified: Tue, 27 Apr 2021 00:43:40 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
