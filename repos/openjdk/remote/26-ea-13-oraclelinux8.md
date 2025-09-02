## `openjdk:26-ea-13-oraclelinux8`

```console
$ docker pull openjdk@sha256:5c4226ac7a315407c15bef159fbaf86cb53e6a4e3356a97dcf6fde5ded30b977
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:26-ea-13-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0463759dd679e4ad8dd6daacb397430dc32e79dc1c91a5338c4af3838bc11a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e30af4a0c47a19cb01b17f9f452d2457971c05271ba825cea042887392ff678`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614dbc68f1a859e70aab9dace669a70347e4f90f9a37ab418478305ad68a7b61`  
		Last Modified: Tue, 02 Sep 2025 17:24:47 GMT  
		Size: 15.0 MB (14977080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc0843455956e94e9156eae567afe14d31e942df411d5aeff32b1e5df4ed657`  
		Last Modified: Tue, 02 Sep 2025 18:28:50 GMT  
		Size: 223.6 MB (223643749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-13-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:aff91952515e482358b6f812b12357adc3ee51ccb03c03416a086db6650019c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a1e78426a867125d4d6b32925fd5c2511995f0c5bca4827c464383904c3b65`

```dockerfile
```

-	Layers:
	-	`sha256:c2a490f522d25e7f3757b3f6f6766ee013a391d41cb36e806a0a8fcfe30201d5`  
		Last Modified: Tue, 02 Sep 2025 18:24:13 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f0822a3fa252d6f8e0f993657a10ed5d9fe2dc3f652e67fbdfa3470372ca72`  
		Last Modified: Tue, 02 Sep 2025 18:24:14 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json
