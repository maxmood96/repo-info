## `maven:3-openjdk-18`

```console
$ docker pull maven@sha256:2a688a65570aa9beff35636df751663623193a4b7c5a4f80a4eb1dbb0815ccc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18` - linux; amd64

```console
$ docker pull maven@sha256:1936d70bb3415a0d7e822ed484cdb4974593b195091c145b52ba7775003dc3f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.5 MB (459538535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c813ec5fd45171e0568f0fd534c362f4c75d17e8782671b9ab022e2045dcd5d2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:44:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 08 Feb 2023 19:45:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 08 Feb 2023 19:45:52 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Feb 2023 19:45:52 GMT
ENV LANG=C.UTF-8
# Wed, 08 Feb 2023 19:45:52 GMT
ENV JAVA_VERSION=18.0.2.1
# Wed, 08 Feb 2023 19:46:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 08 Feb 2023 19:46:03 GMT
CMD ["jshell"]
# Wed, 08 Feb 2023 20:08:30 GMT
RUN microdnf install findutils git
# Wed, 08 Feb 2023 20:08:31 GMT
ARG MAVEN_VERSION=3.8.7
# Wed, 08 Feb 2023 20:08:32 GMT
ARG USER_HOME_DIR=/root
# Wed, 08 Feb 2023 20:08:32 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Wed, 08 Feb 2023 20:08:32 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Wed, 08 Feb 2023 20:08:40 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 08 Feb 2023 20:08:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 08 Feb 2023 20:08:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 08 Feb 2023 20:08:40 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 08 Feb 2023 20:08:40 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 08 Feb 2023 20:08:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 08 Feb 2023 20:08:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b698b7af4b18900b53c768746b1dfb603dfb9aec1eea328fdac86d37001e2a`  
		Last Modified: Wed, 08 Feb 2023 19:48:51 GMT  
		Size: 12.3 MB (12256034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a27dbe0150755fca4304b4afd0d7d6dd6a40ede6fdb30da8568e9e8cdf23a9`  
		Last Modified: Wed, 08 Feb 2023 19:51:01 GMT  
		Size: 188.7 MB (188744944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1420bb97853b75f517c109761badd22d42c2682c1393f81b5cee96d52ca55246`  
		Last Modified: Wed, 08 Feb 2023 20:10:53 GMT  
		Size: 205.6 MB (205629260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a06b7d74e4f66caefb7fc11e4b822ce8df01746707aec3071422e1f8f75e60a`  
		Last Modified: Wed, 08 Feb 2023 20:10:39 GMT  
		Size: 8.4 MB (8351170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c0e262d600482404a491d6a8561ebc8030dc61b09b8e22edff8c3596ac3e03`  
		Last Modified: Wed, 08 Feb 2023 20:10:38 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909ee600276b1d6137fbdbfbbe8724cf6a29beacbe6c1af3051fcc2f3dd60cf6`  
		Last Modified: Wed, 08 Feb 2023 20:10:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:940e7a970d8576d137f95ff0d1e4a4bf6003c13fd68d439f49d7c0dbff2ee364
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.8 MB (470770782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec4d47f5ff9a92b232309dfba27a3b58098e220cf77c2ccec4a6e6f3a2903db`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 27 Jan 2023 22:41:06 GMT
ADD file:63b5b4161762e1845c1eb2bb2c967a07179819b4a1f12ab7596d9c6bd15c9cbd in / 
# Fri, 27 Jan 2023 22:41:06 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 22:58:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 27 Jan 2023 23:00:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 27 Jan 2023 23:00:57 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 23:00:57 GMT
ENV LANG=C.UTF-8
# Fri, 27 Jan 2023 23:00:57 GMT
ENV JAVA_VERSION=18.0.2.1
# Fri, 27 Jan 2023 23:01:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 27 Jan 2023 23:01:07 GMT
CMD ["jshell"]
# Fri, 27 Jan 2023 23:25:39 GMT
RUN microdnf install findutils git
# Fri, 27 Jan 2023 23:25:41 GMT
ARG MAVEN_VERSION=3.8.7
# Fri, 27 Jan 2023 23:25:41 GMT
ARG USER_HOME_DIR=/root
# Fri, 27 Jan 2023 23:25:41 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Fri, 27 Jan 2023 23:25:41 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Fri, 27 Jan 2023 23:25:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 27 Jan 2023 23:25:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 27 Jan 2023 23:25:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 27 Jan 2023 23:25:49 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 27 Jan 2023 23:25:49 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 27 Jan 2023 23:25:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 27 Jan 2023 23:25:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d26cdabfc8c6a31055d655a58d8a8f9757f43e1ce58451b8b6b02c5dd6e6d482`  
		Last Modified: Fri, 27 Jan 2023 22:42:28 GMT  
		Size: 43.5 MB (43456742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175fa1491e9fc183c9d73f4393db52b943e03e50258cf81fd2c6970905be7318`  
		Last Modified: Fri, 27 Jan 2023 23:04:19 GMT  
		Size: 13.1 MB (13068665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d612a13a024d09e570199251483c892cb2e0c651910ecdb1aef12e20dc1d30`  
		Last Modified: Fri, 27 Jan 2023 23:07:12 GMT  
		Size: 187.7 MB (187659354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fe14c393d3aee0154af6de14e86e3da5d6b8e6adf96abec580d0c11174c4ad`  
		Last Modified: Fri, 27 Jan 2023 23:27:33 GMT  
		Size: 218.2 MB (218233640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0303ca529897800cf8f30dca319e189616099ccf69206e67702c2299b44deaf8`  
		Last Modified: Fri, 27 Jan 2023 23:27:21 GMT  
		Size: 8.4 MB (8351172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7c264aab79fd361c6fe5514705dbe8470797720052986c92f068e3b013a3e5`  
		Last Modified: Fri, 27 Jan 2023 23:27:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c37f61dcd123f46e4d5921d16df3ae15294f924bee17baf636cde3aecb6514`  
		Last Modified: Fri, 27 Jan 2023 23:27:20 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
