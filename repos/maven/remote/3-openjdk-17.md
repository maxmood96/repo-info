## `maven:3-openjdk-17`

```console
$ docker pull maven@sha256:1feb63b127b4fb414bd87247c7545392d69a08f9452b0857f5e232f0294b5bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-17` - linux; amd64

```console
$ docker pull maven@sha256:b59171169fab1fbf25ad50a2f848d8e828426e9946819d6d3ebff6c29b400ad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 MB (392628935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9993615dd7ff53bcc395d351562d19813f47bd7e8fbd6d6a4256d1b3a40b8eca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 01 Feb 2021 20:32:17 GMT
ADD file:2ba8f9c8e1d7e464c075fdd46e81f2e15a69d9a5aefb4b991cccb352e082af2f in / 
# Mon, 01 Feb 2021 20:32:17 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 23:54:30 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 23:54:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 23:54:30 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 23:54:30 GMT
ENV LANG=C.UTF-8
# Thu, 18 Feb 2021 23:21:07 GMT
ENV JAVA_VERSION=17-ea+10
# Thu, 18 Feb 2021 23:21:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/10/GPL/openjdk-17-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='89ed24a42ee151bc720dcc6fd76272404a99b080acf107b8ec42b1270d2f3953'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/10/GPL/openjdk-17-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='f5dd69285e57325b130f80b5dc62beffa9ccdab08f881bbdb68ecbe7e3b249ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Feb 2021 23:21:51 GMT
CMD ["jshell"]
# Thu, 18 Feb 2021 23:48:02 GMT
ARG MAVEN_VERSION=3.6.3
# Thu, 18 Feb 2021 23:48:03 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Feb 2021 23:48:03 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Thu, 18 Feb 2021 23:48:03 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Thu, 18 Feb 2021 23:48:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Thu, 18 Feb 2021 23:48:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 18 Feb 2021 23:48:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Feb 2021 23:48:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Feb 2021 23:48:36 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 18 Feb 2021 23:48:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 18 Feb 2021 23:48:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Feb 2021 23:48:37 GMT
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
	-	`sha256:1d252b485c32fd90dfe04301c62e32978e62a4c6543cf3ea30d6d911593b17db`  
		Last Modified: Thu, 18 Feb 2021 23:28:08 GMT  
		Size: 185.7 MB (185678182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c365a397e8d923eb58b8da2be438864fba726d032e814a1ff7fe503dff6f7d3a`  
		Last Modified: Thu, 18 Feb 2021 23:51:33 GMT  
		Size: 142.0 MB (142021477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7412fafba11970b18cc909681e25b920e454b0bb098c09be2560145c0f3868`  
		Last Modified: Thu, 18 Feb 2021 23:51:19 GMT  
		Size: 9.6 MB (9581192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d27af16b26899589e6a99e4c33fe5144d0173ed71a0d01502a68904862efafc`  
		Last Modified: Thu, 18 Feb 2021 23:51:18 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ae853050781217a169020e0cde1f7dc5bbc08e067ca0f426fa2c7488d42d9e`  
		Last Modified: Thu, 18 Feb 2021 23:51:18 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5f97780960c26f3899293a208433bee271f025c7218f9212326b5358aa48cb3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367395631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ab5c5ec2ce0b3054e099fc5706b232b8b0f88409a7c100ce249afd6b2c48d1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 01 Feb 2021 21:00:54 GMT
ADD file:40a46ad11c4530459867a348c980e7ed1ba9fe6bdf74da38208ee8bf7be1f81d in / 
# Mon, 01 Feb 2021 21:00:56 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:05:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 21:05:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 21:05:58 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:05:59 GMT
ENV LANG=C.UTF-8
# Thu, 18 Feb 2021 23:41:25 GMT
ENV JAVA_VERSION=17-ea+10
# Thu, 18 Feb 2021 23:42:14 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/10/GPL/openjdk-17-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='89ed24a42ee151bc720dcc6fd76272404a99b080acf107b8ec42b1270d2f3953'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/10/GPL/openjdk-17-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='f5dd69285e57325b130f80b5dc62beffa9ccdab08f881bbdb68ecbe7e3b249ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Feb 2021 23:42:15 GMT
CMD ["jshell"]
# Fri, 19 Feb 2021 00:18:06 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 19 Feb 2021 00:18:07 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Feb 2021 00:18:08 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 19 Feb 2021 00:18:09 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 19 Feb 2021 00:19:38 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 19 Feb 2021 00:19:43 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 19 Feb 2021 00:19:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Feb 2021 00:19:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Feb 2021 00:19:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 19 Feb 2021 00:19:46 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 19 Feb 2021 00:19:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Feb 2021 00:19:47 GMT
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
	-	`sha256:f7c01f8e67b9089e00c8c8901e115f6f99378f5d62125225a65003de92d6397b`  
		Last Modified: Thu, 18 Feb 2021 23:47:43 GMT  
		Size: 180.0 MB (180043588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e91c63ec8cc1398a77fc4e5c5a5152c723d68135e3ad600ab6dee5b213ef20`  
		Last Modified: Fri, 19 Feb 2021 00:23:19 GMT  
		Size: 121.7 MB (121716306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4336d3a7d808637bd30696d538fa2c67f905ac885a2cbc59a33ec1a43cf9f834`  
		Last Modified: Fri, 19 Feb 2021 00:22:58 GMT  
		Size: 9.6 MB (9581205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5ae941f1bb42e5d830fc26f5084120b61a796f7b18694403376ad6390f503f`  
		Last Modified: Fri, 19 Feb 2021 00:22:57 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c569b6b0be9ff0384cf67ecff1d5ed7a7bd11c097f4f94a9723da51103083a8e`  
		Last Modified: Fri, 19 Feb 2021 00:22:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
