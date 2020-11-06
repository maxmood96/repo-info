## `maven:3-openjdk-16`

```console
$ docker pull maven@sha256:7e8ec060d7682ec2ba79e1cdc419d1b322c35c522934c023d71fd37db5467551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16` - linux; amd64

```console
$ docker pull maven@sha256:602f1406337686cdc6ac5ec6b23a1d9255182f402a4b71964f1e0277cb9b6d36
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381255166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e81fa85ad7a1ae69d4753944d3bc8160aa56a82563d522559ce129bb81a488`
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
# Fri, 06 Nov 2020 19:52:48 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 06 Nov 2020 19:53:09 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_linux-aarch64_bin.tar.gz; 			downloadSha256=25895e31bc111565483e1b9c33959bc6dc943003066921faee80181a9c087232; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_linux-x64_bin.tar.gz; 			downloadSha256=efed45c4c7fd4de6a27845c6457b8b5a86ea95da655bdcf3b8407fdc978f6fbd; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Nov 2020 19:53:10 GMT
CMD ["jshell"]
# Fri, 06 Nov 2020 21:21:42 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 06 Nov 2020 21:21:42 GMT
ARG USER_HOME_DIR=/root
# Fri, 06 Nov 2020 21:21:42 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 06 Nov 2020 21:21:43 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 06 Nov 2020 21:22:03 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 06 Nov 2020 21:22:05 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 06 Nov 2020 21:22:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 06 Nov 2020 21:22:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 06 Nov 2020 21:22:06 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 06 Nov 2020 21:22:06 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 06 Nov 2020 21:22:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 06 Nov 2020 21:22:07 GMT
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
	-	`sha256:b3a2c1abdb17d2dd74dd783bbf555dbcdcfc0de395bf861f29f62217a09cc0cf`  
		Last Modified: Fri, 06 Nov 2020 19:57:03 GMT  
		Size: 183.1 MB (183143382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4add02160334cccf285ece55c8d546a7caa4363a2bcad0c0208c04cc56e6942c`  
		Last Modified: Fri, 06 Nov 2020 21:24:20 GMT  
		Size: 120.9 MB (120857802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da16faa0ed2b181807ea13d48baf1284c0293cd7d846fe01d7afb63e300dcc86`  
		Last Modified: Fri, 06 Nov 2020 21:24:09 GMT  
		Size: 9.6 MB (9581213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e8440deaba290b87c6265ec2bc952150344d5c32ad5b30a5040e2872a0071`  
		Last Modified: Fri, 06 Nov 2020 21:24:08 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea74b86f3bd57d60e16ec519b40fe2b10481d99b85d8f25554ecd03c4fa8976`  
		Last Modified: Fri, 06 Nov 2020 21:24:08 GMT  
		Size: 360.0 B  
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
