## `maven:3-openjdk`

```console
$ docker pull maven@sha256:84b220bb261d822e2ccf58ab3035f55bbdb00c13c42aa34a8992570171a77c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk` - linux; amd64

```console
$ docker pull maven@sha256:cc3e9fdae7afc8155bdd35a1bf78dc31d45d8ec5fe64e35ee4bc28b9cdd2eb8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 MB (397563624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c187947b5cb0a3768d846dd8523b56bd76389c692f1ba849b6ff35a3247400`
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
# Fri, 18 Dec 2020 18:39:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 18 Dec 2020 18:39:23 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 18:39:23 GMT
ENV JAVA_VERSION=15.0.1
# Fri, 18 Dec 2020 18:39:59 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 18:39:59 GMT
CMD ["jshell"]
# Fri, 18 Dec 2020 19:11:52 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 18 Dec 2020 19:11:53 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Dec 2020 19:11:53 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 18 Dec 2020 19:11:53 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 18 Dec 2020 19:12:18 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 18 Dec 2020 19:12:26 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 18 Dec 2020 19:12:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Dec 2020 19:12:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Dec 2020 19:12:27 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 18 Dec 2020 19:12:27 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 18 Dec 2020 19:12:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Dec 2020 19:12:28 GMT
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
	-	`sha256:9e211f51e5c4fddad313a905a3c938d804492f4a74fd37ff59f879d8238ecccd`  
		Last Modified: Fri, 18 Dec 2020 18:44:02 GMT  
		Size: 195.8 MB (195778192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96824cde290f06f39668e5ec4414e6a31a75374cbb76ad9616678ece3725c67f`  
		Last Modified: Fri, 18 Dec 2020 19:15:37 GMT  
		Size: 136.9 MB (136881992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b9cd6527308d566e447c0f1b5944c16659dab13aa0ca369d724eb591f846ed`  
		Last Modified: Fri, 18 Dec 2020 19:15:23 GMT  
		Size: 9.6 MB (9581223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd499092bcc8e896d023f950103e5a15104d7323ef7a22984a7bcd7c61ad450d`  
		Last Modified: Fri, 18 Dec 2020 19:15:22 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ff6abb57ca0d5dc47fd77942c5250e1947f2b4732ceccd176fcd3debd99e6c`  
		Last Modified: Fri, 18 Dec 2020 19:15:22 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a7275c09bb333b4b78468e20354ca071b78d4f38f9ab8e645f7ded39b11158bb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355702499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea0313cd5bea0ee5f163ee8441a4f4c627a7974749f6e3bfe666c600f24327e`
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
# Fri, 18 Dec 2020 19:47:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 18 Dec 2020 19:47:45 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 19:47:45 GMT
ENV JAVA_VERSION=15.0.1
# Fri, 18 Dec 2020 19:48:11 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 19:48:13 GMT
CMD ["jshell"]
# Fri, 18 Dec 2020 20:46:17 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 18 Dec 2020 20:46:18 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Dec 2020 20:46:18 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 18 Dec 2020 20:46:19 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 18 Dec 2020 20:46:58 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 18 Dec 2020 20:47:06 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 18 Dec 2020 20:47:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Dec 2020 20:47:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Dec 2020 20:47:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 18 Dec 2020 20:47:11 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 18 Dec 2020 20:47:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Dec 2020 20:47:12 GMT
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
	-	`sha256:eacb927968b99c3905c97438bc58feab590487875a20ae3a6815878a62425957`  
		Last Modified: Fri, 18 Dec 2020 19:55:03 GMT  
		Size: 174.9 MB (174887912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e26aff745d0f6d232c4d4630ab6e79e6f600103a566f3e964ab902f2d1ccc3`  
		Last Modified: Fri, 18 Dec 2020 20:50:55 GMT  
		Size: 115.2 MB (115187782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d127c5e4d68b5baf9aab664ab739b723b20000b1714da73ef758d337a95cb7b5`  
		Last Modified: Fri, 18 Dec 2020 20:50:36 GMT  
		Size: 9.6 MB (9581205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcd1d76b3c0b9b85a48282d36d0c0afc1ccb4be065c9aeb50ea1ce4e467ed38`  
		Last Modified: Fri, 18 Dec 2020 20:50:37 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344ceff74244a02508bed80cc77e0cd973c4b1c9192279bd317cee083e371330`  
		Last Modified: Fri, 18 Dec 2020 20:50:35 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
