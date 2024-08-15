## `openjdk:24-oraclelinux8`

```console
$ docker pull openjdk@sha256:8ed0857d2a5bf02348823f23561a286e781e398a49553dc2d2f22ae0b6a1a851
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:025721e1821fb93ab36d6efe7af737188f81d3553b7f6c24b53a3c2093905595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278476307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204392c3772443a4946a57bc786d2b87ef0f68fc767e290bad877f25c78ecde6`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 10 Aug 2024 00:48:15 GMT
ADD file:f88a328d16b39a012900e14f6463799b448cd9796472d5fb3c58c2cc5ebdee21 in / 
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:964443381b57e80f40937734e7dfea9e93836abe517bd3e9e9c0fc9f21af4ee5`  
		Last Modified: Thu, 15 Aug 2024 00:21:56 GMT  
		Size: 51.2 MB (51221701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb0ab8ae74a8dd35af88e89e3ca98f4b75421ed858c95b1b299067b9904186`  
		Last Modified: Thu, 15 Aug 2024 00:58:11 GMT  
		Size: 15.0 MB (15035971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e6fb5f20eebacb1d816de856edaebf4061daff2cfb214ccb78bc2275e44a66`  
		Last Modified: Thu, 15 Aug 2024 00:58:16 GMT  
		Size: 212.2 MB (212218635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:8fc5fa60f83da55cef3a6469243b81169f5ddcbe996b35b9a1af83cea3086839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a263893ed427a7eacf00c97ecb920e1838ffefea6ef92ea37f4c9c3235b097`

```dockerfile
```

-	Layers:
	-	`sha256:21676684e3573d8cb73cc89a6a78b8718d6f94c5adb7bcf524202a98584625f2`  
		Last Modified: Thu, 15 Aug 2024 00:58:11 GMT  
		Size: 2.3 MB (2287841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20108576001c086e73c0e325192a26ae20d9a9ca7dee599f9ad99080ad8dd33d`  
		Last Modified: Thu, 15 Aug 2024 00:58:10 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:233ee7da2235af2be7f43fccc1f171136b2da12db622dd600c7d3529947b757e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275669835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9061f19b455e7151a4eb749326291b112ddc47e2107b086434a9af3fe588ea`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 10 Aug 2024 00:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Aug 2024 00:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 10 Aug 2024 00:48:15 GMT
ENV JAVA_VERSION=24-ea+10
# Sat, 10 Aug 2024 00:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='b4c878f685a1333de0743bc33fb94a6cbd60e1ddda7e1d88068c2acc1c91012b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/10/GPL/openjdk-24-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='3640a7ecb431e631d5d23e96d0df679fb45cfed38f527a3810caeebebc44a3a5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 10 Aug 2024 00:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca345db69d5fd49f13cb0fd444dd21dc5576cd6587605dd8acb1793f7ebac2b`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 15.7 MB (15686119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e230df25a26c7218ad92274642db654e949a7785d6f4e50d19a90fae8654af`  
		Last Modified: Mon, 12 Aug 2024 18:29:57 GMT  
		Size: 210.1 MB (210058686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:d955f45428e30dcf8e83676e089ea0f6bd48188d680f1effafcaf0d63813a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39db82c1a5f1e67552af7f1a4f8fa321d38205f4556281d563defbb1302a7bdd`

```dockerfile
```

-	Layers:
	-	`sha256:603a6a80a8497dff73d9c72aeceec1f8dde0980139c679aacd157fca1940bcdc`  
		Last Modified: Mon, 12 Aug 2024 18:29:52 GMT  
		Size: 2.3 MB (2287294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddd8e3c798960247c3d2475bf24aacee26b111fc80fcb4e49887912ce67a4a8`  
		Last Modified: Mon, 12 Aug 2024 18:29:51 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json
