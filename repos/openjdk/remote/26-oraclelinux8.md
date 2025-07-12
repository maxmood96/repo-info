## `openjdk:26-oraclelinux8`

```console
$ docker pull openjdk@sha256:a0ddb0b48cc80cafbbe5885eb7b389c69a41561683593ec4e13a5836e0bf90cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:3a9dee7696c1f19897bc0fb7dff2ade593202162012e9f26de3f122c55d1f915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289699505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4f9f571a73d6be92e48ec083991af8c67549ff3df4335a336283eec7a1bbc1`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:54:13 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:41875d08ddffe10cea627347ab2d190e7a42649b4f26f96bcb1236b617350f27`  
		Last Modified: Fri, 11 Jul 2025 23:03:01 GMT  
		Size: 51.3 MB (51312999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aafb7f4f040d7da6a75138760527d3b7a31d1160a1a4fd7b23f2bc25051beb`  
		Last Modified: Fri, 11 Jul 2025 23:08:51 GMT  
		Size: 15.0 MB (14976288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed771d91f92cf9323bbc8c954de47399cae153ece13e29f02cafdf9b4cc56a76`  
		Last Modified: Sat, 12 Jul 2025 00:29:59 GMT  
		Size: 223.4 MB (223410218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:7dff7816a3af4c6fa4617d9fb614bf4234697a094d80055f809d79039dd7696d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c99849cf1e952e39a32d96e0ac9b86c245b7d5432d4dfd2868c7987e9667bd`

```dockerfile
```

-	Layers:
	-	`sha256:c7b2e9851264637786ac2fbf13c77d032863457c26070f4077031cda6bd7a556`  
		Last Modified: Sat, 12 Jul 2025 00:24:14 GMT  
		Size: 2.5 MB (2451702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e88d5c22e2a3f7c639a37dd61d5253dbdd60c9b7cd10dd2d5f1c3611445707ac`  
		Last Modified: Sat, 12 Jul 2025 00:24:15 GMT  
		Size: 16.0 KB (16020 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0f79e8ae5b8653d2978be0b357c83096200c28ac2090310011ae5a09e4fef78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286882151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50881b36d0ddedb04eb9e178bb250fdfd50874244f4531e026298670f80e981e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:54:13 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 05 Jul 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+5
# Sat, 05 Jul 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-x64_bin.tar.gz'; 			downloadSha256='b43bfaf18ccd153838dbb7979ebf2f4be031eb16da6a977823c2422eefa279e7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/5/GPL/openjdk-26-ea+5_linux-aarch64_bin.tar.gz'; 			downloadSha256='94cab2a012f104ef5ae8201f05912bf495c9f696b58e2f255bf10d6d018fb0c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4dfe820c20154be581827f07570596df525d44687f95b28b72c9da6274369d45`  
		Last Modified: Fri, 11 Jul 2025 23:27:02 GMT  
		Size: 50.0 MB (50031150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2354c264baf5ced06f90feda02f9e83f83a23da58b709069976e09fca065d12a`  
		Last Modified: Sat, 12 Jul 2025 00:01:45 GMT  
		Size: 15.7 MB (15680450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc03b531c3a3010f33e09ad079c2f7c05b4264846e0b131ecfe5f80302e0045`  
		Last Modified: Sat, 12 Jul 2025 00:30:18 GMT  
		Size: 221.2 MB (221170551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:1564157f76ea4b27a4a0b5a5d94718240f8d34a099cd9216a533d494a20f39df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d07c09e82c1e7a5e29abec3bb0e8f1f28a0e92aac4d7bca9d17aae1ceeb7978`

```dockerfile
```

-	Layers:
	-	`sha256:b4a27473e4662b7dc8413a4933811d88a06ee0f365dc9e0011c9cae6e9e7f785`  
		Last Modified: Sat, 12 Jul 2025 00:24:19 GMT  
		Size: 2.5 MB (2450536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad55225df5cfdf59edfd406ef55f33fd77b03cb4e72fa212c87eccc0dd068d5`  
		Last Modified: Sat, 12 Jul 2025 00:24:20 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
