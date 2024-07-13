## `openjdk:24-ea-oracle`

```console
$ docker pull openjdk@sha256:3a4efd5430324f609275cbcea9f7fd05fea923e2d494331154cc465b329ec9c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b35661af838fd678573ed7a908915ece18eba919fd9cdfe66ef6521a68a46133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298372271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9ab2bd8f6cc05811e18d68873ffa8b12ddba5e3ed97bbb84eafac2d40c268f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8248cefd8100d93cb09342af6b39f9d587c5b357f310f33d264ae0cae561eb62`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 37.9 MB (37872104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2607ce261146b862a675d659da86bd460bee43b12ad00b4e1946610ff1445d`  
		Last Modified: Fri, 12 Jul 2024 21:57:27 GMT  
		Size: 211.5 MB (211506431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9b5c3df36b60699bfa334e53400a8f61425801bdf671aab2ddc93c3370fb776a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f4dbbd932830ef702b9a5ffef939c508fb981df9ee3506886993f884732ccb5`

```dockerfile
```

-	Layers:
	-	`sha256:72a23e2052672b35ff321b2b730b1aef1f906e7b8d6729fa33db4e520002d4ce`  
		Last Modified: Fri, 12 Jul 2024 21:57:24 GMT  
		Size: 3.3 MB (3333228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54b80a64657d6c5f3ea776081327024882aca2fd1f55fe181e1b5005bff30dd`  
		Last Modified: Fri, 12 Jul 2024 21:57:23 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0244b120a66df5f3d364e78f6080a739e3a3a15efbe6cab190b21d0858737050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295300597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0988b7857836516ed61f05f46ad591f1908a18af049b2850bd1d05ce724902`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 12 Jul 2024 06:52:24 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Jul 2024 06:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jul 2024 06:52:24 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 06:52:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='85969884f11f2863595c13dff1cb6f6d94149bbe5188c34f0a7aaa284a545a27'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c719648382b7e5d564dc1d39d4408890d92ce5484fd46a5ef338da7380684ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Jul 2024 06:52:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129baf21359e4eb83f9d1391c216edfe6dce92354dbd70df14232415144a124`  
		Last Modified: Fri, 12 Jul 2024 22:04:48 GMT  
		Size: 38.3 MB (38259249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3cc192964be46952701da1855f6d030aafa73ac193e55b5fcf67cfe1d85af`  
		Last Modified: Fri, 12 Jul 2024 22:04:52 GMT  
		Size: 209.4 MB (209388687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:1d12505812136033fb1da564bf5f8d8dce0a22141ba8625e6b4ea5ef31388a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67111f951c8d96df20acf102ccd1ff031601a74a64b3754835aab1feff4d9695`

```dockerfile
```

-	Layers:
	-	`sha256:f22608b80d9a6e2dc485072af5481fc5c5c3e276ff4c5e978a23e9491a063da0`  
		Last Modified: Fri, 12 Jul 2024 22:04:47 GMT  
		Size: 3.3 MB (3331611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93aa333c100c60423b5a9b92a5d30504a00f86992987a30d162fd7e9d78acf2a`  
		Last Modified: Fri, 12 Jul 2024 22:04:47 GMT  
		Size: 20.0 KB (19977 bytes)  
		MIME: application/vnd.in-toto+json
