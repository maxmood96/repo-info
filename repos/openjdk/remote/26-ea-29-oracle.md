## `openjdk:26-ea-29-oracle`

```console
$ docker pull openjdk@sha256:cf84f54a25b256161e54b2da64aafec35784644194c668c3dab7fd96bac7401c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-29-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ec817182d88891f4888f52c818adb868718fb78f232b4d1847973d731f191a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313456906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2121636efb65ec05ff3b191e92abff06ed08849364bcdc9c38954ada384afdf3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:14 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:14 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:35:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:35:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 06 Jan 2026 18:35:22 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jan 2026 18:35:22 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jan 2026 18:35:22 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 06 Jan 2026 18:35:22 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 06 Jan 2026 18:35:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad9d782f3f8782ebff0dd18c48de1ae7dd7e8c7e8b207aee14fd087419cb908f`  
		Last Modified: Tue, 06 Jan 2026 18:24:34 GMT  
		Size: 47.3 MB (47316998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f478cabd179ee9c3f374b09308ea539ea7540a650875f424b90fa9279d17de`  
		Last Modified: Tue, 06 Jan 2026 18:35:57 GMT  
		Size: 38.3 MB (38299116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ca962c31b536de15bf845849d4e726a5aa224bdcd40988749fc8f0e4ce023d`  
		Last Modified: Tue, 06 Jan 2026 18:36:21 GMT  
		Size: 227.8 MB (227840792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f43ecf7edb3741ef6b3d5665eb9b9bf0648bf28a04ae69ab8f9fd83142adf935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe64027f5be37c6c41fbdd8605205695a4af3781dadea2073507d8949c9ac824`

```dockerfile
```

-	Layers:
	-	`sha256:3c36979be061bebaca0b8348ef25bbe47ecc6e243e7b853eb31cf227dbd65766`  
		Last Modified: Tue, 06 Jan 2026 19:23:21 GMT  
		Size: 3.7 MB (3655359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f8ef9920afc8def9792888594bfd0fa03ee3111eccc6decdf84167da39b686`  
		Last Modified: Tue, 06 Jan 2026 19:23:22 GMT  
		Size: 17.8 KB (17837 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-29-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3ac6b52a006c85aaffc08650af5037cf29faf50ccf56012681454250a0ba39a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310355013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20abeb2b456d9547f5a0cc749fab80bc10d776abf7026fd5c1c69cedae96a1b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 06 Jan 2026 18:24:32 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 06 Jan 2026 18:24:32 GMT
CMD ["/bin/bash"]
# Tue, 06 Jan 2026 18:36:23 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 06 Jan 2026 18:36:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 06 Jan 2026 18:36:34 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jan 2026 18:36:34 GMT
ENV LANG=C.UTF-8
# Tue, 06 Jan 2026 18:36:34 GMT
ENV JAVA_VERSION=26-ea+29
# Tue, 06 Jan 2026 18:36:34 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='14b38c0378b8fccf20824a10aed0193c3e5c9732c7933f4e14b1409027db9d5a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/29/GPL/openjdk-26-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='fbf83d509c5cbc2ca19ae7e7456d277a469c94290129cb4230cfbcea05ea7edf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 06 Jan 2026 18:36:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e1814e660b35a8d0d1c9103cf854824718c8d9101e743cca376efd3f99eb9a1`  
		Last Modified: Tue, 06 Jan 2026 18:24:56 GMT  
		Size: 45.9 MB (45905540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad49e81cfb3b889a04f17aba69149004b4c29c1ed0ac0899c44b21e6029a24b7`  
		Last Modified: Tue, 06 Jan 2026 18:37:23 GMT  
		Size: 38.7 MB (38700393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e0887ff0c2790fc423fb3e4b2bcfea093ed5247bff37bfb6f02137db72f0cf`  
		Last Modified: Tue, 06 Jan 2026 18:37:21 GMT  
		Size: 225.7 MB (225749080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-29-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:de4edb94af6990d368c52b4a440c2c5565bd3c235c095e6537a8f879898fd81d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acae86c3806d96ee598bbd2c28e595bebe0c499f7f2d378ebb7324647b087b25`

```dockerfile
```

-	Layers:
	-	`sha256:6246655eb5ba94d074c3e5841ba6c67d99ff2941a150d3c801d5c54f5b5bba23`  
		Last Modified: Tue, 06 Jan 2026 19:23:26 GMT  
		Size: 3.7 MB (3653049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c0527cdf2d4b7e0eae3fc43cc47208df014147c2c167189f9957914590a14a`  
		Last Modified: Tue, 06 Jan 2026 19:23:27 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
