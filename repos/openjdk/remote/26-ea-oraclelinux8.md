## `openjdk:26-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:b936df7e286cf762673884dd2db614dde2da957916dce74207dd6ebc1908734b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f061473f00d0faaa5052d42598c06b6eb3f5498b4919c3159ea074710b167566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292358058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28be536daae4954bc92768271b117b52bb95148a928b6916dbb78e7dc11e7914`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4212291b90fc5c5901a38f76149211cb65ca31f3aa0e41bcafa0ad8f10ea95`  
		Last Modified: Fri, 26 Sep 2025 22:14:57 GMT  
		Size: 15.0 MB (14979214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1888026aa026f3ce6d1456201dc4c9a9445ea7259f917797fd8cfd8ea3907fc`  
		Last Modified: Fri, 26 Sep 2025 22:48:33 GMT  
		Size: 226.1 MB (226055281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6466103f451eaae9ec6f69dd0147eea17309e4f8d5a80c6a8a80fbccf69e03d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8422051bf80f1d9ad669133082f4388ac1aa330e4e6924def25770b2fb7cec27`

```dockerfile
```

-	Layers:
	-	`sha256:dd870ce3566837f679fce62de8f4c11e9776ea3e6c259fdc7851bd1499c87d93`  
		Last Modified: Sat, 27 Sep 2025 00:24:06 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5714c1c18e417a768c3accfa76afe730038024a245a20e8e82a2e9227aa37337`  
		Last Modified: Sat, 27 Sep 2025 00:24:06 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a686689bb59a0c6c0283b6ae6e3595bc89a738057dc7adc894ccefc50d2426f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289662728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac92170d2b40f4ca051f13d2b2962b0f13c9438fd91ab123271f7080a3bdf6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 26 Sep 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 26 Sep 2025 18:48:12 GMT
ENV JAVA_VERSION=26-ea+17
# Fri, 26 Sep 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='0a80f3aa3279fbcd36b9247a873bc99b3688ce092a970c08ff3788e2fac99351'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/17/GPL/openjdk-26-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='d12fc689cf8b2e7c1b503472b988320ad15693d9b40c3e877e9f78aae6fb82a1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Sep 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9866c68be293aa81b529074549b7f38395dba71a8ea8fc528f721fbf8543b957`  
		Last Modified: Thu, 21 Aug 2025 18:57:24 GMT  
		Size: 50.0 MB (50039817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6dc0c16a57d02dd2a67b86f7f05362336ae71d80b2c470d5a332c9c9f84cca`  
		Last Modified: Fri, 26 Sep 2025 22:14:28 GMT  
		Size: 15.7 MB (15672231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabdf7bfec64874c5fdf8ca373b47cb91215780a6a26d244d3f5de24ec1f051e`  
		Last Modified: Fri, 26 Sep 2025 22:48:33 GMT  
		Size: 224.0 MB (223950680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:b3a5bfa7d70b74896996fc7437b0768aef3125f328306b91588da84e69fcd486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14d26c421a742dc0e5987c43c727eb90c605628ec68450e9ad386b310753486`

```dockerfile
```

-	Layers:
	-	`sha256:f60e44de6a873e7ce12a08449ea20814fc11bcba9c0d7a49f00c640d7073e0ae`  
		Last Modified: Sat, 27 Sep 2025 00:24:10 GMT  
		Size: 2.4 MB (2449933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a9a68175728df90ca8ea839ac307d67dc135b264aa613fe9596e9b2c929651`  
		Last Modified: Sat, 27 Sep 2025 00:24:11 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
