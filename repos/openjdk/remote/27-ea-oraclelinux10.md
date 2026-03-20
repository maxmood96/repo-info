## `openjdk:27-ea-oraclelinux10`

```console
$ docker pull openjdk@sha256:edc850fe6540c4c38e84969189d6d0d343b0d5650337cffcc20f05fbac73a7cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:069770e67c4118265f94b8116b4d44ff8566cd956bb463c1b5806a4aba0bf8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309141706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33e5ff723079ba0b089b6474733bb95ffb8d2af1dd817f149c88b92327395bf`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:14:40 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:14:40 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 20 Mar 2026 01:12:29 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 01:12:29 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 01:12:29 GMT
ENV JAVA_VERSION=27-ea+13
# Fri, 20 Mar 2026 01:12:29 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Mar 2026 01:12:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b98cc56637e4fa1749005c0e126912a1b56aaacc09ce33acbc53f090ab5577df`  
		Last Modified: Fri, 20 Mar 2026 00:14:50 GMT  
		Size: 43.1 MB (43050023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c3b13607ff6cde9f88dfbd69b945e421f43cb8e592113e0d759253cbbba1ba`  
		Last Modified: Fri, 20 Mar 2026 01:12:52 GMT  
		Size: 37.7 MB (37656101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96672f4371c0f2322dd863959d93e240896960d26a4fb6390716528e72816159`  
		Last Modified: Fri, 20 Mar 2026 01:12:57 GMT  
		Size: 228.4 MB (228435582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:64b06f16e20177ba19ae9f874d42d0a5d1c6c944aaa241620ace842803c0c16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80e762abaaaa19690977696e52995167b52e5c5a5e2ad69898cbdad6aca9deb`

```dockerfile
```

-	Layers:
	-	`sha256:6143a789231c508be532fe5d83c01352e868080f4d606106441f7bd1bed7a412`  
		Last Modified: Fri, 20 Mar 2026 01:12:51 GMT  
		Size: 2.4 MB (2368335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3f97b070e802cc3d8df707a610e25df9a6ae75e945c0e48d3f014eb84e1ca4`  
		Last Modified: Fri, 20 Mar 2026 01:12:50 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3777c50f321fdfdf9a82c1aaf90e6c8170eeea6f736cfdeec5423052fd4e94f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305543534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecba1a759b0a74538369f8824aad3d2a93a7958bc73d02f97ebfda633388b7e8`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Mar 2026 00:12:38 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Mar 2026 00:12:38 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2026 01:12:50 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 20 Mar 2026 01:13:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 20 Mar 2026 01:13:23 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 01:13:23 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 01:13:23 GMT
ENV JAVA_VERSION=27-ea+13
# Fri, 20 Mar 2026 01:13:23 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 20 Mar 2026 01:13:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0341f6c98c0ded39ac1fd938e19b49e5d1980b5cf0e44b058cbbaac4f81336be`  
		Last Modified: Fri, 20 Mar 2026 00:12:48 GMT  
		Size: 41.5 MB (41455727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e2e53970491fdf89092d29dae81bbc31fe8bc27badd3e4e7855c785dc1320a`  
		Last Modified: Fri, 20 Mar 2026 01:13:46 GMT  
		Size: 37.7 MB (37679573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e31ece74d74ecf3e92543700a63bf220076c16e4d2613f1487f9de45486c701`  
		Last Modified: Fri, 20 Mar 2026 01:13:50 GMT  
		Size: 226.4 MB (226408234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:f8dbf4ca7c2cf4da679701b0355ee6b4b84d6b05e9091732c521eee4884cf782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bb49dd900d2aeb643f5bafc9c2c8c20dbb09788883b260c3f6a1f342fbe880`

```dockerfile
```

-	Layers:
	-	`sha256:8732de0553baf473e47e691d03566fb3d5e4a1a976ff70076bf180465eceb58a`  
		Last Modified: Fri, 20 Mar 2026 01:13:44 GMT  
		Size: 2.4 MB (2367863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3d4057a0379cb5404cbac6facfe67e8143e9ebcfabe5ac6d3b36bfe613efea7`  
		Last Modified: Fri, 20 Mar 2026 01:13:44 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
