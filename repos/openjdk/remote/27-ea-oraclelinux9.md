## `openjdk:27-ea-oraclelinux9`

```console
$ docker pull openjdk@sha256:cc779ae6584056fd4fb5f892f5067b09ccf3a969424f02d3ee9cb0dc6a8546f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:5adaf51783d68e286fe193e63e89f38604864a4a30493fe655bc2888ed8be1a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313844088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23cc9e90a83400a4177ec8eee5a0ba22a3a295460af172ca3be1e5746cf9e92`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:09:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Thu, 05 Feb 2026 22:09:47 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:09:47 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 22:09:47 GMT
ENV JAVA_VERSION=27-ea+7
# Thu, 05 Feb 2026 22:09:47 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 05 Feb 2026 22:09:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde458ea0ff4b78b30f5d919c75eb9e773aceb8420df617f9565a55227465343`  
		Last Modified: Thu, 05 Feb 2026 22:09:26 GMT  
		Size: 38.3 MB (38300090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76e0a0abc2f5db2a0e4e5bc0b20479d8cd2423de1e93600bb300ad100d16be8`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 228.2 MB (228236456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:be944cd582cdc1898e39370f29ea7f720f39184f31cb9f4a37bdcef4dce8b7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b93c4360ff5108ddae965d0b9afb8d64454be6b78a3cc45c1c3129deb32c1c6`

```dockerfile
```

-	Layers:
	-	`sha256:74d4daf4b198c470ee8e12e49b57b73617a8f71e217e50a561934126fdeeba01`  
		Last Modified: Thu, 05 Feb 2026 22:10:06 GMT  
		Size: 3.7 MB (3654783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a43e19c84391ecff9bb42239bf2bf42d7aa2b738a5775728e3ff228aa7f6c992`  
		Last Modified: Thu, 05 Feb 2026 22:10:06 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:33359e7303d23b342db1ef0c3d673e287eb2c70bc59b79fb625bb777fb2c5d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310771848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc0894d1442172795e9ba4fda26b90ade72eb30fbfa25ff5d34193e85c5ce70`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:11:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:11:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Thu, 05 Feb 2026 22:11:22 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:11:22 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 22:11:22 GMT
ENV JAVA_VERSION=27-ea+7
# Thu, 05 Feb 2026 22:11:22 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='951349bfcc6bf08d72f89175460216f0560a6c238848d93c2e194313a78b130e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/7/GPL/openjdk-27-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='3a3b7bac8a0432795430d519edf6eb790b6a3423b00516b74c85e1b7edb053a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 05 Feb 2026 22:11:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12d887e0953ccf6912de866e7547cbd62d244e4e1bbd6f225ba9fb8c0d1cbf6`  
		Last Modified: Thu, 05 Feb 2026 22:11:45 GMT  
		Size: 38.7 MB (38697201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0be2a87387b4c3d5edc2cc8db838fc0e4bf4feb6e6061c9f1e6b6d49771761`  
		Last Modified: Thu, 05 Feb 2026 22:11:48 GMT  
		Size: 226.2 MB (226171237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:e214f31541195b91b17264edb9f2abc63d2bfc0093543058828e97f2c9b5b088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094784ee71528a195b10a415b08eb777fa75f63939ddde242a88f11fbc3552cb`

```dockerfile
```

-	Layers:
	-	`sha256:ac0343545444848919b05c65b789d6e9904bc7977c639bcb3c1472ed562f4d14`  
		Last Modified: Thu, 05 Feb 2026 22:11:44 GMT  
		Size: 3.7 MB (3652473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39159dd9fc49b1ca77af28287663f21cdffa2706f06e5aaed257e77e8e189fd`  
		Last Modified: Thu, 05 Feb 2026 22:11:44 GMT  
		Size: 18.0 KB (18029 bytes)  
		MIME: application/vnd.in-toto+json
