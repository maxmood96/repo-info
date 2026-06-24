## `openjdk:28-ea-3-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:83dc8d2ae937cd4c90f240a9e05270fe5d86903cc51abdf315e8b54cfdae2b10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-3-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:8e021a7c04cb8f580d935c3d730d931f4ede2cd5e4183fb4f31dd07138806077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313608271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def3ed2e9e00e9269e074162421c52b0f4b9069c180d5dd3f6e518d781a305d2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:07 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 23:32:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 23 Jun 2026 23:33:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Tue, 23 Jun 2026 23:33:06 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 23:33:06 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jun 2026 23:33:06 GMT
ENV JAVA_VERSION=28-ea+3
# Tue, 23 Jun 2026 23:33:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jun 2026 23:33:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6b21eb7a1e3e8c85b9f7c55e523b7309abb9be51ed5d639b708a756b2568459d`  
		Last Modified: Tue, 23 Jun 2026 23:31:18 GMT  
		Size: 47.9 MB (47923466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dea8af9874ff41cf2be2c3317dd21af4fa6a4dc07a67ad07f960832afc0f27`  
		Last Modified: Tue, 23 Jun 2026 23:33:29 GMT  
		Size: 38.3 MB (38299824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c8a48c7f770d42547d4a285c075050ce2a77c7d563870b3384f59bdc371e1a`  
		Last Modified: Tue, 23 Jun 2026 23:33:34 GMT  
		Size: 227.4 MB (227384981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:753b65730692617eddee5914de3cbca1d3e8a2e4977f6ee54532641c297ba058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c21409b92c4f31ccad7b323b0ad1e578ed340cc74b334c08b66f81cbbed2ee`

```dockerfile
```

-	Layers:
	-	`sha256:f7a9aa51634392841f58f13d54702f11c46793b763bf22f6a136a661fb29db7a`  
		Last Modified: Tue, 23 Jun 2026 23:33:28 GMT  
		Size: 3.7 MB (3652143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad463f9cf7af2a4fae1e177e1051beb349e17998bc5261ecd16e04f9e953839`  
		Last Modified: Tue, 23 Jun 2026 23:33:27 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-3-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:86af09889e6821e93252a6b29d2e2a926041b12077ebcf4e9664f68b022a373e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310579220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6a9a57e125139c5f397fe2c51dcfef4bfca6bc09c67616d55f728e2014f045`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 23:31:02 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 23 Jun 2026 23:31:02 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 23:33:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 23 Jun 2026 23:33:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Tue, 23 Jun 2026 23:33:49 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 23:33:49 GMT
ENV LANG=C.UTF-8
# Tue, 23 Jun 2026 23:33:49 GMT
ENV JAVA_VERSION=28-ea+3
# Tue, 23 Jun 2026 23:33:49 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jun 2026 23:33:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14f0bac426a67d312501b30c0b419c0d5c2265f32077f348593b94dd76f064ac`  
		Last Modified: Tue, 23 Jun 2026 23:31:13 GMT  
		Size: 46.5 MB (46470688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d10a33fc76dba189001fe74c86890effb3921ded7e88582cd992cc37d19978d`  
		Last Modified: Tue, 23 Jun 2026 23:34:12 GMT  
		Size: 38.7 MB (38690413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395fd934372bb990115c8fae9a6c34bb1b72ce1185a0b016f4b175942210f282`  
		Last Modified: Tue, 23 Jun 2026 23:34:16 GMT  
		Size: 225.4 MB (225418119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:23bc541d48a0b9afde3029dca11661d500555103f0402190a05bfbe21792ddcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f25bd3adb2bcb0eba75811740f3161e43ecaed7a4d00abe7a820b0f542f5d6`

```dockerfile
```

-	Layers:
	-	`sha256:6dac909048a69764002caf94585d0a7ab94627669e0c0fb293b61123f27e5f95`  
		Last Modified: Tue, 23 Jun 2026 23:34:10 GMT  
		Size: 3.6 MB (3649753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edca6e50a4ea03691b33f80169f4bd4dc86f66cf684a23234777910ea1ead74e`  
		Last Modified: Tue, 23 Jun 2026 23:34:10 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
