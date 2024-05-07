## `openjdk:23-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:c444236662946c22b7e129956782d56b3df3dba64881e0122121b20e2d061413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:4be7ec1cef364d45cab64d83e8be819f3bea1f2b9477f4508c245cae60e8ec12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296686707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40733e6f61aa503c9ba97a6d0289fc8a0c7084e48a227c5eee9f9a39321d2da`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 25 Apr 2024 01:42:26 GMT
ADD file:6a8fca96158e62daae8905c2aa3ae7ac8614dfb3918aa6baed38c15923bfb4e6 in / 
# Thu, 25 Apr 2024 01:42:26 GMT
CMD ["/bin/bash"]
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0f6737e7f9187a51747790f2636510ac11e4d7718c4a8927053f6ec486848303`  
		Last Modified: Thu, 25 Apr 2024 01:43:54 GMT  
		Size: 49.0 MB (48965144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36dc94a8c46fccd31251d21871bb5f57f064d3a547509a9a3faa5e2fb28245e`  
		Last Modified: Mon, 06 May 2024 23:05:40 GMT  
		Size: 37.8 MB (37849048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb1b11120d0465282082f1c3f35b896a4aaa1f6e48aefb9e42d62cb6223d6bd`  
		Last Modified: Mon, 06 May 2024 23:05:43 GMT  
		Size: 209.9 MB (209872515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9db67112698c0650743231f060d399281e24729e83b15f6ff611c1e0b7683531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3229b8681bde6d432a7e32769e20eb37b275a641417b0fecb2a47f0ccf9a4081`

```dockerfile
```

-	Layers:
	-	`sha256:a93c4acd9bcfe6fa0e72f8b23a39a0f00a62304ec8a5f16a51e3544c31bc2c7b`  
		Last Modified: Mon, 06 May 2024 23:05:40 GMT  
		Size: 3.3 MB (3332740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ecbb33e64d1c42bd14a8e2801970443440b1b3c77b802408449ba76531a663`  
		Last Modified: Mon, 06 May 2024 23:05:40 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dd441faba361a418e21d365d93659bbed53f2feed761b6e3c545ae24a30f737c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293670861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa3e40aff63f706cbec81f1d31633347f39e545b820f0940ea445484771c34`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Apr 2024 23:29:31 GMT
ADD file:25023c55a282c7a0be958dc9555d115ad07185cff37f25566562575bc91f2d6e in / 
# Wed, 24 Apr 2024 23:29:32 GMT
CMD ["/bin/bash"]
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 03 May 2024 00:48:12 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 May 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 May 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+21
# Fri, 03 May 2024 00:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='20f3d065d5757feeac026eba758dd431f1343b5087c7f0f03ef8bbd2fa606bd4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='33a4798e59e479514004a62ec1863207430915212696689ea072cd7ad0b5d15c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 May 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c095c52d5d232eeebfdc7173cf1b5de6af5dfcf6cc906a66496ba14cf0ffcee`  
		Last Modified: Wed, 24 Apr 2024 23:30:37 GMT  
		Size: 47.7 MB (47662476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f41ba6f9688c4bce77b4d7a157ee07f6f9ad84c8ccf5e0fecf2e83de1b6a883`  
		Last Modified: Mon, 06 May 2024 23:47:00 GMT  
		Size: 38.3 MB (38255293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ded9fffa0ce4c4d525a77e17a0290090a1c6969db410c2375d8135e352ffde`  
		Last Modified: Mon, 06 May 2024 23:47:04 GMT  
		Size: 207.8 MB (207753092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:65d0cf37644469ef35f6f18a135600a97bc4c63fac55399ab013d2973bdbc27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3350868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a5a9fe19a936ffc24704775046a84ade2d1024a4cbcef0d3c5d08f7b3e8eb`

```dockerfile
```

-	Layers:
	-	`sha256:0ed592c0e4dad480823e9301930620e9d6090f7f62f54a9a830681e82325b636`  
		Last Modified: Mon, 06 May 2024 23:46:59 GMT  
		Size: 3.3 MB (3330938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd37b1f88f56b97a81d0f7b9bb297d4788843525e0c68f064c2d14d1486cb09f`  
		Last Modified: Mon, 06 May 2024 23:46:59 GMT  
		Size: 19.9 KB (19930 bytes)  
		MIME: application/vnd.in-toto+json
