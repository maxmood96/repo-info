## `openjdk:18-ea-21-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:cdd6dfd779001fccb03682740b20c168761b61ad58cdc3e8c6142d39ed73465f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-21-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:ec196e338fa8bbd0d9287cc432100dfc2310577c6e39bb691e5c4aad00d6b521
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251855575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e91ba8ba9cb56e993c2ac26ea12609f055911aee8f7860b56f49f35da22f67`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 28 Oct 2021 01:23:11 GMT
ADD file:1ba19f36d1d89d348cc182f0c7feb2c27bcca7bd084032525deaba8822462091 in / 
# Thu, 28 Oct 2021 01:23:11 GMT
CMD ["/bin/bash"]
# Thu, 28 Oct 2021 01:45:25 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 28 Oct 2021 01:45:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 28 Oct 2021 01:45:25 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 01:45:25 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Nov 2021 18:49:22 GMT
ENV JAVA_VERSION=18-ea+21
# Mon, 01 Nov 2021 18:49:33 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c0a1fcdd389abdc8101892215f73413b10975f735f31e6d0484c9653fc9ba5e9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ed86d5c7f9433360bc81b5b283d6b5fc345309d16c77125c8ceff32ed5c9a8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Nov 2021 18:49:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a755c2d4aa362701b6bb477a4b1cb2594cb0dca6d0e6839e07b0636fb824c7f7`  
		Last Modified: Thu, 28 Oct 2021 01:24:42 GMT  
		Size: 48.3 MB (48328962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d0464e417ebb82551686797f3772337ca857388f6f2209630af5603196a562`  
		Last Modified: Thu, 28 Oct 2021 01:53:12 GMT  
		Size: 15.4 MB (15399150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745ba23332f5419699490030c7a251ae318678ad9f335be24081ace19121bf47`  
		Last Modified: Mon, 01 Nov 2021 18:57:03 GMT  
		Size: 188.1 MB (188127463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
