## `openjdk:17-ea-12-oraclelinux7`

```console
$ docker pull openjdk@sha256:f8ac4d3c7fe692ad3a0079b4f80eb1368c5909c653887696aa2ce6fecd4cb63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-ea-12-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:c1ad3f0e1910fa4ec24eeea1dc488decf802d727e5f0d55820e1d54295716719
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249405771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c922cbaa929d755cc1fa9f64132b13ae064e24debb6dc47c73ce40bebf69af8e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Feb 2021 00:53:29 GMT
ADD file:361f165903526126476b03dd2afac1fff0b334906bb56d024e5aee87b948b0cf in / 
# Fri, 12 Feb 2021 00:53:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Feb 2021 01:11:19 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 12 Feb 2021 01:11:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 12 Feb 2021 01:11:19 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Feb 2021 01:11:19 GMT
ENV LANG=en_US.UTF-8
# Wed, 03 Mar 2021 23:38:08 GMT
ENV JAVA_VERSION=17-ea+12
# Wed, 03 Mar 2021 23:38:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='e281f7d1fd2aaa858b02d5be451c51a9ed836c78d002cb82b114e6c36041eebf'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/12/GPL/openjdk-17-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ae713390655d0cfd8302cb2c840553404a3e366162ba5b9a2410ea7b6f1c27'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 03 Mar 2021 23:38:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a61503a3b32ea964eb926d54dcfe6cd7e21f4e0cca1b1373df21cf904388c445`  
		Last Modified: Fri, 12 Feb 2021 00:54:42 GMT  
		Size: 48.3 MB (48263629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2d02ff646cdda3eb210d43b22353e431d4fa3a204470452ad0a0508cdbf87d`  
		Last Modified: Fri, 12 Feb 2021 01:18:03 GMT  
		Size: 15.4 MB (15437000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38da3349d36f236f9150a8a693fb4166ca18bbdaa5d80674e4fefed67b215a2b`  
		Last Modified: Wed, 03 Mar 2021 23:45:32 GMT  
		Size: 185.7 MB (185705142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
