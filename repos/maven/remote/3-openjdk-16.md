## `maven:3-openjdk-16`

```console
$ docker pull maven@sha256:a9b8f75419208b3110aab464752621f9c860ac8fd75823d96ae738fdcfc77b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16` - linux; amd64

```console
$ docker pull maven@sha256:a2c1ddc254ecbddc4d91ca44e69e4132ea54c65d1a2c61b4e92fe2349a0b6790
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.5 MB (353512357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd15bc793cd4fa5c40870364aead74bede9ba8e13c381b676e797b71a0e827b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Tue, 15 Sep 2020 21:22:13 GMT
ADD file:8011e31575cbf4b8ebb243821b300ba24330e02cab925024aa98f4ce27997846 in / 
# Tue, 15 Sep 2020 21:22:13 GMT
CMD ["/bin/bash"]
# Tue, 15 Sep 2020 21:41:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 15 Sep 2020 21:41:02 GMT
ENV LANG=C.UTF-8
# Tue, 15 Sep 2020 21:41:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Tue, 15 Sep 2020 21:41:02 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Oct 2020 17:34:41 GMT
ENV JAVA_VERSION=16-ea+19
# Mon, 12 Oct 2020 17:35:22 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_linux-aarch64_bin.tar.gz; 			downloadSha256=9e7094e0dcba61b6b8111f48934cb7395e6dafb1d1ddea7d2296cb0872d67d66; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_linux-x64_bin.tar.gz; 			downloadSha256=487e44f1ec92106437a96f8af07a83ac314dee51dfd46838c23657e550bc616f; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Oct 2020 17:35:23 GMT
CMD ["jshell"]
# Mon, 12 Oct 2020 18:09:10 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 12 Oct 2020 18:09:10 GMT
ARG USER_HOME_DIR=/root
# Mon, 12 Oct 2020 18:09:11 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 12 Oct 2020 18:09:11 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 12 Oct 2020 18:09:24 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils
# Mon, 12 Oct 2020 18:09:26 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 12 Oct 2020 18:09:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 12 Oct 2020 18:09:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 12 Oct 2020 18:09:27 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 12 Oct 2020 18:09:27 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 12 Oct 2020 18:09:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 12 Oct 2020 18:09:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:79701ada7495177c292979fd69d41eee91dc93ef0feea5ff95bb453f4ab7a1c5`  
		Last Modified: Mon, 14 Sep 2020 18:35:00 GMT  
		Size: 54.2 MB (54164063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47708145bbc56f1e73084e03c4662a6b29535708cfe5d51510cdae37bc363ba3`  
		Last Modified: Tue, 15 Sep 2020 21:47:10 GMT  
		Size: 13.5 MB (13491818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499afc7d5d1fe83ff9daf193859ad32eccfb8d949a94313bede60b88640dc280`  
		Last Modified: Mon, 12 Oct 2020 17:39:30 GMT  
		Size: 196.5 MB (196547147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c53a7a72c23b115b17ae27fca8000a1e2b44af947295311b27b0ecca7b224a5`  
		Last Modified: Mon, 12 Oct 2020 18:11:28 GMT  
		Size: 79.7 MB (79726895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1776ee31134b39e3645995a0ebb873d03e904a30e67c6c01c6bdd20c13edf4b6`  
		Last Modified: Mon, 12 Oct 2020 18:10:56 GMT  
		Size: 9.6 MB (9581219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae0677f9150498a0bf0027810c8eb315a8d580b801c27758e226f156f54ea0`  
		Last Modified: Mon, 12 Oct 2020 18:10:54 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca187e6e59af7a88aeda722d0668cdbfb154cd0d3bf149adebdf44da48b5ee7`  
		Last Modified: Mon, 12 Oct 2020 18:10:54 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:728cb1eeb08ae202a01a94b2a303f326182c0561b42947b6af4d5a6d872f08bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308817476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc19d9befca7fd287d91fe143caad4b70adf440ee6c1f1dfa10b414fbc68655`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Tue, 15 Sep 2020 20:41:01 GMT
ADD file:b3bd5c2ec8ff0efe8a0b1384563b42f02d6bcf7531132d9ec4748ecfe264d476 in / 
# Tue, 15 Sep 2020 20:41:02 GMT
CMD ["/bin/bash"]
# Tue, 15 Sep 2020 20:58:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 15 Sep 2020 20:58:31 GMT
ENV LANG=C.UTF-8
# Tue, 15 Sep 2020 20:58:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Tue, 15 Sep 2020 20:58:39 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Oct 2020 17:45:55 GMT
ENV JAVA_VERSION=16-ea+19
# Mon, 12 Oct 2020 17:46:39 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_linux-aarch64_bin.tar.gz; 			downloadSha256=9e7094e0dcba61b6b8111f48934cb7395e6dafb1d1ddea7d2296cb0872d67d66; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/19/GPL/openjdk-16-ea+19_linux-x64_bin.tar.gz; 			downloadSha256=487e44f1ec92106437a96f8af07a83ac314dee51dfd46838c23657e550bc616f; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Oct 2020 17:46:41 GMT
CMD ["jshell"]
# Mon, 12 Oct 2020 18:09:26 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 12 Oct 2020 18:09:27 GMT
ARG USER_HOME_DIR=/root
# Mon, 12 Oct 2020 18:09:28 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 12 Oct 2020 18:09:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 12 Oct 2020 18:10:03 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils
# Mon, 12 Oct 2020 18:10:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 12 Oct 2020 18:10:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 12 Oct 2020 18:10:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 12 Oct 2020 18:10:12 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 12 Oct 2020 18:10:12 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 12 Oct 2020 18:10:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 12 Oct 2020 18:10:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a805b9845b615e5963d09def3e5e9919b39e76b5122c2abecc98d4a4bb358394`  
		Last Modified: Mon, 14 Sep 2020 17:43:27 GMT  
		Size: 54.3 MB (54266593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f893975677f1e890e793bb79d6684177489551bc055499096c3c153bc305e940`  
		Last Modified: Tue, 15 Sep 2020 21:04:39 GMT  
		Size: 14.4 MB (14366569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b559be1e73192a25483c03e133e5019d8d615a52508eee13d766036f45acbb06`  
		Last Modified: Mon, 12 Oct 2020 17:50:37 GMT  
		Size: 175.3 MB (175265043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c2169b419ff0e9544ed6febaee3b9a95fcea08c83aed81fc46dc1082855ee6`  
		Last Modified: Mon, 12 Oct 2020 18:11:25 GMT  
		Size: 55.3 MB (55336842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e89f608c62050c03345f86755fa60ead49149eb91a057f502cae2d23fa110e`  
		Last Modified: Mon, 12 Oct 2020 18:11:18 GMT  
		Size: 9.6 MB (9581207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2ba94f85a4a9612ec4c8386da53e87ef81c6f25ee492abca90bf472b3a64a2e`  
		Last Modified: Mon, 12 Oct 2020 18:11:17 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8e608946408d9c79004960181d3db4a6d33382d63dc4268b33c606cc0a25d`  
		Last Modified: Mon, 12 Oct 2020 18:11:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
