## `openjdk:27-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:e4da96c22d9aa1c8f0731a4e73e36f1e5e60907071396507f0e5488fde7586f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:8ff9fa0e1726cd1d3e08b8a9ea43d7966d541312be28e34971fa40d460402eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.5 MB (312524642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099412c556c37ed2f52426ac6c18dcf5219d86673974c0c594e686f63a469ef3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 20:06:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 09 Jun 2026 20:06:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 09 Jun 2026 20:06:17 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:06:17 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:06:17 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:06:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:06:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724f880358fbd6876d0f4f763b5d50145d681a65d192ec1342a95e85df0f1840`  
		Last Modified: Tue, 09 Jun 2026 20:06:42 GMT  
		Size: 38.3 MB (38267904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a9cfb5b0d110f819a474b95cdf1052e51a59125ca84368699edd831dc5f9e4`  
		Last Modified: Tue, 09 Jun 2026 20:06:45 GMT  
		Size: 226.9 MB (226947165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:ab73b7061d29337a05c8d516f09d6bafeba60095e096079c52a1fed46256a429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8faa2eed1b6f45f1447b0336f2c724cdd4ecb16b784d95a3ed03d42b9ac1b421`

```dockerfile
```

-	Layers:
	-	`sha256:9774d39f9f1cf5e2dbbfaa53a8ff921f077d5b56d66ab0569108692df8e13cca`  
		Last Modified: Tue, 09 Jun 2026 20:06:40 GMT  
		Size: 3.7 MB (3650422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96d568122c1f8d01ecae496b73366f235371cd8a8a8b74b30cb47c95725f4090`  
		Last Modified: Tue, 09 Jun 2026 20:06:39 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:827619bd8d5588d72c7e1e2a5d6935bafb5e2bbfd3ad457e0ea5410e3f66885d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309497250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c39834c27403c8039177fd538071b97dbea22d948df786b646aee31dd51b4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 20:05:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 09 Jun 2026 20:06:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 09 Jun 2026 20:06:08 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 20:06:08 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 20:06:08 GMT
ENV JAVA_VERSION=27-ea+25
# Tue, 09 Jun 2026 20:06:08 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='6287dc1b8b810fc6fb0ecf2ff0f15464e7bbd5b44c45008588224072bbfbaa87'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/25/GPL/openjdk-27-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='6f13903699316f8ee6089a0551ef28686b3bae5b195a98cc4051b365819396cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 09 Jun 2026 20:06:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db2ff6bd976f21cbde31d3da0a14b1f025f9e0f292f5b4aedaa868e0f75938b`  
		Last Modified: Tue, 09 Jun 2026 20:06:31 GMT  
		Size: 38.7 MB (38665537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e0495a5b6e3e0e3c1e6d2aa07932d7f11703a58bc04d62bbac66482a6e782`  
		Last Modified: Tue, 09 Jun 2026 20:06:41 GMT  
		Size: 224.9 MB (224932623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:6fcffcc41a80f2e51ab3f3489adcb1146db36fb3f7916b19ac5b4b3ecd3b1eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178a667786f17664fbac4dc2f5d510cda6a7d3317d6e803bec18d65dfe5856d1`

```dockerfile
```

-	Layers:
	-	`sha256:cf5016c243496ddef166093933be2895948fceab5fb71ae2bfe76bdadcdd3fd5`  
		Last Modified: Tue, 09 Jun 2026 20:06:29 GMT  
		Size: 3.6 MB (3648016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0ebbf17a9cdd0334c998cecb7284deace07d935adebcb9d431249b75fb14d4`  
		Last Modified: Tue, 09 Jun 2026 20:06:29 GMT  
		Size: 15.5 KB (15461 bytes)  
		MIME: application/vnd.in-toto+json
