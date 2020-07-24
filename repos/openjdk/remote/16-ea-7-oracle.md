## `openjdk:16-ea-7-oracle`

```console
$ docker pull openjdk@sha256:196e02d5927eb965caec12f48405c6b61d68d8164213de41b85c65b8148b1423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-7-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ca49b44788ed7186980537fab57e19eec084a521e9dfed198eb16c555a53c0b5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260691631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61629661a557cb8d1abafcf92568e629b9fd114362b4b9d25923512284856224`
-	Default Command: `["jshell"]`

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
# Fri, 17 Jul 2020 02:53:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 17 Jul 2020 02:53:07 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 19:13:23 GMT
ENV JAVA_VERSION=16-ea+7
# Fri, 24 Jul 2020 19:14:06 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-aarch64_bin.tar.gz; 			downloadSha256=0e2c7dc384e914fa785087a3970b0ab14f983447e55e663fe5a7b507104f9b7c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-x64_bin.tar.gz; 			downloadSha256=e6d7f1485772b4ac0bdd4681af093a63eb1af7590efca05e950df04a25045a78; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Fri, 24 Jul 2020 19:14:06 GMT
CMD ["jshell"]
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
	-	`sha256:267766eb096589c26b5e5a9345c6b25b65f4fbc8bd2a7ea2f88b413f7de36701`  
		Last Modified: Fri, 24 Jul 2020 19:18:48 GMT  
		Size: 196.5 MB (196489615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-7-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bd8db2a0fc397d45ed26a8a551c8e5e71fd94fed618f53305dc0e417d0f978a3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240133130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c50e99597f196d923f7795f8e50c56a361aa715d96f94215cbb564e7d66d94`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 17 Jul 2020 01:45:21 GMT
ADD file:f07cad218c7e24e1cbce662268da25d9318627f636feebb0f669155354c7f365 in / 
# Fri, 17 Jul 2020 01:45:25 GMT
CMD ["/bin/bash"]
# Fri, 17 Jul 2020 02:03:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 17 Jul 2020 02:03:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Jul 2020 02:03:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 17 Jul 2020 02:03:34 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jul 2020 19:29:12 GMT
ENV JAVA_VERSION=16-ea+7
# Fri, 24 Jul 2020 19:33:37 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-aarch64_bin.tar.gz; 			downloadSha256=0e2c7dc384e914fa785087a3970b0ab14f983447e55e663fe5a7b507104f9b7c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-x64_bin.tar.gz; 			downloadSha256=e6d7f1485772b4ac0bdd4681af093a63eb1af7590efca05e950df04a25045a78; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Fri, 24 Jul 2020 19:33:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5053e285643065e9638a069d53c6f62fd6bf1d6d4d16001d48a66ee024d7397`  
		Last Modified: Fri, 17 Jul 2020 01:45:56 GMT  
		Size: 48.6 MB (48633508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7d1facfda57a46d98e2882cdeac87e1b92ca135e73948039ab5c8e3c1f5598`  
		Last Modified: Fri, 17 Jul 2020 02:13:50 GMT  
		Size: 16.4 MB (16442484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858e4401f009c248ffa152309373bf3704a905b37355c44a40982aa405604a35`  
		Last Modified: Fri, 24 Jul 2020 19:38:41 GMT  
		Size: 175.1 MB (175057138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
