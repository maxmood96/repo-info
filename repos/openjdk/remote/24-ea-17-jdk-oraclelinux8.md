## `openjdk:24-ea-17-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:a69035e53c4d70f8ea0fdb1f53e9b1dbc947281086a6926b303f658e37ebc049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-17-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:d857c9523788898a0d0b6c69ab31bfbd3219659ad29d92fe3a7eeb9a2ed5a92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278940550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5a927e56fa673457bbd2d1d7f08bea2116c4457f495cd42913497bf848e554`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 27 Sep 2024 06:48:27 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 06:48:27 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_VERSION=24-ea+17
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='983faf25eff38b5b396afabd191a91b239a1d803a0dadd01863861ecf731f034'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9eb980b4f1fde9c2387e0fab6b91b6f68cb109e3ddd43eda0013d9ee345f2dc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7d760ad2fe664c6995a4d9508e389d78b6bdf1b1f154b4a216d0fd3ad9a46bc`  
		Last Modified: Tue, 10 Sep 2024 01:03:41 GMT  
		Size: 51.3 MB (51293960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aa2f67d411dffc440afcbd6f20d3f127fc0813da4b4fd81d1bf84ef9fadc4f`  
		Last Modified: Sat, 28 Sep 2024 01:01:39 GMT  
		Size: 15.0 MB (15041705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6a03f2827f798e5fab355ee847912994088b7910ae40c33083367e9f440d9`  
		Last Modified: Sat, 28 Sep 2024 01:01:44 GMT  
		Size: 212.6 MB (212604885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-17-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:dedb6d28221e51a57a53950c6481dc1e9089bec64d695f645b34554ed76bd7c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2441780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8b437bfd3f952080410190c129b9c8f856d46f36a5e7c67ddd4b423a473c51`

```dockerfile
```

-	Layers:
	-	`sha256:0423fd49182b7c312c2c8c7924ee1fdd56eb63fe6f4b1ab4665663dcff399d73`  
		Last Modified: Sat, 28 Sep 2024 01:01:39 GMT  
		Size: 2.4 MB (2425776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a0e4f499a15ec69cfedf17af2eb10561b2bda0b77a2ca96fdfbc8709b1a3fb1`  
		Last Modified: Sat, 28 Sep 2024 01:01:38 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json
