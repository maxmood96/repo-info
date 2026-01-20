## `openjdk:26-ea-30-oraclelinux8`

```console
$ docker pull openjdk@sha256:4d221de4e1ed545f39d6d4e0f44f39f32254dc9191c507db2f66e90ea72dfe16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-30-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:c2a3fdb432344cc6fda6c677f4212264ab5241a8b88f941535b10443dd254533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294764917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18fe4f01e938e8d3cf119fc7ed8834768f56400755fc34caae4ed7bc91a2f22`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:45:16 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:45:16 GMT
CMD ["/bin/bash"]
# Sat, 17 Jan 2026 00:24:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 17 Jan 2026 00:24:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 17 Jan 2026 00:24:50 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Jan 2026 00:24:50 GMT
ENV LANG=C.UTF-8
# Sat, 17 Jan 2026 00:24:50 GMT
ENV JAVA_VERSION=26-ea+30
# Sat, 17 Jan 2026 00:24:50 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 17 Jan 2026 00:24:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9c709a374865394632aa738429a90691dd8d7699af8be91820b62e8c54881b2`  
		Last Modified: Fri, 16 Jan 2026 23:45:35 GMT  
		Size: 51.5 MB (51468262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c4c3858642e79e316b98eed5193253901074b37e741ca48d69dc72685c3faa`  
		Last Modified: Sat, 17 Jan 2026 00:25:10 GMT  
		Size: 15.0 MB (14993925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498543cf66f7f451fbc823e60897691d49f5810944e96aaaf9e2b1629a1a0f1b`  
		Last Modified: Sat, 17 Jan 2026 00:25:40 GMT  
		Size: 228.3 MB (228302730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f174b82e2c1579b77fd2f5eb8f942eb4ad6632723c1e3bb5f7f2b58b165bc786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d879e2508fa74bf8e7cac6d54e7e3f0a21705d8c7cea08f40eb035da68c7c8`

```dockerfile
```

-	Layers:
	-	`sha256:874b1bcb265d1fe26418d758d521bf7c0b107cba12355381eff0ab9fabfaeda9`  
		Last Modified: Sat, 17 Jan 2026 00:25:10 GMT  
		Size: 2.4 MB (2448684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddff297ca8a45a3f501cbd0658411e47158e62c5b1bb102a33b75527d6d379a4`  
		Last Modified: Sat, 17 Jan 2026 01:23:39 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-30-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c6b49cf56bdbce976ac56b442894cd619579949299c55827f4146972f6289c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292131125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302876fc22cd25828dafabc3b2f35bc633bbb92e7c623bc056e31c7068630f4e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Jan 2026 23:45:22 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 16 Jan 2026 23:45:22 GMT
CMD ["/bin/bash"]
# Sat, 17 Jan 2026 00:16:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 17 Jan 2026 00:16:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 17 Jan 2026 00:16:33 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Jan 2026 00:16:33 GMT
ENV LANG=C.UTF-8
# Sat, 17 Jan 2026 00:16:33 GMT
ENV JAVA_VERSION=26-ea+30
# Sat, 17 Jan 2026 00:16:33 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='300f7c67876f470e3ddacfd75be07c3c92812847b43933eb3600e258a9662e2d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/30/GPL/openjdk-26-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='466961f9222d91364dbc631bb8c76216dbecaf025464f0189b3acc96dd516a96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 17 Jan 2026 00:16:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d32cf4966caecd91a10183493338f37f77a209057fd98d8c3aff049ad44e3619`  
		Last Modified: Fri, 16 Jan 2026 23:45:44 GMT  
		Size: 50.2 MB (50200257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b7b5152fbad35c554d5dc5f7dd5b5a4d0aa3fc1219aa165aedbda8fe3ea869`  
		Last Modified: Sat, 17 Jan 2026 00:16:55 GMT  
		Size: 15.7 MB (15692698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326d4bc21b87843bf065a8e087f902de863fb75cc482f2927e3f399996963573`  
		Last Modified: Sat, 17 Jan 2026 00:17:13 GMT  
		Size: 226.2 MB (226238170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-30-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:e1c0a63f02ad9f138c1757de6e954f6a76abd1bf77edbea28de9960b4780f349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c6878b8b019b6946a72ee0498ed3c8af559cc5d361f4af73789d821e409aa2`

```dockerfile
```

-	Layers:
	-	`sha256:d3bedf0707932e68a4bbc94a5c7c553c717431c3b815153597c9fe03259f9b61`  
		Last Modified: Sat, 17 Jan 2026 00:16:54 GMT  
		Size: 2.4 MB (2447494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068f82c53feaaf6ba483f2fa22c469c10ee63a5cfb4d1d0fca34e598484b71ae`  
		Last Modified: Sat, 17 Jan 2026 01:23:44 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
