## `openjdk:27-ea-9-oracle`

```console
$ docker pull openjdk@sha256:f7c897e8c5f89a9019dd2b87855f02a27322f664b454eae7e2e306e1e399b3a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-9-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:8330d2eb6d3d3733d54d6313d07d277ab7cedcba4e47a55aa81f30baf20a4d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313973083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6223698c3ed0dc44f01c47856d0ad0dfc3e70463164e4b09f004a0f707a5d901`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:11:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:11:41 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:38:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Thu, 19 Feb 2026 19:38:36 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Feb 2026 19:38:36 GMT
ENV LANG=C.UTF-8
# Thu, 19 Feb 2026 19:38:36 GMT
ENV JAVA_VERSION=27-ea+9
# Thu, 19 Feb 2026 19:38:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 19 Feb 2026 19:38:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74a8e4bbd9fe8a9fb7df9f028398fc37d20efc1cde6bf66eeeabef7755e5f5fe`  
		Last Modified: Thu, 19 Feb 2026 19:11:53 GMT  
		Size: 47.3 MB (47308871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e68466e7cb33ce0944f33391420e5b0f1895d23c7000c5c4f12ab96a04b5e4a`  
		Last Modified: Thu, 19 Feb 2026 19:39:00 GMT  
		Size: 38.3 MB (38296194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04601720671448427e66a7bfaa606272a4a42d7c06067602a11e8fdd79d9e1bb`  
		Last Modified: Thu, 19 Feb 2026 19:39:05 GMT  
		Size: 228.4 MB (228368018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-9-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:acfe4ba32ebc27bfbda42041122638bd73d3844a7a7a8b19b2544212f7f21f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2fce7f814503d0e88f2ebd13bfc727d0af38803b16ac4b08e83564b20c5a54`

```dockerfile
```

-	Layers:
	-	`sha256:85a04a4c076d48c9c74bc769983d72e1e2466513a5e851fe2a7cdad4fb0414cf`  
		Last Modified: Thu, 19 Feb 2026 19:38:58 GMT  
		Size: 3.7 MB (3655421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44d57e908c5c3b1239fc35f840e2fd32d3e0c7d31c41a2f395700e0393d54771`  
		Last Modified: Thu, 19 Feb 2026 19:38:58 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-9-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5efb48e20be10aaf62af3aaea21961a6e24518e491a48de5a4414d4ba4e7ce8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310908583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d73282fbd8602aa69b9d70a96f867ff5da00bd51b7f15ea32308a91649d1c6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Feb 2026 19:06:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 19 Feb 2026 19:06:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Feb 2026 19:37:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Thu, 19 Feb 2026 19:38:05 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Feb 2026 19:38:05 GMT
ENV LANG=C.UTF-8
# Thu, 19 Feb 2026 19:38:05 GMT
ENV JAVA_VERSION=27-ea+9
# Thu, 19 Feb 2026 19:38:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 19 Feb 2026 19:38:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:482e8d56575a6fbe539cfb44150fa96593766f3af0610165cb5c8a63fa68d8db`  
		Last Modified: Thu, 19 Feb 2026 19:07:09 GMT  
		Size: 45.9 MB (45901980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d54dce5ddeb617a42d78e887ced87b7680614f70c5eb164e124957c312d42f`  
		Last Modified: Thu, 19 Feb 2026 19:38:29 GMT  
		Size: 38.7 MB (38693415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57484575fbe404e7fb9194a3d0a255a366bc983916d3e7020a150e0f4b25e27f`  
		Last Modified: Thu, 19 Feb 2026 19:38:33 GMT  
		Size: 226.3 MB (226313188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-9-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9e54731c2c3a0665af1aaf5084fb919bd60a53ac7d5c51847f898fe7a04ef2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1421c3b25065c9bf90220af3ce2421741879161980689ffed1e35bd146ff0e9b`

```dockerfile
```

-	Layers:
	-	`sha256:f716246f175a6612c1505dc9e753a9757e0e9f57aaae8b554ced85b6b3329f0c`  
		Last Modified: Thu, 19 Feb 2026 19:38:27 GMT  
		Size: 3.7 MB (3653111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d93fc1b1de080ade7217d6af31e405d274a38cfb95e33f3f6622c454793b57`  
		Last Modified: Thu, 19 Feb 2026 19:38:27 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
