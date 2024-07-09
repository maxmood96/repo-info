## `openjdk:23-ea-30-oracle`

```console
$ docker pull openjdk@sha256:65ec214d49e61ce2150700c64b1d9dfd210d9586a1e5026b5c1e4cc13cb18efc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-30-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:ea89a291c463c32f8180283157cc04cc468d45e5c2cfe3b3cebe27c146bc91cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298166532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2063cb0321e5ae7370182de25fd9d90580167ae79a1718b0891165d20d4116e0`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jul 2024 00:48:12 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Sat, 06 Jul 2024 00:48:12 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ccc2989fe366baef9d1e013e9965b0fe5690be534061b75cb402c1f2d43bab`  
		Last Modified: Mon, 08 Jul 2024 23:57:36 GMT  
		Size: 37.9 MB (37862673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1547d05e2545e89063d5d8b0aeaf307ab01832f82443016aa201cd73275d00c`  
		Last Modified: Mon, 08 Jul 2024 23:57:39 GMT  
		Size: 211.3 MB (211310123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-30-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:6266586cf9fea04f22e73c1a05e79790a559f7d3c1918665e543de546d645974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca00eaf87d53e19d611004102f4aef9a2f65b0780b275c0b63a6b2b9ee25012e`

```dockerfile
```

-	Layers:
	-	`sha256:8b710254bb4db33acb71590821574654bb89e9a6a6dbf38e97b35cdde7f8f8b6`  
		Last Modified: Mon, 08 Jul 2024 23:57:35 GMT  
		Size: 3.3 MB (3333244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241dbd7a6c499e01088878d35d5041336bc13ee27c492baabbc02b86ec624115`  
		Last Modified: Mon, 08 Jul 2024 23:57:34 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-30-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e269ce572408a82070db8ac612f884d8b0f7032177bd019122c9d3b4706ab705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295090688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306ffde352b0df13368e9b6caeb03acea4dbe142c8a4827f72ed5bdf54a9b428`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 06 Jul 2024 00:48:12 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Sat, 06 Jul 2024 00:48:12 GMT
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
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e0ae27700e3c3cc1e9befcc8c7351e618434dd681f418b3d8c7321b50b530`  
		Last Modified: Tue, 09 Jul 2024 00:01:40 GMT  
		Size: 38.3 MB (38256416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc96c93cd91173673cf2f2e2325036a33a3d02345bf1f6c6ef663e6589da4f`  
		Last Modified: Tue, 09 Jul 2024 00:02:32 GMT  
		Size: 209.2 MB (209181611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-30-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:2b2c65fa10b7b0717c20a050c5223a0d04c35880dad1400fae9f7b0cf2d705f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c258348a933b5021fb720a1376f8b568f83bfabffb7de3513f8321632197f864`

```dockerfile
```

-	Layers:
	-	`sha256:70af054e49a03770cd4125cb7d2faa14b4da4e9725adced8d48ac6163bf0b3ca`  
		Last Modified: Tue, 09 Jul 2024 00:02:27 GMT  
		Size: 3.3 MB (3331627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f0fee43bad3c0b75758b911376d134078161540d6bb22e4ce08b7cb56e2847`  
		Last Modified: Tue, 09 Jul 2024 00:02:27 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json
