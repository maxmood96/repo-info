## `maven:3-openjdk-17`

```console
$ docker pull maven@sha256:b7b48077cd1d42d1f9a845440b78f3dd7df43b52a1d14e57593e9969205f0259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-17` - linux; amd64

```console
$ docker pull maven@sha256:78af8dd8fe2ded6d535a3df33985a7adbb00e4922a71ca4a745628caac29ae3b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421547372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0496046eba70e3a1dd8b4c568011a0446e9e241947d8ee810a27ce30460b79`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 23 Jul 2021 01:13:10 GMT
ADD file:c047ac1784a3670f52d12ad67cf238654237149dc2c9d7b921cd005c7ec42105 in / 
# Fri, 23 Jul 2021 01:13:11 GMT
CMD ["/bin/bash"]
# Fri, 23 Jul 2021 06:40:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 23 Jul 2021 06:41:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 23 Jul 2021 06:41:12 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 06:41:13 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 18:24:04 GMT
ENV JAVA_VERSION=17-ea+32
# Fri, 23 Jul 2021 18:24:14 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/32/GPL/openjdk-17-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='9e5b6c4e27d2adda491036edeed79fafea2961c78a96265a34dd4bb82d7bbf0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/32/GPL/openjdk-17-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='28445241fd8ac0a8572f1dc202f7b492389c3a28d510b8c23cf7538a53b17eab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 18:24:14 GMT
CMD ["jshell"]
# Fri, 23 Jul 2021 18:58:40 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 23 Jul 2021 18:58:41 GMT
ARG USER_HOME_DIR=/root
# Fri, 23 Jul 2021 18:58:41 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 23 Jul 2021 18:58:41 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 23 Jul 2021 18:59:08 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 23 Jul 2021 18:59:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 23 Jul 2021 18:59:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 23 Jul 2021 18:59:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 23 Jul 2021 18:59:12 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 23 Jul 2021 18:59:12 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 23 Jul 2021 18:59:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 23 Jul 2021 18:59:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1da50e1664e1b58d93182fe5af093c642668ec93f67fcd8215b9c1979930b84d`  
		Last Modified: Fri, 23 Jul 2021 01:14:27 GMT  
		Size: 42.2 MB (42178827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8e5a84542212d0126ce88facd146befb1c731fb4faafb50a7b96ad0568cd9`  
		Last Modified: Fri, 23 Jul 2021 06:49:18 GMT  
		Size: 13.4 MB (13390485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bf0ab8475d0a5ceeaebb41197f9558580d90e8dd5e3bb12c99f5b47b488df0`  
		Last Modified: Fri, 23 Jul 2021 18:30:10 GMT  
		Size: 187.1 MB (187121353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd9e0b2e09e0add1282572433c4fc8022ea8aa31f4b1b5e13ce58b3af33dfb`  
		Last Modified: Fri, 23 Jul 2021 19:02:20 GMT  
		Size: 169.2 MB (169244534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7de9acd1dd99dc70cc5f020af1657c0026f8ba00f998e2b6658b09f950eba4`  
		Last Modified: Fri, 23 Jul 2021 19:02:06 GMT  
		Size: 9.6 MB (9610961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684cc9b7b579d921f5cbe80803fa7bcb02faf69ddbaedbb17b2660097d478f18`  
		Last Modified: Fri, 23 Jul 2021 19:02:05 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4cbadb62f717f75c2af18500f4f0004f2bb7a80f3a476b87108b8057160fe76`  
		Last Modified: Fri, 23 Jul 2021 19:02:05 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:70d90d59a56f7f61a0c3229a8601753beb33e6dd53bc8e62ad5e0f3e94ae3967
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401246658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aec28c531770a361d9ec7a5878f4b82fd93236a01fb2b4fdcf029ae2f41feeb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 23 Jul 2021 00:50:01 GMT
ADD file:2b2b9653730f3bb9d3a6327d4b9a6b425279decd90b84755c033b95536ebe027 in / 
# Fri, 23 Jul 2021 00:50:02 GMT
CMD ["/bin/bash"]
# Fri, 23 Jul 2021 04:34:01 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 23 Jul 2021 04:34:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 23 Jul 2021 04:34:49 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 04:34:49 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jul 2021 18:48:15 GMT
ENV JAVA_VERSION=17-ea+32
# Fri, 23 Jul 2021 18:49:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/32/GPL/openjdk-17-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='9e5b6c4e27d2adda491036edeed79fafea2961c78a96265a34dd4bb82d7bbf0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/32/GPL/openjdk-17-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='28445241fd8ac0a8572f1dc202f7b492389c3a28d510b8c23cf7538a53b17eab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Jul 2021 18:49:05 GMT
CMD ["jshell"]
# Fri, 23 Jul 2021 20:19:32 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 23 Jul 2021 20:19:32 GMT
ARG USER_HOME_DIR=/root
# Fri, 23 Jul 2021 20:19:32 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 23 Jul 2021 20:19:32 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 23 Jul 2021 20:19:56 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN microdnf install findutils git
# Fri, 23 Jul 2021 20:20:05 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 23 Jul 2021 20:20:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 23 Jul 2021 20:20:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 23 Jul 2021 20:20:05 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 23 Jul 2021 20:20:05 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 23 Jul 2021 20:20:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 23 Jul 2021 20:20:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a21bf021f71862240d392ffdd7f376294fa46f2729f1771f269c1a888d0aab25`  
		Last Modified: Fri, 23 Jul 2021 00:51:19 GMT  
		Size: 42.0 MB (42040756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20d17a0583d5448fece8a45dc16fcd83266885f5eabbeaa44c9bcc8738ed0fa`  
		Last Modified: Fri, 23 Jul 2021 04:45:32 GMT  
		Size: 14.2 MB (14170914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6986f01540e442567196c466887cfc14438901fd8081c66a5b9368fb75417bf`  
		Last Modified: Fri, 23 Jul 2021 19:00:28 GMT  
		Size: 185.9 MB (185930056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e98cffe3edbbfa03eef53afefa02696a7bb5a053ddfb24244f63b5e3b712c`  
		Last Modified: Fri, 23 Jul 2021 20:25:00 GMT  
		Size: 149.5 MB (149492744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55778280c118d8ecd62c9457a8498cd24a67a36fb619005ba99551c1124a0538`  
		Last Modified: Fri, 23 Jul 2021 20:24:45 GMT  
		Size: 9.6 MB (9610971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f326de0b94e0b16bf4b2a69c574443c951ccd030239a27f2de59313121647b77`  
		Last Modified: Fri, 23 Jul 2021 20:24:44 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57cfe04f4b568bb54430399c895ef2a25d03efea6735b633d4276c1aaac7c54`  
		Last Modified: Fri, 23 Jul 2021 20:24:45 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
