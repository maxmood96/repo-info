## `openjdk:23-ea-33-jdk-oracle`

```console
$ docker pull openjdk@sha256:71e7c2ce79b68cb2c7131c0023fd471c16867c591cb2003b2e21eb3ea4f2cde0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-33-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b4a37f14bb87508fd662706a8ba291be0823428525eb382a08da74ca92f54c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298181348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447ec9a45a5221a2661848046e553b863243102b7055c4cead536e064489195e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Sat, 20 Jul 2024 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Jul 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Sat, 20 Jul 2024 00:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+33
# Sat, 20 Jul 2024 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='d44748cfdec1fe164da0725a95fb05f7e4b94070a669f2688f8604154d14df5b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/33/GPL/openjdk-23-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='e25276d4f0cf9fb6f67b3a1be8087fbf0cceadfa33cab8ffc17e99c83e105e74'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f4595bc8923bd33baaa9fa3da6b9402101e55c0cfb4f5a4637936efc2dd5df`  
		Last Modified: Mon, 22 Jul 2024 21:00:18 GMT  
		Size: 37.9 MB (37871908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c618c551b0e48c8cc866b767ccbb68fca45ce7598a5d14225b338fda73ddc407`  
		Last Modified: Mon, 22 Jul 2024 21:00:22 GMT  
		Size: 211.3 MB (211315704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-33-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:02f026f991132fae536219d7d88927d841bf4ac06f41294fa5418114197f0410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be25c7e47f5b037bb97e1a6798a84a1185a575c281eb79d57b8976d2f841ea2`

```dockerfile
```

-	Layers:
	-	`sha256:4d9b381741c931bbe3fa5eec1dbe300e567d36d53712f5fc4daba8336b0bb6b2`  
		Last Modified: Mon, 22 Jul 2024 21:00:17 GMT  
		Size: 3.4 MB (3358211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f4812b80b97bff7734c002486adc1bfecba5703cca1b7f31897d212a394ce24`  
		Last Modified: Mon, 22 Jul 2024 21:00:17 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json
