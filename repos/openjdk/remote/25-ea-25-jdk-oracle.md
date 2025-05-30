## `openjdk:25-ea-25-jdk-oracle`

```console
$ docker pull openjdk@sha256:018ceb6f64e8d20a29bfd80ce1da9ad3aec8b7ddb1178ffcfa7f5554541c85fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-25-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:34436c0f3955a3b70a86b2c84d2d92de043fb584af93003ee9ebcce595012e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.8 MB (309812177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bde49acb181bd6ce9dd854a751d5701cf2d2bef43be64645b9daa772874d208`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:26:20 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:26:20 GMT
CMD ["/bin/bash"]
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c2eb5d06bfeaafd2195d3612935e86f925a4620bf5bbcea5112a1fb07138dd80`  
		Last Modified: Tue, 29 Apr 2025 18:16:07 GMT  
		Size: 49.1 MB (49093011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332db3d6af219572d154ecf31dafe2f75df70b18d4660969e62490a815a80727`  
		Last Modified: Fri, 30 May 2025 17:38:01 GMT  
		Size: 38.1 MB (38107856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657ad9545aa97cc2c517b69825adb8015003698663eba2563e1c0e4de3d9759`  
		Last Modified: Fri, 30 May 2025 17:38:03 GMT  
		Size: 222.6 MB (222611310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:0396cd101723ad9a7f41812e04fc4a0d344b178da4f9572ebbb4d8b902927965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3656980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc71e76092f20e8b79da21807b6888086766209f2e6fd747d3461dfa82dced34`

```dockerfile
```

-	Layers:
	-	`sha256:061564c16073ca43b7b802deafbad670a2345ecafceb746b498595fcd9954336`  
		Last Modified: Fri, 30 May 2025 17:37:58 GMT  
		Size: 3.6 MB (3637234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4823c756b4895a1ddef3295f669aac37d787874120c8b97d0efe93af176deee8`  
		Last Modified: Fri, 30 May 2025 17:37:58 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-25-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:973ea176735ef544a3ff3412035c19c21edfd904a55747b52682a19b3eb9eac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306579063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c281201bcdf685ed381efb8612af1721eb7ec1aa68c069e27f2640e6996f6c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Apr 2025 16:27:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 29 Apr 2025 16:27:11 GMT
CMD ["/bin/bash"]
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:88a33dc8906274baf54eb28aeefeba84c17922e3854e6fd41883f273d87d330d`  
		Last Modified: Wed, 30 Apr 2025 01:59:51 GMT  
		Size: 47.7 MB (47672989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e8f48247967a699fa218a455f1d13e36e0c3234a40dbaea0778d86531fb66b`  
		Last Modified: Fri, 30 May 2025 17:37:45 GMT  
		Size: 38.5 MB (38514187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e5516841f4a81cc502d79f568c4c0946518c903f220ccd4fd07442c0f3a3f6`  
		Last Modified: Fri, 30 May 2025 17:37:48 GMT  
		Size: 220.4 MB (220391887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-25-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:8392fc798e7959d9370487029037dd122a31c86fa3fc69b43741e84b2af3019e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3655029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9beec4666fcecdb9e4a721d5840ce37bc5297a81dd2c3c079f82cdc3222552d`

```dockerfile
```

-	Layers:
	-	`sha256:3e6b288daa7e1eee046a68fb5ae45183e1dc9bd9dfc3e7a8cd0ddb39aedae25f`  
		Last Modified: Fri, 30 May 2025 17:37:44 GMT  
		Size: 3.6 MB (3634996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a5700850aa2a2eef02bb0ba4c103e5f6b0462cc1b4fd503d797128b427e74ba`  
		Last Modified: Fri, 30 May 2025 17:37:43 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
