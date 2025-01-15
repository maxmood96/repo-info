## `openjdk:25-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:d6d91185dee240a5fdd7552376f8ab2714693eda0c15608f7feed601687fbbc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:e6f395ce10c93e4049a31da085cb34ce5f08f9f775e41f94c38f21a05a2bb121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279624689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f3dade6f4a512855ea2b6962633e3cd51c8a7c4c2c241f8074d39a50dade8f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 13 Dec 2024 17:23:13 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f759775a99d9a0c777b45e12f57efd8d8286f11cc7819b377dc2aed74d4a5`  
		Last Modified: Wed, 15 Jan 2025 04:30:58 GMT  
		Size: 15.0 MB (14975078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cb679bb0671daa57cb688f6b7e2813a8f284aae5a3aa0a3ff8775205349823`  
		Last Modified: Wed, 15 Jan 2025 04:31:10 GMT  
		Size: 213.4 MB (213374619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:56117746aae5f733358e1a522094befa5e97f8dd0db3d0b896bd3c4f0be026f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856b445a4c49ff2f209066f6880dddcd2f314665295f480e89cd41e704b8e7b1`

```dockerfile
```

-	Layers:
	-	`sha256:571331db2934ae17b502299d3fd815d69265811cc652535b58bb6fe5a808b04e`  
		Last Modified: Sat, 11 Jan 2025 02:30:02 GMT  
		Size: 2.4 MB (2441577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a5b3d24dea4254a6fe407c22d205476f2b5f940b744ca6afeca772af0da00d`  
		Last Modified: Sat, 11 Jan 2025 02:30:02 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ddae43cda1f3dc70da7b0dcbacb9d9f437c75d79d6c7b027cd8b1ad87339cb58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (276991047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261156a8e332e39aa658a617de753e5ab54598fbbd6fc2f0f8af6fdb126df7c4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 10 Jan 2025 07:52:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Jan 2025 07:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 10 Jan 2025 07:52:09 GMT
ENV JAVA_VERSION=25-ea+5
# Fri, 10 Jan 2025 07:52:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b4ee63f91536c06f46e6f0d9c45e820bc2cb552046df27aa5c77d0bacc35aa21'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/5/GPL/openjdk-25-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='43d1f9c863580d839b21121bc0c09ef0525d80ce1a3fbe26ea22fe2d77eadf7a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 10 Jan 2025 07:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Sat, 14 Dec 2024 02:10:44 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944cd63dffddb127d99cc2a7ba13ba2ac1f47dbc72b57d4efb7ec8ed046aa53c`  
		Last Modified: Sat, 11 Jan 2025 03:21:57 GMT  
		Size: 15.7 MB (15660035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93639f2a3270920450015831c08fc9cd8a07d99f0036374f96c0518c7def54b`  
		Last Modified: Sat, 11 Jan 2025 03:43:02 GMT  
		Size: 211.4 MB (211350737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:f9d2f41ac968250687d5ae4fcd10973ef0e6b31add674ce32806449e57bb2568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c490cfb3c993fae5654cc6f572ee407b9118bd4f55e31766fbd41dfb3423533`

```dockerfile
```

-	Layers:
	-	`sha256:82d716cab5f1484d71db2cd641ec4e16082aa2ad71b04ca05e90e342be9d14be`  
		Last Modified: Sat, 11 Jan 2025 03:42:57 GMT  
		Size: 2.4 MB (2440423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5438f7ef30d4a92abd68c70944c82953e025efef8a8c03359d6515f0a9ce4116`  
		Last Modified: Sat, 11 Jan 2025 03:42:57 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
