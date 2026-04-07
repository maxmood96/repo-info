## `openjdk:27-ea-oraclelinux10`

```console
$ docker pull openjdk@sha256:151cd384a4affd4761bf1e96591899b441e85f203d139c002bf424d5aed62751
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:3fd24a3628c9f11410908bade3481cedb4d4f834ff791cbab5166c3734a87c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309539871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eeb6291d69d56c3815374146a66a8d59077a8f7bcb074b8c9f708cb292c678`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Mon, 06 Apr 2026 18:24:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 06 Apr 2026 18:24:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 06 Apr 2026 18:24:40 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:24:40 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:24:40 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:24:40 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 06 Apr 2026 18:24:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1101a6a16bdd51aef6dda35e785dca1d7934d2937fdc0c8dfc0f002ced99f85a`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 43.1 MB (43068827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bad064764c9cdc9f064864f294e76ab15178c55145f51897ee66cc9a58111`  
		Last Modified: Mon, 06 Apr 2026 18:25:01 GMT  
		Size: 37.7 MB (37679171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac96a95ecb13c0123ebe6a94f0b7592bbc861fc6c5652a71e911b147fdee87d`  
		Last Modified: Mon, 06 Apr 2026 18:25:05 GMT  
		Size: 228.8 MB (228791873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:4e56747123c8003d1c5c3e7128f433a757a205cface8b813824ecbb6ce07e966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1059e6b0e357a06004d423d83c2cd695d2ff6c7494626533690b56dc8138c231`

```dockerfile
```

-	Layers:
	-	`sha256:3f7b6d823671076efd86874b8bf81ecc33d75101b8241c1099088246c6d7a4a3`  
		Last Modified: Mon, 06 Apr 2026 18:25:00 GMT  
		Size: 2.4 MB (2368347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6801b2e257ab885cb45ac11b3ef304a84afab23dbf50a074262d05be9e8d9687`  
		Last Modified: Mon, 06 Apr 2026 18:25:00 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1367fdbec048916da4316d05cb03e2041c6b9a15eb32dcb2b6018cc3c43cb3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305921504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f26de63ec08cb96d36e67a76ab20ad3d2d6f213deb91536c8d440194f8755d4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Mon, 06 Apr 2026 18:24:03 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 06 Apr 2026 18:24:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 06 Apr 2026 18:24:33 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2026 18:24:33 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:24:33 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:24:33 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='a9c8f46b87d1c973c4749728845de23d38a1897dc78b85e362f76ce98ca826eb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='cc96a894335065d7218341881222321567d1eca6950b3d6433fc387295d8d3b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 06 Apr 2026 18:24:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3db22c05661dd4dd65ed2c3add4946b3292ef86d7a62c06699ee25367fc2e1b`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 41.5 MB (41474500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169191e7a1b452ded0d6b5c4b4881bba8e3bae3cca641b8ec2114e4bd4d73035`  
		Last Modified: Mon, 06 Apr 2026 18:24:56 GMT  
		Size: 37.7 MB (37687605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2e7c0d3a615ae73ae254a6cc2272cab7f6cffd7bf90de7b69393ae67986489`  
		Last Modified: Mon, 06 Apr 2026 18:25:01 GMT  
		Size: 226.8 MB (226759399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:0e92a901ea2f92ebc102f75f9af8bbe4815fb86a70b63197e973c39263e8cd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8d5861d6b9a28db8cc8f049278c6c0aa31e463113cdf502403160f76927fd9`

```dockerfile
```

-	Layers:
	-	`sha256:015aac055b5b0f7438c987a86de22d4a81e78783147868f4fbfd29959b18fcdd`  
		Last Modified: Mon, 06 Apr 2026 18:24:55 GMT  
		Size: 2.4 MB (2367875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb6e5e807ab37a84a4cbb1caee9d349fcabc383a41d895f285a775b495cb7d0`  
		Last Modified: Mon, 06 Apr 2026 18:24:55 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
