## `openjdk:23-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:75f66b3612f322392c2e16d762ba8556bb3e350da15bba1ac0bd05e7e78fa510
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b85fb3d647110633a96751f14ccdcb062cb51b9e685a59d21be5c2311beb5fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267724155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a1cc9f928c39d253d4525a3346017b2fdacf2dce8d9e2b3d96b8edf7c9460c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:52 GMT
ADD file:6c43f1bc1b598f7b1a5fc6f5c7951e8525eee01704f8f5e5caec8a944a4ecb4d in / 
# Wed, 14 Feb 2024 01:47:52 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ff90099b5a4df32952d1822d472a72c931c53a68c05a3ba7431ea0f85d54135`  
		Last Modified: Wed, 14 Feb 2024 01:50:04 GMT  
		Size: 50.4 MB (50389833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d77b16c15096dd00c7bc5081246910898281009980981a1dff1b4ad9411a276`  
		Last Modified: Sat, 17 Feb 2024 00:53:28 GMT  
		Size: 14.2 MB (14231534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e75ee8bcae255c91d4d4dee42d544c6191fb41594a7551dab421da92b436b4`  
		Last Modified: Sat, 17 Feb 2024 00:53:30 GMT  
		Size: 203.1 MB (203102788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:f1d2e8d977dfdca8ffa4a31103949b4194314247708abe40a21ad735b3a9279c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55311c78b59893083bb90a1077e934e3b1d0f7ad8388c32a54fda6c1615acb1b`

```dockerfile
```

-	Layers:
	-	`sha256:5da099c6ac9b0ccd9a5b877d86d345bd3edb2d75d85f17b6e7b1e1ad64a95547`  
		Last Modified: Sat, 17 Feb 2024 00:53:28 GMT  
		Size: 4.4 MB (4429923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0392a8eada4e679a4bf5f1dc8c4c7e3980a6db5e204260d917ad2b3b085435f4`  
		Last Modified: Sat, 17 Feb 2024 00:53:28 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:299495ef04a0fc6a8a7ec49797a5f2b8f447a9f2f74bfb6b765112e3f109ecde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267224618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02048fc9946d7ac72d389d368dd4fca07ef3d2283fd8d5de227079d752959f16`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:45:11 GMT
ADD file:8a1de5e2eb0c974503a07ee47335076f6fd201d377d647cbc5454453b71f05dc in / 
# Wed, 14 Feb 2024 01:45:12 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 16 Feb 2024 20:22:31 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 20:22:31 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 20:22:31 GMT
ENV JAVA_VERSION=23-ea+10
# Fri, 16 Feb 2024 20:22:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='9b583a20351ff9be1b782ba71d5e61d7f8e4731c81277e4f2566c5509db052b0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='b646bcb58d932236e066c97dbc32d6df53a9a823c78565cd22bd6bf05a0cea7d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Feb 2024 20:22:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f12fd75c9aeabed692ef7b5d8a691db1e8f77911ac84bdaba43458300ab36fb9`  
		Last Modified: Wed, 14 Feb 2024 01:47:06 GMT  
		Size: 51.0 MB (50996218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f5782b608cb55c41f80fe5c4e8c6606f42add68733d4172117af3cbf2d90aa`  
		Last Modified: Wed, 14 Feb 2024 11:17:14 GMT  
		Size: 15.2 MB (15244449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec9d86a519fbb07d7eef5540bf952d7edfad310ce96d724218fd2ecd34fc02e`  
		Last Modified: Sun, 18 Feb 2024 05:16:33 GMT  
		Size: 201.0 MB (200983951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:82e77915de1b08f8d0564a0fd10b382e3d1c0ee1ff8303f69c9ebc516000e82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4441830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1f0d86a100ebe10e77244f420f86f95a0a9a5d6267e3bbe6c9fa38d30aa8b8`

```dockerfile
```

-	Layers:
	-	`sha256:2d66aeb996ec45ce8a9ad9cc82764e107be37477e2cea440102fb286d2789a8a`  
		Last Modified: Sun, 18 Feb 2024 05:16:29 GMT  
		Size: 4.4 MB (4425580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8936e7364871b8df94c7de8a9feffa378140e4fd0b7142e0d7bcc97006022d62`  
		Last Modified: Sun, 18 Feb 2024 05:16:28 GMT  
		Size: 16.2 KB (16250 bytes)  
		MIME: application/vnd.in-toto+json
