## `openjdk:24-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:d54709a8ff0932f89565c1187c5c0b7ac41f5d69aa570ae922bf762eb51d72a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:978d2b89bd02a3cf30fcaa472562e751a9c99d5139c27215b82a0d00365f1406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310653663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25bd4391fd4bfca95107489b6287b98ca22e2862f782170ed0211ef6d74d9f7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67129e99a8251215d567322a5b5fec4ef0ff328c73a15967badab8fc2dea870`  
		Last Modified: Tue, 28 Jan 2025 23:28:49 GMT  
		Size: 48.8 MB (48774894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099be1039d82361e2024543871eedfaf30f47e08228a95afbb65029981ad6a9a`  
		Last Modified: Tue, 28 Jan 2025 23:28:52 GMT  
		Size: 212.8 MB (212780067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f1a6e3f77f7a4e76aedc990ea6c1c762769763bfea87e9d0eeda5a3d359119ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f9f1f6e3b5cb61730b139160a540b5beea3042219f43aeeae57223889384e3`

```dockerfile
```

-	Layers:
	-	`sha256:d9b59c0ab7c47ff91dce57d0528b01afc4501dac5b99611dcbf11666cc706a6a`  
		Last Modified: Tue, 28 Jan 2025 23:28:49 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa0f17c50da899e6a10375cb0bb848c3f15edd421921c5dbab2703895deb07b`  
		Last Modified: Tue, 28 Jan 2025 23:28:48 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c55acd6a7006bad3404b227e8f078777f297f8bc20c9bd7bc740fc333e3d75af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307610707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de3b7d96e459cbca7aee0e4ff70712eb01b8fe6f5d58cbd31a80b48a0784411`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 25 Jan 2025 01:48:18 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:48:18 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:48:18 GMT
ENV JAVA_VERSION=24-ea+33
# Sat, 25 Jan 2025 01:48:18 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='5cd9eb14e10702aded61b4752ce6db2a472f3f950d0381afd88ab448a1e43fe8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='7600c4f929f6db2755ee2b9664ce8bfc409abea10bc7d129f5140ea49f62433a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9527a70a5df0c50a0919b2bbc807b6789f8d6833d49f997079d3ab5dd2e735`  
		Last Modified: Wed, 22 Jan 2025 02:29:30 GMT  
		Size: 49.2 MB (49203729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1713698d5edb05b05fe127407023a4d5a20d8602482e77a177203d69b26cac`  
		Last Modified: Tue, 28 Jan 2025 23:37:55 GMT  
		Size: 210.7 MB (210739586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:20254ddf111a8d31e0134dd75b1e122e9b43a32971ccc5b424c2ecdf6a091eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb92f7b15ac79090eac3aecf5efeee2c574ab4c20e5a074ac8558bf212fa85f`

```dockerfile
```

-	Layers:
	-	`sha256:9df52185e98e64c1690cc1a79afddd93dac5e2f3985494959f8399cbf75adb22`  
		Last Modified: Tue, 28 Jan 2025 23:37:50 GMT  
		Size: 4.9 MB (4905337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b9c2ee87efdb8625c974acb815229ea08460c9ca2a86abadc1c382cb4d0846`  
		Last Modified: Tue, 28 Jan 2025 23:37:50 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.in-toto+json
