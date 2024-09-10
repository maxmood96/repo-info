## `openjdk:24-jdk-oracle`

```console
$ docker pull openjdk@sha256:65dd85e6ba49c6080b0e08cea1182fba72df324fcc75092cb08273e3b67acb40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b159ded0cf121c02fd216f9037a1c9175c7c11af45b5552e87d089de20175a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301489577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6db179c05511cd99f61dba6ced7ca2ab8bea8626a013c4f7d6e0121b52cfdb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 06 Sep 2024 18:48:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5e407bf3af905fb1f6edf271f870052697e79b018f921119921615cd25365fdb`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 49.2 MB (49239252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a87f9d67e2d21e2798c86432dad12f7f48ed183498d0975b68916bc4102c1a`  
		Last Modified: Tue, 10 Sep 2024 01:54:50 GMT  
		Size: 40.4 MB (40418113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9285c8120b81c73c125c64f3a20e9459f1cd26ed2dc6b7f5cbee8c6e994e91`  
		Last Modified: Tue, 10 Sep 2024 01:54:52 GMT  
		Size: 211.8 MB (211832212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:260ac5795c0020d08bf40ce793e13fcd12e28fdb25272dac38f9a2bab029f3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac388db3710a73a9541725631bb7baecbf4019716e3cd2c4d4f70714458fcb3`

```dockerfile
```

-	Layers:
	-	`sha256:6804131feb910f8b3cf8f6d2af1529778b3ee6b4ab6625bd4077021a066adef1`  
		Last Modified: Tue, 10 Sep 2024 01:54:49 GMT  
		Size: 3.7 MB (3670499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b5d8c3c243cea077a1f9f1baa8d2f6aa88f43f52be2d47206e016edbd69d20f`  
		Last Modified: Tue, 10 Sep 2024 01:54:49 GMT  
		Size: 19.7 KB (19711 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2aee2e344f25c64f610492f3bb0570e3535246eb5689c3ce29771854b2a8be4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298440742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df4746cecdcf50e5d091cb52bda3efcd9e1fee19d1b7d68100e4f5bdca773db`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 06 Sep 2024 18:48:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["/bin/bash"]
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 06 Sep 2024 18:48:13 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 06 Sep 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+14
# Fri, 06 Sep 2024 18:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='e3cf94d73e0ca63c536e901858cb97a0053c62606f8bb9d5b2ca20e1cc573d0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/14/GPL/openjdk-24-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='0d13500ae2e96601c70e90fca2ad928c3bf541afc71c293aed33924a2361d97a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 06 Sep 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed6a7145c00ee1c4b91b6b37765e2a7addef2d9b96e12546b2f7aad0a198ae3f`  
		Last Modified: Tue, 10 Sep 2024 05:32:56 GMT  
		Size: 47.9 MB (47913808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb8c247ecf1b88686d212c2f55e0f5ac4d4ba8cde9b5d6f216ca338a07e7b87`  
		Last Modified: Tue, 10 Sep 2024 06:43:07 GMT  
		Size: 40.8 MB (40844369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a72a008ebaa9bb3ede37884b879b51cf951f85041072ba6452f0c21c29d0b24`  
		Last Modified: Tue, 10 Sep 2024 06:43:11 GMT  
		Size: 209.7 MB (209682565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:937563d7d466e22eb8fa0a84d5da1ff478f610f7c4cb6730b09ae0e5f2dabce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295fb42a8de154fdb8f982b5bbdffe9a03c6efabd167a30c227bbb801c374c7b`

```dockerfile
```

-	Layers:
	-	`sha256:9cab0fbd0e3192c3ae01112bae8f67a80cd4d625056ce1d999a77cc5d08bffda`  
		Last Modified: Tue, 10 Sep 2024 06:43:05 GMT  
		Size: 3.7 MB (3668882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4d4fe2df8e3d3e022a6e9cd9fc77d8e07e506f1f9ac4d18271a03f498bb56c`  
		Last Modified: Tue, 10 Sep 2024 06:43:05 GMT  
		Size: 20.3 KB (20264 bytes)  
		MIME: application/vnd.in-toto+json
