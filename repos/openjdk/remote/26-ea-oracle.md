## `openjdk:26-ea-oracle`

```console
$ docker pull openjdk@sha256:942059b12b1ca588fe12df9ace8abfd06060067cc4852f2e2b513cef4caaee6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:523fb57e418827e911712efb99c3a4130c7e2132d2754f699f2f0f693374d999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313456100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c0506400ce5698088153ba874b4cf5fa7f4ba26c2f7aeb0385cab9de1fc0dc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:05:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:05:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 23 Jan 2026 01:05:56 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 01:05:56 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jan 2026 01:05:56 GMT
ENV JAVA_VERSION=26-ea+31
# Fri, 23 Jan 2026 01:05:56 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Jan 2026 01:05:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7567ec5ead2f2a3d46652fe66e8c9ff777d9df550b7f827115b76680ca7b1f26`  
		Last Modified: Fri, 23 Jan 2026 01:06:18 GMT  
		Size: 38.3 MB (38296810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54b9f1b2da02e4e9f5aec977f4ae8378495225cadc13fac8b8c5cd8b54b98f6`  
		Last Modified: Fri, 23 Jan 2026 01:06:21 GMT  
		Size: 227.8 MB (227845742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:51b637a26fdc72a3c758c0477b96807de7c79a62a5f94049f11ce722724a2c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a78c3740ffc4553c786e94888caf334ee3a6cdcd120e066600916b37db1e3`

```dockerfile
```

-	Layers:
	-	`sha256:ca2d7317fa899efe42786c697f13d87105ca8c99b17bb98e152c518c853cf763`  
		Last Modified: Fri, 23 Jan 2026 01:06:16 GMT  
		Size: 3.7 MB (3655375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f5098fd16fe9f1e17b65a86a751213c8d0364aca24b413cf54507a02ce38f8`  
		Last Modified: Fri, 23 Jan 2026 01:06:16 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b7d170a9e52d54b7627ba68c06278239ef6f4c82b56a6d0c5c8b8049818f66fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310387370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c51afdbff92ed488ac6cf97abd06c004521029fa73eb133cc7b4346741bb0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:09:42 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:10:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 26 Jan 2026 22:10:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:11 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:11 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:10:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3406d1b672322cac1d921038924382b1febfdff7b6d1f9a7efe9318884089819`  
		Last Modified: Mon, 26 Jan 2026 22:10:34 GMT  
		Size: 38.7 MB (38699962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa4dc73d1a3c649e420584a6bf128f378bc87759368888ad5b67b032a424d4`  
		Last Modified: Mon, 26 Jan 2026 22:10:37 GMT  
		Size: 225.8 MB (225785498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:40d9d16314c7f0b803c67a210ca87e2d80630a10734d7e249a1e1598d4a3de70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28106e24a3e5713f255aba3cd04083a3fe1ac60a5904e3073811121f9aef3f60`

```dockerfile
```

-	Layers:
	-	`sha256:fdf3bd1608c9d4a32dda7c299db2c29a273e259a84c18e339736e47a4ce1f4ea`  
		Last Modified: Mon, 26 Jan 2026 22:10:33 GMT  
		Size: 3.7 MB (3653065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:962158e3e07c8945039cb5c6c952e98a90dde8281b1af5d0f16b8e8a99625a98`  
		Last Modified: Mon, 26 Jan 2026 22:10:33 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
