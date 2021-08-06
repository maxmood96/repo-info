## `openjdk:18-ea-9-oracle`

```console
$ docker pull openjdk@sha256:62f9ac3c354f358d3b9eaed01702bb26b7ce917bf9960671daf6494e3449cfe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-9-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a4bfd0a7ee322bcfacff142aab82954dba2f87dcdf5c349db1c3a4c444724030
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243095280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdae4df4d5e028625748fba54497a2a42ef3c790cf014efe43f87c0c646b2f29`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jul 2021 01:13:10 GMT
ADD file:c047ac1784a3670f52d12ad67cf238654237149dc2c9d7b921cd005c7ec42105 in / 
# Fri, 23 Jul 2021 01:13:11 GMT
CMD ["/bin/bash"]
# Fri, 23 Jul 2021 06:40:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 23 Jul 2021 06:40:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 23 Jul 2021 06:40:32 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 06:40:32 GMT
ENV LANG=C.UTF-8
# Fri, 06 Aug 2021 22:27:02 GMT
ENV JAVA_VERSION=18-ea+9
# Fri, 06 Aug 2021 22:27:14 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/9/GPL/openjdk-18-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='892cb159ff07b80db4ac5b1e3343d740c5113d323aa2485aa2d931203e15af61'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/9/GPL/openjdk-18-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='35862c7271eec4456da50f777dafb216bcd8e9034e0b77ba8ca9cca9b317b3b8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 06 Aug 2021 22:27:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1da50e1664e1b58d93182fe5af093c642668ec93f67fcd8215b9c1979930b84d`  
		Last Modified: Fri, 23 Jul 2021 01:14:27 GMT  
		Size: 42.2 MB (42178827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8e5a84542212d0126ce88facd146befb1c731fb4faafb50a7b96ad0568cd9`  
		Last Modified: Fri, 23 Jul 2021 06:49:18 GMT  
		Size: 13.4 MB (13390485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44cfd9ec47ac0661d1568721d544165063deecc013021b4ac226d21c2c37d07`  
		Last Modified: Fri, 06 Aug 2021 22:41:05 GMT  
		Size: 187.5 MB (187525968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
