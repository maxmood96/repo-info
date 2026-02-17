## `openjdk:26-rc-oracle`

```console
$ docker pull openjdk@sha256:be6cd47a6ec284a09039a5547d7b9457659a334126e402cb28be98331148fa9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:656499047d3c756bc09904cf10bc60d0891f1c18d05082365cf70639f14a0494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313544289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1509934edc1b5410a68aa47f9f7beed7b0d7bbc0c17c4a8d4f4b880c4f6641`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 19:29:41 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 17 Feb 2026 19:29:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 17 Feb 2026 19:29:52 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:29:52 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:29:52 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:29:52 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:29:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aadaff0bd8679a94fdd889e32963002f451e9b92197eb49e74fa0b6fed117bb`  
		Last Modified: Tue, 17 Feb 2026 19:30:15 GMT  
		Size: 38.3 MB (38300130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231effb416ddf83312bf693f2c2ed4f46b2a8d40117fd1cd9693920538f5dd46`  
		Last Modified: Tue, 17 Feb 2026 19:30:23 GMT  
		Size: 227.9 MB (227936617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f598101b21c45dec1fc4eced1858ee22bc8d8712d43ebfa78647fe0b7c5a1cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce826b4bc92698ea6a4ed721254bdad34bd7556be1d9f5cdc9b945e21df400e`

```dockerfile
```

-	Layers:
	-	`sha256:ad9193852402390f4e83843f25f622975201b759188de2ef1d2e8da857e261d0`  
		Last Modified: Tue, 17 Feb 2026 19:30:13 GMT  
		Size: 3.7 MB (3654107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabba63706616bd0b3e2fb36e9c54a1f14467ed2a2518bbe64adbf55d820206d`  
		Last Modified: Tue, 17 Feb 2026 19:30:13 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7364e253017867614dcc858d1527b4e8432f6586f2a05d07215dad8920afac4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310465123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177c81618daec62c7974966d7190e99f6bd41c336ceb82d2eccf949b608435b2`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 19:29:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 17 Feb 2026 19:30:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 17 Feb 2026 19:30:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:30:06 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:30:06 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:30:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:30:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0781907790c2447374c0228498ba64f12fe8a8aeca26dbb472cb16dd7516a831`  
		Last Modified: Tue, 17 Feb 2026 19:30:29 GMT  
		Size: 38.7 MB (38697476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429901d8524a4655c5da20d986d854d8634ba991c8078161c592efbafb74630`  
		Last Modified: Tue, 17 Feb 2026 19:30:32 GMT  
		Size: 225.9 MB (225864237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:38670785138524d5903fd5d7d739ddc459531af687ce3b94ef12c3d7e3421cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b142867dfe7703fbc7446595a980498db26de05f10e73949ac1c62ea75a257`

```dockerfile
```

-	Layers:
	-	`sha256:0a0035fcd25bf8efbe301d89a732643c1013364b6a317a56c35ed6140442c784`  
		Last Modified: Tue, 17 Feb 2026 19:30:27 GMT  
		Size: 3.7 MB (3651725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8a12063ddcf151e9c614620b5657b93a37a2b6b47063785e2bc5b8932378f1`  
		Last Modified: Tue, 17 Feb 2026 19:30:27 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json
