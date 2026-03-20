## `openjdk:27-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:fb875d00c28b44b94d126e22f48615fe07ac167e28d6625883a15575e99ec99c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:f69305e69b16072a2243482d6d846a9e17f7ef17949a3fcb7dc214cd41eb395c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314043323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b792927f1d83daffcab927f7ac2483cab6b61f05e552d4872831fd015cf1a416`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:15:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:15:07 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:13:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 20 Mar 2026 01:13:09 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 01:13:09 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 01:13:09 GMT
ENV JAVA_VERSION=27-ea+13
# Fri, 20 Mar 2026 01:13:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Mar 2026 01:13:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d4c7048d1cf1fb6137e2c8f7ae456b3950d5b1e9986feb08e68d4b0d7508481c`  
		Last Modified: Fri, 20 Mar 2026 00:15:18 GMT  
		Size: 47.3 MB (47310269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4777abf893697dc3393987f6696e8751e0173067928e4cb9613d282d33bc5781`  
		Last Modified: Fri, 20 Mar 2026 01:13:32 GMT  
		Size: 38.3 MB (38297614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3049932e39363b2e0032611bb5c16b4795894f3b2f7204711bdc4d712583b24b`  
		Last Modified: Fri, 20 Mar 2026 01:13:35 GMT  
		Size: 228.4 MB (228435440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:8309601099744116ec4dc64bb61862afea54d7274b7fc799a2366edbbe297ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3668290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e4b52070a468563784bcfaa7615067ac45f9846031a690bf3c1688cb25c46`

```dockerfile
```

-	Layers:
	-	`sha256:0edcf6821f336f9da81e083274eaecf83d8fd97810576ac8509785e5d8424faf`  
		Last Modified: Fri, 20 Mar 2026 01:13:30 GMT  
		Size: 3.7 MB (3652947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1174c78b907dad1c4006acdbf8dc110eed09cd39ef43b790231823153fe43864`  
		Last Modified: Fri, 20 Mar 2026 01:13:30 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:55708000ed161dbd76545c2982bbbe61eb9c76241af942d99d7ddc45673d2c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.0 MB (310998475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c937cbc418aa9fcc64d2263dc1c396928548de1ac88ae5511accca67847197`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:41 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:41 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:13:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:13:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 20 Mar 2026 01:13:47 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 01:13:47 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 01:13:47 GMT
ENV JAVA_VERSION=27-ea+13
# Fri, 20 Mar 2026 01:13:47 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Mar 2026 01:13:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e36e0b048a4420df1bab6b010b9e17a6211259ed3a0cf40f631a601ec3396cbd`  
		Last Modified: Fri, 20 Mar 2026 00:12:52 GMT  
		Size: 45.9 MB (45897982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ac266d8c5e72191e12942bbfadb94c14575df3d89b75128ab99cb385b8644e`  
		Last Modified: Fri, 20 Mar 2026 01:14:11 GMT  
		Size: 38.7 MB (38692409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d611994c5dae65bac7233c133f85f8b035cb6df8233bd7933581029fa8880552`  
		Last Modified: Fri, 20 Mar 2026 01:14:16 GMT  
		Size: 226.4 MB (226408084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:d7d697636e7c7859b2f5d436831e7e69b6932503112d41b28bcd00a8efb5ae39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3666003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637cc0b82777438e143688c85e17fd051a36b1059ece87b9a87de54954a0408`

```dockerfile
```

-	Layers:
	-	`sha256:9ffbfa82f834eebe4d298694b8aefc5661fdc5fb6b22cf4a867f9aca528873a4`  
		Last Modified: Fri, 20 Mar 2026 01:14:10 GMT  
		Size: 3.7 MB (3650541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01efc000495d2400743ea060cbed982b0945cebfcfb7ab0eae1516c05adb43b9`  
		Last Modified: Fri, 20 Mar 2026 01:14:09 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
