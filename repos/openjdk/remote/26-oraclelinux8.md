## `openjdk:26-oraclelinux8`

```console
$ docker pull openjdk@sha256:bc0acb47055826fa1cc630e86070cc4e829d15052944ca8b22e2619f15f0d140
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7a19d429c6575b906aad2907cd8579a7033637b4bea2d6dfbdab075f40f3c503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292427890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1333f42a41c890129e0289c78cadc04b9d7b98da56f606e1fb9c7d066e1b37cb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66700e2b18e01c0550984729a0cbc6c7137d4f5489a563e0fe17c014042a3f6d`  
		Last Modified: Mon, 06 Oct 2025 21:05:30 GMT  
		Size: 15.0 MB (14979318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e1f494740626563ccae0cc342381da710e8427d48e698295ea4d81f9ff8c5`  
		Last Modified: Mon, 06 Oct 2025 21:53:04 GMT  
		Size: 226.1 MB (226125009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2ef34c04c6baa6797b2be8328dc8a554f165a2bba291a78be97638daf8e39b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fc685a82a04057d93b22a386057bed20df67bf059cd892098c5f489498eab9`

```dockerfile
```

-	Layers:
	-	`sha256:00ba45374ba87e3fdb65d2af010f2d541e0342e2f23ab5c71ff6b03e0b7c668e`  
		Last Modified: Mon, 06 Oct 2025 21:23:52 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77fdf486d0e7bf8b511aba42626882e148d011fd53ddd700ae358416aa91eff`  
		Last Modified: Mon, 06 Oct 2025 21:23:53 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6624cc1f97a7313b8fb88d4b26f420e0818d3d835db1f0cfdad81b035342b299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289704233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4762e5bbc8319a8689efe8d40b59d02a6f8cb3d9f0aaa2ba6625202eae9d6752`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 04 Oct 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Oct 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 04 Oct 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+18
# Sat, 04 Oct 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='efaa7c08b216ca30d5769c56a81337742b795188f8ab45532f711cd0fedd7971'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/18/GPL/openjdk-26-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='2176c4bff69a4a7825dbbd296ac2ab318460f5dfe104d5590be6f3f470d7dd5c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 04 Oct 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9866c68be293aa81b529074549b7f38395dba71a8ea8fc528f721fbf8543b957`  
		Last Modified: Thu, 21 Aug 2025 18:57:24 GMT  
		Size: 50.0 MB (50039817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836cbdc7065174286a41ca00b97b31573809669bf27c84a698670a7e65f7160`  
		Last Modified: Mon, 06 Oct 2025 21:08:04 GMT  
		Size: 15.7 MB (15672276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089ca4d578f536186ba88046584460d49584f964a11d39dd46077155839fe6a8`  
		Last Modified: Mon, 06 Oct 2025 21:52:25 GMT  
		Size: 224.0 MB (223992140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:2f7f34a548abcc78c36a2732a1bee7aaaf27771f8ee5ba685c62c4672683bdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c3b4fe72697f46bc2221ab6583790fe51781ea546c3c7930d6ddfe8c8c2abd`

```dockerfile
```

-	Layers:
	-	`sha256:3039ea5c3f8e57cbb0eb93b52509892dda756aa3dc5175f2a0cc178b08823753`  
		Last Modified: Mon, 06 Oct 2025 21:23:57 GMT  
		Size: 2.4 MB (2449933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa189a476a1d3b22fbcb2bf82c4d7586ded9e224ef310205fb45b0a5df71890`  
		Last Modified: Mon, 06 Oct 2025 21:23:58 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
