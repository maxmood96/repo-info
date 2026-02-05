## `openjdk:26-ea-33-oraclelinux8`

```console
$ docker pull openjdk@sha256:c2a631c8c8bdfd9773e5106cc855c271e6847e2bf0c27b8baecfdf4e01e95f8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-33-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3360c4178fef95eff5fac00f6d74a771807c05906bea2390f9827f6d61ad8548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294779444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beae55d94a5f7a3a3c0b7fd295137e2cd39ae7da0d28fb62ca0a2965730842de`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 17:47:46 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 17:47:46 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 17:53:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 17:53:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 05 Feb 2026 17:53:17 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:53:17 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 17:53:17 GMT
ENV JAVA_VERSION=26-ea+33
# Thu, 05 Feb 2026 17:53:17 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 05 Feb 2026 17:53:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:491a81275e9334940c80f680a1adb0db6fd283efcb818f679954c68fba010df0`  
		Last Modified: Thu, 05 Feb 2026 17:47:57 GMT  
		Size: 51.5 MB (51465258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca65e5e32e593478ed6a1c3d7cb39dfd9f94c6f300d1fd0a6a50758eeb1efc5a`  
		Last Modified: Thu, 05 Feb 2026 17:53:36 GMT  
		Size: 15.0 MB (14991548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a353e7f53f2fc0c4cd3a164f13ec1d8785add5d5f370160e6bb54f04d58bca`  
		Last Modified: Thu, 05 Feb 2026 17:53:40 GMT  
		Size: 228.3 MB (228322638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:83140da364a71f5722866455a9991f2490ea6e0f7d515281b87189f7cad530eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc3354d4b93a7c24b5b20bbd375c5578bd2130a9da2778e04c6142dabaafc3c`

```dockerfile
```

-	Layers:
	-	`sha256:854172b0815b7be35c7ebf990e62d3d85cc4fe8093c2cd0433f18ae1eeaa95d8`  
		Last Modified: Thu, 05 Feb 2026 17:53:35 GMT  
		Size: 2.4 MB (2448688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f7a2de9541dfaaa989f58dea9b2fffbfa2147ec17112dc645268371881a567`  
		Last Modified: Thu, 05 Feb 2026 17:53:35 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-33-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ccdd6a83c3fb0bd6a336a173d4a5ce8e83ead97c41a7add785af58a8086ab197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292150667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53b44c90d56e7d39b32d5498b2e10b2baede0ce205948eda27e421d3b8d4b8c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Feb 2026 17:49:16 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 17:49:16 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 17:55:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 17:56:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Thu, 05 Feb 2026 17:56:06 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:56:06 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 17:56:06 GMT
ENV JAVA_VERSION=26-ea+33
# Thu, 05 Feb 2026 17:56:06 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='9491eba6266080ac690d5e31b7776f5c94188c3f8092874d9fd250660d51050e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='f9ebfe93a1ff1ebbc6d7b3a4348b1197797f1c57c9f7a69b2bed30014af4039e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 05 Feb 2026 17:56:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13fbaff937e13295e4b8a7721c793f2982cdaf237b88f7bec2c123e9744840e6`  
		Last Modified: Thu, 05 Feb 2026 17:49:27 GMT  
		Size: 50.2 MB (50197611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb8bf6de641db4485fb384ab7b7f4912939b01920244c4ca35c8a4ee4883da2`  
		Last Modified: Thu, 05 Feb 2026 17:56:27 GMT  
		Size: 15.7 MB (15695116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c160a2359265816c81d55563439e2babf33dbfd8bdee06933a182b00737fc140`  
		Last Modified: Thu, 05 Feb 2026 17:56:32 GMT  
		Size: 226.3 MB (226257940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-33-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:5f5a6f59caacc0aa60530dff910ce1d42cae7d3545e6814b7d6f93941c03d7f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4901214785784502576cdf6d1eca88e53c7eb1b179fc52d8f96d053b29b65972`

```dockerfile
```

-	Layers:
	-	`sha256:6b6b9534a8199a175254de2f780b1a12bdfe0540f2087ad409662c51235fb3be`  
		Last Modified: Thu, 05 Feb 2026 17:56:27 GMT  
		Size: 2.4 MB (2447498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7e5986cadc449bb36a035e567cf294e34675a4aa3a71ac92752403d2f093bfb`  
		Last Modified: Thu, 05 Feb 2026 17:56:27 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
