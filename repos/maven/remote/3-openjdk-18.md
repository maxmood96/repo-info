## `maven:3-openjdk-18`

```console
$ docker pull maven@sha256:8494d00767bd41257d2f001396002ca58b6ab618df48bbfc76ff9225a91373fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18` - linux; amd64

```console
$ docker pull maven@sha256:af2d53c826eb37b1b62aac06ceb13ed1a7003eb6e93389170aa246101ce9d5c5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455675448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b419cda6ef24b2f5542a24bd5f3ce270ec86789f2f7ad0fd6745449686ed12b6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:43:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:45:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Tue, 29 Nov 2022 19:45:14 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 19:45:14 GMT
ENV LANG=C.UTF-8
# Tue, 29 Nov 2022 19:45:15 GMT
ENV JAVA_VERSION=18.0.2.1
# Tue, 29 Nov 2022 19:45:25 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Nov 2022 19:45:26 GMT
CMD ["jshell"]
# Tue, 29 Nov 2022 20:08:45 GMT
RUN microdnf install findutils git
# Tue, 29 Nov 2022 20:08:46 GMT
ARG MAVEN_VERSION=3.8.6
# Tue, 29 Nov 2022 20:08:46 GMT
ARG USER_HOME_DIR=/root
# Tue, 29 Nov 2022 20:08:46 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Tue, 29 Nov 2022 20:08:46 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Tue, 29 Nov 2022 20:08:48 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 29 Nov 2022 20:08:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 29 Nov 2022 20:08:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 29 Nov 2022 20:08:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 29 Nov 2022 20:08:48 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 29 Nov 2022 20:08:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 29 Nov 2022 20:08:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1233d0894f0a77c915206fb2429d895953c3cef4150186d415a3c1c256a7f1`  
		Last Modified: Tue, 29 Nov 2022 19:48:00 GMT  
		Size: 12.2 MB (12246997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7d7205b01f8db0cfa3620fa33ba456fa64e6284005b16b80d497255a6756ff`  
		Last Modified: Tue, 29 Nov 2022 19:49:42 GMT  
		Size: 188.7 MB (188744796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95973aee7424c0536a551e172316c0dd0fba6fc6b2ddee85bc2f09ece5840b0`  
		Last Modified: Tue, 29 Nov 2022 20:11:14 GMT  
		Size: 202.1 MB (202071341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb7cd96e8d01c2c95897f33df19d1a6d6da149fff747052197dac25b74486c7`  
		Last Modified: Tue, 29 Nov 2022 20:11:00 GMT  
		Size: 8.7 MB (8739491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c24ec02679744b3378fe2ad2fa918a1eb41adb9ceb9af8cfc76866124d6308f`  
		Last Modified: Tue, 29 Nov 2022 20:10:59 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c3b4a228330b929c7eb72ab654355dfb87eb36d5e6e9ad54408c4fed1d2a3f1`  
		Last Modified: Tue, 29 Nov 2022 20:10:59 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2c48289ac52858176581bf7b710d109439efa405f86d61c6cbf02e455ca0dae8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.6 MB (464644801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f43d529128fe4d2dca333744b2678e5abf05572e44dccfc10cc002024b01dd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:06:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:07:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Tue, 29 Nov 2022 20:07:20 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:07:20 GMT
ENV LANG=C.UTF-8
# Tue, 29 Nov 2022 20:07:20 GMT
ENV JAVA_VERSION=18.0.2.1
# Tue, 29 Nov 2022 20:07:29 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Nov 2022 20:07:31 GMT
CMD ["jshell"]
# Tue, 29 Nov 2022 20:29:33 GMT
RUN microdnf install findutils git
# Tue, 29 Nov 2022 20:29:35 GMT
ARG MAVEN_VERSION=3.8.6
# Tue, 29 Nov 2022 20:29:35 GMT
ARG USER_HOME_DIR=/root
# Tue, 29 Nov 2022 20:29:35 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Tue, 29 Nov 2022 20:29:35 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Tue, 29 Nov 2022 20:29:42 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 29 Nov 2022 20:29:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 29 Nov 2022 20:29:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 29 Nov 2022 20:29:43 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 29 Nov 2022 20:29:43 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 29 Nov 2022 20:29:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 29 Nov 2022 20:29:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa7949e83b2b403f5e3a79f19d33aaa5ea4a1adb33854be91352471fec3fb34`  
		Last Modified: Tue, 29 Nov 2022 20:10:17 GMT  
		Size: 13.1 MB (13066550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb608fad8388f76635f793e4f21b26a4f01ecdc600aa40c7dde11234dd65c76`  
		Last Modified: Tue, 29 Nov 2022 20:11:51 GMT  
		Size: 187.7 MB (187659375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed9fbaf7c2fc26933560fabf4aa7c286e550dd515a5f469ef09ae61dd051d67f`  
		Last Modified: Tue, 29 Nov 2022 20:31:32 GMT  
		Size: 212.4 MB (212403063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124d892472e2507e97ec64f5234a60e31bd646d49775878811e939a8ffe51aed`  
		Last Modified: Tue, 29 Nov 2022 20:31:21 GMT  
		Size: 8.7 MB (8739494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85744f4924fef4b1550aec194ce11e006214b2531a6c71f136f463eac3e0e307`  
		Last Modified: Tue, 29 Nov 2022 20:31:19 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f69f45e831884462468031b01c7baa8407e3d7c777bf133fea651ec6429e08`  
		Last Modified: Tue, 29 Nov 2022 20:31:20 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
