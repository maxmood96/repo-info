## `openjdk:26-oraclelinux9`

```console
$ docker pull openjdk@sha256:a8c3355fe179f1a34021cc147db5b63c879295481c9667ca32e8a27cd1520a25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:f435c58cd39d589948752cf05f19fd11288cb910f25bd3243e553d2041322d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290044123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c3ea5ce6aefe762475a1630a1e09ac8d8ffd71a80390d45ff7bc84dd3f3d22`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:36:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:36:51 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20970b710dabff28318bba6125553e1344b7fac9dfb1ceff5fcbd3b7de61de1d`  
		Last Modified: Mon, 16 Jun 2025 17:51:15 GMT  
		Size: 17.8 MB (17776180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d834b6a0f92cc067bba90f5f0ffe487815f03d0641765832e081fa7cc5d030`  
		Last Modified: Mon, 16 Jun 2025 18:30:50 GMT  
		Size: 222.8 MB (222767046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:01a76142cb535ae266afd2ed4a6fe79092b5b58d45aa13f9a333f9f561df0fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2963b51c96bdc4c33c95855000f06aa9259d430e4ed2904ad5f3c195f48fd09d`

```dockerfile
```

-	Layers:
	-	`sha256:dace497595592b7efe9d7f9dcd97c64ed774a0c838ac9a000717f6c2493d5e5c`  
		Last Modified: Mon, 16 Jun 2025 18:25:15 GMT  
		Size: 2.6 MB (2603105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19438dffc8fb63a3a7da43eba2d2f5cee6915f22688413ee3751b4b0ffd1e380`  
		Last Modified: Mon, 16 Jun 2025 18:25:15 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f435804bc973ba372eb8e323aca37eca30d87a0412cbcf7205936d50129b9edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286987689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75abde1eccefb24f8ab6cd898793aa7bad06f53e4536e919d65f6e3de4c2768`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:37:07 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:37:07 GMT
CMD ["/bin/bash"]
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 14 Jun 2025 00:54:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Jun 2025 00:54:06 GMT
ENV LANG=C.UTF-8
# Sat, 14 Jun 2025 00:54:06 GMT
ENV JAVA_VERSION=26-ea+2
# Sat, 14 Jun 2025 00:54:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='433a629dd1072b3147cce33cf79ae06ba8c7aa9aac53f403330e8f10ec12ca76'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/2/GPL/openjdk-26-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5f413ff4f8e92fcdeaf0da5315a51d2165a4017852a4a6c7e2731a8aae19e2e7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Jun 2025 00:54:06 GMT
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
	-	`sha256:0e7eaf5a9f5d2efa53320883debff828fb983f74e382a5891b6a91c8506c40fa`  
		Last Modified: Mon, 16 Jun 2025 18:53:30 GMT  
		Size: 220.6 MB (220576381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:24fe49d3e83f50f98dd4a1ad02c3beae167e4fa294a6ed10adeef4460909b330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0547661e3da4544c893eb5101a4eb434e9f301920e90bd42d94c4d17460049fa`

```dockerfile
```

-	Layers:
	-	`sha256:24d052c31aa1ffa973b17ac76125e8819810260c43801f00ca46c44dec757838`  
		Last Modified: Mon, 16 Jun 2025 18:25:20 GMT  
		Size: 2.6 MB (2602097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf8b147a23f9ab8a489ff075c1f19d457abe2e81fdcb68bd13a9cf5edd6adc9`  
		Last Modified: Mon, 16 Jun 2025 18:25:21 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
