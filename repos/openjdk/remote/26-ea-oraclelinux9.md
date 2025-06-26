## `openjdk:26-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:a4373ba5e8162131d60529fed0639dbff0cfd49539a43f99c7333029865ae701
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:f05622866b7a9220bcb02fd66da3567d565ce01d5f38614e459239c283d12da4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310447201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ce8a75a7928d9f40daa2668f2a3f00c1f4bf770ac22b66667d6d6bf9ad016e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Jun 2025 18:54:20 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 18:54:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 20 Jun 2025 18:54:20 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:54:20 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:54:20 GMT
ENV JAVA_VERSION=26-ea+3
# Fri, 20 Jun 2025 18:54:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='f043a64fd0a2cacf76196c3e6a05de743c7e40f992e4e268ff829d094995e367'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='62251f3d724a03e4c25ceeca4bb75755b9e70ce275e5a4bf2cbb1e6579699839'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed0a8990cecb9184137c5a24c1d1534998531e6345ab03def7333d572661be1f`  
		Last Modified: Thu, 26 Jun 2025 00:04:55 GMT  
		Size: 49.5 MB (49500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af143664e8bd162caa2d5bdffd3e1c4156f1ad616cb77f95e80fa52e13af7ba`  
		Last Modified: Thu, 26 Jun 2025 00:08:52 GMT  
		Size: 38.1 MB (38092140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4883a7a0837ce984ab360a359f022253be8846dd52bdf6924fecc56c977926`  
		Last Modified: Thu, 26 Jun 2025 03:24:43 GMT  
		Size: 222.9 MB (222854399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:74d62158964a3f9c44cddcce59520dc982f8767fa1bbd9962fdf70d3b7e12baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d11c02532325314984694609454907fc6e1c581f7592710a450aadb5c89d9ac`

```dockerfile
```

-	Layers:
	-	`sha256:bb19425a8a8207e06aca7f9b0949a7e47f78d5f7cdba34bb506855ef97120b55`  
		Last Modified: Thu, 26 Jun 2025 03:24:10 GMT  
		Size: 3.6 MB (3641292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ca2eb2a0915b129773733a4c32e205a67d4a70e113a73f2699555b3be7338d`  
		Last Modified: Thu, 26 Jun 2025 03:24:10 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9dcb69a03bd9bb9773227491a69c9c926950c7f8d5c946508520727f3a588c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307229336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393500416aae13a5eebb0da9bb75f198e0a09c06fa34ca258cdf4386da2c8730`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Jun 2025 18:54:20 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 18:54:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 20 Jun 2025 18:54:20 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Jun 2025 18:54:20 GMT
ENV LANG=C.UTF-8
# Fri, 20 Jun 2025 18:54:20 GMT
ENV JAVA_VERSION=26-ea+3
# Fri, 20 Jun 2025 18:54:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='f043a64fd0a2cacf76196c3e6a05de743c7e40f992e4e268ff829d094995e367'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/3/GPL/openjdk-26-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='62251f3d724a03e4c25ceeca4bb75755b9e70ce275e5a4bf2cbb1e6579699839'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Jun 2025 18:54:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8651adb19772f22f50f38bb61855702b5099b0a0045fea8c9db8dcc1cadfea34`  
		Last Modified: Thu, 26 Jun 2025 05:13:18 GMT  
		Size: 48.1 MB (48087180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf0ee1c604fdbae17917604a097f1f42ae8abcc22cd62c1260386266d1d6ac8`  
		Last Modified: Thu, 26 Jun 2025 04:43:33 GMT  
		Size: 38.5 MB (38495135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb249bcb725cee75f6011799a9fb4abac44c427f73a92d9fb36985aa5eb755c`  
		Last Modified: Thu, 26 Jun 2025 09:11:19 GMT  
		Size: 220.6 MB (220647021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:68a9aacbea566a42ee05ff4f968d27c0311106ac171568fcd3129a025b87dca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bc6cbf375483d73fedca17010b3ee785e141ab362de04cacd088a49a5b07a7`

```dockerfile
```

-	Layers:
	-	`sha256:d2110a2a48c3ba2760ba53563b17a38d837e81f09b1204b101680b277104de8b`  
		Last Modified: Thu, 26 Jun 2025 06:24:15 GMT  
		Size: 3.6 MB (3639054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e64c46ff04e3e8bc18bf38e15776074dda3173fc7ad2e90bb5557f9ee54dae36`  
		Last Modified: Thu, 26 Jun 2025 06:24:15 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
