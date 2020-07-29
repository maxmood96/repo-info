## `maven:3-openjdk-15`

```console
$ docker pull maven@sha256:e0d6efbdbb796155f6294c11563f6e381a893af6b7615b2c2d6326de003b2c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `maven:3-openjdk-15` - linux; amd64

```console
$ docker pull maven@sha256:ee17e2db30ba63c8904777e623a9d71cd0ab7059f2b7d36ff5ea30b9bc70b5e1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269541659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf714f121562a867fc12d5b01ad808981c565c7a0b563b5f076040e3b9b500f`
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
# Fri, 24 Jul 2020 19:14:54 GMT
ENV JAVA_VERSION=15-ea+33
# Wed, 29 Jul 2020 01:25:38 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/33/GPL/openjdk-15-ea+33_linux-aarch64_bin.tar.gz; 			downloadSha256=124fd9ba4611895460ff1547df282cd49b0e9ba2f00c9ead211b59142cc642c4; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/33/GPL/openjdk-15-ea+33_linux-x64_bin.tar.gz; 			downloadSha256=6de169c1de7d37e6c5d5b59a12410a908f22576c07f98d9915a586d91909fc12; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:25:39 GMT
CMD ["jshell"]
# Wed, 29 Jul 2020 02:34:08 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 29 Jul 2020 02:34:08 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 Jul 2020 02:34:08 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 29 Jul 2020 02:34:08 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 29 Jul 2020 02:34:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 29 Jul 2020 02:34:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 Jul 2020 02:34:10 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 Jul 2020 02:34:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 29 Jul 2020 02:34:11 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 29 Jul 2020 02:34:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 Jul 2020 02:34:11 GMT
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
	-	`sha256:96404449b7cb701955a7902c6ac02d881756413c45add2104f3442609eb485f3`  
		Last Modified: Wed, 29 Jul 2020 01:33:38 GMT  
		Size: 195.8 MB (195756770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610b1fabe2546b9603ccc56444cbbfa40b0531a3662be0cccb849b81d247782`  
		Last Modified: Wed, 29 Jul 2020 02:35:56 GMT  
		Size: 9.6 MB (9581661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b950bbcd8b9dac1631841548e7bff4715e7fa48297b9788a972c9d765e48070`  
		Last Modified: Wed, 29 Jul 2020 02:35:55 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fff2accc1c3121d85dd1e76bf989f27099d1345173d1877a2651b2ec2f5ea86`  
		Last Modified: Wed, 29 Jul 2020 02:35:55 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
