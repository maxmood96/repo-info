## `maven:3-openjdk-18`

```console
$ docker pull maven@sha256:d7015af320ef544bc1d929ea975e13a81ef9680a3f2434f91ce7fa1e1d742162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18` - linux; amd64

```console
$ docker pull maven@sha256:f1074d3d7ad84a189e84281906b57b4de05594bbcb2ab71d7990bb5682ee785c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 MB (433599320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e4ac551946b37ee883e8b5980b751a983a3ff66e33153bfc1e67fa9f70e8b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Jun 2022 17:20:45 GMT
ADD file:03d0377f5864198b250372de990ebf0ef7597cfdcc2e18421e8e0025394a7572 in / 
# Thu, 30 Jun 2022 17:20:46 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:37:33 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:38:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 30 Jun 2022 17:38:38 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jun 2022 17:38:39 GMT
ENV LANG=C.UTF-8
# Thu, 30 Jun 2022 17:38:39 GMT
ENV JAVA_VERSION=18.0.1.1
# Thu, 30 Jun 2022 17:38:48 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 30 Jun 2022 17:38:49 GMT
CMD ["jshell"]
# Thu, 30 Jun 2022 19:03:27 GMT
RUN microdnf install findutils git
# Thu, 30 Jun 2022 19:03:28 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 30 Jun 2022 19:03:28 GMT
ARG USER_HOME_DIR=/root
# Thu, 30 Jun 2022 19:03:28 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 30 Jun 2022 19:03:29 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 30 Jun 2022 19:03:30 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 30 Jun 2022 19:03:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 30 Jun 2022 19:03:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 30 Jun 2022 19:03:30 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 30 Jun 2022 19:03:31 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 30 Jun 2022 19:03:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 30 Jun 2022 19:03:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:337897a5aaf7b54e691e2ed305fbf00e0e8933d5a8a3c07d6fbb95f10b15c644`  
		Last Modified: Thu, 30 Jun 2022 17:21:37 GMT  
		Size: 39.2 MB (39221672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1e7c755c4cccc19ca62372088ce86de7711ff0e0e2e7e18f65711eb2299602`  
		Last Modified: Thu, 30 Jun 2022 17:45:09 GMT  
		Size: 13.5 MB (13509384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12189f728fce80d933f5de5c25b96f870ba7a58ad1df842ee829fab891836aa3`  
		Last Modified: Thu, 30 Jun 2022 17:48:10 GMT  
		Size: 188.7 MB (188723749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6deb11ea4148461ba7ba172bbf98d70b8bcd2a82d383a4895d6f4bab7511c`  
		Last Modified: Thu, 30 Jun 2022 19:06:10 GMT  
		Size: 183.4 MB (183403805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db84804e00a2f66ac2c7a4fd2ffbab0a1775080111cb03418b648adc86904826`  
		Last Modified: Thu, 30 Jun 2022 19:05:57 GMT  
		Size: 8.7 MB (8739499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2169f6b38f97fad9d981937dfee433e0f7ae181839e354442edc515534c36e2`  
		Last Modified: Thu, 30 Jun 2022 19:05:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d9431ef631042bbaf1a6ac2bb6ec9749ff6adb18379b7eac1298abb024ab41`  
		Last Modified: Thu, 30 Jun 2022 19:05:56 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c15fa85128554de9f053c0495ef6e7808066823e7b659c585a42c9193cb6cfd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436693550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27967af9ad45035ea390c5304f1127cb5ba4c61f0dc01177ae1932027d83a22c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 14 Jun 2022 18:41:36 GMT
ADD file:4a6ee90ad73353bfb87b2f121e06bddaed6104536e485baa83fadbe7facc774c in / 
# Tue, 14 Jun 2022 18:41:37 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:58:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:59:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Tue, 14 Jun 2022 18:59:49 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jun 2022 18:59:50 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jun 2022 18:59:51 GMT
ENV JAVA_VERSION=18.0.1.1
# Tue, 14 Jun 2022 19:00:01 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 14 Jun 2022 19:00:01 GMT
CMD ["jshell"]
# Tue, 14 Jun 2022 19:49:16 GMT
RUN microdnf install findutils git
# Wed, 15 Jun 2022 18:41:51 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:41:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:41:53 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:41:54 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:41:57 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:41:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:41:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:42:01 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:42:02 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:42:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:42:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2bbc1bf883bd601c0da5735b538963308bcc17f90d36525ecc93456ffad79064`  
		Last Modified: Tue, 14 Jun 2022 18:42:39 GMT  
		Size: 38.0 MB (38012371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde7855ef536fce06527372a019087e1972db9d092b2ec88091b6017cfc5a16`  
		Last Modified: Tue, 14 Jun 2022 19:10:59 GMT  
		Size: 14.3 MB (14260872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d034f99bc541465c71ffbf364c3fffd21f29e37fd10ba025b194b8d7749b7cf`  
		Last Modified: Tue, 14 Jun 2022 19:12:36 GMT  
		Size: 187.6 MB (187644816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fba70f5da6233e9318f29d5129774b4c5ba9116c8a5c955144d70a1fe8a7802`  
		Last Modified: Wed, 15 Jun 2022 18:50:57 GMT  
		Size: 188.0 MB (188034806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4931e93408cbf106c7358c21a9b6211b83a30f00b953555cb534b66fe7d5c672`  
		Last Modified: Wed, 15 Jun 2022 18:50:41 GMT  
		Size: 8.7 MB (8739469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9316d21182f7a9048c7208341b40d9458cd2d2ec12f1709ab9dc80ac838532`  
		Last Modified: Wed, 15 Jun 2022 18:50:40 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068aab82940b45fbd38386ee68b1890214b8858bd68aa712b2056cda5c546b2`  
		Last Modified: Wed, 15 Jun 2022 18:50:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
