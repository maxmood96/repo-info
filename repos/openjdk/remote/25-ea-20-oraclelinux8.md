## `openjdk:25-ea-20-oraclelinux8`

```console
$ docker pull openjdk@sha256:0f078ae2b25781e29546bfb592e80437be9805c997fca361e10a941ae76ed752
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-20-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7c593f173eeebd6d1198a6b3719d6a5de5ac8b59bd1b2773325e76ed1e1af37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279194471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24894beedd622e932eb77288084ceee5f912bd60822edcbb4aaa4264192d563`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 18:48:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7ee6d2b4bc3292763eeab29f03adacbfcd179273f648dc332abeb3f2f9cf99a3`  
		Last Modified: Fri, 25 Apr 2025 22:19:54 GMT  
		Size: 51.3 MB (51312878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f2815cc96cb43c96ce34f2d02555b2c76fd37930ef2f9d6beebb4b8d131ff4`  
		Last Modified: Fri, 25 Apr 2025 23:08:21 GMT  
		Size: 15.0 MB (14997946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788d5d36e1d2de55790a7e196f02dce321e1ef732a963ec90081bf06d0a88aac`  
		Last Modified: Fri, 25 Apr 2025 23:08:26 GMT  
		Size: 212.9 MB (212883647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-20-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8b6f900b853464822d33fdd1f2637da239b28d880d26ff144ff27110f0887a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7633ffbdf732b9c1996428136eeb810c6cb599f1428b372292c5e51af752140`

```dockerfile
```

-	Layers:
	-	`sha256:9dec6de93aca492b193fc87fa21b99f8c36db4e4458ef7c41de347d6cfa879b1`  
		Last Modified: Fri, 25 Apr 2025 23:08:21 GMT  
		Size: 2.4 MB (2442873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e058eec437397d7ad206456c1161c2b0892f3885813d8d0f118eceeeba8112a`  
		Last Modified: Fri, 25 Apr 2025 23:08:21 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-20-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c313658c521027efb23831d44810ffedff1a6756e64555f049fc09a0cc69867b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276406348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde0024547037e72e17a9a8be81fd681ae844e4d35b0066b7c77d824aad26f38`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Apr 2025 18:48:12 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["/bin/bash"]
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Fri, 25 Apr 2025 18:48:12 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Apr 2025 18:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 25 Apr 2025 18:48:12 GMT
ENV JAVA_VERSION=25-ea+20
# Fri, 25 Apr 2025 18:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='6bc1d37add3f10b8826fef26bfc5ab51183b308c32a12f08a18ee2b6d9e28111'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/20/GPL/openjdk-25-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='e6b42d0f5816ea1fd6c27505ddf93dc11eae12fc2cc64b4139350d7c0acdd55a'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Apr 2025 18:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f9f09355eb5a75f94b3d65a17269700229fb600c0fa7b446c5cabbd22d410e6`  
		Last Modified: Fri, 25 Apr 2025 22:20:08 GMT  
		Size: 50.0 MB (50027777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a940b0109afec58930ed82af330c90718664351944577010959491e7e3d4ab3`  
		Last Modified: Fri, 25 Apr 2025 23:08:07 GMT  
		Size: 15.7 MB (15667728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2a54f1e2889d2bcfe2406c6998de71c18b556d53c4d8f5e87e9ee8171d6ac7`  
		Last Modified: Fri, 25 Apr 2025 23:08:11 GMT  
		Size: 210.7 MB (210710843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-20-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:801f0a7347127dd7fe7efb550488820c85ddd02d2df8338f54db2039fbb26b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7257ad8df51e0661e2ce34b78c591991c83105706c1c7d59dbc654882ba149e`

```dockerfile
```

-	Layers:
	-	`sha256:8de280ed86ca2751f2cf9ff1f9507e40f3279d3ad1846c40854b1c0bee1aac4b`  
		Last Modified: Fri, 25 Apr 2025 23:08:06 GMT  
		Size: 2.4 MB (2441719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4307959a13e7e0b881f4df5a1f870947fc2ef797915a4b5c7dcd3c70e53a5868`  
		Last Modified: Fri, 25 Apr 2025 23:08:06 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
