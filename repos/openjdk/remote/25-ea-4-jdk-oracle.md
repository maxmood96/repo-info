## `openjdk:25-ea-4-jdk-oracle`

```console
$ docker pull openjdk@sha256:f89ad4e930cb2197284792caedbecfa5e251006b5516a27367c8d8b42d5f3cb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-4-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:be1ba5f09d2061b2f6b2ac6c154ec6cc2d439e5eae52e3bdb487bef8a3efc267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310792571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf4c65c2e7295459b2df3efaabce9ff3dc22b39ff41d0e13e3e99e820c89639`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
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
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07afacb21e616d9ac41fa5658804ed38571980eb6ecd0779713c64842bb8582f`  
		Last Modified: Mon, 06 Jan 2025 20:28:35 GMT  
		Size: 48.8 MB (48774167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2430e51b0977958fcc6a84677be0bd3832b2ffd321fe9736ea32a3bb089435bd`  
		Last Modified: Mon, 06 Jan 2025 20:28:37 GMT  
		Size: 212.9 MB (212919702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-4-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a57ec4b2e910e02ffe9cb03734620aaa3442bed8d0d8421a0528881613c6c1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604dc0eea6b2b16f0038c7296491ed0994182f092a92a4c0bcb22edef8647cb7`

```dockerfile
```

-	Layers:
	-	`sha256:cf4ea34c44838a565fa0b949678acc8589db14bb51f2fe56c5189b34e188afc3`  
		Last Modified: Mon, 06 Jan 2025 20:28:34 GMT  
		Size: 4.9 MB (4907559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53218db3a441ce569385b2966e708a3cb6bed148a0439211df5ff1c65f8e2855`  
		Last Modified: Mon, 06 Jan 2025 20:28:34 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-4-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f946914047a7d1b86d55c712ca88139e29570b7d72b49707e74c9e0b8062c8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307732026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165ddf036e71bf46b71ff460fce5c89204bb6c838201d012e4aa15c2761107f0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
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
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50730d7cdebc9dd971fe547b229ac9b36632531d0634a0903681766460bf2cf8`  
		Last Modified: Tue, 10 Dec 2024 01:26:17 GMT  
		Size: 49.2 MB (49196487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56e753fbc124d85cbb99e125d01d4ce454601183ab9db8a8f35680fe7ce5ac7`  
		Last Modified: Mon, 06 Jan 2025 20:28:19 GMT  
		Size: 210.9 MB (210868147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-4-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:dfbcc76c9a2dd23955c4a02e29fe580fea76cd4978389a88ab9caf7e7e9c430a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aeb2845f8c2f8550ff53c787cb8348b61e44fc86d05ed0e5703b0a4e4610d02`

```dockerfile
```

-	Layers:
	-	`sha256:d659fc32fe81a9959feea75d7b1921df5db26f0f7c05ea543ae4bb8e763355e9`  
		Last Modified: Mon, 06 Jan 2025 20:28:15 GMT  
		Size: 4.9 MB (4905321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99ed112db1a9ef5f019ca0d2ae06a2901d3e8e992846053d93c39e27eddc6352`  
		Last Modified: Mon, 06 Jan 2025 20:28:14 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
