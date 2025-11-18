## `openjdk:26-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:686190befdf21323a7311139bf74d905b73589378a8d4997572c66d1382f7f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:05c4b08ff961e166bd54c389d76f303d5aeec6cae3985147a615e4841dd2871c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315301379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d0eeb3bcdde50e786b2477651a2183811f29249876e8600766f900e74a31c8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:51:41 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:51:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Nov 2025 02:51:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 18 Nov 2025 02:51:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 18 Nov 2025 02:51:52 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:51:52 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 02:51:52 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 02:51:52 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 02:51:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:023a182c62a0ce5adf24030e7fee994ceaa333b22cdb5f1a0835501015edf3ed`  
		Last Modified: Sat, 18 Oct 2025 00:10:14 GMT  
		Size: 49.5 MB (49496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163b56e3480660870a8bee5bee48821261e595e15933ab3b232fe3e3cdfa523b`  
		Last Modified: Tue, 18 Nov 2025 02:52:28 GMT  
		Size: 38.1 MB (38086366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232cf054569d7fb1128047ceb11e9a58320c3adbee129a5258629211eeb1c83`  
		Last Modified: Tue, 18 Nov 2025 04:26:13 GMT  
		Size: 227.7 MB (227718508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:27318170b2b4ead165cbb5565b16bfaccbb9947240d608a30d4330979a8c357e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3654220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d3c7a8c3f67617ad7578a447021720078b9b319e106e7ca82e52118e1a61b6`

```dockerfile
```

-	Layers:
	-	`sha256:9fabe252d29b36e222f1f96777da11f9cf53040ced79515b777981561aa018ce`  
		Last Modified: Tue, 18 Nov 2025 04:25:21 GMT  
		Size: 3.6 MB (3636382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1882267d2d121ca0caa420a4861142de1ccb4ab61f90406bd6fab5ac6b125b46`  
		Last Modified: Tue, 18 Nov 2025 04:25:22 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:64f06091e19d3cf3a3368d17a1e26267755a6300c1aa3cd886764fece267a669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312144259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3349e53b47e54ccbbe71f0a4a221b2d5938a3f10de608525f0b152f649348500`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Oct 2025 22:52:46 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Oct 2025 22:52:46 GMT
CMD ["/bin/bash"]
# Tue, 18 Nov 2025 00:19:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 18 Nov 2025 00:19:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 18 Nov 2025 00:19:21 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:19:21 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 00:19:21 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 00:19:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 00:19:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d86225d469f0ff347ff30258f3d1cb485b7b232705fcdf92e57ac5d6895ea30`  
		Last Modified: Fri, 17 Oct 2025 23:46:23 GMT  
		Size: 48.1 MB (48086901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4d5e9460f5041124f702152c9d8fd7fa567fec9a29f1b8af7c958391529f1`  
		Last Modified: Tue, 18 Nov 2025 00:20:10 GMT  
		Size: 38.5 MB (38490933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db2c3873b1f82ac9d84fbfa7f7286e3b66d1ac35f65197bc2ba979bc290454b`  
		Last Modified: Tue, 18 Nov 2025 05:18:54 GMT  
		Size: 225.6 MB (225566425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:fa2bf3b257bda356a824bd032ac79426b197e4c58dfa77d397a62a85ed721520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3652126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a59cf4397598801adf665d10e9c9baf798891bab9e97f36c2946cab676b002f`

```dockerfile
```

-	Layers:
	-	`sha256:da70abe4b594c0ae698bd715a53b4f484676774b636477c91175c5ebf9ff33db`  
		Last Modified: Tue, 18 Nov 2025 01:23:25 GMT  
		Size: 3.6 MB (3634072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8ced96518f2e690c1a712d693dc91ca3c04e8509e9066f8018276d780124965`  
		Last Modified: Tue, 18 Nov 2025 01:23:26 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
