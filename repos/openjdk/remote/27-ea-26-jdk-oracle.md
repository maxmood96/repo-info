## `openjdk:27-ea-26-jdk-oracle`

```console
$ docker pull openjdk@sha256:d448c3bf8044346bd11bdaf0e4ebb00e22fc239c6530c05f7b483af2f449956a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-26-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ea308ed9eb5e9efcc359c535f3d5edab649ea11633ae7f63778bb4f96dd633a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307715538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c126e3e72d6bfdc662d307b3ef7e51aa54165e05fafc27ac563cb7ad354c59`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:31:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:31:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 16 Jun 2026 23:31:37 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:31:37 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:31:37 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:31:37 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cbc7f082e7d0c1c9979a5acfc4a0f6b0c3336b36f7a3addbacb9d47fd443d`  
		Last Modified: Tue, 16 Jun 2026 23:32:00 GMT  
		Size: 37.7 MB (37687391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b813bd85c57c220ad4c58d09a771354707344f0c41e23c6189453a2ac79420`  
		Last Modified: Tue, 16 Jun 2026 23:32:04 GMT  
		Size: 226.9 MB (226947565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-26-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c7baac34390cbe594e51b7454ffe2b6a7cf47d2f1bfa60a6d707446e1a72bae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbd76f310c5645e06ac9584e8b7fad24e45db9950914a295a58aeb9c160a729`

```dockerfile
```

-	Layers:
	-	`sha256:2c3105fd08d5c43f9199d6285ed5c6c32eff20ea5076b74e52cf1be12bf56cb1`  
		Last Modified: Tue, 16 Jun 2026 23:31:59 GMT  
		Size: 2.4 MB (2366462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8fd09569efea5e92a3fca02cbdac27c5c1a43b5cb611ca534ae38d7f46e109`  
		Last Modified: Tue, 16 Jun 2026 23:31:59 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-26-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c6a2c23c40d225b22c2dca73324ff9ec9da148616e5965d22b2fd3106a980497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304122519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc6cf257421964379760739c129219276bfc1aa7ae58031bf445fbbc55c5088`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:30:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:31:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 16 Jun 2026 23:31:21 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:31:21 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:31:21 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:31:21 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:31:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d539b4c7dea4cf17efc76208e411eb8ce3654593864bacd673b0dad98ec806`  
		Last Modified: Tue, 16 Jun 2026 23:31:45 GMT  
		Size: 37.7 MB (37696021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4843f662ec6c5189f1f80161ff40fd93b1be9ced601d03d717781bdcdcb8af8`  
		Last Modified: Tue, 16 Jun 2026 23:31:48 GMT  
		Size: 224.9 MB (224930803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-26-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9bbb97d04b1b88439e99f7b2ea09ba7fcf2cba7f6a1ddc1a8c9de98cd122592f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e1edf3707e18acb28871e35958faa08f104fb251508cdf2ffd92082ce1b862`

```dockerfile
```

-	Layers:
	-	`sha256:02a07ff5c05beba6ada95457642cac2645bd12332a8d60281cb88cd18e2b8f42`  
		Last Modified: Tue, 16 Jun 2026 23:31:43 GMT  
		Size: 2.4 MB (2365990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b26df06334af5bbd2c000e8e2fb814bcfecb795082965a0f09f7f073b5c79a`  
		Last Modified: Tue, 16 Jun 2026 23:31:43 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
