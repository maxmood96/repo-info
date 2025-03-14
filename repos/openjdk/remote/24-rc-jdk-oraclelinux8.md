## `openjdk:24-rc-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:83ac877db4f179f26a987a9050517d7a4960ca54cfe841b7342a28c32b9efc18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-rc-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:678a8b858517a3404c5aaaffcdca3d12c485a352db3f88ef4d98292758310a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279601713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7428f39f8b241c54d642bada5fa90546a1392d3bd36722a7477e9bae573ca143`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:035e56311411a7644fa1341dfc093e1b278feac7d55c98ae09177e1755672600`  
		Last Modified: Fri, 14 Mar 2025 19:00:09 GMT  
		Size: 51.3 MB (51288940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5c98cd20bef727195aa1228bfb0d761a29ea18c9c09458caf53aa67b5ce756`  
		Last Modified: Fri, 14 Mar 2025 19:09:14 GMT  
		Size: 15.0 MB (14996437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e796e2f221d6dd800cc8d1b9f28081290790971ff646c82e5514d4c001e3b21`  
		Last Modified: Fri, 14 Mar 2025 19:09:18 GMT  
		Size: 213.3 MB (213316336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6fe7d8a011f1a74e4f5ec0122b0efe77503ada6a3e2159fbbb4c585e8530fa66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955ba1789151f123f778aa2b5c8618359ab9e1cd4827661b271a10b3e0593c7a`

```dockerfile
```

-	Layers:
	-	`sha256:ec1179f882469b6408746c17847ef01b55c7b012b5c0e15f92bd8c1afca9bd3c`  
		Last Modified: Fri, 14 Mar 2025 19:09:14 GMT  
		Size: 2.4 MB (2444669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd42ad6adc3ee51015bf2d0c61c88cdc0134a66c9ff11d98ac52b236f8d32700`  
		Last Modified: Fri, 14 Mar 2025 19:09:13 GMT  
		Size: 15.4 KB (15434 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-rc-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a0447cdb9f98a03c1eb4309c3c6243d1bc6d168584da04737c1d0e6c5f5f7af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276943758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e882e656ed4c421ccd29d55ecedea1e9bd19afc8061de4075addc97be1d3b1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e6d27d0384ed91610f17d7a9ef2bb948c3574306ac40526f54329f54140d2f0`  
		Last Modified: Thu, 13 Mar 2025 21:07:17 GMT  
		Size: 50.0 MB (49989436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69e77c2995841cd0e340bc286b91ceb1b42cf941fc975e2014d23fdda3f999b`  
		Last Modified: Thu, 13 Mar 2025 22:09:21 GMT  
		Size: 15.7 MB (15683725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d9e8326543766e2fc20b993b6f691315ea0c0617d54d68c704baa122fd49ad`  
		Last Modified: Thu, 13 Mar 2025 22:10:17 GMT  
		Size: 211.3 MB (211270597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9e031d850f43e8f81e1621f6ef58723033118a995218b9d69030f87319f9b861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24a97158e32586e6e68b8a0ce5fce886c69b18ad636ff5916a3847ab83af9d4`

```dockerfile
```

-	Layers:
	-	`sha256:04b675de4959872b8dbaa6d79cd917ab14b24a696e00d092280bafc977ff4f8c`  
		Last Modified: Thu, 13 Mar 2025 22:10:12 GMT  
		Size: 2.4 MB (2443491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b70aca8e1ba44a99c3650284748484740795f20c97698da8ded9f064b692a7b`  
		Last Modified: Thu, 13 Mar 2025 22:10:11 GMT  
		Size: 15.6 KB (15553 bytes)  
		MIME: application/vnd.in-toto+json
