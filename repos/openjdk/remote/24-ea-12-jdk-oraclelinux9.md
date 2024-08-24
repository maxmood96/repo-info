## `openjdk:24-ea-12-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:9648046ddb1a6ac095e6f638b8c211815ad0feb93d0880e09f843070bffd9356
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-12-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:fbb92fb9196f02603baf872756a756aaa90287db24b89bf07cd53b96eb5505d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300148732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1347f9366e5556bf48d72c06a140d5decb3bae7b77706b9994a844645d750`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Aug 2024 00:48:14 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Fri, 23 Aug 2024 00:48:14 GMT
CMD ["/bin/bash"]
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 23 Aug 2024 00:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Aug 2024 00:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 23 Aug 2024 00:48:14 GMT
ENV JAVA_VERSION=24-ea+12
# Fri, 23 Aug 2024 00:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='9a859e4f3840e3f0890051a26b06413cd18dc8a1b7d68b221f47b38ba2f5add4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='4631ab62c58dbecfc00983df819c9a669b3d4fb681d7f6c3d95af11b7aacf087'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Aug 2024 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a10e892c16f36e7fb4af9a6a56936363b87fd56d0e768358d4cf072b3fcac84`  
		Last Modified: Fri, 23 Aug 2024 21:11:20 GMT  
		Size: 39.1 MB (39067960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b0e8aac0bf4d4536b62e44edea3b083ebf784f451035cbfcd96f468a9dbe7d`  
		Last Modified: Fri, 23 Aug 2024 21:11:25 GMT  
		Size: 211.8 MB (211846708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-12-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:8efe77a7160bb7e27a0f2bb57becaa9c339a09453e406bb3d21ecffee40c9da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4f032e5f9b894b609fbc4412533606441a9c32b8346e6eed6390e8cb3fd5e8`

```dockerfile
```

-	Layers:
	-	`sha256:24ee69eb15fa08486126f4f8005616cc398910e8731157c553f920df0e91b9a5`  
		Last Modified: Fri, 23 Aug 2024 21:11:20 GMT  
		Size: 3.6 MB (3644251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c65cddca1c338c09d97d0260bfdacbe7c98b455c8771d5a0a0f54a6408c8d4c5`  
		Last Modified: Fri, 23 Aug 2024 21:11:19 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json
