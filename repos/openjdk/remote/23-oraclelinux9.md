## `openjdk:23-oraclelinux9`

```console
$ docker pull openjdk@sha256:483540081788665ee833ca03f42a41d588321cf955446728c686dab5a23f77e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:81166b080281130d01efa5d2ff92de6107a9f1bfbaff7589caf9325fbc46d5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298166342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b5c08babb935a51206a44353a6f182743b003e0f4251d6d734b40354e578cb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
CMD ["/bin/bash"]
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a86f206f7a00e62de9fda8aa5c873810bdf3fb49c017978600da26ac89126d`  
		Last Modified: Mon, 08 Jul 2024 20:57:04 GMT  
		Size: 37.9 MB (37862476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916eba7076067fd0844063269e3932629f10182999f86e5f8180fe49d39d3bc2`  
		Last Modified: Mon, 08 Jul 2024 20:57:05 GMT  
		Size: 211.3 MB (211310213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:57e185970f744d9ef8cd2d39142f8bdc64c64e64a1cdbd6dddda30645032538a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2fd959798b364dd32dd14614743033d379116268eb20cc56d74bbb79d21446`

```dockerfile
```

-	Layers:
	-	`sha256:33a337f876300c7c0011fc0df22198511a29fe4974f7e6a6ba793390b5f5e08d`  
		Last Modified: Mon, 08 Jul 2024 20:57:03 GMT  
		Size: 3.3 MB (3333244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751ab99141f40653172bee29234f7dcefc40bcfbd078aea62f65be9a71d4a238`  
		Last Modified: Mon, 08 Jul 2024 20:57:03 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5f8c3c5ef4d975a320f8f33becded8313aa6560b3c12a87be557bb953d5603ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295090760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9a2d5c3c46646cd7e335582cfac8cdc8b784c76e8ebefd08f80af284c10a96`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 19:41:42 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Fri, 21 Jun 2024 19:41:43 GMT
CMD ["/bin/bash"]
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 06 Jul 2024 00:48:12 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Jul 2024 00:48:12 GMT
ENV LANG=C.UTF-8
# Sat, 06 Jul 2024 00:48:12 GMT
ENV JAVA_VERSION=23-ea+30
# Sat, 06 Jul 2024 00:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='847f053c0a1e23b388353fdfa7c43ebe7eae98f8221e43d561a0ad3a4c486681'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/30/GPL/openjdk-23-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef0255786108e95110839309fe5ed09fc730c0e3d78dd3d84d3f0f7e520a0d93'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 06 Jul 2024 00:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090038af1dc654e39101a0e5c1948e4487961717162abcaa289f614004326864`  
		Last Modified: Mon, 08 Jul 2024 20:57:10 GMT  
		Size: 38.3 MB (38256393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b2bfc9af6150ffee2cd8751ae806feb523844ce9cd5787805376f7f8dde125`  
		Last Modified: Mon, 08 Jul 2024 21:03:12 GMT  
		Size: 209.2 MB (209181601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f6c65f16a995004b95d4fe1b48ff503a8886614cb9a1f0719b458448ef7ab76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa2e5e51c7b5a5d7e9d54dd538ba3e2e61166524b0b4caa5e0b1f826fdf3308`

```dockerfile
```

-	Layers:
	-	`sha256:23447f2fe27a7ed2855a6b93cfd33dca62270374bf079a5b332deea6ca891047`  
		Last Modified: Mon, 08 Jul 2024 21:03:08 GMT  
		Size: 3.3 MB (3331627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccffa0d0f622e148b9c20647a63a29e0b2e3df7ef753225825c09076599118f3`  
		Last Modified: Mon, 08 Jul 2024 21:03:07 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json
