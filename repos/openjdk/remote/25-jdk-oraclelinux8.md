## `openjdk:25-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:be9f75d62bf41f64f44ddbff7fa1f1d31e33a9883b0e6d653d88378f6a00892e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ac6d140ed4536533f44ce17b3c9a023a98f337575025f5e247b6aa7501bdab61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289408915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec27cbfa6aa266857d84ebc8aef8b61a59ce42e1975ca6a0ca1c1fcea2d3e9c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:19 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:19 GMT
CMD ["/bin/bash"]
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ee6d2b4bc3292763eeab29f03adacbfcd179273f648dc332abeb3f2f9cf99a3`  
		Last Modified: Fri, 25 Apr 2025 22:19:54 GMT  
		Size: 51.3 MB (51312878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f4ed7587a8ee5bad87ca36e365b15fb1a547a71062da20cdf63cbaedc1abbc`  
		Last Modified: Fri, 30 May 2025 17:38:13 GMT  
		Size: 15.0 MB (14997920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44afbad73b881de8096c58bddb71cfdadd708598fa4da47c9b59775ecf4a7c4f`  
		Last Modified: Fri, 30 May 2025 17:38:18 GMT  
		Size: 223.1 MB (223098117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:601011db926e632f513e3a08c36c8cdfe83fd27ff537d22d6690ec7575df73a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e9317500878851dc5226eda36e088e3c9159cf9be3f4de91da8cc5e51d610d`

```dockerfile
```

-	Layers:
	-	`sha256:f12cf3e5512907c915e8fabac8a19c282c97a2178febcfa454786a6e342ccf29`  
		Last Modified: Fri, 30 May 2025 17:38:13 GMT  
		Size: 2.5 MB (2451048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94903ec8268430fb4492d3f995728c35a572f156df012ed96f6f8815678c4d70`  
		Last Modified: Fri, 30 May 2025 17:38:12 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:29f5c164980452a8cc89f3ac6424372f24da969ed919dc7ca3089dfbae0f3992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286565130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fc8cefcf6188ba4d53ffe4e67e3ec71fc012424682f3661d00ad652e70a0f0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 21:48:43 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 21:48:43 GMT
CMD ["/bin/bash"]
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f9f09355eb5a75f94b3d65a17269700229fb600c0fa7b446c5cabbd22d410e6`  
		Last Modified: Fri, 25 Apr 2025 22:20:08 GMT  
		Size: 50.0 MB (50027777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0355e89bd92c2a9ea2a9cffcd5e68fbb4942d49186eb5a083910caf9caf9b6`  
		Last Modified: Fri, 30 May 2025 17:39:13 GMT  
		Size: 15.7 MB (15667695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933e982dd03b885e609bbd0796a835962da7b00c82f0a1f8d0eab1ac80015dd7`  
		Last Modified: Fri, 30 May 2025 17:39:19 GMT  
		Size: 220.9 MB (220869658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1bf021a34a9acad46dbe8091479e1b17447dcd475fe2814cb1b024aab60b0acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab7efda10a8383cc2cdf10a08ae2d5b6930d8f1898e6f6bb11ce9e707fb17fe`

```dockerfile
```

-	Layers:
	-	`sha256:a3de975d321bc80346526832301ae10a970922592471af0aaf5437f3da7422ca`  
		Last Modified: Fri, 30 May 2025 17:39:13 GMT  
		Size: 2.4 MB (2449894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f737dbf7773320ee5a33f58d68d14caa11ae02b6eb28539dc7bd3e586738eb5a`  
		Last Modified: Fri, 30 May 2025 17:39:12 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
