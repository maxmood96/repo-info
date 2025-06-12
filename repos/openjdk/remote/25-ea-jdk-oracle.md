## `openjdk:25-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:d138e74eaf258407650c5da325e647a32d601d83293a89663e84ade6f5985ba8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:7c61a77efcda275a3884cc7b4a3cdbdc0af56bdf531167be970d9b3d899ba0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310560377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c685aa29d4361533a9408156d721351ff9908990e728ab8155259bd05842f31`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Jun 2025 06:48:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55da7740d2fc1993092582883380bd30f04279370067363e4920f684c4603c4`  
		Last Modified: Wed, 11 Jun 2025 17:33:44 GMT  
		Size: 38.1 MB (38081375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c87f4af59a1769a173b3061f069d6a7c3e1a0c1bbe082ad924db3e0a53e437`  
		Last Modified: Wed, 11 Jun 2025 18:25:01 GMT  
		Size: 223.0 MB (222978105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:95d6e55a7a96d783271bd88de43f22aebf62bb37616a2d405063769009cfaebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139184294d550cae41c20ca84262cee3f857f4f15224b70a7e4d0886cf14148b`

```dockerfile
```

-	Layers:
	-	`sha256:6a80b3172083238b584ebcdd2679f29d5e0ca6d75c5d94bf25ef56402d076d5a`  
		Last Modified: Wed, 11 Jun 2025 18:23:19 GMT  
		Size: 3.6 MB (3641236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc318ebc1584df833e373c79d8aba00bae79e2d49e7ba4fb8a9c160481cef0e7`  
		Last Modified: Wed, 11 Jun 2025 18:23:20 GMT  
		Size: 19.7 KB (19744 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3247e49b8aba95881c9eb6c490b8833564064a16890c2bd5907cfba3708be8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287180177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0670d3c07342faa0285461a50bff71b6796f2d007651e118e47a02eecc0a039d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Jun 2025 06:48:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["/bin/bash"]
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Mon, 09 Jun 2025 06:48:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 06:48:11 GMT
ENV LANG=C.UTF-8
# Mon, 09 Jun 2025 06:48:11 GMT
ENV JAVA_VERSION=25-ea+26
# Mon, 09 Jun 2025 06:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='bec0201fc359c9fa1075d95f49a422113ce6aa004345eb6af1b6945a56880994'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/26/GPL/openjdk-25-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c5be9b0a161ba87ed6632b21490aa7556cf615a4794dafe2dc87c93dd0ea9b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 09 Jun 2025 06:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7e489c978e38b5afa5d393fea94c54ad3525e6f544c411be6e80f47ef76d0a`  
		Last Modified: Thu, 12 Jun 2025 06:41:39 GMT  
		Size: 18.3 MB (18321513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e0812642b08329ceabd90447927d4bcd76f54c7a56379ac034d51f85f954cc`  
		Last Modified: Thu, 12 Jun 2025 07:22:48 GMT  
		Size: 220.8 MB (220768869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:4c93b1499f35901fd0f5b573948d4756c91abd854eb1c02f231510a32a8baaa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e4a3cfe384cfa5de5951928ade1faeebfa41ded10754fac503f6582b7ea626`

```dockerfile
```

-	Layers:
	-	`sha256:532a6f850bc5208c98a7d9b76e59c7edd6f3d3c08a94f6e391a7a8068cfd4edc`  
		Last Modified: Thu, 12 Jun 2025 06:23:20 GMT  
		Size: 2.6 MB (2602115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91142ecd489b9b39aa77d06eb47ec659a924a5eb5e7b7c3cb3e3a06db418e646`  
		Last Modified: Thu, 12 Jun 2025 06:23:21 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
