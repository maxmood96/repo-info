## `openjdk:19-ea-22-oraclelinux7`

```console
$ docker pull openjdk@sha256:7d3b9880fa1e8e8a27ff23dc0f4c959d0444367f6f7eb6c0ae279bd9a5313270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-22-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:60d500b05b484dfc216568eff05d5ca66417717df487e96a07d65f600f7dc074
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258745716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3606dfc799d60a6c4ccc1ef27bf9b85287122b96ce93909ccc1d223470004e40`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 May 2022 18:21:17 GMT
ADD file:60c2a17c0433d95caf7d6bac5520da02174f48bf0c50f6f369b00bf8f9774f82 in / 
# Thu, 19 May 2022 18:21:17 GMT
CMD ["/bin/bash"]
# Thu, 19 May 2022 18:22:53 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 19 May 2022 18:22:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 19 May 2022 18:22:54 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2022 18:22:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 19 May 2022 18:22:54 GMT
ENV JAVA_VERSION=19-ea+22
# Thu, 19 May 2022 18:23:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/22/GPL/openjdk-19-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='38430a128f794293c22ccaadbf7528f60a021055de72d33e210e9cf8e3a12aa6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/22/GPL/openjdk-19-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='6884df76f084c7c190b86bac76643132226ba99ebbb61352b1050494fae20e17'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 May 2022 18:23:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f0182e2fe516824cf8f93b207b7c4b65d05c48db476f53312b17b5cd952bfcc3`  
		Last Modified: Thu, 19 May 2022 18:22:04 GMT  
		Size: 48.8 MB (48757934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf5bd358537747774933b2ee9c613076ddeadddfb40f451054ba3989a4b2a80`  
		Last Modified: Thu, 19 May 2022 18:29:27 GMT  
		Size: 14.2 MB (14244311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d92ba6d321094876c85bd7cd00dc793fccd9117ab227792afd513fd029bf1e7`  
		Last Modified: Thu, 19 May 2022 18:29:40 GMT  
		Size: 195.7 MB (195743471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-22-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f20c56a69d2a0a5d2d7b2019e1ab62804ff71d431c3f6cd2b195acb59c3c10de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259187318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71581f438cafb85f8a4c1173bb616ff99b03ddc0f2b026814d1b46df6a100863`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 May 2022 22:09:29 GMT
ADD file:b866e521d7e920b2210ec5ba4013715f28d1ad0636a38a13cec969d5b3586d44 in / 
# Thu, 12 May 2022 22:09:30 GMT
CMD ["/bin/bash"]
# Fri, 13 May 2022 00:26:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 13 May 2022 00:26:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 13 May 2022 00:26:05 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 May 2022 00:26:06 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 May 2022 01:02:04 GMT
ENV JAVA_VERSION=19-ea+22
# Wed, 18 May 2022 01:02:21 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/22/GPL/openjdk-19-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='38430a128f794293c22ccaadbf7528f60a021055de72d33e210e9cf8e3a12aa6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/22/GPL/openjdk-19-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='6884df76f084c7c190b86bac76643132226ba99ebbb61352b1050494fae20e17'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 18 May 2022 01:02:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa569c775ec815d1a2d6e7b4f6e989b8afe4f0749c119d04101e4cb016365983`  
		Last Modified: Thu, 12 May 2022 22:10:25 GMT  
		Size: 49.3 MB (49340765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a850683079b99a0cee3fbeb957ff22bf46a963d7306f33b059cba19183ee75a`  
		Last Modified: Fri, 13 May 2022 00:37:40 GMT  
		Size: 15.3 MB (15269457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648cbfa788c920c4572e9c60ca6cab583b8ef0e3e81bb1d13c5632d743192812`  
		Last Modified: Wed, 18 May 2022 01:14:17 GMT  
		Size: 194.6 MB (194577096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
