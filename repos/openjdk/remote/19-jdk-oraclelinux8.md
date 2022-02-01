## `openjdk:19-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:f889dce36d1568b10a753c6d7fbe2a5ecaea2631528642dd147b1c4a583e37a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c0134c318519132c282ea32b3bf97971b3f6bbbc7be82ca0c7f28d11475760ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245242991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d7449f0524eb732109f46e07c0c04426a44b35e7b6e6980762b4f2f894290b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Dec 2021 02:20:57 GMT
ADD file:15b307e0b1aafead42c103e34d3e51a271acea1ab0b68961e239f11af3b0d179 in / 
# Thu, 23 Dec 2021 02:20:57 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:37:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Dec 2021 02:37:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 23 Dec 2021 02:37:55 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Dec 2021 02:37:55 GMT
ENV LANG=C.UTF-8
# Tue, 01 Feb 2022 03:10:03 GMT
ENV JAVA_VERSION=19-ea+7
# Tue, 01 Feb 2022 03:10:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/7/GPL/openjdk-19-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='a982fa9bbeef025e84a74f1b1f1e1d5e52f3e93ca630f2bcb82ae04a4ee7bc63'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/7/GPL/openjdk-19-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='f30f8f94a7bda4835eadfa80762dfd17adc878971fb94a1bad48a3fd5272505e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Feb 2022 03:10:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:155aced2666332ddff5a741b0236f360820e7aa3fc3dde2224fc17a91fc48db6`  
		Last Modified: Thu, 23 Dec 2021 02:21:56 GMT  
		Size: 42.1 MB (42105152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5901c58ecb29b61159b5e3a63dfbb0fb520b2de1d33c9fb038d9b697e3fcd4`  
		Last Modified: Thu, 23 Dec 2021 02:45:32 GMT  
		Size: 13.5 MB (13520734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497b5d06c9e854771ec95e7add66ba5bec5339881acae4e63ce75a45112aab87`  
		Last Modified: Tue, 01 Feb 2022 03:20:08 GMT  
		Size: 189.6 MB (189617105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:81fe48aabcef863dca51a882ced18d27647e3b6afe7156d8490db0a9c1fdd311
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (244966839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326d8c002945693313dfa45f010a1dc1b1dd4d62f92de62077690758a7752326`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Dec 2021 02:40:45 GMT
ADD file:140d632303428d802f77f473aef33fa52daacdfc76b23edde4344be661c1d4b0 in / 
# Thu, 23 Dec 2021 02:40:46 GMT
CMD ["/bin/bash"]
# Thu, 23 Dec 2021 02:58:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 27 Dec 2021 17:43:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Mon, 27 Dec 2021 17:43:39 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Dec 2021 17:43:40 GMT
ENV LANG=C.UTF-8
# Tue, 01 Feb 2022 02:43:38 GMT
ENV JAVA_VERSION=19-ea+7
# Tue, 01 Feb 2022 02:43:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/7/GPL/openjdk-19-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='a982fa9bbeef025e84a74f1b1f1e1d5e52f3e93ca630f2bcb82ae04a4ee7bc63'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/7/GPL/openjdk-19-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='f30f8f94a7bda4835eadfa80762dfd17adc878971fb94a1bad48a3fd5272505e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Feb 2022 02:43:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53f096d4aa0757c30613f325df1e03a90db9d9879ea251b394e3ab0a068b5610`  
		Last Modified: Thu, 23 Dec 2021 02:41:44 GMT  
		Size: 42.0 MB (42018351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921862a08fd8bc652539d62804daf06ab6464bd5b42061f5bedbdfa73bd62136`  
		Last Modified: Thu, 23 Dec 2021 03:11:46 GMT  
		Size: 14.3 MB (14303905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd4465b99b9cadb31f12bdcacdd679c0c8480687ca96adbde6da30a8a34fa8`  
		Last Modified: Tue, 01 Feb 2022 03:00:33 GMT  
		Size: 188.6 MB (188644583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
