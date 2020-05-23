## `openjdk:15-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:749c1423a598921b5b520413e7a42e58ccf9e8e405b7aab3bf7b21574d001e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:625ac4f4ded50212c2fce4788807ec129e3383c04d9e991759531f663b0fdb1a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253996663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a4bc691c50db6dc51ec191a886b62409b5c508c5f5a9df5f77b82b3a1c6495`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 04 May 2020 20:20:53 GMT
ADD file:d23891d2372d6aae3d738388c74dacd92f9406083ee0c1ac0e2bfd140f92ec2b in / 
# Mon, 04 May 2020 20:20:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2020 20:38:21 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 04 May 2020 20:38:21 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2020 20:38:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 04 May 2020 20:38:21 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 May 2020 01:24:34 GMT
ENV JAVA_VERSION=15-ea+24
# Sat, 23 May 2020 01:25:25 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_linux-aarch64_bin.tar.gz; 			downloadSha256=912b1ecb8b9329a67c577d1fa3a0391d48d60e3643c95f923f375b03c7ae51d9; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_linux-x64_bin.tar.gz; 			downloadSha256=b1557a00210626792629afdd5a00e01c8939bb701b13475549063c82619e9a26; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Sat, 23 May 2020 01:25:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83755823a002357171a0b229ef5769a60db47a90b624adc45f8c6b7cd1d1394f`  
		Last Modified: Mon, 04 May 2020 20:22:07 GMT  
		Size: 43.5 MB (43455265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e105caaf23acf967db67aa1f683d428603dbb51e12295bfe8f5df6a4cce8bb`  
		Last Modified: Mon, 04 May 2020 20:40:58 GMT  
		Size: 14.8 MB (14758294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811468801e13b529c7981ca11573f98ad743fa92738c1fa7b9f4d0f8b151cad`  
		Last Modified: Sat, 23 May 2020 01:28:08 GMT  
		Size: 195.8 MB (195783104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c3c0ab23d1be8cf429b7050223e9f9fcc4f018068351a7d2ea93b7edea3b726c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233528389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26f869b731d1fbe27f8dc2440a6539e3d74bcfb22db82e159d15273531eaf92`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 04 May 2020 20:42:34 GMT
ADD file:b059ded860ba734fbe035c768d5c7e01a82decd7db5ca12f093672dab3b204c3 in / 
# Mon, 04 May 2020 20:42:37 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2020 01:43:47 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 22 May 2020 01:43:48 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2020 01:43:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 22 May 2020 01:43:49 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 May 2020 00:53:03 GMT
ENV JAVA_VERSION=15-ea+24
# Sat, 23 May 2020 00:54:31 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_linux-aarch64_bin.tar.gz; 			downloadSha256=912b1ecb8b9329a67c577d1fa3a0391d48d60e3643c95f923f375b03c7ae51d9; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_linux-x64_bin.tar.gz; 			downloadSha256=b1557a00210626792629afdd5a00e01c8939bb701b13475549063c82619e9a26; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Sat, 23 May 2020 00:54:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa5299bfe4aa00db1c3f39321cc679889e30f51f690a75b8c75163698c4c7831`  
		Last Modified: Mon, 04 May 2020 20:43:38 GMT  
		Size: 44.1 MB (44074523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342df9bce1d80b8bdf565c6ceb8cbb008ee180f7fd52e3006d84ae4f81d0dc67`  
		Last Modified: Fri, 22 May 2020 01:48:19 GMT  
		Size: 15.0 MB (15028449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9ab01802bc30e91c078df280682ba51bf16bff359b8a100b1109c927bd543a`  
		Last Modified: Sat, 23 May 2020 00:57:33 GMT  
		Size: 174.4 MB (174425417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
