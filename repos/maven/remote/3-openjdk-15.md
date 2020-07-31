## `maven:3-openjdk-15`

```console
$ docker pull maven@sha256:767a5f50f11d164b5654fd5b11b39f26f665b172be1592bbb8a60a81d6bfe917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-openjdk-15` - linux; amd64

```console
$ docker pull maven@sha256:81a5164daa7204cb1d781eb361f38931c90ed576c20357659dc141982d809526
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269541497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0027be60bb9bd6af63a6d14a5591950ed89d2f404a64251c74a8f8542da496`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 17 Jul 2020 02:36:32 GMT
ADD file:0846801b1ef59a7513feb7e2704d8b0c5618da23e28ecff72f64ac14799ee0c1 in / 
# Fri, 17 Jul 2020 02:36:32 GMT
CMD ["/bin/bash"]
# Fri, 17 Jul 2020 02:53:07 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 17 Jul 2020 02:53:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Jul 2020 02:54:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 17 Jul 2020 02:54:21 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jul 2020 22:23:20 GMT
ENV JAVA_VERSION=15-ea+34
# Fri, 31 Jul 2020 22:23:46 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/34/GPL/openjdk-15-ea+34_linux-aarch64_bin.tar.gz; 			downloadSha256=c3d653467f34723f6d2eeb8a1d9c0266f2222af6d07c18f58ca697e8ae2de1c2; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/34/GPL/openjdk-15-ea+34_linux-x64_bin.tar.gz; 			downloadSha256=359d74ed4010ef32ae32bb0665a7a62bc5d440aa17c382f22a6d103bf83589a5; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Fri, 31 Jul 2020 22:23:46 GMT
CMD ["jshell"]
# Fri, 31 Jul 2020 22:46:17 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 31 Jul 2020 22:46:17 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Jul 2020 22:46:17 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 31 Jul 2020 22:46:17 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 31 Jul 2020 22:46:20 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 31 Jul 2020 22:46:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Jul 2020 22:46:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Jul 2020 22:46:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 31 Jul 2020 22:46:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 31 Jul 2020 22:46:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Jul 2020 22:46:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bce8f778fef067eed3d092243c838d674cb1ef39441d85d0ca84382084a69093`  
		Last Modified: Fri, 17 Jul 2020 02:37:13 GMT  
		Size: 48.0 MB (48014772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778faef342036a08101af5d8806ab4f17eda31d2a4e102e33a115bc619bc019`  
		Last Modified: Fri, 17 Jul 2020 02:58:39 GMT  
		Size: 16.2 MB (16187244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607312b29d1c750b6baa72567548fbec9c5b69666c39d1b7323c4a51797de3e2`  
		Last Modified: Fri, 31 Jul 2020 22:27:51 GMT  
		Size: 195.8 MB (195756610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9c03875d4c097f183a757cce3cec8767f36d15a2db5d9e4d71b88314194bd4`  
		Last Modified: Fri, 31 Jul 2020 22:47:57 GMT  
		Size: 9.6 MB (9581657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e51b61b9a1a72cdd8ba492815b945ac20427c32b025b81995538e6a9811c39a`  
		Last Modified: Fri, 31 Jul 2020 22:47:56 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403e4be743d5f6c5fd371297b2fba2851275e09997c72871a37a217f37ecea12`  
		Last Modified: Fri, 31 Jul 2020 22:47:56 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
