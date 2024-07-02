## `openjdk:24-ea-4-oracle`

```console
$ docker pull openjdk@sha256:0d251f1bc1b4e2cbed9fbc86a3d8973f915f3a6f2aa3e8aaea6ef52435c97a0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-4-oracle` - linux; amd64

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

### `openjdk:24-ea-4-oracle` - unknown; unknown

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

### `openjdk:24-ea-4-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3530282a432d43f4c7fbccfc992731a4f3d1df0a060bb87955d803ac982180cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1f78f9746a32d595b0c9dbe79fd95fe2eeb35b6e5880bb3b0202ec4971e8c6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
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
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ed45272c7719731d967108403425288bfe312d1a6e9b1c0035540ac6a1674`  
		Last Modified: Tue, 02 Jul 2024 08:45:27 GMT  
		Size: 38.3 MB (38256468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c115b9f6f142f853c2c40630eb5f866fbd74e2cb553f7facb8ad37a6608148`  
		Last Modified: Tue, 02 Jul 2024 08:45:31 GMT  
		Size: 209.2 MB (209184222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-4-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c029d8deceaf5aeeb95fd04fecc15e8c8107ff285a6e6ba9c4f985715deb06c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74c75e106817249a63fc5d5bfea6fa5b66443ea9af064e883a3cef7f3e2958c`

```dockerfile
```

-	Layers:
	-	`sha256:3fbf883a99ac4539ec0aec10e884bdff1dd53123cbd22496e268d31ca8841e4c`  
		Last Modified: Tue, 02 Jul 2024 08:45:26 GMT  
		Size: 3.3 MB (3331611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03756c544419caac372a9dc5c946132cd49b94fa164e51c80bf0f3c1c378b0fa`  
		Last Modified: Tue, 02 Jul 2024 08:45:26 GMT  
		Size: 20.0 KB (19976 bytes)  
		MIME: application/vnd.in-toto+json
