## `openjdk:26-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:1b8e5dbd3f2c1e3f23882d9a35e72cc8775547c85f73e5eae326f061526cc483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:abaa015a748a1812c1d49fb3e8245a00c4ad13671e06a42997b408092902acfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310436661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5735176c13571ca35c93ba6fc80a19e26099b26dc9981246c60212e0fcc6d4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:36:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:36:51 GMT
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
	-	`sha256:43c486e74c6d5afed80291ce1e8693695e0fbf029fc0f4c3d1e289a8b890a8fd`  
		Last Modified: Wed, 11 Jun 2025 17:13:14 GMT  
		Size: 49.5 MB (49500897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc85d888ffd0aa0aec5ba5d7d9771822df5fed46ff0d2aa43d8d0b4d4ce6a756`  
		Last Modified: Sat, 21 Jun 2025 03:28:16 GMT  
		Size: 38.1 MB (38081422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7358f2f86309cd21060151ea414d8553d487f11c654ff71e7d2d7604117ce8e`  
		Last Modified: Sat, 21 Jun 2025 03:28:25 GMT  
		Size: 222.9 MB (222854342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:2ed04fb82d2e7d88995a66057feafe31a62140f127f77aa06c2d3e489992708b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8d9cd6465cdbe71fb9c287734bab0bd3fdd65b853311201dfd72767713ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:4e20ffb6b28b9556d1b580bcf1be4cfae5051d378797b9105f8e432e9c18a3ce`  
		Last Modified: Sat, 21 Jun 2025 03:25:26 GMT  
		Size: 3.6 MB (3641220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789fe0d427e0e39e2ae8cbcb02800b54fd05debc59489a77779a06d8e4a2b6f2`  
		Last Modified: Sat, 21 Jun 2025 03:25:27 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:38d02c602dd8ce7e1dc22bd170e5721bb72bd8dbeab42dcc592b3ec4ad6d2768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287058242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cdd5456f8b8169046d4a36d7ca1a55af134bee20300edf7e51efaa11fbd588`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Jun 2025 00:37:07 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 11 Jun 2025 00:37:07 GMT
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
	-	`sha256:1281dea9bbdccb3c77c7f3a63c78eed96dc7efa9ab8208994aebc20dc76cbf26`  
		Last Modified: Wed, 11 Jun 2025 18:32:45 GMT  
		Size: 48.1 MB (48089795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7e489c978e38b5afa5d393fea94c54ad3525e6f544c411be6e80f47ef76d0a`  
		Last Modified: Thu, 12 Jun 2025 06:41:39 GMT  
		Size: 18.3 MB (18321513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8320a83caf09159f3ef5ca59145ae5f6f72efe1aa0a023f0565df5c34be8161d`  
		Last Modified: Sat, 21 Jun 2025 00:28:30 GMT  
		Size: 220.6 MB (220646934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:1d4cb43bb7b8fc1c5d7b8d907df4722e6fea3a241fa94d581c8e1e47833d00a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31f1d631cd47cda895d7c933ca4fe0a3bc32457982909f2c502052ddae6880c`

```dockerfile
```

-	Layers:
	-	`sha256:316ffb67a01fd322eeed5b4589df01789ee51f27972ea3f178e9650cec6292d2`  
		Last Modified: Sat, 21 Jun 2025 03:25:31 GMT  
		Size: 2.6 MB (2602099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a4e25c94771749cd175e004347c5f62736fd13c902e0bca1a97efc9cf6456a7`  
		Last Modified: Sat, 21 Jun 2025 03:25:32 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
