## `openjdk:22-ea-19-oracle`

```console
$ docker pull openjdk@sha256:61bed7df6f38e0d52ebec829a5e7790bb2ec9ed3a15f752e2faa2d204693a5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:22-ea-19-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:e8ada696009b82ddf72710fe752f58ce2ab1db1697f835a5d06abf595d04e33a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264473687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd203a05159a6dc9ddac66ce02f9ef8ce82d078f654faba404499a0d4c82fa5e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Oct 2023 21:28:30 GMT
ADD file:3c65f844bba9cf4decac4432464fc55e211e28f5e9753ab337fe057357fee7b5 in / 
# Thu, 12 Oct 2023 21:28:31 GMT
CMD ["/bin/bash"]
# Thu, 12 Oct 2023 22:19:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 12 Oct 2023 22:19:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Thu, 12 Oct 2023 22:19:08 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 22:19:08 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 02:02:09 GMT
ENV JAVA_VERSION=22-ea+19
# Fri, 13 Oct 2023 02:02:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/19/GPL/openjdk-22-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='70bc0434cc0a8e1fa5351daa062cdd86b29caa784525f22e8a0cc0028e34a157'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/19/GPL/openjdk-22-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='973d8beb242379ed3bec118f7374dc61a99699411c38875ecdf158e506b0a3c0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 Oct 2023 02:02:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:210eb976c4c725a4b96ff6ec8a7e848396482dbb1e18d401ee1789c1c6aa6ae0`  
		Last Modified: Thu, 12 Oct 2023 21:30:01 GMT  
		Size: 44.3 MB (44279111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1ad07e4410c408630c3fb5115e2de88151893a626b68399eeac7004b53a1ae`  
		Last Modified: Thu, 12 Oct 2023 22:20:41 GMT  
		Size: 15.0 MB (15015192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abac6306571aa24262275f2fcc7721d5f743ed8ad273b619b590674615f804c1`  
		Last Modified: Fri, 13 Oct 2023 02:06:04 GMT  
		Size: 205.2 MB (205179384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
