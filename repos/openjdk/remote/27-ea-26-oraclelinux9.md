## `openjdk:27-ea-26-oraclelinux9`

```console
$ docker pull openjdk@sha256:a39c3d600fd1ed7b7798eb909e6c666210b16d6772ae0093d564209e4c51698c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-26-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:350eb8699b0a901e31002866d24d8a6eed3150a6ea5980459d8eefbe6e72bf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312524735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a790b6f20f4189b2d5d285239c0ab50ba5eaf00425f6328ab431ad5778140a3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:32:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:32:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 16 Jun 2026 23:32:20 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:20 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:32:20 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:32:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:32:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e621cb4a5285fc6a1e235583270c066a82354cf61348aea04f7c9fc4727b6c`  
		Last Modified: Tue, 16 Jun 2026 23:32:44 GMT  
		Size: 38.3 MB (38267933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8e94dff08a1a0ef70194b67af8959d80bb59933eb5171dfc85e7c3b25c49df`  
		Last Modified: Tue, 16 Jun 2026 23:32:47 GMT  
		Size: 226.9 MB (226947229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-26-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:70a5d19c214d26b32ac51b9fd0f95f37777f9c5b1d918abd27f783c90d655389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2c42e36f1a06dc4be6ac0f19eb7a5a37bde88dffbe2d58c0c2d51a9bca82e4`

```dockerfile
```

-	Layers:
	-	`sha256:14343b23734138b3a0986f119e79706bf89422dbb72ff101fc8d1baf9d5700fa`  
		Last Modified: Tue, 16 Jun 2026 23:32:42 GMT  
		Size: 3.7 MB (3650422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c8504f5b70582e2b245355b799aa4efa58b6a6345c3d14bac9f518320f14e3`  
		Last Modified: Tue, 16 Jun 2026 23:32:42 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-26-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fbbb8c7d59d060d2f11acfddf6e4d5e2c8bf8d7d0597e2a8fd83f3a5fb23bf46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309495356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587844758380c1a1f9172a6776e2c8d149dfedf90d5d072499bc17d373e87aa5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 23:31:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Jun 2026 23:31:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 16 Jun 2026 23:31:54 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:31:54 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 23:31:54 GMT
ENV JAVA_VERSION=27-ea+26
# Tue, 16 Jun 2026 23:31:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='8b55960efe73b9eb24c424f6d7dd1dae088eb2571c81dacfa76d05a2b9e24523'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/26/GPL/openjdk-27-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='062f3bc3a420c426c85bac9a0051044a4ce17a8f67b382efbd3f5406cb9c184d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Jun 2026 23:31:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c9eb01b0d01b7fa3eccecdf416f8a481897c23af14ad970ca9fd1f8ebd8a6f`  
		Last Modified: Tue, 16 Jun 2026 23:32:17 GMT  
		Size: 38.7 MB (38665595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ada3fd3abc785c8a067574b0072b007e3120c23004000acbe645938cf489153`  
		Last Modified: Tue, 16 Jun 2026 23:32:21 GMT  
		Size: 224.9 MB (224930671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-26-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:81283134ad021a1a8b333748e4dac63a6e7f0f2a97e804769d77bad49932c116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e4e4935ef0da199a1fb61f6c7a99df9c1d4c8e90bc09310b7725d774b61c2b`

```dockerfile
```

-	Layers:
	-	`sha256:ab7e31fe0e0cff7d2549748a403860f428a365aed0f15a2083d6363dc4d937d6`  
		Last Modified: Tue, 16 Jun 2026 23:32:15 GMT  
		Size: 3.6 MB (3648016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d6f0c6be1f7d5a5e0d347197669ca926798c0f437bfa2bbfbc8252f61b0fb5`  
		Last Modified: Tue, 16 Jun 2026 23:32:15 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
