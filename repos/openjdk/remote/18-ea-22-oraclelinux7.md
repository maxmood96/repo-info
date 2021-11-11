## `openjdk:18-ea-22-oraclelinux7`

```console
$ docker pull openjdk@sha256:28857b88f79eb55e5564e06397c66e9f2943aba99a141857198f9f0f8d7de468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-22-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:ce4c326af7ac5a60c8ca40f44ae6ebb71a43eb165afe0d18716114faa2ae9241
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251995533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bb93f8d111d78b4b3aafe543ea16de5c32e350d9517726baf0852b2f6f63c3`
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
# Thu, 11 Nov 2021 02:28:04 GMT
ENV JAVA_VERSION=18-ea+22
# Thu, 11 Nov 2021 02:28:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/22/GPL/openjdk-18-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='71124796aac929f184d54cf5b2a3ba3a31c0cef1ba9b5b5e1535ec5a5d482a8b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/22/GPL/openjdk-18-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='714a0b84e6ed39e5442ca0044dab9ebecddeceffc9b78aed8e4d7ba2fbefb8aa'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 11 Nov 2021 02:28:16 GMT
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
	-	`sha256:60632eff72aeb95abb140b5e33b41e9e4d1f089f71271807f25b3f35c9257b0b`  
		Last Modified: Thu, 11 Nov 2021 02:35:25 GMT  
		Size: 188.3 MB (188267421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
