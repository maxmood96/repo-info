## `openjdk:23-rc-jdk-oracle`

```console
$ docker pull openjdk@sha256:66a3e8fe8d607e3ae4fa3c798af5d5f9fe282727762df11b7870292e543d4a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-rc-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:0f458e3b47d16ffdb8089e6e35b0da7d4c9a78bb0a6f7eb8d9585f3962e678d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 MB (299345608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e7c80537140db57e5635ff65203c9fd3f0ddf2826ebe965caa1937c8877c6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd99a730f2ce347114a97667e995d24883880ce844e1e3a1fee2a4d5193dccf9`  
		Last Modified: Mon, 12 Aug 2024 17:59:23 GMT  
		Size: 39.0 MB (39047159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee034621b4a9cfec94c8fb4f91561a108732a3f5addb24aa00c3755a03a872`  
		Last Modified: Mon, 12 Aug 2024 17:59:25 GMT  
		Size: 211.3 MB (211304713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9b145f0940c48e91444e14f88619a6ca4f6c86d2b0a82a461372462023403e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64de40233849ff148439c2de052e6ca99a9c0a5d2bbc54a9a715275ae80a279`

```dockerfile
```

-	Layers:
	-	`sha256:0426d3fdc471bd6e8a7fdb47b3f8fe394f1c323da9df0be9c67c3b9d0fa4613f`  
		Last Modified: Mon, 12 Aug 2024 17:59:22 GMT  
		Size: 3.5 MB (3544037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6be9f5d06355d8877cee1084fd8593ddf67d06380303de117cae7567c58b72c`  
		Last Modified: Mon, 12 Aug 2024 17:59:22 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-rc-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f8b0713f6b0b0da3d2685d2d03f172799874e5e5f0003590cfc14f592c4d4dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296313741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dc91c35c7a7ff6928f1e83207e578c3fd604f450aebd6b1dd7647acdfc20d7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 22:40:25 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Mon, 08 Jul 2024 22:40:26 GMT
CMD ["/bin/bash"]
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 09 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Fri, 09 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='d8d169ae7a0285e09872565bc3044ad97697d3780e678d2a5ae9f8451c207cfc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5cad336e22d64a4a578f59d089223c226d67455c410cbaeb91f5fa0503ce2f96'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e12335bb1126bd80cd31b34b4fde93f2ccb7bb979403e778624cb60c3ece28c`  
		Last Modified: Mon, 29 Jul 2024 16:56:31 GMT  
		Size: 39.5 MB (39479870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dae405cd0c91e2db058ab92394a314cccbe643a8759a6d82f5c7c1ee0284c7`  
		Last Modified: Mon, 12 Aug 2024 18:35:17 GMT  
		Size: 209.2 MB (209181210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:48f4f599bc3bccbc2adf6010f3af185be854772c0ac2614bf60da2ca9e1715c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31abd35de71948a94bc1b44f3b020acfd95928834ed7ffb157df26b2374bcca0`

```dockerfile
```

-	Layers:
	-	`sha256:fec81f5b75b52b42aeb0d2ebfd7176ffb68ec861a6652bed4a66cd20483d683f`  
		Last Modified: Mon, 12 Aug 2024 18:35:12 GMT  
		Size: 3.5 MB (3542348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2116a519cfc1286dfb3d1d4f52ada0852decc469c5340a3d4c6afb3a0cedf2d9`  
		Last Modified: Mon, 12 Aug 2024 18:35:12 GMT  
		Size: 18.1 KB (18067 bytes)  
		MIME: application/vnd.in-toto+json
