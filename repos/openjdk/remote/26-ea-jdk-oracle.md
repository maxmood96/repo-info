## `openjdk:26-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:3b817c4ff5037d2e5f721ab7a06128a82b082d0318c2b5434e08e5a8e24ac26b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:4802e9ca51fed485a8b9132b07e5376b316a573094e30da7985c01a7e1e97c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313459396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713ebe03df94bf5fee575a717832bda2065781e6da449ba1a1e76b880d13330d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:18:49 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:18:49 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:11:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:12:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 24 Dec 2025 06:12:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:12:06 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:12:06 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 06:12:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:12:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:26040ca4b0ffc7e767eb7fad043771a9a22da611177cce207dd56f39d9afb606`  
		Last Modified: Wed, 24 Dec 2025 05:19:09 GMT  
		Size: 47.3 MB (47319756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7fbd0606bf652338cda711637745621d8ae4489eb8fbdda6a036497a68e3d0`  
		Last Modified: Wed, 24 Dec 2025 06:12:52 GMT  
		Size: 38.3 MB (38298841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3ae727004f4b42ede108361044c73d4acdd311087ca402dbd95c5efa559130`  
		Last Modified: Wed, 24 Dec 2025 06:12:47 GMT  
		Size: 227.8 MB (227840799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:b324cd4a81b95437761e4c5956367ddc32bd2e6a7b427d14a07538cd7b29f2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52551678c33b337dd6123fd964c655b08c9b00eba912c4b033360f8272a7056`

```dockerfile
```

-	Layers:
	-	`sha256:18284b277847061f63c90cf2be06cd8b39ef23b3e6902a7fa07d98b08de402e3`  
		Last Modified: Wed, 24 Dec 2025 07:23:27 GMT  
		Size: 3.7 MB (3655355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42bdd56d12ac5f97e1d306a2683656d57014e50fe5a946a1de6868825628ca1d`  
		Last Modified: Wed, 24 Dec 2025 07:23:27 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4ddd4e4f2f7dc648707352705f997462604a63270ca43d5e6ca3e0b4a1d014d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310351933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca38fe3f104c4237b59b6898db1a95c8cf1d96c9ded1235d3a0b7f63ad20f2a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Dec 2025 05:19:35 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 24 Dec 2025 05:19:35 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 06:12:00 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 24 Dec 2025 06:12:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Wed, 24 Dec 2025 06:12:10 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:12:10 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 06:12:10 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 06:12:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 06:12:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9f8d71516ac44dff9289c2a411cbcbc9f061034b8711fb20d11502cac20d92d`  
		Last Modified: Wed, 24 Dec 2025 05:19:55 GMT  
		Size: 45.9 MB (45902993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0fb65748fc4dcfdda29d78df4121c65773fbd830ff83085882e89b5645212b`  
		Last Modified: Wed, 24 Dec 2025 06:12:45 GMT  
		Size: 38.7 MB (38699946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5339c0e2b57f8c0470402f8055e188ddb9b4a893b6b6b93b4c7c5cfcde267848`  
		Last Modified: Wed, 24 Dec 2025 06:13:26 GMT  
		Size: 225.7 MB (225748994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:73fed3a1fe7f8b2c98356a22d3121885ce699aaf8242c99acaa35f9d6ba1827c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c2439cf021208cfaee3fbc057e116617bc1e3b237d3dd176b81d767f4884b6`

```dockerfile
```

-	Layers:
	-	`sha256:79af29c943846687cd2dd8974298799c3102198c55c33a52161a40f0966a074d`  
		Last Modified: Wed, 24 Dec 2025 07:23:32 GMT  
		Size: 3.7 MB (3653045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e31cf8002dd453a42a7ecd538385b2c2026fa3949bfcf5df403278f30f1b32c`  
		Last Modified: Wed, 24 Dec 2025 07:23:33 GMT  
		Size: 18.1 KB (18053 bytes)  
		MIME: application/vnd.in-toto+json
