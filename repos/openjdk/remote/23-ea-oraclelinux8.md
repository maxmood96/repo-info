## `openjdk:23-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:a7c87763283542ea0d8ebc42bb70ae726f93eb9cfa7f103985b46a7690701a18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:faa15863182a402131d230d443c2b3ffc6d71ec086284188debe9965012ad73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277889035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ceaa1044103ea5393cb0afcd996551eba29ff4959e1d5b3caad1f8de5b55dd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2024 00:48:11 GMT
ADD file:8f1e63c197fd50c6b0e1841be870ed49e0149654eb523d4ceebf9dbd1c9eaa92 in / 
# Fri, 31 May 2024 00:48:11 GMT
CMD ["/bin/bash"]
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 31 May 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+25
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='155a1386301d0ac6cd1ce5769b31f550bb400d652f4211454b9988bf25fa173d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b00cd1591ad9727c48c07e598f57cdec15fa40b605ae712b67f35f221534d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7739e1b0a17a1112aae4b01fa39d979aa72dfa002be5059a8488942f3c2753fe`  
		Last Modified: Sat, 01 Jun 2024 00:50:45 GMT  
		Size: 51.2 MB (51220385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bcf9f4fc6bbe9faec110af0dfc8c13b10385102559a7aa73d0b7a66f2558f6`  
		Last Modified: Mon, 03 Jun 2024 19:01:25 GMT  
		Size: 15.0 MB (15031168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02622f7176ac4bc74c8f86d59b9ee3cf31226f152fede1ec41a94be7d83f787`  
		Last Modified: Mon, 03 Jun 2024 19:01:29 GMT  
		Size: 211.6 MB (211637482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:af08d940e70651a100c6b1be7d4b8e4de31c1a91859ab2cb0ff78acbf93bab9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7252ba372a3544d31c2baa7b0ed2fccdd2ff32bec4eb4967ee46e34cf3ff94a`

```dockerfile
```

-	Layers:
	-	`sha256:ad8faaada980f728328b22ef3dce9166771f6e08eb5277dcb73e3a83e4e7f4e0`  
		Last Modified: Mon, 03 Jun 2024 19:01:25 GMT  
		Size: 2.3 MB (2267552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20974d7b067bdffc238403cf32560342af192fe876b69c31deacf8d780a9825`  
		Last Modified: Mon, 03 Jun 2024 19:01:24 GMT  
		Size: 15.8 KB (15771 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3e794b519f7dd301c534a6075fe0433e3c4fe0ef4e15a66d1388558c8c23be7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274447939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68260f245dc175a16a8be0a6e3bc214e886985fcc9507cf61492a155b1c7a38c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 May 2024 17:23:46 GMT
ADD file:642db2e4816164ecc2aca9ff0beff49e4f7f14d45baeaf3e47206248573386c2 in / 
# Wed, 29 May 2024 17:23:46 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 29 May 2024 17:23:46 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 May 2024 17:23:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 May 2024 17:23:46 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 17:23:46 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eebed7702933983781b97d468d8772f419c150d1c7354f82f15dd07d79be2b17'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ff14d6b86a66b88540ffd39b93e2e1ce8a529048d0ffbd3a5ff5b5dd14f8345'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 29 May 2024 17:23:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7a9efb140c071370d538de519ecc7162c4519d69442bd0526104d3f7037ab2d`  
		Last Modified: Sat, 01 Jun 2024 01:50:04 GMT  
		Size: 49.9 MB (49926364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128cbcef85b143dda183d4e8b2a8fe5e9782a59a0055650bbc4c7bf6c8cab3a4`  
		Last Modified: Sun, 02 Jun 2024 02:35:09 GMT  
		Size: 15.7 MB (15689465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1342b030a7d03b98d9440fe62103991f0418e61aee350134bda816b445665448`  
		Last Modified: Sun, 02 Jun 2024 02:35:13 GMT  
		Size: 208.8 MB (208832110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:dbd3ec65cbbe22bebfb2a8065c31804405696a3ae43249577b6738de6e79c85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f7c88e17d9244da6dcb898e2eddefc9556cc4af145b2414f0fc62940c3f412`

```dockerfile
```

-	Layers:
	-	`sha256:fb2dbdb00fa8df4e60c3e98edf200668e6098c54254cef93cffcdabc988a4307`  
		Last Modified: Sun, 02 Jun 2024 02:35:08 GMT  
		Size: 2.3 MB (2267021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d6c5b910ef77be41612af85cc3e7b59dbcea28d8a61ba584d91e237f60a17b`  
		Last Modified: Sun, 02 Jun 2024 02:35:08 GMT  
		Size: 16.1 KB (16102 bytes)  
		MIME: application/vnd.in-toto+json
