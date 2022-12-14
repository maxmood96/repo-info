## `openjdk:21-ea-1-oracle`

```console
$ docker pull openjdk@sha256:7bcbe24d22c9ada93738a7fcc1c9626c172785fa1dc2ef310324b9ad9e36c259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-1-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:cfa53e78f25c037a24bd0c98259b03d61e89ff5a4ba5b72f6233021ee36a9a81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255056819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746e3dff2e53345737d0da9f58b4e5c0b8aec71c6a181b2c285f22f52bb2e818`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:27:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 14 Dec 2022 00:32:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 14 Dec 2022 00:32:51 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:32:51 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2022 00:32:52 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 00:33:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='46d9f514e49067eebb9e3bf5033195e2ca1b834be98f3910ea1726c40e97dc22'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='950a4a33ac9737bc7ecf824d2292f4fea92b1d9301a4f89d3c32e86f4d04bd23'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Dec 2022 00:33:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3502f40d35be69b4df858d92b5ac60d6b792eec7beabb7cbd78c816329f47b7f`  
		Last Modified: Wed, 07 Dec 2022 02:30:44 GMT  
		Size: 12.2 MB (12248357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e2a8d7c376cad299c7e71c7434b01d62a0ae672d5369d7ff0133a063e8bf29`  
		Last Modified: Wed, 14 Dec 2022 00:38:03 GMT  
		Size: 198.9 MB (198939724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-1-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:177e09b5d5fd561bdf7c66ee01d778a1257f6b49ddb470cee663ca68124b0625
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253264528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fee9600dc39af3a7525be8f4e69167355de8a60130f5ea959469b110ae0452`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:53:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 14 Dec 2022 00:53:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 14 Dec 2022 00:53:26 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Dec 2022 00:53:26 GMT
ENV LANG=C.UTF-8
# Wed, 14 Dec 2022 00:53:26 GMT
ENV JAVA_VERSION=21-ea+1
# Wed, 14 Dec 2022 00:53:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='46d9f514e49067eebb9e3bf5033195e2ca1b834be98f3910ea1726c40e97dc22'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/1/GPL/openjdk-21-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='950a4a33ac9737bc7ecf824d2292f4fea92b1d9301a4f89d3c32e86f4d04bd23'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Dec 2022 00:53:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e459b46a4edc515fedc5c9be076b28ba6b0606f3cc90d412ea3d88b15576e`  
		Last Modified: Wed, 07 Dec 2022 02:57:10 GMT  
		Size: 13.1 MB (13058882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84eb1a61835f1b487a0e0e0f0f57816a1cd0b258bda8f98c2be769abb4031b3`  
		Last Modified: Wed, 14 Dec 2022 00:58:42 GMT  
		Size: 197.4 MB (197433587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
