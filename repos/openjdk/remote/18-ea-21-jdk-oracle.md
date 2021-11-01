## `openjdk:18-ea-21-jdk-oracle`

```console
$ docker pull openjdk@sha256:419a8686a58b9d0e73b96eac66a6a9c4770c9cee5c8cdd7615a06f15fdb6b5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-21-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:42f9491a6728ed6e548c8a88fdb8ddfa3251a54b8b297f3224c83ba583931cf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243588227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ff2325c1eedb17c158c957f2231200134cd5d9f9569fcce932b4a99a8f5cb2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 28 Oct 2021 01:22:47 GMT
ADD file:45a1eba89256c6e3801f14738faca9e260b17b306f0fc8769ba0b0f94f0fdf68 in / 
# Thu, 28 Oct 2021 01:22:47 GMT
CMD ["/bin/bash"]
# Thu, 28 Oct 2021 01:44:41 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 28 Oct 2021 01:44:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 28 Oct 2021 01:44:41 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 01:44:41 GMT
ENV LANG=C.UTF-8
# Mon, 01 Nov 2021 18:49:02 GMT
ENV JAVA_VERSION=18-ea+21
# Mon, 01 Nov 2021 18:49:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c0a1fcdd389abdc8101892215f73413b10975f735f31e6d0484c9653fc9ba5e9'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/21/GPL/openjdk-18-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ed86d5c7f9433360bc81b5b283d6b5fc345309d16c77125c8ceff32ed5c9a8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Nov 2021 18:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f420596490555ff89c8ec7d6b74b4e46c2b3b98dc775c9d19494d8afeb475852`  
		Last Modified: Thu, 28 Oct 2021 01:24:04 GMT  
		Size: 42.0 MB (41970837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a9c63ed3ba0226d765a092dd6fcc06fe5ece8a2dd0fd11e1add9c0ddee488e`  
		Last Modified: Thu, 28 Oct 2021 01:52:24 GMT  
		Size: 13.5 MB (13491622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d85e38bbd4ab66e13d497afb8b106154349b686aa357fb65b7654edc55f0491`  
		Last Modified: Mon, 01 Nov 2021 18:56:17 GMT  
		Size: 188.1 MB (188125768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
