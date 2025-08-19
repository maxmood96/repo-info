## `openjdk:25-rc-oraclelinux9`

```console
$ docker pull openjdk@sha256:15e5a0bbf07cfd8047ee33bbd1ae418324bf8b7c55f14b7d33a554fc491ad2b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-rc-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:b86fa57dc930a686fb02b4abad846b4c3f2ad5bb4a17c5ca8877f5cf7471f28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310572770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b42c0e65bb14cbb625e7ec50ee6f162eea396a4f8ae6405c596749fd600dde7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:10aec8a104c7ecf055b7137fb34a3666fce4dff1b9f6d210fb88eaddd4c8c329`  
		Last Modified: Thu, 07 Aug 2025 23:49:00 GMT  
		Size: 49.5 MB (49497127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2e59f9a91047c70671f0111ff4bf1a5bc4d559bca5e6bb22f83d743c143e91`  
		Last Modified: Mon, 18 Aug 2025 18:17:03 GMT  
		Size: 38.0 MB (38007234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9c740b492dde7a71ed7871f62b7a797273c5db472e3a031651677d1535932b`  
		Last Modified: Mon, 18 Aug 2025 21:36:55 GMT  
		Size: 223.1 MB (223068409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:117d8f4c50ae141f011e25d0a2c302d2a80f8a0833ebc2ea3975a816962ea990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3657300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382a0c64549d3a6800f8592899ccd2dfdf3d3b07d8386ceef2f08d0f52e9e045`

```dockerfile
```

-	Layers:
	-	`sha256:f93e67094444e939131dd379e0906315a38cdf1ef8c4e6fe45cb9eee0b039270`  
		Last Modified: Mon, 18 Aug 2025 21:23:24 GMT  
		Size: 3.6 MB (3639418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6eb82463a28dad04207b481ff9b52f98cffe6ef69c25128cc52a71a5361ef0`  
		Last Modified: Mon, 18 Aug 2025 21:23:25 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-rc-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:19ecc23a61eb4621fd827f16ce51e58b070763dd4dcb008956557fbfc4a0b351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307365568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de0111f97136cf5d4806cdf238cfd94ddfb3d15227ce6ee1b0d6a43e1cfdc80`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 16 Aug 2025 00:48:25 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 00:48:25 GMT
ENV LANG=C.UTF-8
# Sat, 16 Aug 2025 00:48:25 GMT
ENV JAVA_VERSION=25
# Sat, 16 Aug 2025 00:48:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='59cdcaf255add4721de38eb411d4ecfe779356b61fb671aee63c7dec78054c2b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/36/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f4a8d27429458a529148f90ebafcd1ae9b1968fa323f9e5e40d579a5c8c0288f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 16 Aug 2025 00:48:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c27940f400cbdef01d301fb84d1331162f6c76466797e235ea774e439f357`  
		Last Modified: Mon, 18 Aug 2025 22:21:13 GMT  
		Size: 38.4 MB (38409969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bede8aa2cca3e1f421e557147221cd5d1046b7936655046e896c4e78da3efc5`  
		Last Modified: Tue, 19 Aug 2025 00:43:10 GMT  
		Size: 220.9 MB (220868688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-rc-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:f2f6e4737953e95be3f7c6cde84da34d76f08b72b5e4ac64da8a0fdf1efcc412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3655205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef23305da8e9590f8a18625a6d1b8fa20083b2e4c392c65a8fb933bc38143776`

```dockerfile
```

-	Layers:
	-	`sha256:14b21294e8f7591a34baefd9f65f0f808cee25537f56366efc1b0515b0bd050d`  
		Last Modified: Tue, 19 Aug 2025 00:23:33 GMT  
		Size: 3.6 MB (3637108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75783c8a72266fa3ca174dc6bc364236cd79be8cf773d164b28838dd5e354ce`  
		Last Modified: Tue, 19 Aug 2025 00:23:34 GMT  
		Size: 18.1 KB (18097 bytes)  
		MIME: application/vnd.in-toto+json
