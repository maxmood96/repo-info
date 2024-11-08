## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:7c011604685c2dc19da1130da2885e532862e49b64a3f01bcfdd4f66af1f15a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:eb57ac75a74134f13f94b56bc172d4502d33390122cbd44ea6ff2e6cfd936d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278809927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb41380b58d9fbd6750745e5a5305017fde98ed1d5f27846d6bb780c82f44f14`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Nov 2024 00:48:11 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8df6f63f2e2929475f749cf187aea26bf8fb9ab4d9a3bd0bab1fa00562e234f3`  
		Last Modified: Thu, 07 Nov 2024 20:58:25 GMT  
		Size: 51.3 MB (51274428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8596c1dd96d9dae58bef999de373927bfb582674df830055831e7f866ed09f2`  
		Last Modified: Thu, 07 Nov 2024 21:48:31 GMT  
		Size: 15.0 MB (15029431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d069b43de0c0117404960c10bcf1a7eff2e3048c77aedbb0edd72579290b51d0`  
		Last Modified: Thu, 07 Nov 2024 21:48:35 GMT  
		Size: 212.5 MB (212506068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:fda5d66eda3e27609010d1ad7584b344b005d89bfb4a8d4a4110fc9ca8c80e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9af64fc98e7a791e0ad62675582c1a228d4fb76c91a7f306bc61e879fa68fb`

```dockerfile
```

-	Layers:
	-	`sha256:ebc5b6ced0b9a9b118b57b47809826fbc40b14919305b3a77d996eaffa3f29bf`  
		Last Modified: Thu, 07 Nov 2024 21:48:31 GMT  
		Size: 2.4 MB (2425811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b478063d5a8f06250a85599391bc212669eb57072af3a5fdded65327b3c5cdf`  
		Last Modified: Thu, 07 Nov 2024 21:48:31 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:08138c6b26274b2a45b1e33e8de4553c83b765b3eb92b44523ce79644d6227e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276038892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad277fc5e718c0ba51f4bfc806775e5ec967b48dfe5c67f3cc90d0f8caff6ca0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Nov 2024 00:48:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1eb947feb489743470a528a50fbdbbe5f33202c89f643437b01546e583abf260`  
		Last Modified: Thu, 07 Nov 2024 21:00:01 GMT  
		Size: 50.0 MB (49982495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8835d30e8162a2f089f49e425d12f0ddd1e5275c283a756d2c38fc17519577`  
		Last Modified: Thu, 07 Nov 2024 22:10:09 GMT  
		Size: 15.7 MB (15710467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae1aaa00946910f5c91d005e4e6bc180fa9e50aca5430cb4c623078fe075e2`  
		Last Modified: Thu, 07 Nov 2024 22:10:15 GMT  
		Size: 210.3 MB (210345930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:406b5d9ddd02ed9dbedf584de27766e068d4af7c295c2715a6048903f70887e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e1951f83a585e85d2f24e5bddecfaeca5df1e2f0b8c512fb6c8412400f68b`

```dockerfile
```

-	Layers:
	-	`sha256:781ee01bd53dc000981d3b00a4d85da120c5bd0ea39c33c4c82d0681e306395e`  
		Last Modified: Thu, 07 Nov 2024 22:10:08 GMT  
		Size: 2.4 MB (2424033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009897079055819a45e382cb2bdb934ddaa79c2a8ef847ab505323f82036f5e0`  
		Last Modified: Thu, 07 Nov 2024 22:10:08 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
