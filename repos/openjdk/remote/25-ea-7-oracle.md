## `openjdk:25-ea-7-oracle`

```console
$ docker pull openjdk@sha256:8847c281ec121467bbe2311cbefc55a8b51ff8d9922b04d991ab9bd11de22db8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-7-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:c6f178c727d1148b0eded6bccd0e6658d490f41be5826bc8aac0ab8ba52f6e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309563136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89876c29f5fa27c233a3df61ba10a2c4b1543a3f98d66a0d1590045e8295637d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ad7cd79dc68c5fb4b88ce26761b817bcac823ce273efebd361e4de5afab8c`  
		Last Modified: Tue, 28 Jan 2025 23:28:55 GMT  
		Size: 48.8 MB (48774991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df433994f66419351a00d7660295e9799688c69a1a7be99a715f8b9bfbb7cf4`  
		Last Modified: Tue, 28 Jan 2025 23:28:59 GMT  
		Size: 211.7 MB (211689443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-7-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:55113cfc0f34b69ed51ab6ac1cc314e3c1e385ae7962de4538c35bd5d423980a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d151de075a33e8a638281888a1e7fb99177d67b9b548d0b833828a4f224316fa`

```dockerfile
```

-	Layers:
	-	`sha256:d019f4df7979f6ef93de7f47df9c7940fb9a1d9a18a8913b078dcbc597ad5c59`  
		Last Modified: Tue, 28 Jan 2025 23:28:54 GMT  
		Size: 4.9 MB (4906931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def200ddd033beceb46943a9f05e8e47fb7b2f7a301b260cace24429ee5a56e8`  
		Last Modified: Tue, 28 Jan 2025 23:28:53 GMT  
		Size: 19.7 KB (19720 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-7-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e25057ce82fb7bdbff94cdd17261118e600af70f6953797f6d2673dc063c3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306523823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395dfb33aed0181ab531465c94c1c12231bc44f45b2fa4c9e96ea2ee122c5cd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 25 Jan 2025 01:52:19 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Jan 2025 01:52:19 GMT
ENV LANG=C.UTF-8
# Sat, 25 Jan 2025 01:52:19 GMT
ENV JAVA_VERSION=25-ea+7
# Sat, 25 Jan 2025 01:52:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='7feccd12886711c8902b12a7af32cb26a34993f148b00a36aa93068ce1e3b128'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/7/GPL/openjdk-25-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='8f29e5e012a3477812ef892a16022af8410235782f12c41d09d2a7082e20849e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 25 Jan 2025 01:52:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9527a70a5df0c50a0919b2bbc807b6789f8d6833d49f997079d3ab5dd2e735`  
		Last Modified: Wed, 22 Jan 2025 02:29:30 GMT  
		Size: 49.2 MB (49203729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae0949b656b700eb965121b445e19828c0619060dadef5a281201f9ec21832`  
		Last Modified: Tue, 28 Jan 2025 23:32:26 GMT  
		Size: 209.7 MB (209652702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-7-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:d838bf2bea2adc92f71afc021ddc9204fb4ed2e50fe2b3b040bacd139ccfb9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bf9a6c6fe3a9f6ce02a5cfb36bcccefdc69b97effffed8d6b4f7452d3bb656`

```dockerfile
```

-	Layers:
	-	`sha256:535da638224f593a367cf225f0a3b4e8d19e0b37c87f8a86b2299c4ec87c2887`  
		Last Modified: Tue, 28 Jan 2025 23:32:21 GMT  
		Size: 4.9 MB (4904693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a8eb067d49b8f9ac78380932c6b258a3db7bdbcfb0e7271cb790402d58a94e`  
		Last Modified: Tue, 28 Jan 2025 23:32:21 GMT  
		Size: 20.0 KB (20008 bytes)  
		MIME: application/vnd.in-toto+json
