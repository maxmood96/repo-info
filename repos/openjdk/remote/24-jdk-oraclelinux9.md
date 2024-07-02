## `openjdk:24-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:2935f0e24214e3605c3ac5846bbb926edba47b7ceb251659feb450676ace9918
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:9aadef1fdb138330c3e0cf6e7c910891b27feb4aa5efddadc6ff2c9b4120a703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298171618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25da023794f6155919522ef1f467c621ff346e0a3de5ccdc3361149cdcfd2e42`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 29 Jun 2024 00:52:17 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Jun 2024 00:52:17 GMT
ENV LANG=C.UTF-8
# Sat, 29 Jun 2024 00:52:17 GMT
ENV JAVA_VERSION=24-ea+4
# Sat, 29 Jun 2024 00:52:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='64aa493b28493a2d223626bdad774640cb148b0d52f392b081b2776532a980a0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/4/GPL/openjdk-24-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='3d0b65f191528ab241b4e238568e52fa7199975b4f4b7badcf58a279b1fac426'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 29 Jun 2024 00:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaa553e046eeac03f941d9c5aeff3b502c3f1ce8778bbcd065d0a8d6fb57b34`  
		Last Modified: Tue, 02 Jul 2024 00:57:35 GMT  
		Size: 37.9 MB (37862476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aa169db96cd047ff2618e1d057812c40fd64b9b3b13af4826f43b8ddb53fb3`  
		Last Modified: Tue, 02 Jul 2024 00:57:38 GMT  
		Size: 211.3 MB (211315489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:bcf7b9a06bebfae8144b2c7dc8d17c82161e89416dcc6aa9dd5b8005c091e403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ec84814c514157837261d3006b9e2c44e595c06e689bd2c3eb489edd846c8e`

```dockerfile
```

-	Layers:
	-	`sha256:d5665a463a3e0270a9af9fe5b51ae990a479d7fe58cb929e073b8534eee8ce42`  
		Last Modified: Tue, 02 Jul 2024 00:57:35 GMT  
		Size: 3.3 MB (3333228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae88bc31ebbad7d65a632a331b1c210135613d4395f8f95e1ace39608ff7a6b`  
		Last Modified: Tue, 02 Jul 2024 00:57:35 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f51ceb413bb0ea2e42ed05e9364ecb4c694cf6206e3ec14080c277f4449be679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295121336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c9723862e12d7e48d4f7a2d2dcdabdabf7be1f51c99f6bcbe3bf6ee40f669a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 18:52:10 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 21 Jun 2024 18:52:10 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:52:10 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:52:10 GMT
ENV JAVA_VERSION=24-ea+3
# Fri, 21 Jun 2024 18:52:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='dad750c864049dba95a01fa89ad1c52c3b702ba87c3c865e5e64fa624f9e3de0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/3/GPL/openjdk-24-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='4a5515c226db56008676461bef7443163ccfe369415342136b8d9691ecd5130b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:52:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e03e86442d91879ee632bd4444507fcf4dadd66cc8c2b8458e11db03d0883c`  
		Last Modified: Fri, 21 Jun 2024 20:58:16 GMT  
		Size: 38.3 MB (38256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5843006ae468b96ecdee72b763966993d99590f92f2505d70cc86455c0492b`  
		Last Modified: Sat, 22 Jun 2024 06:16:10 GMT  
		Size: 209.2 MB (209212140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f9d8d4e16c951771d8579b5c6318d1d153b195a53302e9a85264a1bec58913c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d021404f19396d134b8296a538f74547a178fb135d45881f073cd7a567097cf`

```dockerfile
```

-	Layers:
	-	`sha256:1e6cab75b0a4adb5e1e825036613b5cb85ee9e53d2e224e952088502718b2328`  
		Last Modified: Sat, 22 Jun 2024 06:16:05 GMT  
		Size: 3.3 MB (3331611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25da4184b2b06c5043021db97f0ed5c6d3a94d213debe879a239edbf6ae1b800`  
		Last Modified: Sat, 22 Jun 2024 06:16:04 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json
