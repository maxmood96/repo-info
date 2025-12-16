## `openjdk:26-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:d2fcab0c7ea093ed6543aca991286b92d09ec4da2e6eac99556e2816145c9a6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c617c09fadf51eb7ecb820637ae8d07cb33643c3d3ebc54ae8013205dbbac1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294659399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9109b2efac5b67f90a550fd21deb4289e2d963e01237bab74e9ce5bdba50ccc9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:50:37 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:04:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:04:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 16 Dec 2025 00:04:27 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:04:27 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:04:27 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:04:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:04:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b436d89f13c92f9703618820d992b4e1f2b38ba243024b251c81a610f04c67b1`  
		Last Modified: Tue, 25 Nov 2025 23:51:01 GMT  
		Size: 51.4 MB (51378078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30407d526b5338c7315f9d44f3231892815b046f75924cc8898df7a1f8b672a3`  
		Last Modified: Tue, 16 Dec 2025 00:05:05 GMT  
		Size: 15.0 MB (14999287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2485a3cd99009d16f677cbb75e16bf6c8f993aa3422373314a2f5191067e16a9`  
		Last Modified: Tue, 16 Dec 2025 00:06:59 GMT  
		Size: 228.3 MB (228282034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2c279e6c018545e878bf53facb1f5db40f6c2fa5f18be78a10cd38451a599fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69a31ac4b7bd990b937ffebc567766d98406b3de71f29f55b79cc828016276f`

```dockerfile
```

-	Layers:
	-	`sha256:79e3e8432c79d94db1b156ae3cf709aba30e54dd8b23df3304830a7fb66865f0`  
		Last Modified: Tue, 16 Dec 2025 01:23:54 GMT  
		Size: 2.4 MB (2448013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2efa86ae0f77453640d146c02a782bcab5b5a178d1912a15885791695a1bb5`  
		Last Modified: Tue, 16 Dec 2025 01:23:55 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3824c3894cd07139eac92c835b58ec7ba9c214dd2eb5be9e15682525d6f296b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292006037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb7429136110af3b416873135cb02dc3cf81fda0f2a08537a05d0f86b7b0740`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Nov 2025 23:37:54 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 25 Nov 2025 23:37:54 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:02:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:03:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 16 Dec 2025 00:03:24 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:03:24 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:03:24 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:03:24 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:03:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:674388ef21c06396c4d40407ba2af1c3a42c30a5cb162fd4355950be7600edf7`  
		Last Modified: Tue, 25 Nov 2025 23:38:20 GMT  
		Size: 50.1 MB (50103076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96bfe97b4f46ce365dce6920d82e8ecb468b22d723c7738391f639b1ac7ff5a`  
		Last Modified: Tue, 16 Dec 2025 00:03:59 GMT  
		Size: 15.7 MB (15691654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551d6e604ee733229926a6727201403ee34ff7f4cfe06b05fef8387855d9c754`  
		Last Modified: Tue, 16 Dec 2025 00:04:07 GMT  
		Size: 226.2 MB (226211307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:de770ee9e5eec0863476d4639769d2d8d1ad3579715655629def04347a02eb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d9f398c9b68a1bff3ff2771bc556da30463fb893fa6e35494b7260ddb30117`

```dockerfile
```

-	Layers:
	-	`sha256:63815f0805e21a80fc89c62d0053dff0a3c1bc438a44d2265f48e32a1aa23851`  
		Last Modified: Tue, 16 Dec 2025 01:23:59 GMT  
		Size: 2.4 MB (2446823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7419f5bc38d9d40ed85992ac1a0570e3721c29510eca0577d0edd1ed68994e1e`  
		Last Modified: Tue, 16 Dec 2025 01:24:02 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
