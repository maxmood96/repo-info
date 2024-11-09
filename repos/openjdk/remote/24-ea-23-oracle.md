## `openjdk:24-ea-23-oracle`

```console
$ docker pull openjdk@sha256:e44c74b5af9343aa79b2540adb4e06ed7fe13bfb3d12b8935127f141e974d648
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-23-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:94eeb56d8a9ce92ba8298df55df81d5e95f0959332eb0c8713c6bb1f8f9b934b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301639083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2253df8c65b70001719a36a372d6c55fe649acf12b0ef6e1f2f54b31a59f06`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Nov 2024 16:23:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 06 Nov 2024 16:23:18 GMT
CMD ["/bin/bash"]
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 07 Nov 2024 19:48:11 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 19:48:11 GMT
ENV LANG=C.UTF-8
# Thu, 07 Nov 2024 19:48:11 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 07 Nov 2024 19:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='4a83df6c5ba87f963cb8f7830f1ddef7dbe387b6884749411cdd4db6f3be6ee4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/23/GPL/openjdk-24-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='76fba0034d8bd3edd8983162ebe459dfcdeb8d19e0202eb42803716fedf61a32'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 07 Nov 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd22421e3d3a484fe2583805f43113ae71c5a9fabd02702c36c8e044f08b34bc`  
		Last Modified: Sat, 09 Nov 2024 02:06:42 GMT  
		Size: 39.1 MB (39050497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7953493ff30f0d86f60ba9e87801dda6a2b0e3762510dbd0291bf1bab9f8433f`  
		Last Modified: Sat, 09 Nov 2024 02:06:45 GMT  
		Size: 213.4 MB (213370527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-23-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f3f0bc5d00a6c1d9086b633f50b88437bb208e5300170647f2b7a15a255d3581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4b8c31446b2942e39b4d8155f15726a45073b261032ec954a7f10b7033cd1f`

```dockerfile
```

-	Layers:
	-	`sha256:7792dd1ba00156ba2c7a2d1dae92a425e02247454b2b9487d4226e6977bffd46`  
		Last Modified: Sat, 09 Nov 2024 02:06:42 GMT  
		Size: 3.8 MB (3782205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17beb02bb5d6333319cf714b8e9dc572f920b44c7407bb8f6737ab44d1d136cf`  
		Last Modified: Sat, 09 Nov 2024 02:06:42 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json
