## `openjdk:26-rc-oraclelinux8`

```console
$ docker pull openjdk@sha256:8a9461cf1dcc42d6c5ac2ad84c9185fc58952100fd7cd81c4a0a18cbeba8810d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:da84888db05b48cbd274b5e2bbbd9cfff36e98519e91feaa669130bc0e34ecbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294780621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4592709d8868be255d4dc0461f6db7ae3d321253885f2d5f54b04bc21d6f8986`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:50 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:50 GMT
CMD ["/bin/bash"]
# Fri, 13 Feb 2026 00:00:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Feb 2026 00:00:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 13 Feb 2026 00:00:19 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:00:19 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:00:19 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:00:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:00:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df558405081e8d5c6af13745e322e2d270802ff99fe9a1eea2b63615844efa1a`  
		Last Modified: Tue, 10 Feb 2026 23:03:01 GMT  
		Size: 51.5 MB (51464982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaafe3a7096d3ad88f049f0787af7dcfe7646dff7c4a6396e5afe67c0c4d434`  
		Last Modified: Fri, 13 Feb 2026 00:00:43 GMT  
		Size: 15.0 MB (14991630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc426f1c57f1354b70cc8963a3b92eab9d5a6745346a242a7eb91562dcec680a`  
		Last Modified: Fri, 13 Feb 2026 00:00:46 GMT  
		Size: 228.3 MB (228324009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:00b432daced0e9614836a1f13e2ece97acc3991d380fdb25c33bdd656e5feeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856e64a0ff5e7363f6f10f6b1817391e580f5f2585dcdb1adb38162790ad197`

```dockerfile
```

-	Layers:
	-	`sha256:4f2dd28ce6212286ffb5b36aa68592fb87b4f889bb2adb87f8e0a3727a8878de`  
		Last Modified: Fri, 13 Feb 2026 00:00:42 GMT  
		Size: 2.4 MB (2448014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980135d558076bf975d4dc3f364474b8054a6a6c9c17c33d2c0632d3fb341177`  
		Last Modified: Fri, 13 Feb 2026 00:00:44 GMT  
		Size: 14.7 KB (14739 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:60d337a3f82249d1fe7f61be0ad40b1d293f4ee4843eb415861975c15d4d92f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292144992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4434804ed63dc5de900bb52147bb0ed2e9dd7543b056e7f26b9ab148ea61628`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 23:02:07 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 10 Feb 2026 23:02:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Feb 2026 00:01:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 13 Feb 2026 00:01:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 13 Feb 2026 00:01:22 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Feb 2026 00:01:22 GMT
ENV LANG=C.UTF-8
# Fri, 13 Feb 2026 00:01:22 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:01:22 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='e7c907ec1036e5480609f8212e6f1e7f710310e029d097e4e1a9645c43676945'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='aeb9ccc00550a012197834334a9a6cbc03e7938774fcaf59dfa7ed158b66465f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Feb 2026 00:01:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07a1effc9605f90c3e2f6e8e5b85d7de94a80b436a975fd605cfe7f53acd6ca5`  
		Last Modified: Tue, 10 Feb 2026 23:02:19 GMT  
		Size: 50.2 MB (50191339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d4dde0101f064cc066bcc7e3aae4973c1b7265940f89098fa55a1dab565710`  
		Last Modified: Fri, 13 Feb 2026 00:01:43 GMT  
		Size: 15.7 MB (15690832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413431783f288aa47d75f654754e25099b760aabf931362036e1cabdf64674a5`  
		Last Modified: Fri, 13 Feb 2026 00:01:47 GMT  
		Size: 226.3 MB (226262821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:789631b8201eaf4cd4cf56241357875341ec474ef522692ada51dd2e03132723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aeaae2e21e9ec17b7441b5f25dace9cf2d6af4143c849d1bc33fdaf69b87f43`

```dockerfile
```

-	Layers:
	-	`sha256:19858b371c05100db2b65f3706e73858981c93786a4a40a85e822e63789b8ee9`  
		Last Modified: Fri, 13 Feb 2026 00:01:43 GMT  
		Size: 2.4 MB (2446800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3edd55a7140a0d121856b331369848c06ffbee7c8925778bf30a67cd72862d`  
		Last Modified: Fri, 13 Feb 2026 00:01:43 GMT  
		Size: 14.8 KB (14834 bytes)  
		MIME: application/vnd.in-toto+json
