## `openjdk:27-ea-9-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:b1818375c406c8a1cdf3093dbd7f176c1e88fcea83025f37f4efbb91ded8d497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-9-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:03c25b1dc7254bc6b9396c7711b1f99072be3b6cf3374dc816f7c984e854c4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295279206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cadfc06c828cd25b8c501c5842bd4a6e748d0c73f520d56af1ce6f9ffe9d8db9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:50 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:50 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 19:32:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 17 Feb 2026 19:32:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 17 Feb 2026 19:32:34 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:32:34 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:32:34 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:32:34 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:32:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df558405081e8d5c6af13745e322e2d270802ff99fe9a1eea2b63615844efa1a`  
		Last Modified: Tue, 10 Feb 2026 23:03:01 GMT  
		Size: 51.5 MB (51464982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06248070052cd0a999aecbb3dd89d363b8a7779ba84d56b634b134d341d1246`  
		Last Modified: Tue, 17 Feb 2026 19:32:55 GMT  
		Size: 15.0 MB (14991734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1527a061705461bdcfdfa05245ff253a3185a952f4a9f1c80ab39d084a06c7ae`  
		Last Modified: Tue, 17 Feb 2026 19:32:59 GMT  
		Size: 228.8 MB (228822490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-9-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6b7402f6bb1c962ec475bbbe3b8c59d683d5932fa08a7a191289e3dba6546497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a753021e7627b9f5e557ba3ad3b06b41b6a236ee8653f028702d66cca945e5a1`

```dockerfile
```

-	Layers:
	-	`sha256:ec130f36bbadfd0f38a988b9a9f36563ebcd7b12320a8be678c98ca198d046e8`  
		Last Modified: Tue, 17 Feb 2026 19:32:55 GMT  
		Size: 2.4 MB (2448694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:586423da2be650f578a790e7f28a5853e65c7771e27f0847eb2bb1841cd67dc7`  
		Last Modified: Tue, 17 Feb 2026 19:32:55 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-9-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a3771de7c5d3b964e785805f21975cd4df44e95a3ab2500008fdf72ea4b085a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292674459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e2cba11a419985fcc39557526ee470dfa71ee2823f094483c5f38d0bba26df`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:07 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:07 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 19:30:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 17 Feb 2026 19:31:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 17 Feb 2026 19:31:05 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:31:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:31:05 GMT
ENV JAVA_VERSION=27-ea+9
# Tue, 17 Feb 2026 19:31:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='63b3704a0d6aac8050df9534d12f1e063e64ceae89a77131e1a9f01e0d1e223b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/9/GPL/openjdk-27-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='58393a7f38ddf3532c68f68b614756b3cb7953bbd54e64897221be7f071ee41b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:31:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07a1effc9605f90c3e2f6e8e5b85d7de94a80b436a975fd605cfe7f53acd6ca5`  
		Last Modified: Tue, 10 Feb 2026 23:02:19 GMT  
		Size: 50.2 MB (50191339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdc6208fec1d52f0a63ed6097d590d349f76ee3561dfce7395c38999f118f32`  
		Last Modified: Tue, 17 Feb 2026 19:30:42 GMT  
		Size: 15.7 MB (15690809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71152f196e772aada0b4bf6722ff36494795113146e2355d6c577f5fbb204cd`  
		Last Modified: Tue, 17 Feb 2026 19:31:29 GMT  
		Size: 226.8 MB (226792311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-9-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:85a396ead171d511176a710f7c2fb75952f3ae08ce43dbcbd7b9369105af3915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0baba3680910d187aaffe7071b6a59455c22e044b22fa63f4a0c972925f440`

```dockerfile
```

-	Layers:
	-	`sha256:fb9eee575de5742245f4f107e2b513a8bf0917aac02acb8db24632cfce373cda`  
		Last Modified: Tue, 17 Feb 2026 19:31:25 GMT  
		Size: 2.4 MB (2447504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54714a28995eb3270379baaffadc9cb3f6fa31e9863ec7f17294b739af9bf901`  
		Last Modified: Tue, 17 Feb 2026 19:31:25 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
