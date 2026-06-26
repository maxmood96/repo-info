## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:9fcf2fc68fe8d6d058c3699bf748b03a3cc7fcedfde59afd85e8a0e8cdc8a844
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:d9147cee74c24e21d67aca7b091b26f98e610a2bfa8c1b0ee3a0fb5d49133343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313204186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a338d75b6e564481a1a52acb26542092dd2e7fbe0a37bbdfe373729cc7f7469a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:49:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:49:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 26 Jun 2026 17:49:19 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:49:19 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:49:19 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 17:49:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='45707add322e7be16c9eaf4e6f15febf5bd06baeab88aea73d3a89fae0d7bcd7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='1fe32bfb8b4a3533d1cbd2199cbdb9c62d72032b409da56d58135460a7e0c5a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6b21eb7a1e3e8c85b9f7c55e523b7309abb9be51ed5d639b708a756b2568459d`  
		Last Modified: Tue, 23 Jun 2026 23:31:18 GMT  
		Size: 47.9 MB (47923466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84441e0d67067a41af7d97e954ecb71da11e1730b38b1f8ec7ef33788f0f9b9`  
		Last Modified: Fri, 26 Jun 2026 17:49:42 GMT  
		Size: 38.3 MB (38301396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739ed317633aee495c132db22bc17a960639a62ec7a62257ee5979f29a2034f`  
		Last Modified: Fri, 26 Jun 2026 17:49:46 GMT  
		Size: 227.0 MB (226979324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:fcb7065c8357849fdea7c58250c9cb93583be4082b37c6a1a8ecd776b6444407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9097ba65b99a5481b9b994f8b487a0ead216c71f2ba61654a5b38b974429a663`

```dockerfile
```

-	Layers:
	-	`sha256:32dcd8487e995ebf0bb9b6f5e9d9132f82beb8d3158c9e88e438c3f25dda8bc0`  
		Last Modified: Fri, 26 Jun 2026 17:49:40 GMT  
		Size: 3.7 MB (3652167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fcc1a4b3b2bebc267c86f587535fbbc9e4dc257dbc49971df2371c9b2838f6f`  
		Last Modified: Fri, 26 Jun 2026 17:49:40 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6c3a32b4f893f5615b96ff6b283bfc14289df01b5a1b0834d505741ae1da030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310106543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578afe26c0288f790e5eaa5a00dd2613a5ca6f6582f9503018960c29b85c6bb4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:54:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:54:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 26 Jun 2026 17:54:15 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:15 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:15 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 17:54:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='45707add322e7be16c9eaf4e6f15febf5bd06baeab88aea73d3a89fae0d7bcd7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='1fe32bfb8b4a3533d1cbd2199cbdb9c62d72032b409da56d58135460a7e0c5a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14f0bac426a67d312501b30c0b419c0d5c2265f32077f348593b94dd76f064ac`  
		Last Modified: Tue, 23 Jun 2026 23:31:13 GMT  
		Size: 46.5 MB (46470688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d317f126b25de4a4a8e6727346b36df840daf0ec6a332565b86eda0b2097b8`  
		Last Modified: Fri, 26 Jun 2026 17:54:37 GMT  
		Size: 38.7 MB (38691238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5077b0aa82c7ce88edc906b145627d41492b14cebe2344cb5dac858d35b1f5f`  
		Last Modified: Fri, 26 Jun 2026 17:54:41 GMT  
		Size: 224.9 MB (224944617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:24bea801f0d434ba7061d38384ad006aaa5722d961bdfb43cd5142057b5c1c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a07cd02f34a195ec6e071e177d3011990cbfac37b2ee5f6071f50a0e46c0d49`

```dockerfile
```

-	Layers:
	-	`sha256:5990f88f41ff511397bc0ec9f0c8615d5aeb62c4b398d34f963ee19309cd956b`  
		Last Modified: Fri, 26 Jun 2026 17:54:36 GMT  
		Size: 3.6 MB (3649777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5bb2f4791db572c3693df81197e436a11b6afe8fb7e0b71722964a8dc73434`  
		Last Modified: Fri, 26 Jun 2026 17:54:36 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
