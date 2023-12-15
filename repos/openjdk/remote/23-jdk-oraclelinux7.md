## `openjdk:23-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:1dc0c6389db3234a2745e26e902b740a08d29cdd8a2ef9cf4de5f86d8b51b973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:23-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:f6867f898ad3965e4de31225849153249230cd3239a9be1eb06d75f524bd7572
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267530360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5685c7d5b489fa569165d28e0012b023c8d54f8bab12f72f158f89a412c875`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 14 Dec 2023 23:21:44 GMT
ADD file:74b33794f8e61e810f09c38da020f9becc9f6987d22fa6f42af6b4226505e6ca in / 
# Thu, 14 Dec 2023 23:21:45 GMT
CMD ["/bin/bash"]
# Thu, 14 Dec 2023 23:42:36 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 14 Dec 2023 23:42:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Thu, 14 Dec 2023 23:42:36 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 23:42:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Dec 2023 23:42:36 GMT
ENV JAVA_VERSION=23-ea+1
# Thu, 14 Dec 2023 23:42:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='740a84253d35402b9213bf187ee4f058817c614f8cc47cb3414e02760f05099f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='74fe7c8e67c5b80f868ec20daecb112fc090fb91c58bf4ce5297cf77c9935fa5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 14 Dec 2023 23:42:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20e4dcae4c693910efbf28a556e2fa88ef717e15364f63da7e0a4a130b9b714e`  
		Last Modified: Thu, 14 Dec 2023 23:23:14 GMT  
		Size: 50.5 MB (50499235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291741a113838df70588f92202102813130a0a1ffc256860de0b8c13b8ec6939`  
		Last Modified: Thu, 14 Dec 2023 23:44:17 GMT  
		Size: 14.2 MB (14235978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac51f2fa31b59e9aff8f75adb2230e41bcb147c2b637c6c6c0f5273e969d62c6`  
		Last Modified: Thu, 14 Dec 2023 23:44:30 GMT  
		Size: 202.8 MB (202795147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bb0aab2976812e8007a73031fdeceb7c17120bf640749a9571a309708f9ea946
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267206874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669971268f20fba512586fc6531e09b8463feaa247ab1255fcd2c0a32499acbf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Dec 2023 00:02:56 GMT
ADD file:7f9b20722f4f2c781b7814e113711ee10ee458be84fe343e7d61658ede9c4711 in / 
# Fri, 15 Dec 2023 00:02:57 GMT
CMD ["/bin/bash"]
# Fri, 15 Dec 2023 00:20:21 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 15 Dec 2023 00:20:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 15 Dec 2023 00:20:21 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 00:20:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 Dec 2023 00:20:21 GMT
ENV JAVA_VERSION=23-ea+1
# Fri, 15 Dec 2023 00:20:39 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='740a84253d35402b9213bf187ee4f058817c614f8cc47cb3414e02760f05099f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/1/GPL/openjdk-23-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='74fe7c8e67c5b80f868ec20daecb112fc090fb91c58bf4ce5297cf77c9935fa5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 15 Dec 2023 00:20:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01eab324a7fc4cacc34c78d38ce9548750df098b20899d269b500307b6765a1d`  
		Last Modified: Fri, 15 Dec 2023 00:04:16 GMT  
		Size: 51.1 MB (51110815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0c92b2a0403c99f9b8b57a84e65c115d05d0c4d6644795f60ccf2a3a122e4f`  
		Last Modified: Fri, 15 Dec 2023 00:22:13 GMT  
		Size: 15.2 MB (15245630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef0b76679d2ac3ba5631b0085b33ec7ae1b7324de3a074821b8ff15725a955e`  
		Last Modified: Fri, 15 Dec 2023 00:22:23 GMT  
		Size: 200.9 MB (200850429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
