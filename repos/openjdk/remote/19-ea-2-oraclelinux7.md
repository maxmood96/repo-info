## `openjdk:19-ea-2-oraclelinux7`

```console
$ docker pull openjdk@sha256:cf4d0440a8ffce13e0c33e30c8964309f76b49de84b41272bc51fa2481231d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:19-ea-2-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9d6fcab6139579a6105b39606d0c2cb05085c01f489280cdcd9f1cd1fb95b684
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253798492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103a2918e4dcb6e6b70efe02261c89ce3c27cf02487500b061cadc5d559244ba`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 02 Dec 2021 08:51:25 GMT
ADD file:9e54130641553fdfd5c6fccb94502b8821e5f6a3a312a5b58537b439bf8b2670 in / 
# Thu, 02 Dec 2021 08:51:26 GMT
CMD ["/bin/bash"]
# Thu, 02 Dec 2021 11:01:07 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 14 Dec 2021 01:59:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 14 Dec 2021 01:59:09 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Dec 2021 01:59:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Dec 2021 23:41:04 GMT
ENV JAVA_VERSION=19-ea+2
# Fri, 17 Dec 2021 23:41:20 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/2/GPL/openjdk-19-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='66b20dfbd8d0c7ce80d61fef923fb91721244f6194b191b90f130a3380be459d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/2/GPL/openjdk-19-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='4e19a1ffdaf1f9890ff45d8ff7264b4c4cc968714466abdfe2b47229aa2e4e2f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Dec 2021 23:41:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:badc99e3da86862c7fae71e717cef8fd1a5a34023f0932c8c979275fb8de6a32`  
		Last Modified: Thu, 02 Dec 2021 08:52:20 GMT  
		Size: 48.9 MB (48905570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56494d755d6c4fa6e0ed158c6946591b3ec2ad7e02e9c86d1434bcf5b27c263`  
		Last Modified: Thu, 02 Dec 2021 11:21:55 GMT  
		Size: 16.5 MB (16464679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e5c30e9a859bc3a0ef46ab15761d5a86f9af61741f5f09a6a567f53c0081d`  
		Last Modified: Fri, 17 Dec 2021 23:57:21 GMT  
		Size: 188.4 MB (188428243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
