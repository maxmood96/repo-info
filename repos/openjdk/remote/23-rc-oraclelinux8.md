## `openjdk:23-rc-oraclelinux8`

```console
$ docker pull openjdk@sha256:8d5c3ab52787be4ccc60cd0eea098ad5fe6e03d3d1106f372c8f6f512028827d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-rc-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ee4df0a8f47b815078492a3901a461ec3f08b2a6119dd815f6903044b6c325fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278001001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8161ea15717154c06953728087d7ef62f973ec85dc4bb36b17ea7f48371368`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:50 GMT
ADD file:f88a328d16b39a012900e14f6463799b448cd9796472d5fb3c58c2cc5ebdee21 in / 
# Thu, 15 Aug 2024 00:20:50 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:964443381b57e80f40937734e7dfea9e93836abe517bd3e9e9c0fc9f21af4ee5`  
		Last Modified: Thu, 15 Aug 2024 00:21:56 GMT  
		Size: 51.2 MB (51221701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fe253de49acd9ffaa99b541612b0fdac7dc007c65f3aadc3f37ddef689287d`  
		Last Modified: Wed, 21 Aug 2024 21:03:46 GMT  
		Size: 15.0 MB (15036094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de935fa6c91d46094a4b59ee98a7ca34c801b0d7c41574b2b673a31979556c6`  
		Last Modified: Wed, 21 Aug 2024 21:03:48 GMT  
		Size: 211.7 MB (211743206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:dd0ab74a1b1c039679f39797e745f186dd790a589170a0a9c6d06715cb4c1f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edf5240ab3179150dcbfdfa1b5ea236413bfca3d22a19ac31630d45b46c6224`

```dockerfile
```

-	Layers:
	-	`sha256:bdb246dc55f83503a13f01e4c26af9b2494a67766fb958da52a8829fd625e602`  
		Last Modified: Wed, 21 Aug 2024 21:03:46 GMT  
		Size: 2.3 MB (2287161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457a3933694954707064dee1bc3cc06c7b76dcca8071da76bb66eb71833faf72`  
		Last Modified: Wed, 21 Aug 2024 21:03:45 GMT  
		Size: 15.2 KB (15216 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-rc-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1104ff1bc5de432e393b1e22e25267aee1c002711510842623ae790543f5f877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275344907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e3d1ae7662f6e81af18509fbb19134730a7ca4c47cd91c61b2b7c50d6f2ce3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:6b13879bf605622e279dbcac5c590af19f2ada3a9a83051585288eac41ef5a5b in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee4bb281b07b90a8d48b631141dbbfe6ee3f5d88680eac4b43c59de36db45ca5`  
		Last Modified: Fri, 23 Aug 2024 00:42:25 GMT  
		Size: 50.0 MB (50007867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f312e00b787dbc2b511697306ec64b5bfc43ad7382974bf128f204ebae9d1242`  
		Last Modified: Fri, 23 Aug 2024 01:56:06 GMT  
		Size: 15.7 MB (15702871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f59690953c0e341ef8f368f81e6b7cb94dbfebd6dc7251e2a6e73fbba0c1b7`  
		Last Modified: Fri, 23 Aug 2024 01:57:46 GMT  
		Size: 209.6 MB (209634169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f200a36f6627060c8d3d9738699e7a0b012874ce6b3edbfb7f92e1048b15b195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3bc7844230767bbbcfc0e81137a8eeae743346d58e9023f38967cc18e86bfd`

```dockerfile
```

-	Layers:
	-	`sha256:b15cac7339c35fbd17fcbbd47c732a8687137cece0242b77361468ed643c9c95`  
		Last Modified: Fri, 23 Aug 2024 01:57:42 GMT  
		Size: 2.3 MB (2286634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0aa23d1598e265a90fdab596cdeec0c83d55ce80e61eec2b1614728c2f2e2e`  
		Last Modified: Fri, 23 Aug 2024 01:57:41 GMT  
		Size: 15.5 KB (15522 bytes)  
		MIME: application/vnd.in-toto+json
