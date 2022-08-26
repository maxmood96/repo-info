## `maven:3-openjdk-18`

```console
$ docker pull maven@sha256:f0274abc67acea265cd843e824812d6ba16e4796d9bef9a0a97ebf0b55ea9892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18` - linux; amd64

```console
$ docker pull maven@sha256:991f06415ecdb46ff5fc94ab73265a4b915be8cc2076a05c8a8991b078bbec28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.9 MB (438898190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73477cf79264692d89558f498deb5e00f297facc0c20d7b227b97aace62fae4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 26 Aug 2022 21:25:57 GMT
ADD file:923c2af16ef366fe4e85b8ba8979b8a31da0cdbc606c08148463849bf66c395b in / 
# Fri, 26 Aug 2022 21:25:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 21:43:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 26 Aug 2022 21:46:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 26 Aug 2022 21:46:11 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 21:46:11 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 21:46:11 GMT
ENV JAVA_VERSION=18.0.2.1
# Fri, 26 Aug 2022 21:46:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Aug 2022 21:46:22 GMT
CMD ["jshell"]
# Fri, 26 Aug 2022 22:11:53 GMT
RUN microdnf install findutils git
# Fri, 26 Aug 2022 22:11:54 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 26 Aug 2022 22:11:54 GMT
ARG USER_HOME_DIR=/root
# Fri, 26 Aug 2022 22:11:54 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 26 Aug 2022 22:11:54 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 26 Aug 2022 22:12:02 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 26 Aug 2022 22:12:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 26 Aug 2022 22:12:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 26 Aug 2022 22:12:03 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 26 Aug 2022 22:12:03 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 26 Aug 2022 22:12:03 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 26 Aug 2022 22:12:03 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ee4ca39e1b6ea333d785f1cbc6b64b874a4f16f1200dad9e17d2015c925d1d57`  
		Last Modified: Fri, 26 Aug 2022 21:27:39 GMT  
		Size: 39.5 MB (39520501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f806f92441177162c8149eb36189b0eae2287007a7837b949d24fb72102008`  
		Last Modified: Fri, 26 Aug 2022 21:49:14 GMT  
		Size: 12.2 MB (12237733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1696af5de174e3277da93d90c596cc818fbde72bfb742ecf22a8f5361d3feae`  
		Last Modified: Fri, 26 Aug 2022 21:54:08 GMT  
		Size: 188.7 MB (188744805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815cff02c46b3ca4fdf9d389b5c4f660eb19d9c7e2d899334942224b577b6cc3`  
		Last Modified: Fri, 26 Aug 2022 22:14:49 GMT  
		Size: 189.7 MB (189654435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb367b338bf6ae67b579acf9402daee2a36a973796b378608274412feaa8f548`  
		Last Modified: Fri, 26 Aug 2022 22:14:35 GMT  
		Size: 8.7 MB (8739498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d76d78a493a718d21da1007976377aca62baca5a4b641a7bf744d07caee9257`  
		Last Modified: Fri, 26 Aug 2022 22:14:34 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c1b9f2204995c75df80cf0955145c16632bd7c77632010afb21337c665a7e`  
		Last Modified: Fri, 26 Aug 2022 22:14:34 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c7f54851ef64bd0ead7fb389f08ab0a3cd6afbfee0c09ec2057b1cf4321b1f4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.3 MB (447332256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc89839f96e126b11772cc4217ad93ea46fd531e09cfa8f0239144a0447fac4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 24 Aug 2022 19:54:55 GMT
ADD file:2016956ebf5b305d0029ca641d3175f879fb9c5f35f801b5c52927afeb8f8422 in / 
# Wed, 24 Aug 2022 19:54:56 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:30:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 24 Aug 2022 23:34:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 24 Aug 2022 23:34:28 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 23:34:29 GMT
ENV LANG=C.UTF-8
# Wed, 24 Aug 2022 23:34:30 GMT
ENV JAVA_VERSION=18.0.2.1
# Wed, 24 Aug 2022 23:34:41 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 24 Aug 2022 23:34:41 GMT
CMD ["jshell"]
# Thu, 25 Aug 2022 02:41:57 GMT
RUN microdnf install findutils git
# Thu, 25 Aug 2022 02:41:57 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 25 Aug 2022 02:41:58 GMT
ARG USER_HOME_DIR=/root
# Thu, 25 Aug 2022 02:41:59 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 25 Aug 2022 02:42:00 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 25 Aug 2022 02:42:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 25 Aug 2022 02:42:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 25 Aug 2022 02:42:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 25 Aug 2022 02:42:14 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 25 Aug 2022 02:42:15 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 25 Aug 2022 02:42:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 25 Aug 2022 02:42:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4fad3655bea38b31843315fea6a076b3b13bee189d1b3d017cf9beb5feb39909`  
		Last Modified: Wed, 24 Aug 2022 19:56:49 GMT  
		Size: 38.3 MB (38320858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299639459c280cc4a1b9d1299ff192e2925aef24610273aa1288cbbecdd6e689`  
		Last Modified: Wed, 24 Aug 2022 23:40:50 GMT  
		Size: 13.0 MB (13041901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cde497040e2ab480e57c3cab47b15ba50b1cfa492a00c90b48ba1689b8ab0e`  
		Last Modified: Wed, 24 Aug 2022 23:44:36 GMT  
		Size: 187.7 MB (187659483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1360f0fb9a43f8bbcf5d42a59c480676ca50ba671aa03274406bd77584d51c`  
		Last Modified: Thu, 25 Aug 2022 02:46:29 GMT  
		Size: 199.6 MB (199569325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7fee35f6debdfdf88222e58b6cfdff05d23a735d224427453f4f4745bb492b`  
		Last Modified: Thu, 25 Aug 2022 02:46:11 GMT  
		Size: 8.7 MB (8739474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b8c35bd38b2417ee05fe0868178bac87662afb0b27fb9ee114221b684f351a`  
		Last Modified: Thu, 25 Aug 2022 02:46:10 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910e524defa8dedd1dd1dc6fad102cca067d4dc42b4f88b955e920164cdf4bdb`  
		Last Modified: Thu, 25 Aug 2022 02:46:11 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
