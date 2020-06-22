## `maven:3-openjdk-15`

```console
$ docker pull maven@sha256:72585919c073eb6251dc68fffe8658510d2a76ab9adbdff2a819d92a79731611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-openjdk-15` - linux; amd64

```console
$ docker pull maven@sha256:c4599d88dde6c80a696ef858a27d37e165d4fa0a6d7026fe151205078cf083cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263552622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289c5adcab06712a0b5ecbbd9b84226ba6014f60dcef42d4a43669405b957fa8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Wed, 10 Jun 2020 18:22:32 GMT
ADD file:79bb5b8b89fe54ba99fd9d42d4f8774bfb9c1319ac3ead17a2005a3bde852451 in / 
# Wed, 10 Jun 2020 18:22:32 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2020 18:39:27 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 10 Jun 2020 18:39:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 10 Jun 2020 18:39:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 10 Jun 2020 18:39:28 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2020 19:32:16 GMT
ENV JAVA_VERSION=15-ea+28
# Mon, 22 Jun 2020 19:32:54 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/28/GPL/openjdk-15-ea+28_linux-aarch64_bin.tar.gz; 			downloadSha256=5537ebe5b7beaa80af444a8494dcc1bad474ffae19803ba5327a14071a244869; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/28/GPL/openjdk-15-ea+28_linux-x64_bin.tar.gz; 			downloadSha256=dd7a0712379df213edd7dcee8c7e0ab06b117d851f05c55dbcaabf72536c347e; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 22 Jun 2020 19:32:54 GMT
CMD ["jshell"]
# Mon, 22 Jun 2020 20:12:47 GMT
ARG MAVEN_VERSION=3.6.3
# Mon, 22 Jun 2020 20:12:47 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2020 20:12:48 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Mon, 22 Jun 2020 20:12:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Mon, 22 Jun 2020 20:12:55 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 22 Jun 2020 20:12:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2020 20:12:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2020 20:12:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 22 Jun 2020 20:12:56 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 22 Jun 2020 20:12:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2020 20:12:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fa926a7d213a8145d6a906d68a085b21909a4b26871f142804e68b322bf8881f`  
		Last Modified: Wed, 10 Jun 2020 18:23:43 GMT  
		Size: 43.5 MB (43457466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aed8993d2fb0bb3a658c631a1dfbd05c0e5d42218f419d18238996bd06ea08`  
		Last Modified: Wed, 10 Jun 2020 18:42:25 GMT  
		Size: 14.8 MB (14760261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cde1bcc6ba8d97daf9be05979625d205bac58d7c4b5d771477f5de479c0283`  
		Last Modified: Mon, 22 Jun 2020 19:38:00 GMT  
		Size: 195.8 MB (195752001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14a69c3dd4e458a57d6c7b0df679e019b73a66f737d830a03ec42a96624c859`  
		Last Modified: Mon, 22 Jun 2020 20:14:14 GMT  
		Size: 9.6 MB (9581679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3bf317599361632feffb2d690e8e80d1ba729433b9b1a228197efd08bc6452`  
		Last Modified: Mon, 22 Jun 2020 20:14:13 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432c5f5aeaba6eb1f79f66645c110cbc90e893c82bbadb3723168f5700430a50`  
		Last Modified: Mon, 22 Jun 2020 20:14:13 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
