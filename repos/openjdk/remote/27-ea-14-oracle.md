## `openjdk:27-ea-14-oracle`

```console
$ docker pull openjdk@sha256:b87052b059f00007dbb33d765dfe258e41179cbebf01926ac95ae630d2aa362a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-14-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:bca85a735f3bd9805653a4d15a4739d1a995023d7b7b712541b8f498d34b5f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309217594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3178fe4f7c18ec835aa829c38eee7e025172098aa5de4ebe0b649cd0212a64`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 01:10:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 27 Mar 2026 01:10:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 27 Mar 2026 01:10:19 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 01:10:19 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 01:10:19 GMT
ENV JAVA_VERSION=27-ea+14
# Fri, 27 Mar 2026 01:10:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Mar 2026 01:10:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1101a6a16bdd51aef6dda35e785dca1d7934d2937fdc0c8dfc0f002ced99f85a`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 43.1 MB (43068827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f85b608e844819071e90ec9f2730786411ba729bccf926f4ca5a6aba08fd741`  
		Last Modified: Fri, 27 Mar 2026 01:10:42 GMT  
		Size: 37.7 MB (37678788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c406f44af41a4016f5cd6a2c79b9638fa1f28d25e8799ba5ef6896334907cb60`  
		Last Modified: Fri, 27 Mar 2026 01:10:46 GMT  
		Size: 228.5 MB (228469979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-14-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a8c71806c55053f222f92c0c0d6b5a01480b32f16fc46f431ff8c6fcd800c8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af3a1eb96f4538139909e10fd984c142610da2c258b55b04c29563f88626cc6`

```dockerfile
```

-	Layers:
	-	`sha256:a60574f8a393fa23d839e6df8e05afcb5c881e31e328c4dc3b8ef375fa83f57a`  
		Last Modified: Fri, 27 Mar 2026 01:10:41 GMT  
		Size: 2.4 MB (2368347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7a2c729b9cbc46f509c0f488efae4ab563184deaa0f374c201212683504e247`  
		Last Modified: Fri, 27 Mar 2026 01:10:41 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-14-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7ce42a1eb8d3eff41eff030b441b19efa2665608b15b4a3e7f18dbe66210b20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305603782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfacd6df1e77a86cb403a337c4b54425aac0d491e54603a972f7cb75481d682`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 01:10:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 27 Mar 2026 01:10:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Fri, 27 Mar 2026 01:10:27 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 01:10:27 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 01:10:27 GMT
ENV JAVA_VERSION=27-ea+14
# Fri, 27 Mar 2026 01:10:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Mar 2026 01:10:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3db22c05661dd4dd65ed2c3add4946b3292ef86d7a62c06699ee25367fc2e1b`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 41.5 MB (41474500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01da72c8161489573ed1b15645ace25a734feac77daf368f0ec059b535220816`  
		Last Modified: Fri, 27 Mar 2026 01:10:52 GMT  
		Size: 37.7 MB (37687865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff988c323a01cc1da09a3a2371b3c110a3b73dde8755dfe299dc57caca90245`  
		Last Modified: Fri, 27 Mar 2026 01:10:54 GMT  
		Size: 226.4 MB (226441417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-14-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:c8475d86ee6e004b8df35380e8c455b54ccc93c03a9257ea9b7afa57001449b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56cc753e34a2d3365abcef693fa9878ca5ad2e23511b56ed0a3cdc426e4658d`

```dockerfile
```

-	Layers:
	-	`sha256:3dbd1def0013f23cfcfeb82132a468beb44e7b5590b309c7815b07ee4d4b9979`  
		Last Modified: Fri, 27 Mar 2026 01:10:49 GMT  
		Size: 2.4 MB (2367875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3120e3fcb1daa6addf922bfe54e13223161afb5f2f4e57af9c5a524fe65129c`  
		Last Modified: Fri, 27 Mar 2026 01:10:48 GMT  
		Size: 18.1 KB (18064 bytes)  
		MIME: application/vnd.in-toto+json
