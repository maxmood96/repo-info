## `maven:3-openjdk-16`

```console
$ docker pull maven@sha256:305c28b84925240b9e5fa58ee5b902f3907d0481b4936b8321ffc704fea6cebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16` - linux; amd64

```console
$ docker pull maven@sha256:d3f466a4c1a1547f1cccabc8e532a692a1083de07fdb5b3e1ac42c386051d8e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.9 MB (379891285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98be79119bee11afc11dcafcade93ac239b6e0cbb3ee2ae27bbc27a0a91dd86`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Fri, 30 Oct 2020 02:05:51 GMT
ADD file:ca74b6a4572ba9ecd7ceca8360a2d15560bf779277672ae9a37e25c53f8d1226 in / 
# Fri, 30 Oct 2020 02:05:51 GMT
CMD ["/bin/bash"]
# Fri, 30 Oct 2020 04:37:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 30 Oct 2020 04:37:30 GMT
ENV LANG=C.UTF-8
# Fri, 30 Oct 2020 04:37:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 30 Oct 2020 04:37:31 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Nov 2020 19:20:09 GMT
ENV JAVA_VERSION=16-ea+24
# Fri, 13 Nov 2020 19:20:45 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/24/GPL/openjdk-16-ea+24_linux-aarch64_bin.tar.gz; 			downloadSha256=9085bbb4f9e4d70ac385f85fbd706ab1fa570417beb28d09ff71e4908684cd8c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/24/GPL/openjdk-16-ea+24_linux-x64_bin.tar.gz; 			downloadSha256=ad1e33e43f923a8cde6e611e8ada1b76047f156d44b981d16daa440251f71823; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Nov 2020 19:20:45 GMT
CMD ["jshell"]
# Fri, 13 Nov 2020 19:53:12 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 13 Nov 2020 19:53:12 GMT
ARG USER_HOME_DIR=/root
# Fri, 13 Nov 2020 19:53:12 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 13 Nov 2020 19:53:12 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 13 Nov 2020 19:53:38 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 13 Nov 2020 19:53:40 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 13 Nov 2020 19:53:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 13 Nov 2020 19:53:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 13 Nov 2020 19:53:41 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 13 Nov 2020 19:53:41 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 13 Nov 2020 19:53:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 13 Nov 2020 19:53:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9f8aeb516aa1b01143452930dec1cadef36b4298bcdb43224755b12ab4bc9289`  
		Last Modified: Fri, 30 Oct 2020 02:07:57 GMT  
		Size: 54.2 MB (54163019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6199265ff0195874d7975d360d91e2ed48bc621c12633d52a4fe5207953ff202`  
		Last Modified: Fri, 30 Oct 2020 04:42:34 GMT  
		Size: 13.5 MB (13508533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6278dd085bbe385de1a9528363c7067e52119599c26cf46a36e5ed3e0cb4cfb`  
		Last Modified: Fri, 13 Nov 2020 19:24:08 GMT  
		Size: 183.5 MB (183540099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9789d2246fc7a0cc250e39abea629f56fb59cf9becb11018c5936a275627ff`  
		Last Modified: Fri, 13 Nov 2020 19:55:53 GMT  
		Size: 119.1 MB (119097189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34098b575e5367da1c5ebfebe3cf5d618e70dbb4e2216365729eca7ff9e54e2`  
		Last Modified: Fri, 13 Nov 2020 19:55:42 GMT  
		Size: 9.6 MB (9581225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7993728b7d54a51d2f3f76f810c8971479927147d1188267f4d365f74680847`  
		Last Modified: Fri, 13 Nov 2020 19:55:41 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0c2ba4c6c6dd7fc8e587c773c3199ccd93f1f5383a57593b7f7211bddc907e`  
		Last Modified: Fri, 13 Nov 2020 19:55:42 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b8700a5b6b9cfe073907a1f078abe027b7984a414facee2192ac28e03e6336ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 MB (352958362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b3239c45af5ae270f429bca0a573f52e3d97fcdf648a956e9fe9b9bc399f8d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Fri, 30 Oct 2020 03:44:45 GMT
ADD file:9cec0313dda06011e5a2f413448db8dc2a3f2e6305dbfd3afa2f78c9e571c080 in / 
# Fri, 30 Oct 2020 03:44:49 GMT
CMD ["/bin/bash"]
# Fri, 30 Oct 2020 04:03:41 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 30 Oct 2020 04:03:42 GMT
ENV LANG=C.UTF-8
# Fri, 30 Oct 2020 04:03:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 30 Oct 2020 04:03:43 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Nov 2020 19:45:29 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 06 Nov 2020 19:46:27 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_linux-aarch64_bin.tar.gz; 			downloadSha256=25895e31bc111565483e1b9c33959bc6dc943003066921faee80181a9c087232; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_linux-x64_bin.tar.gz; 			downloadSha256=efed45c4c7fd4de6a27845c6457b8b5a86ea95da655bdcf3b8407fdc978f6fbd; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Nov 2020 19:46:29 GMT
CMD ["jshell"]
# Fri, 06 Nov 2020 21:18:24 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 06 Nov 2020 21:18:25 GMT
ARG USER_HOME_DIR=/root
# Fri, 06 Nov 2020 21:18:25 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 06 Nov 2020 21:18:26 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 06 Nov 2020 21:19:02 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 06 Nov 2020 21:19:08 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 06 Nov 2020 21:19:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 06 Nov 2020 21:19:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 06 Nov 2020 21:19:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 06 Nov 2020 21:19:11 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 06 Nov 2020 21:19:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 06 Nov 2020 21:19:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e3e30b00fc3497706dcd32508109092c83b0a5b47bd1dbd485dc8a0da352da68`  
		Last Modified: Fri, 30 Oct 2020 03:46:38 GMT  
		Size: 54.3 MB (54268366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2870a34311e6e2480637a34f3904b567d224baff73277563033ebcee672d93`  
		Last Modified: Fri, 30 Oct 2020 04:11:09 GMT  
		Size: 14.4 MB (14365455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b563e426cd1af9d3ff889fea8f376a264bfa4ad2e14b55bde3a7a55cf29558`  
		Last Modified: Fri, 06 Nov 2020 19:50:28 GMT  
		Size: 177.6 MB (177568510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59af88d3a92d9c4f6b676ab4cad9288528893b986e45b40ee7ffb612ec2062b5`  
		Last Modified: Fri, 06 Nov 2020 21:21:35 GMT  
		Size: 97.2 MB (97173612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95314f617aad5b1d740adb1fae2dbd076dea255556411a33fba59ddc4a4f6c4c`  
		Last Modified: Fri, 06 Nov 2020 21:21:21 GMT  
		Size: 9.6 MB (9581205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f391a640981d060d60376fdfdb28a27eb7c9a97b821e65879994cf4485deba7`  
		Last Modified: Fri, 06 Nov 2020 21:21:20 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91a67fe436bcd6fcc2bce9a3bc1145c3d5d3ad2678c2e8e658c780729389568`  
		Last Modified: Fri, 06 Nov 2020 21:21:19 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
