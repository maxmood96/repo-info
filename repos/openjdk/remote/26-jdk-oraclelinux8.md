## `openjdk:26-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:16ce24f94767a07f06247ac322398a03a147e02d4e4626e0674d896a6bb6ffcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b2a34248872c275afc16d1f605710685288219981c1d8c4e0aad610b471507c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289699509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94cdfafb1cc96a26733c156219bf469f3f3a438e2851542c90310f984e878e33`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:42:18 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:42:18 GMT
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
	-	`sha256:0915556054e5fcd1f04e454b0deedf305bb209616c5a72a8b2d83db9191e5115`  
		Last Modified: Thu, 12 Jun 2025 21:07:27 GMT  
		Size: 51.3 MB (51311558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc759c8e682a4c47cd4aaf29ecf5f6f87b893af25f2689f2b53ef77450fcb12`  
		Last Modified: Mon, 07 Jul 2025 20:59:56 GMT  
		Size: 15.0 MB (14979447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34534c00051652a31a75ec9187f8bee0b7fd5398956cde17a59b734411fa000f`  
		Last Modified: Mon, 07 Jul 2025 21:41:54 GMT  
		Size: 223.4 MB (223408504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:bf4ffba243a374e417752055b1bf73cce28c3e52c0ed711768abb25ede941447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88121d63681b97dbefb7c90fffe7d49245ceea3fd1d94138b87ddd03f95fa01`

```dockerfile
```

-	Layers:
	-	`sha256:7f3bc4717bc3136e1a6813e72bf38c6213e1929830043b781f1ee8e9d816888a`  
		Last Modified: Mon, 07 Jul 2025 21:25:24 GMT  
		Size: 2.5 MB (2451698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14403cf5e12ee4b811269826af38ebaa3bf1c282aab905dbc3fb48c9aaad5eb1`  
		Last Modified: Mon, 07 Jul 2025 21:25:25 GMT  
		Size: 16.0 KB (16021 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f8c68870f76b3edc980c94257d165e4ee6f5c53b697cdcb4447bbe46fd3675c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284092552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e1255157aad2919a0abbaa00687072873bddf72bfdd47ae19a707fe0a7767f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Jun 2025 16:43:09 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 12 Jun 2025 16:43:09 GMT
CMD ["/bin/bash"]
# Sat, 28 Jun 2025 00:54:13 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 28 Jun 2025 00:54:13 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Jun 2025 00:54:13 GMT
ENV LANG=C.UTF-8
# Sat, 28 Jun 2025 00:54:13 GMT
ENV JAVA_VERSION=26-ea+4
# Sat, 28 Jun 2025 00:54:13 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='49aa2a8f29bd63727be9ab8e279ffceba2ee6d09beca9d221a69784da673476f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/4/GPL/openjdk-26-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='529cc863c692cfa63afec612e73bdb9f2d8097a509454664315649e9955a16c2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 28 Jun 2025 00:54:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d998890baf088acce50ef79f8e8dc3eab36a2dc008c7774fa6e1e1140c89c3c3`  
		Last Modified: Fri, 13 Jun 2025 01:08:32 GMT  
		Size: 50.0 MB (50039112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cddf61b157a492a5e9e87c2aa66c8d9d39517125432aef6e1db78ce8635515`  
		Last Modified: Fri, 13 Jun 2025 00:42:33 GMT  
		Size: 12.9 MB (12917586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b02057acc0eee1e208d42b74660c2045ecf279ae3bde4fc932339391646fb4`  
		Last Modified: Mon, 30 Jun 2025 18:32:04 GMT  
		Size: 221.1 MB (221135854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:ad7d49cc43cb2e17b1c44498238715425820f88c12a0d2271678d5cb3568c438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2453151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f2e517dfe5321ebc1e99b48e6e0dd78522bd623541f2c330ce1d6bb3060de`

```dockerfile
```

-	Layers:
	-	`sha256:36bb5bb7d8d69543c1fff7bbbb3719bdcad5b6a0038c56a0c41d44cac126bdf3`  
		Last Modified: Mon, 30 Jun 2025 18:26:01 GMT  
		Size: 2.4 MB (2436987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf8f5143fbf86df2bde3db86da23320703f0e82476b551c4f7924270a306f1d`  
		Last Modified: Mon, 30 Jun 2025 18:26:02 GMT  
		Size: 16.2 KB (16164 bytes)  
		MIME: application/vnd.in-toto+json
