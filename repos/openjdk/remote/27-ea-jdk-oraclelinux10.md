## `openjdk:27-ea-jdk-oraclelinux10`

```console
$ docker pull openjdk@sha256:261bde7b4c400c9b712c7fdb4483d25b6f1c9bddee213b1d0e181ac82bb42818
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:19fc1624a9bf10152440f71173af202a30878eafd52f7e5cfc0d865867fcbd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307648803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62012a908cb20d64322470def7cade793aa637fb6f70046301c47d2313aaa7eb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 07:11:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 07:11:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 02 Jun 2026 07:11:44 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:11:44 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:11:44 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:11:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:11:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b413b89640d95a57eb7b842085e6fd4439d390d91cd5d1c4a37e13c30710f`  
		Last Modified: Tue, 02 Jun 2026 07:12:04 GMT  
		Size: 37.7 MB (37687493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365ea1fa2e28b538f48a1a4810554b70175c7cbcfd900d39e942a0067c8b7bb4`  
		Last Modified: Tue, 02 Jun 2026 07:12:08 GMT  
		Size: 226.9 MB (226880728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:85733fd04435de7e43d12c9572954cdd6784294b39ea76334018cc12b591c6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c361e706569be356e9331c8c66e864a819bd1111eb4828ca8c21fcd1c43f6`

```dockerfile
```

-	Layers:
	-	`sha256:86b9b2c2c80128106e99753d5c7e6ac355fe62d6bc9f4972a2d777881a0aa66f`  
		Last Modified: Tue, 02 Jun 2026 07:12:03 GMT  
		Size: 2.4 MB (2366462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2cc41e29928469e32aa9f5316d5b11c8c99063d12f453607416bf5116267c4`  
		Last Modified: Tue, 02 Jun 2026 07:12:03 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8e6a0aea2e4bda804104559eea071364a97b1d8ecd461b69c76e866820817dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304086647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2cf318391be84467d3fc7056eb7fb2605af62abc67c89ae6b5a8fd9bc8308a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 07:11:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 02 Jun 2026 07:11:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 02 Jun 2026 07:11:32 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:11:32 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:11:32 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:11:32 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:11:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a29592fc483b3f4c221695150f5f9389362613cc717fbc34a247f61c398955f`  
		Last Modified: Tue, 02 Jun 2026 07:11:55 GMT  
		Size: 37.7 MB (37696164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64763745e63ee44cb77154aa917cb6492f750af516c2ad48e6cc1261e3fa0f4`  
		Last Modified: Tue, 02 Jun 2026 07:12:00 GMT  
		Size: 224.9 MB (224894788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:18e43328367e73f9935d21167c799796a456e851df1e954763b0fc9d4c4a11e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e48ab6aa0722b65ba859e34cd0ae792c2dfba5c1e9cb4152dd9f270c94670c`

```dockerfile
```

-	Layers:
	-	`sha256:9dff09b3be493d2dd5be82d0e77f2bd962785389f7d018c4076f384274e57a57`  
		Last Modified: Tue, 02 Jun 2026 07:11:54 GMT  
		Size: 2.4 MB (2365990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232964f836fb0fb3a1d4f40e9fbc76b30edf5483ebed631919604a5ec35bec18`  
		Last Modified: Tue, 02 Jun 2026 07:11:53 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
