## `openjdk:20-ea-24-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:e381bc81e44e4b45f51405e32f6a60a3ce6efb3b20575ef972320d2c49d757ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-24-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:4161b57e782fd14e3361cd6ced1de5b8e70dc3fd91254566c5fe6b46b3a84bb9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262322312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfaf97886fdc20ceae985a611fe8ac249d7092908fda11e8fc23ee0bd806421`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Nov 2022 19:21:24 GMT
ADD file:ec2c8d4fc7614a3584827f15c6278d01c6d7f42892747f20aeccfa2feb526412 in / 
# Tue, 29 Nov 2022 19:21:25 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:44:29 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 29 Nov 2022 19:44:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 29 Nov 2022 19:44:29 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 19:44:30 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Nov 2022 19:44:30 GMT
ENV JAVA_VERSION=20-ea+24
# Tue, 29 Nov 2022 19:44:53 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/24/GPL/openjdk-20-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f73656bed38d61eb8b7c771a59ad326adeb625e5f18e92b7fd11f657d1005d54'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/24/GPL/openjdk-20-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='58fb9a1ea196a73f54b3ab94189cb6eaece44105eb82d113db57b6ab51aca5e6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Nov 2022 19:44:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d96bccd7291ff1dc9e55f40b596e14900d110382763aa46814bc43ac1b40f57c`  
		Last Modified: Tue, 29 Nov 2022 19:23:17 GMT  
		Size: 49.8 MB (49828163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dc1504ba6d49eee445e92e7d82d816810257ac694a462bb310e1d2bf178fd8`  
		Last Modified: Tue, 29 Nov 2022 19:48:44 GMT  
		Size: 14.2 MB (14217773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21206d15a4c45e7de3f249a8a1bc4727be2510f6003126a4a3b7b516dadfd3fb`  
		Last Modified: Tue, 29 Nov 2022 19:48:57 GMT  
		Size: 198.3 MB (198276376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-24-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:81fd67377931ce37c071236af23c5639bf03fd5e300f078e2d415457bd039b04
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262509799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029b7752344097501e38bb33242c05228c21858d89b44b5c003c6afd08756a1d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:43 GMT
ADD file:5019a53be0205e5de5a1e1425dc3a4e8d6300733ab4bb1cdc29a6dbfc6a6a12c in / 
# Tue, 29 Nov 2022 19:48:44 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:06:51 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 29 Nov 2022 20:06:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 29 Nov 2022 20:06:52 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:06:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Nov 2022 20:06:52 GMT
ENV JAVA_VERSION=20-ea+24
# Tue, 29 Nov 2022 20:07:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/24/GPL/openjdk-20-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='f73656bed38d61eb8b7c771a59ad326adeb625e5f18e92b7fd11f657d1005d54'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/24/GPL/openjdk-20-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='58fb9a1ea196a73f54b3ab94189cb6eaece44105eb82d113db57b6ab51aca5e6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Nov 2022 20:07:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32a97da7a0b03315fbde64fde482eae59f8581d380cfa0e24b35ffd3ad1d1bf2`  
		Last Modified: Tue, 29 Nov 2022 19:50:24 GMT  
		Size: 50.4 MB (50399247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7565e5cd26c7105898fa9f6b8389575df84b097aec6966840da625b7e2a3c7e9`  
		Last Modified: Tue, 29 Nov 2022 20:10:57 GMT  
		Size: 15.3 MB (15268420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11589cf1fb2229ea72fe4f4cea1be8a505a737b43249b60a66e94164bea84677`  
		Last Modified: Tue, 29 Nov 2022 20:11:08 GMT  
		Size: 196.8 MB (196842132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
