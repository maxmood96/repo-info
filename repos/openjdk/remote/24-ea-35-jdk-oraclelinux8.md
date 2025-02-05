## `openjdk:24-ea-35-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:255ae230173a9fafc403d2aec9894acadfa20e2a7543c2bc61aafb3f2fd70b9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-35-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3e0e647c303955dbcb5fe410c3c32c590c077da3eaeae4fc3c18a166304ced14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279561875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16ceab6b51ff639e7167039e8ffe74a32bc77004db154c1e1a2dea7a5fbaa4a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Jan 2025 18:59:24 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 30 Jan 2025 18:59:24 GMT
CMD ["/bin/bash"]
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Tue, 04 Feb 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-x64_bin.tar.gz'; 			downloadSha256='bf5289b474e53b34a9ece42dcd3ae073e5ef7df63fcb9c44fbcac92496dedd99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_linux-aarch64_bin.tar.gz'; 			downloadSha256='96e6ce86751c7aceb6e5f435be31ecbd0629592097abbd67d1c0f5c5b85c8f78'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 04 Feb 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b976166ae00f0fda8e12b934d92a7265904c082bbb675e0cb9bd4bbe93bedb30`  
		Last Modified: Thu, 30 Jan 2025 23:27:50 GMT  
		Size: 51.3 MB (51277963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f722755cb0bafed35b98ed85e4d99aad697196c067ade205f0fe490bac37a1e5`  
		Last Modified: Tue, 04 Feb 2025 23:32:59 GMT  
		Size: 15.0 MB (14975269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbfde12fead67e27126f45f59aa859f2d728c10ddfc1e94b773a7b058968874`  
		Last Modified: Tue, 04 Feb 2025 23:33:03 GMT  
		Size: 213.3 MB (213308643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-35-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8938dddb49bd987a9b1e350fa27d9475d368cc857ceeeb654ac6ea7790465f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f97e23cd7c92dae5be54160dd506cbcf81923fdfaeba74b0993396e165e36e`

```dockerfile
```

-	Layers:
	-	`sha256:351f7f753903fe10d5694b5579c4714f7adb7443c6a9367565458fe14bf36277`  
		Last Modified: Tue, 04 Feb 2025 23:32:59 GMT  
		Size: 2.4 MB (2445351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2d6a671978134af5e8171ce91783c20f42adf06a202c746ab283e089b99bd0`  
		Last Modified: Tue, 04 Feb 2025 23:32:58 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json
