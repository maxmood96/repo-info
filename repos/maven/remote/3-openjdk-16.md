## `maven:3-openjdk-16`

```console
$ docker pull maven@sha256:f21c0e82937d9a9216ec5def4ef0b6e9e17ffcf0f56ed082e812c729fb55a339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16` - linux; amd64

```console
$ docker pull maven@sha256:1cc0d55f54f422369af218c86d4f9035d989b888ca6c0cb45c3e1c9712c337a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 MB (389329752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9605d3b459b2bc84da204b0f0da6f9426667ac8e7ded5c6e33c26c1cc33f54ee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 15 Jan 2021 00:30:38 GMT
ADD file:2987f8143a9c4f758731c17e307a6c7ca9e5e1a974df3405a17d2699da7d8351 in / 
# Fri, 15 Jan 2021 00:30:39 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:56:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 15 Jan 2021 00:56:53 GMT
ENV LANG=C.UTF-8
# Fri, 15 Jan 2021 00:59:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 15 Jan 2021 00:59:09 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Jan 2021 01:23:02 GMT
ENV JAVA_VERSION=16-ea+33
# Sat, 23 Jan 2021 01:24:00 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_linux-aarch64_bin.tar.gz; 			downloadSha256=1da1b96306a0ede9e1c7b4284772b5de3c9f8f08f895e082f561f5f3c86ea3be; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_linux-x64_bin.tar.gz; 			downloadSha256=ba2ac6ccca898cd63090d768b89a95fba76b6303a55c41e851d75dd0c5afcee8; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 23 Jan 2021 01:24:01 GMT
CMD ["jshell"]
# Sat, 23 Jan 2021 01:58:02 GMT
ARG MAVEN_VERSION=3.6.3
# Sat, 23 Jan 2021 01:58:02 GMT
ARG USER_HOME_DIR=/root
# Sat, 23 Jan 2021 01:58:02 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Sat, 23 Jan 2021 01:58:02 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Sat, 23 Jan 2021 01:58:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Sat, 23 Jan 2021 01:58:37 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 23 Jan 2021 01:58:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 23 Jan 2021 01:58:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 23 Jan 2021 01:58:38 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 23 Jan 2021 01:58:38 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 23 Jan 2021 01:58:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 23 Jan 2021 01:58:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a73adebe9317092fb1f120a1d0d21f460296e9bde7ac683fd452cfc628c528cf`  
		Last Modified: Wed, 06 Jan 2021 20:23:26 GMT  
		Size: 42.1 MB (42069921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b73bcd34cfec7fc27d7cd00bc22af06df0471526a6d2ceb8e77391a82f300f0`  
		Last Modified: Fri, 15 Jan 2021 01:08:29 GMT  
		Size: 13.3 MB (13277589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f070b002d4e996ca4a83633cb288926fc647b73a5780b943ea710f611cf888`  
		Last Modified: Sat, 23 Jan 2021 01:31:47 GMT  
		Size: 184.8 MB (184764743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db80b3ddfa58704da90e452303ba5e1f44efc7f94a3f4af2b9de3f1a11545259`  
		Last Modified: Sat, 23 Jan 2021 02:01:24 GMT  
		Size: 139.6 MB (139635089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5424ef547c111e1ccd45302e431fd27cee37f9f3a30c7ef06d769dc09844aa`  
		Last Modified: Sat, 23 Jan 2021 02:01:10 GMT  
		Size: 9.6 MB (9581190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e523cae2730934840b33799b48503f2378457361f800c00fd62008d150731`  
		Last Modified: Sat, 23 Jan 2021 02:01:09 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0d39c7c278b19990351305cd7e43530c3a803c013dd0a6e13d04334e403966`  
		Last Modified: Sat, 23 Jan 2021 02:01:09 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1d94643cd0dc93f227553ad43e685cc2188ee91eb7150c283b530b97b21f868c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.4 MB (362425984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabac6e9d8c84d310fd6d24ee9b91f3490357ef07cd7574cb9dc87bdde73d8e1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 15 Jan 2021 00:05:48 GMT
ADD file:ad2b2ddca8e17229cc8d1380ecda32c4b2c04f1e2aed8f493f745c6352b34e60 in / 
# Fri, 15 Jan 2021 00:05:49 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:43:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 15 Jan 2021 00:43:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 Jan 2021 00:46:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 15 Jan 2021 00:46:49 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Jan 2021 22:48:03 GMT
ENV JAVA_VERSION=16-ea+32
# Fri, 15 Jan 2021 22:49:01 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/32/GPL/openjdk-16-ea+32_linux-aarch64_bin.tar.gz; 			downloadSha256=c4ccb6df63b7b973504ad4dec0164d308d5dce7a5e2dcc508180deda33d4e61a; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/32/GPL/openjdk-16-ea+32_linux-x64_bin.tar.gz; 			downloadSha256=c951c0f2d55bc67fecbe0913675811721d13de16f4a81bf5363b660d17c02f0b; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 15 Jan 2021 22:49:04 GMT
CMD ["jshell"]
# Sat, 16 Jan 2021 00:28:23 GMT
ARG MAVEN_VERSION=3.6.3
# Sat, 16 Jan 2021 00:28:23 GMT
ARG USER_HOME_DIR=/root
# Sat, 16 Jan 2021 00:28:24 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Sat, 16 Jan 2021 00:28:25 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Sat, 16 Jan 2021 00:29:50 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Sat, 16 Jan 2021 00:30:02 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 16 Jan 2021 00:30:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 16 Jan 2021 00:30:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 16 Jan 2021 00:30:05 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 16 Jan 2021 00:30:05 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 16 Jan 2021 00:30:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 16 Jan 2021 00:30:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d0eecbd2c3e7306adbf5b4a0d9bebc7d266ebe78bda044d35b0994c1cf655a54`  
		Last Modified: Wed, 06 Jan 2021 20:47:00 GMT  
		Size: 42.0 MB (41996293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8f86f1d6521cdc8416801b8dd0b15d9a5a85bfa3eb8f9afa832aa8cc652732`  
		Last Modified: Fri, 15 Jan 2021 00:55:15 GMT  
		Size: 14.1 MB (14057398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d1278f211ac54faae9306e9dda291d7e00388b5b672542d754d9a70a628173`  
		Last Modified: Fri, 15 Jan 2021 22:59:17 GMT  
		Size: 179.1 MB (179130770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae4139ac43bacf26977d131698a90a59d0b11263b4ddd739b60facbadc88407`  
		Last Modified: Sat, 16 Jan 2021 00:34:27 GMT  
		Size: 117.7 MB (117659110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d05c99f24cb8b28d442d7d30b648c64bdf4d0497119003bf0debe45d40f597`  
		Last Modified: Sat, 16 Jan 2021 00:34:13 GMT  
		Size: 9.6 MB (9581196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4719c963a9ac6136d17e6a04f0625c612961410769c7bf2845c8b1f0ab7be2e8`  
		Last Modified: Sat, 16 Jan 2021 00:34:07 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de1b562a7430f785409f7fa70ae3ccbc2ae031aecaac35e4dcbee8a68ffdfd1`  
		Last Modified: Sat, 16 Jan 2021 00:34:08 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
