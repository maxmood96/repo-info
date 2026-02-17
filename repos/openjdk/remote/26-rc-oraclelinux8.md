## `openjdk:26-rc-oraclelinux8`

```console
$ docker pull openjdk@sha256:458d6e16a52aac296e506b156e698cc6d5abd633a4c8326fdd2c5a57c5128227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:2176c78eae82e935ebdaa88884b4093473eb29d5499638b4853aea8cf2d7ce5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294847474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7536b41e699b829582626e4f690d3b6d552fb0e21ebf00a726b82489fecfac43`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:50 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:50 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 19:29:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 17 Feb 2026 19:29:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 17 Feb 2026 19:29:54 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:29:54 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:29:54 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:29:54 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:29:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df558405081e8d5c6af13745e322e2d270802ff99fe9a1eea2b63615844efa1a`  
		Last Modified: Tue, 10 Feb 2026 23:03:01 GMT  
		Size: 51.5 MB (51464982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f37eb3536627634c26e7bcc9accbeb2ffcb4ff7f6fca52dc6aaa3d624a1ea3`  
		Last Modified: Tue, 17 Feb 2026 19:30:14 GMT  
		Size: 15.0 MB (14991419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb100dad3be12666e0412fed1f9bf9a33c3ebece14a19d4ccd44da9a17f3c98d`  
		Last Modified: Tue, 17 Feb 2026 19:30:18 GMT  
		Size: 228.4 MB (228391073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:79f23336edbffd6e2091db245f882dfdf37cb0ce49c95e1d89f3a68e44d7f59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672b36f6c4c5276e7b5c79e35d5878c891bdcf4c232cb8c331823a5ede198b21`

```dockerfile
```

-	Layers:
	-	`sha256:801f4e40d51aa7f02690c180995311a5417cb1ed9d853445989d3f721e1ca90c`  
		Last Modified: Tue, 17 Feb 2026 19:30:13 GMT  
		Size: 2.4 MB (2448642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43ad4ed992da415d31e5fe89e324bf7d55742dfce429553c241c28df89cb995`  
		Last Modified: Tue, 17 Feb 2026 19:30:13 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2db092dd1d8754cdf905b2d62d649da3f9104a7269c58fb9da50eb1892993ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292226420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ba2fcb1894e0d91dbe855be2e439561269263774a0f46a8dbf96a446cc9de7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:07 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:07 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 19:30:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 17 Feb 2026 19:30:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 17 Feb 2026 19:30:20 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 19:30:20 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 19:30:20 GMT
ENV JAVA_VERSION=26
# Tue, 17 Feb 2026 19:30:20 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 17 Feb 2026 19:30:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07a1effc9605f90c3e2f6e8e5b85d7de94a80b436a975fd605cfe7f53acd6ca5`  
		Last Modified: Tue, 10 Feb 2026 23:02:19 GMT  
		Size: 50.2 MB (50191339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdc6208fec1d52f0a63ed6097d590d349f76ee3561dfce7395c38999f118f32`  
		Last Modified: Tue, 17 Feb 2026 19:30:42 GMT  
		Size: 15.7 MB (15690809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f456c445a61627c96fa6c1a7ebe6b6a399e515e9fc729c63f0be9b02f8c4485`  
		Last Modified: Tue, 17 Feb 2026 19:30:46 GMT  
		Size: 226.3 MB (226344272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:09248adc0d62cb14a1b5b8bc8b524ea6a86fde1ca4a64a6173ab3d6677348d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173bb671c630f6c07b27113bc8e696a4407c53c97c5b87b7eea47628be155a5f`

```dockerfile
```

-	Layers:
	-	`sha256:d15fe1bea4b915a050b8f4d56a54a901df676766c0d55b8f512d0368e3fca17b`  
		Last Modified: Tue, 17 Feb 2026 19:30:42 GMT  
		Size: 2.4 MB (2447428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1204a74c7ef258c5187541dea753bc795f0efef5181831b30942b9a3921aaac`  
		Last Modified: Tue, 17 Feb 2026 19:30:42 GMT  
		Size: 14.8 KB (14834 bytes)  
		MIME: application/vnd.in-toto+json
