## `maven:3-openjdk-18`

```console
$ docker pull maven@sha256:4bafe931d580ae46a605216b04e8cc60d4aac3bedb4c4f05dfade5fcda98ae79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18` - linux; amd64

```console
$ docker pull maven@sha256:ff7f1f0b4009184f1ae23046f141c2b628b9a1d517a0e99ae6b9f268eae7feba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 MB (432290711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8535a5b7e5fe5984100574589a1dfb84d9a7852e92918b51c6b0f167b56855`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 17 May 2022 22:41:42 GMT
ADD file:bbaf69bdffd0f506e447fbc52dca450a8966d950b8fa9aebd3a1bd5bd98f8b28 in / 
# Tue, 17 May 2022 22:41:42 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 22:58:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 17 May 2022 22:59:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Tue, 17 May 2022 22:59:37 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 May 2022 22:59:38 GMT
ENV LANG=C.UTF-8
# Tue, 17 May 2022 22:59:38 GMT
ENV JAVA_VERSION=18.0.1.1
# Tue, 17 May 2022 22:59:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 May 2022 22:59:48 GMT
CMD ["jshell"]
# Tue, 17 May 2022 23:35:36 GMT
RUN microdnf install findutils git
# Tue, 17 May 2022 23:35:37 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 17 May 2022 23:35:38 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 May 2022 23:35:38 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 17 May 2022 23:35:38 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 17 May 2022 23:35:40 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 17 May 2022 23:35:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 May 2022 23:35:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 May 2022 23:35:40 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 17 May 2022 23:35:40 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 17 May 2022 23:35:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 May 2022 23:35:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:90a00d516db16c568d3da8e0a7a5a78fa6fef5a39f3d688f831d254b77791565`  
		Last Modified: Tue, 17 May 2022 22:42:38 GMT  
		Size: 39.2 MB (39220501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fc60984518a14e9454222efb6ec0a4e8c3d479f4aaf21961fa45df6b0622e3`  
		Last Modified: Tue, 17 May 2022 23:05:19 GMT  
		Size: 13.5 MB (13504594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f239d0320f82b37907196b2228feab4805e44f61970a28b1a34db7c3b07761`  
		Last Modified: Tue, 17 May 2022 23:06:43 GMT  
		Size: 188.7 MB (188723793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ac8230040c4f131b8964a893c8c4e9f9cf7f2b03cfd9b13d26cfda193f20a`  
		Last Modified: Tue, 17 May 2022 23:38:19 GMT  
		Size: 182.1 MB (182104219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a8bb3ea5156c984d339450050798ddb6eabe512fd31abdfc24a969b11bbbf3`  
		Last Modified: Tue, 17 May 2022 23:38:05 GMT  
		Size: 8.7 MB (8736386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93be4d8f96c82317af05c1951e5414c0bca56af012590177fd23e72772081479`  
		Last Modified: Tue, 17 May 2022 23:38:04 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9069c36849a55dcdb865b3d516a89f4aae2e735636ca856b18e85d2db8c87e0`  
		Last Modified: Tue, 17 May 2022 23:38:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:95f100597c41ba36bcc7940e2009508aef46cdd7797910aa23d33ac0cb772dfd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.8 MB (430780776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195866e129f95457f8d04fbfc287c8aa2ef0f0bcda271c4777bf78d4566c5f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 17 May 2022 22:52:38 GMT
ADD file:263fe8ce0663428b324fa2909814084a77bf17118d772058d41546b804a4b968 in / 
# Tue, 17 May 2022 22:52:39 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:12:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 17 May 2022 23:13:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Tue, 17 May 2022 23:13:09 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 May 2022 23:13:10 GMT
ENV LANG=C.UTF-8
# Tue, 17 May 2022 23:13:11 GMT
ENV JAVA_VERSION=18.0.1.1
# Tue, 17 May 2022 23:13:21 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 17 May 2022 23:13:22 GMT
CMD ["jshell"]
# Wed, 18 May 2022 00:30:43 GMT
RUN microdnf install findutils git
# Wed, 18 May 2022 00:30:44 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 18 May 2022 00:30:44 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 May 2022 00:30:45 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 18 May 2022 00:30:46 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 18 May 2022 00:30:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 18 May 2022 00:30:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 May 2022 00:30:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 May 2022 00:30:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 18 May 2022 00:30:59 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 18 May 2022 00:30:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 May 2022 00:31:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0dbddf5847a3e154a061766ddebe6a3cae471c97cabb3be2871f6d91f265d137`  
		Last Modified: Tue, 17 May 2022 22:53:43 GMT  
		Size: 38.0 MB (38012703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6f1a9466bd7ec91933e510c0258839b2df2301b1d385203492a27a3d66f0ab`  
		Last Modified: Tue, 17 May 2022 23:23:18 GMT  
		Size: 14.3 MB (14273985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3719ea44a5b1f9b64a08e21e76812caac05b904b287c315559c054b99b94181f`  
		Last Modified: Tue, 17 May 2022 23:24:57 GMT  
		Size: 187.6 MB (187644826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13b8dd1ecd50b1be07500d38d107d856541546548ff2a7eaeb77efe511a0001`  
		Last Modified: Wed, 18 May 2022 00:34:37 GMT  
		Size: 182.1 MB (182111705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de50b3cf3b804cbe69e928ac9e13a52d2d59c3117919b7cfff6ea3e442e34c4`  
		Last Modified: Wed, 18 May 2022 00:34:22 GMT  
		Size: 8.7 MB (8736336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af4134d5ee73406fdf09b195254ddd8e80ee17fb762e9d38011f5f30604434c`  
		Last Modified: Wed, 18 May 2022 00:34:21 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61480cefed924285c05040b86940ffb58527d4d9f2df5a384cc3ff1d61ec621`  
		Last Modified: Wed, 18 May 2022 00:34:20 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
