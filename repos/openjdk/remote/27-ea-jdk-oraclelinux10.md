## `openjdk:27-ea-jdk-oraclelinux10`

```console
$ docker pull openjdk@sha256:1930862579cddcca8142c4a7ce7cda1fab66a9df57c54be1bed15e5ae3ed00aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:cdde5fe0382216ca6ee00cef08c30a6c11ec7d23ab4f1315eb44ef3709e02a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307715364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f329b90e4af8411234198c5ffe0e335c39db4bd1c698abaaca15ee8ae4ac939`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 20:05:49 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 09 Jun 2026 20:06:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 09 Jun 2026 20:06:00 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:06:00 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:06:00 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:06:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:06:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197949bdd2d7b8ad2f9adf00ef1a428e8091453257a0b269f98d328d53342f9c`  
		Last Modified: Tue, 09 Jun 2026 20:06:23 GMT  
		Size: 37.7 MB (37687554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f48a60e1f9cde7751520ec91e88ed484a5cc204e99ad277d45dc0b85592d13c`  
		Last Modified: Tue, 09 Jun 2026 20:06:27 GMT  
		Size: 226.9 MB (226947228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:50b389887db6fcfbe46cf1f8dd15a910bf7f7f076545bd5305b308175055da94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cf5aa9da7e04d17aa031b5a3c93a91cd4563b62b3c9e5ebe4dd23d69b81a7b`

```dockerfile
```

-	Layers:
	-	`sha256:430e97f54fd48d0f28bc96e983f603588b7d6ca9b4f9713f06126a333ee5f79a`  
		Last Modified: Tue, 09 Jun 2026 20:06:22 GMT  
		Size: 2.4 MB (2366462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ceae8cd093538a1b17b7fb16a15750971d10faa34373d018f2d1b1c704ab54`  
		Last Modified: Tue, 09 Jun 2026 20:06:21 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:66ed22165b7c903e9e6b0db6496b301d6bce4aeda0a6762f69cfbac70c5cb1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304124197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74cf151a321da3b85f05bbbdb132b84887b92c8433b5249f4cb75649590f06b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 20:05:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 09 Jun 2026 20:05:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 09 Jun 2026 20:05:42 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:05:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:05:42 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:05:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:05:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e200c6d841596c0bf04991621458238854b204790e67988da089131e623914`  
		Last Modified: Tue, 09 Jun 2026 20:06:05 GMT  
		Size: 37.7 MB (37695864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c46f8f2e7177f3b3129c164afeed6c447a3e62cd644d37e9ee853bdaf9f97`  
		Last Modified: Tue, 09 Jun 2026 20:06:09 GMT  
		Size: 224.9 MB (224932638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3b34b9a4a6c593d9ba78a13b9f9fadd052cce8bd0fd44556706ff6619b68351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ed547878ce474c89dcbbfd8194610f1f6032a08a9d8fb1894cf0514e5f1e03`

```dockerfile
```

-	Layers:
	-	`sha256:6fe366ad27d4cc79c5a3eaf1f7df27cecc78eeda1d197ca8b023f054ff147b37`  
		Last Modified: Tue, 09 Jun 2026 20:06:03 GMT  
		Size: 2.4 MB (2365990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5187e8791e10bfc777a16e0071499094e91c843b94f71c73e8071f0f5ed974`  
		Last Modified: Tue, 09 Jun 2026 20:06:03 GMT  
		Size: 18.1 KB (18063 bytes)  
		MIME: application/vnd.in-toto+json
