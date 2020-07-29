## `openjdk:16-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:383858828ce8a065dd91993baa3cebadd6ab58bf8f9c05eca9f94eb41360e2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:1572f284bc05e404b97cd6fe995e399d0bdd749110ed236dcd0a00c79b970d3f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260691900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634ee03781ec296683c8bf5dfdb500d89e77dc627313f18ec5e969e8a7021e32`
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
# Wed, 29 Jul 2020 01:22:42 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-aarch64_bin.tar.gz; 			downloadSha256=0e2c7dc384e914fa785087a3970b0ab14f983447e55e663fe5a7b507104f9b7c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-x64_bin.tar.gz; 			downloadSha256=e6d7f1485772b4ac0bdd4681af093a63eb1af7590efca05e950df04a25045a78; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Wed, 29 Jul 2020 01:22:43 GMT
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
	-	`sha256:bdba5953953a8334fd996acf082e0b217c525a65db3e13bc68cb7a18ec62a039`  
		Last Modified: Wed, 29 Jul 2020 01:31:57 GMT  
		Size: 196.5 MB (196489884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a4c6369fb30310a48c1120348df39365da40cc667ae409da099ada8aa07abc6f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240132196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a358a56e9183a793c73cede49002ee2bcf765560a50be7345674c454193819`
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
# Wed, 29 Jul 2020 00:46:38 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-aarch64_bin.tar.gz; 			downloadSha256=0e2c7dc384e914fa785087a3970b0ab14f983447e55e663fe5a7b507104f9b7c; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/7/GPL/openjdk-16-ea+7_linux-x64_bin.tar.gz; 			downloadSha256=e6d7f1485772b4ac0bdd4681af093a63eb1af7590efca05e950df04a25045a78; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Wed, 29 Jul 2020 00:46:40 GMT
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
	-	`sha256:f8ff26fe290f7293089269d3c7969464b3a97706f7f44edaebc863f16364116f`  
		Last Modified: Wed, 29 Jul 2020 00:53:04 GMT  
		Size: 175.1 MB (175056204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
