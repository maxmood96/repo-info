## `maven:3-openjdk-16`

```console
$ docker pull maven@sha256:dad8be1c8aec27a8a2ce19e80d07d8ad4f15505aaa603ef62ede8c269372280a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16` - linux; amd64

```console
$ docker pull maven@sha256:90bc0aa5a8b1b7cc655bc491cb34f5ab6a0730eb0e055bdf0f88145a491422b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386622256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c41276207627b7ed2dccc9039ae09bb8efd309c033c98e0b86a86b5f0fdaad`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Fri, 18 Dec 2020 18:20:53 GMT
ADD file:ae640751036e8faf191ef80903201a939fb88b6280ec402d34f100cf54e41b5d in / 
# Fri, 18 Dec 2020 18:20:53 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 18:38:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 18 Dec 2020 18:38:18 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 18:38:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 18 Dec 2020 18:38:19 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 20:52:52 GMT
ENV JAVA_VERSION=16-ea+29
# Fri, 18 Dec 2020 20:53:28 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/29/GPL/openjdk-16-ea+29_linux-aarch64_bin.tar.gz; 			downloadSha256=2a273d305f8c5ed1eec0cec322ed37660eddd7bcf1b381583e6c6b66fe020eda; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/29/GPL/openjdk-16-ea+29_linux-x64_bin.tar.gz; 			downloadSha256=484b901cea7c2b6fafea3a4215028f12f225c17807d5413a2d52edcd604ef6ec; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 20:53:28 GMT
CMD ["jshell"]
# Fri, 18 Dec 2020 22:02:27 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 18 Dec 2020 22:02:27 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Dec 2020 22:02:27 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 18 Dec 2020 22:02:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 18 Dec 2020 22:02:53 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 18 Dec 2020 22:02:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 18 Dec 2020 22:02:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Dec 2020 22:02:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Dec 2020 22:02:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 18 Dec 2020 22:02:58 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 18 Dec 2020 22:02:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Dec 2020 22:02:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:edcbc9047efe2641ebc4f2393b0e5717733c062c211b0db349abc2ea82364e57`  
		Last Modified: Fri, 18 Dec 2020 18:22:18 GMT  
		Size: 42.1 MB (42059283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096c31e209d76bfb493c22693ffe401d20bd3b9b8bc2256934fda17f29780bb3`  
		Last Modified: Fri, 18 Dec 2020 18:42:59 GMT  
		Size: 13.3 MB (13261719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e3dc93c31fced6e2db901e8ea9090f160981061f0de656512433ca3501f00`  
		Last Modified: Fri, 18 Dec 2020 20:58:05 GMT  
		Size: 184.8 MB (184835874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd05af60855c7d7638e49faf922fde3aa2b8cd5dde6a0a3da9a4868e5e56d85`  
		Last Modified: Fri, 18 Dec 2020 22:05:45 GMT  
		Size: 136.9 MB (136882952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1f9fe6fdfcf695cfae59802b5d2e49f1d04854dd2f92a1de0394e2a534cd6`  
		Last Modified: Fri, 18 Dec 2020 22:05:32 GMT  
		Size: 9.6 MB (9581211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d262b606406395e4dfa6120bc95ef0966f608b0ab3251c5b94f0daa8a7413d0e`  
		Last Modified: Fri, 18 Dec 2020 22:05:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6715c61bd0c3006d49d179fdf110ce39230a4cbd1dbde12d31a042cb88adca6`  
		Last Modified: Fri, 18 Dec 2020 22:05:31 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ce554dc1c45411607b41e8cf29d647e5a295c4c573c0361a5f1d09ebb6a4fe17
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.0 MB (360017587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9ccbcc187feb1f4f1a0fe1f01886441b8da12cd2d9cb5793c02205f32c8a2e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Fri, 18 Dec 2020 18:43:40 GMT
ADD file:be2d17640c58ed7d6ce818b679805972eedbbacd4ab5ae5e15f5c8542d1ff8ea in / 
# Fri, 18 Dec 2020 18:43:43 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 19:43:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 18 Dec 2020 19:43:59 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 19:44:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 18 Dec 2020 19:44:01 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 19:44:01 GMT
ENV JAVA_VERSION=16-ea+29
# Fri, 18 Dec 2020 19:44:43 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/29/GPL/openjdk-16-ea+29_linux-aarch64_bin.tar.gz; 			downloadSha256=2a273d305f8c5ed1eec0cec322ed37660eddd7bcf1b381583e6c6b66fe020eda; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/29/GPL/openjdk-16-ea+29_linux-x64_bin.tar.gz; 			downloadSha256=484b901cea7c2b6fafea3a4215028f12f225c17807d5413a2d52edcd604ef6ec; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 19:44:45 GMT
CMD ["jshell"]
# Fri, 18 Dec 2020 20:47:30 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 18 Dec 2020 20:47:31 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Dec 2020 20:47:31 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 18 Dec 2020 20:47:32 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 18 Dec 2020 20:48:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 18 Dec 2020 20:48:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 18 Dec 2020 20:48:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Dec 2020 20:48:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Dec 2020 20:48:19 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 18 Dec 2020 20:48:20 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 18 Dec 2020 20:48:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Dec 2020 20:48:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:68012513ce8f557e79d400caae7326eb282a43c35afa4fd0a04e0c6470a0c6da`  
		Last Modified: Fri, 18 Dec 2020 18:45:16 GMT  
		Size: 42.0 MB (41984474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19435fd29840d5adb1fcf43416b769187aa10d3f70e390e22cd1edadb7415d63`  
		Last Modified: Fri, 18 Dec 2020 19:51:11 GMT  
		Size: 14.1 MB (14059908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8943f4ade502129912565fc904075ebbcf20da82a5faba818fe75c19898e4b`  
		Last Modified: Fri, 18 Dec 2020 19:51:34 GMT  
		Size: 179.2 MB (179202947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f39ce85d0ea369424899d263ab837cbfce199c48f9f6538e44fb3569d5c705`  
		Last Modified: Fri, 18 Dec 2020 20:51:43 GMT  
		Size: 115.2 MB (115187835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c37c45b1c2f9a9b8289222bcb674ee3d425d6e83dcb63a1681d49c96cb780d`  
		Last Modified: Fri, 18 Dec 2020 20:51:26 GMT  
		Size: 9.6 MB (9581204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5343f271627bc5b52e13ae14733b092b0891df0a7ab5bda828722c22dabd3e3f`  
		Last Modified: Fri, 18 Dec 2020 20:51:24 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297fb9af792ee8ee8c87f123ada85a3910b43fc6c6f2ffe6c37f2cbe5d2c5c9e`  
		Last Modified: Fri, 18 Dec 2020 20:51:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
