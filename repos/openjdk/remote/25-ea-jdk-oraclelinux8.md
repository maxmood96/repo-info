## `openjdk:25-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:3994ce1c5e0da51e8c6f69de9704235b73ce00aea91a432be547f02ba2c59cd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3e7174a463ada1c59dfe0a51b82ecb452d4c2523e64a2ad91f100ad4430c93a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279634695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35e5bf0b6c39c030811a58007855bfd3b2306eb9c717816d311a9aea65f2af8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:58:17 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:58:17 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 03 Jan 2025 19:53:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:53:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_VERSION=25-ea+4
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='57eb4b2610608286fb271949bd4f1acb9ce6d550325d0797f445c1bd0587de50'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='2ebebc0344b40c03cd47ecd8936fe2aee3f0624e5e2463340054d7174b3f4e1d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54e52ba1e1af00a6cb64b854c133cad87f069ebce22ab349a764375631164be`  
		Last Modified: Fri, 15 Nov 2024 23:04:32 GMT  
		Size: 51.3 MB (51274992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b16633a256f6563f85b46f0972b1c9a0df1b667c612642dcc6eb301378ba12`  
		Last Modified: Mon, 06 Jan 2025 20:28:20 GMT  
		Size: 15.0 MB (14975014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc586caba9fde18599104b9974807e221425dcc74db87e19a3b668905ac0f30`  
		Last Modified: Mon, 06 Jan 2025 20:28:23 GMT  
		Size: 213.4 MB (213384689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:80871f6fdfdf33d881b717e43f4218fcd5b9105653fe3b4b77bc7021a070f306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f8ad3cbcca0a831690c9f0bf9ef1f8894f6900e87de4cfd2ec703faa0de24b`

```dockerfile
```

-	Layers:
	-	`sha256:524727c4757cfae370b407260ec725e9c5e9f33ee9b8a57be1cc805783b635b4`  
		Last Modified: Mon, 06 Jan 2025 20:28:20 GMT  
		Size: 2.4 MB (2441577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43eb9d0984ec3b6b202d97074e146b26d692b05980088c4d3b29d70b180d8d4b`  
		Last Modified: Mon, 06 Jan 2025 20:28:20 GMT  
		Size: 16.0 KB (16020 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c52014873b22f67fa7d0452ab6dc10e96d6cc93757e3cf1d0803be6b5cb8b5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (276980626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0c23d725728e169b069875896875ea86d2a9cad769de1242cc58b6d57f9a2b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Nov 2024 20:59:08 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 15 Nov 2024 20:59:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 03 Jan 2025 19:53:11 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Jan 2025 19:53:11 GMT
ENV LANG=C.UTF-8
# Fri, 03 Jan 2025 19:53:11 GMT
ENV JAVA_VERSION=25-ea+4
# Fri, 03 Jan 2025 19:53:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='57eb4b2610608286fb271949bd4f1acb9ce6d550325d0797f445c1bd0587de50'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='2ebebc0344b40c03cd47ecd8936fe2aee3f0624e5e2463340054d7174b3f4e1d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 03 Jan 2025 19:53:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7288e96bcae8e1d96f887149d393459a95cb964c7336b7fa79a18d30b08622ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:54 GMT  
		Size: 50.0 MB (49980275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69acd795388d1f1fedcb65b1fe1cb71800f56a9beccbb0acf86fbdad421cc605`  
		Last Modified: Tue, 10 Dec 2024 01:27:38 GMT  
		Size: 15.7 MB (15659937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e709cfbd9263fae4e032bf1e5109b54db508e2ab7d22ff01f1dee58003652`  
		Last Modified: Mon, 06 Jan 2025 20:29:15 GMT  
		Size: 211.3 MB (211340414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce11f340902ffd44739de11a02b03d88a50fbd05b50d6b2802b4ebb54a300461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b137d33d4ceb6f7989a830dec0e0731b7fa9f0e9a602657884087d813d13f4`

```dockerfile
```

-	Layers:
	-	`sha256:51d9eeae0f84b7c068c5b4f0b0480045db5751a60f76d6231bd4715bccd3b91a`  
		Size: 2.4 MB (2440423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26827251be40cf105528bc7ec81e257f7cbf62b0e22afa4d3b1b13343772fb2d`  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
