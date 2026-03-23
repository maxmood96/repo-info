## `openjdk:27-ea-jdk-oraclelinux10`

```console
$ docker pull openjdk@sha256:f92d0a8268446a46659673acb7d1f936550c0876eb5e2ac6dd11276837a04830
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:4c37a837a65589a336ace24f8733a1fb87f4299356feea039f540442b0a24f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309176023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3fad46629398254c865da08d4e74e872b01de0a1c6601f3cec4505283a9f4a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:14:40 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:14:40 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 17:58:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 23 Mar 2026 17:58:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 23 Mar 2026 17:58:15 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:15 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:15 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b98cc56637e4fa1749005c0e126912a1b56aaacc09ce33acbc53f090ab5577df`  
		Last Modified: Fri, 20 Mar 2026 00:14:50 GMT  
		Size: 43.1 MB (43050023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8ac8ba5fa4edd11f2fc63a4a43df4e29a46cdafe49311d0c1c698f80214fc5`  
		Last Modified: Mon, 23 Mar 2026 17:58:36 GMT  
		Size: 37.7 MB (37656003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84ea033de0bed3c8fd8ef42b2b72e3ae64f2b11924baf4d952263014dbbfeaf`  
		Last Modified: Mon, 23 Mar 2026 17:58:42 GMT  
		Size: 228.5 MB (228469997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:be56120e4b3daed16b37c9ff246ec1d1721ec3bded747316d07871e6bddbf408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb0c6c6e59765015fb517019cb81ab21d8ec8f04e979c00030fb1333527cd6e`

```dockerfile
```

-	Layers:
	-	`sha256:f4af94e979ec3688285f719e9159226e6b7524e6b42ece2f766cb6788586cb08`  
		Last Modified: Mon, 23 Mar 2026 17:58:35 GMT  
		Size: 2.4 MB (2368335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9c6a0f9f005f83f2394bd20d62813f922bb5e7da15912240afc8197e85086d`  
		Last Modified: Mon, 23 Mar 2026 17:58:35 GMT  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f66bb377e26854fb6a37faf18c91fe3dfb3e3347d6866ec0a21c58e84855039b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305576852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25f02b074b7cdf0cee5aa6604a0dc8f3fe90a68318fd44118b331855e7afd6e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:38 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:38 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 17:57:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 23 Mar 2026 17:58:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Mon, 23 Mar 2026 17:58:10 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:10 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:10 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0341f6c98c0ded39ac1fd938e19b49e5d1980b5cf0e44b058cbbaac4f81336be`  
		Last Modified: Fri, 20 Mar 2026 00:12:48 GMT  
		Size: 41.5 MB (41455727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fe5779896c3eb1b6d3e846d83e4aab19460999fb5696defab0276d7c283f93`  
		Last Modified: Mon, 23 Mar 2026 17:58:32 GMT  
		Size: 37.7 MB (37679719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4abf4d42372f8099e7a70e47982223a2968d5fe2a95f549afe579e6865bfc3c`  
		Last Modified: Mon, 23 Mar 2026 17:58:36 GMT  
		Size: 226.4 MB (226441406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:0269474f634b9b21e6d9ac1b5178f55a9ca55a88075331c674e978d84575a590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7f70703fa2451ff8f3b8be9cdd7b095d8d5d4d6a5023c271099658d672d297`

```dockerfile
```

-	Layers:
	-	`sha256:659a9e4031d1c0c4ce21dbf17fd214015fcac61896a228b32a515fe1009a0420`  
		Last Modified: Mon, 23 Mar 2026 17:58:31 GMT  
		Size: 2.4 MB (2367863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e9d3a00a402d3f27d1a3c305bba65d42d29b2a498748f6495015985416d123`  
		Last Modified: Mon, 23 Mar 2026 17:58:31 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
