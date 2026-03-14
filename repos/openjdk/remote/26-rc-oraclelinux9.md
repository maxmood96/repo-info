## `openjdk:26-rc-oraclelinux9`

```console
$ docker pull openjdk@sha256:47ded4b3f18053b93277daa8803c84d5bb0cdd12af76314728b9a75068b1df89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:dd55693886dda9fe5f0878fd19ce2e33881ea7708a180fa5a99b393ad44ea6b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313537789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574f5889ef8791cc713690d1e712cfcdd22a4d0f46db394afde46921e104af2c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:12:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:12:36 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 13 Mar 2026 23:12:36 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 23:12:36 GMT
ENV LANG=C.UTF-8
# Fri, 13 Mar 2026 23:12:36 GMT
ENV JAVA_VERSION=26
# Fri, 13 Mar 2026 23:12:36 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Mar 2026 23:12:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebf71672e4b8b6e263c937c7877c7dfcfca0b6b7b6657877db14fe3b47d7ef1`  
		Last Modified: Fri, 13 Mar 2026 23:12:59 GMT  
		Size: 38.3 MB (38296891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34b8f91864db1429f9ad5e916f79edbf7b29cc9b50abe7e414d5b69e8f9a7de`  
		Last Modified: Fri, 13 Mar 2026 23:13:02 GMT  
		Size: 227.9 MB (227936688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:06d49d654417e80467f544f75ac2c2247657ecae5ad30a7df8734501c266fed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3670097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7294218904657dfd26bbf06531f2d07b5225a0de7e90c93605c9631c7d4a2fa8`

```dockerfile
```

-	Layers:
	-	`sha256:c0cd525af32b0ff396c5ce7159dbb632c2882695ffb28e9d9eaca2db07e9f729`  
		Last Modified: Fri, 13 Mar 2026 23:12:57 GMT  
		Size: 3.7 MB (3654123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445968017929f5fb748dc155110ddc9245c7ee1e223c022943bf9a3c7296ee20`  
		Last Modified: Fri, 13 Mar 2026 23:12:57 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1d284bbc3bf9ce802ed77b21824d0a2562d898ec4ec19066e04538f3debcdfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310459850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c8491ff4b731eda09b14e6424a4e14681b25dad45819a0b577b5962cabb70a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:11:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:12:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 13 Mar 2026 23:12:07 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2026 23:12:07 GMT
ENV LANG=C.UTF-8
# Fri, 13 Mar 2026 23:12:07 GMT
ENV JAVA_VERSION=26
# Fri, 13 Mar 2026 23:12:07 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Mar 2026 23:12:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aac32375182e2929693cb1d3af90cc88714117a07ee1304d248a8c8c1d6ccea`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 38.7 MB (38695544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05c2bc90417070dfd08c3ad03d160880899260ef58c473e7a812a9edee2782`  
		Last Modified: Fri, 13 Mar 2026 23:12:34 GMT  
		Size: 225.9 MB (225864120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:2cec99f49f2550fba94e489fa4dd7bcc0a2e355f91b05a1e6f885805cd851203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3667859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc9a1ac124539612f1c0cc3cbaddf45e541a3161e0b8ce1ddfea41bd2056e0c`

```dockerfile
```

-	Layers:
	-	`sha256:c3d77b625038a44a4b48af2b20f63e2f07506c1d2c1dde42d8c227cfc5e8fb76`  
		Last Modified: Fri, 13 Mar 2026 23:12:29 GMT  
		Size: 3.7 MB (3651741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b053c02b18d8ec7b17aab8f289e304553f07c1c09e3c56868a0a23ee1355d4fe`  
		Last Modified: Fri, 13 Mar 2026 23:12:29 GMT  
		Size: 16.1 KB (16118 bytes)  
		MIME: application/vnd.in-toto+json
