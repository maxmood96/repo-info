## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:f122ee0d37b324f530448a91296b57d66351ab79012dbdf43cf95c25bc602d9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:39e4f3deec66d13c1e72bf28ccd445447f516c36d20441ad9d37127f7ab768d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294719929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b652c6f9066526a5fafb4482d00e6775ccf56c61b5ffa10c7ae4ffc831540c6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Oct 2025 17:25:39 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 31 Oct 2025 17:25:39 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 22:39:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 24 Nov 2025 22:39:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 24 Nov 2025 22:39:30 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:30 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:39:30 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:39:30 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:39:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fff3d29c5b5b28d342ba8d967679d9f76705eab0cf1b9c1c2a8d43102cc524c8`  
		Last Modified: Fri, 31 Oct 2025 17:26:00 GMT  
		Size: 51.4 MB (51383677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a35646c3728060af3acb01d0340a4e8d2d5eb5b8151eff0566f3c51f6ab78f`  
		Last Modified: Mon, 24 Nov 2025 22:40:18 GMT  
		Size: 15.0 MB (15014443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c35ff78e64e6b5e84e78eaf273fe4ab74f272316c4c9aa4497334f9a90caa14`  
		Last Modified: Mon, 24 Nov 2025 22:45:59 GMT  
		Size: 228.3 MB (228321809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:72826c337019c50eb5dc846eaef4d633b0df2b6022e3d1dd1fe053ddb4b788aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7cc03ea73dfb18beaa82eb943fb3a503f405d2a24204e4a4b2e6804d6a47b3`

```dockerfile
```

-	Layers:
	-	`sha256:a6a138d6615075dda57fe3ee5ad29fc2a2243dd421de467d300f32a6db54a566`  
		Last Modified: Tue, 25 Nov 2025 01:23:58 GMT  
		Size: 2.4 MB (2448013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f13c7ddbff9525097ba8873ea5a6e2995711ffcf1e5e589c82a8c9de089d96`  
		Last Modified: Tue, 25 Nov 2025 01:23:59 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6f4f92d124a7b6cf8d9a52d7af676b56b913461754f9ab3a1797be3293342de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291960384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca4c2cbf991397fa7ccd13352b5f7c66a6bcdcae1dbcbd6e4d4f1523c2c4f2e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Oct 2025 17:25:14 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 31 Oct 2025 17:25:14 GMT
CMD ["/bin/bash"]
# Mon, 24 Nov 2025 22:39:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 24 Nov 2025 22:39:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 24 Nov 2025 22:39:58 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 22:39:58 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 22:39:58 GMT
ENV JAVA_VERSION=26-ea+25
# Mon, 24 Nov 2025 22:39:58 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='34a09a42f38d04f223c2c3c3665e4638bcda263c69c38e8e363760be8ceeaffd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/25/GPL/openjdk-26-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='33e9133fcee05a36df65b43ceea8dd2c16ff6fe9c0186acd0a697547c2bd7a42'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 24 Nov 2025 22:39:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:913708617406390e2c3446d7f989f45259d9e8bc8c18aeb2c7030c867ecfb5d6`  
		Last Modified: Fri, 31 Oct 2025 17:25:36 GMT  
		Size: 50.1 MB (50102610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4c6adefab00ee0c9dce9ff2c9706f169a2641a4f81199a976b868a87ed262a`  
		Last Modified: Mon, 24 Nov 2025 22:40:40 GMT  
		Size: 15.7 MB (15685880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562ffd73a9d557f9264efbadf80d0d2c9e76a01cfd00bb2ca9bd74a83e4ad30`  
		Last Modified: Mon, 24 Nov 2025 22:40:24 GMT  
		Size: 226.2 MB (226171894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:139d7781fa6c8fe990f8e483a3a3146e6618d4e2e07363150b2fe47ac63bd404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90be85296f9b9d28eb2dc04fb3fa936d6a4221663293db99aad82af72168858`

```dockerfile
```

-	Layers:
	-	`sha256:1e3f81e32275f11461e88572a083d5803c32397868bcaf9674c17a0b0ca3ecff`  
		Last Modified: Tue, 25 Nov 2025 01:24:03 GMT  
		Size: 2.4 MB (2446823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b523e074b8d43d7c0fbb9d8b83b3ee27600d757c3f47884171d987dd28faab`  
		Last Modified: Tue, 25 Nov 2025 01:24:03 GMT  
		Size: 15.5 KB (15460 bytes)  
		MIME: application/vnd.in-toto+json
