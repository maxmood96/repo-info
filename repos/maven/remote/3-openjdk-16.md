## `maven:3-openjdk-16`

```console
$ docker pull maven@sha256:0e80f783d91676a73c0bd92559d9632d5d341835a06294bd92476380b1446c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-16` - linux; amd64

```console
$ docker pull maven@sha256:57a5fb3ddb98bf5d83ebd87e298a3e2209a95d6615d12e99c52645d6204639a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 MB (389389419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7d9bedbda2935acb6451250ee4616f84e9588cc346ae789238a57982ef08c7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:17 GMT
ADD file:2ba8f9c8e1d7e464c075fdd46e81f2e15a69d9a5aefb4b991cccb352e082af2f in / 
# Mon, 01 Feb 2021 20:32:17 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:54:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 23:56:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 01 Feb 2021 23:56:33 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:56:33 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 23:56:33 GMT
ENV JAVA_VERSION=16-ea+34
# Mon, 01 Feb 2021 23:57:13 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='11fd069e3a17a17268b9bb0c8bfd440016af686acfe8d3a4bfd71381fbce22dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='9c294a8b7c440c45968fc16d3aa3261be71b00a7fad22b7aafa2a7b7381e5f2c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 23:57:14 GMT
CMD ["jshell"]
# Tue, 02 Feb 2021 01:17:07 GMT
ARG MAVEN_VERSION=3.6.3
# Tue, 02 Feb 2021 01:17:07 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Feb 2021 01:17:08 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Tue, 02 Feb 2021 01:17:08 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Tue, 02 Feb 2021 01:17:55 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Tue, 02 Feb 2021 01:17:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 02 Feb 2021 01:17:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Feb 2021 01:17:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Feb 2021 01:17:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 02 Feb 2021 01:17:58 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 02 Feb 2021 01:17:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Feb 2021 01:17:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:63e877180dd1388e46564a2b7a72ddf3559dc506f4b6e8b435ed569643811c02`  
		Last Modified: Mon, 01 Feb 2021 20:34:13 GMT  
		Size: 42.1 MB (42069114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cce05db0e2c91e801a9a4024eedc06badf46bad72a11ee564bbacdbc4cbfb40`  
		Last Modified: Tue, 02 Feb 2021 00:04:16 GMT  
		Size: 13.3 MB (13277751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260149ecf640941b8ea7517668ad3a7abe98ca52fe490b61a48cec5ffb7f2148`  
		Last Modified: Tue, 02 Feb 2021 00:05:37 GMT  
		Size: 184.8 MB (184761935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125bba410296c4da157db4e12054b4a1fe0c31919f00f2b947e68ceb3c33ed61`  
		Last Modified: Tue, 02 Feb 2021 01:21:03 GMT  
		Size: 139.7 MB (139698217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86af76a3943c5660433389fd71586485fb8e86a98456fd1d8a382b30211af76`  
		Last Modified: Tue, 02 Feb 2021 01:20:50 GMT  
		Size: 9.6 MB (9581183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2132b4ce430dc3a9cc127243f5f308ee1b942f3bbc28c8992603b24672ed7ab`  
		Last Modified: Tue, 02 Feb 2021 01:20:49 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617958789e89418aef1409491f33f078a6ba1f2e04eea331a64060170599e143`  
		Last Modified: Tue, 02 Feb 2021 01:20:49 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6bb21d34264a6dcdf83343b62ac198073c0415e1e0ef4645f4fa26f446dd44c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.9 MB (362865030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2927a76eaa92b02ecadf018fbceb36b6861c6564fc949adde7a8728b6172ca0b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 01 Feb 2021 21:00:54 GMT
ADD file:40a46ad11c4530459867a348c980e7ed1ba9fe6bdf74da38208ee8bf7be1f81d in / 
# Mon, 01 Feb 2021 21:00:56 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:05:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 21:08:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 01 Feb 2021 21:08:49 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:08:50 GMT
ENV LANG=C.UTF-8
# Fri, 05 Feb 2021 23:05:20 GMT
ENV JAVA_VERSION=16
# Fri, 05 Feb 2021 23:05:58 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/35/GPL/openjdk-16_linux-x64_bin.tar.gz'; 			downloadSha256='25f51624a17545a769e97ded5d51075ab31f9a52de925f7292cff951becf8fd2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/35/GPL/openjdk-16_linux-aarch64_bin.tar.gz'; 			downloadSha256='5afe8561d1c6f777bf0f70bf5d994187ff607b8c4c6ff1194f849a0bb933d805'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 05 Feb 2021 23:06:00 GMT
CMD ["jshell"]
# Sat, 06 Feb 2021 03:18:18 GMT
ARG MAVEN_VERSION=3.6.3
# Sat, 06 Feb 2021 03:18:19 GMT
ARG USER_HOME_DIR=/root
# Sat, 06 Feb 2021 03:18:19 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Sat, 06 Feb 2021 03:18:20 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Sat, 06 Feb 2021 03:20:03 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Sat, 06 Feb 2021 03:20:08 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 06 Feb 2021 03:20:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 06 Feb 2021 03:20:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 06 Feb 2021 03:20:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 06 Feb 2021 03:20:11 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 06 Feb 2021 03:20:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 06 Feb 2021 03:20:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:17e75779b55909cd6075d706cc3fc9f838f287de73b35be3d551231217cbd32c`  
		Last Modified: Mon, 01 Feb 2021 21:02:50 GMT  
		Size: 42.0 MB (41996203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fad58a53edbb48f3027bc56f941db82a77fd6d28a6fc25d4bf2462f3bc62bc`  
		Last Modified: Mon, 01 Feb 2021 21:15:35 GMT  
		Size: 14.1 MB (14057108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39954b1b9e0525425b91844bef6e6ca6595f071efbed409080b1166cea6885c7`  
		Last Modified: Fri, 05 Feb 2021 23:14:53 GMT  
		Size: 179.1 MB (179146092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6403dd5349d88124405f273bf75cf3ea22c6be911ed88499e5527123afb0eb`  
		Last Modified: Sat, 06 Feb 2021 03:23:00 GMT  
		Size: 118.1 MB (118083206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fda1161320bc463bdb5514e7122f2f2a3d03faf90dd62b92810ace0f2f49f24`  
		Last Modified: Sat, 06 Feb 2021 03:22:37 GMT  
		Size: 9.6 MB (9581201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c5b884204595b16e6e4aff9ea9fec6075467d21b9e6feb838a40b9eddde5a4`  
		Last Modified: Sat, 06 Feb 2021 03:22:36 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628cdb95f39533b4a6ab956c3542920cf069c5f445a8306e558ee9b6f303d4af`  
		Last Modified: Sat, 06 Feb 2021 03:22:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
