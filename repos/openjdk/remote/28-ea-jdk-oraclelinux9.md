## `openjdk:28-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:b0208417ddf25859e070febd3f3a548af10bcfbc1d4953c050abb740d1f8c6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a22c10813d6777920794f681c2bc7f0aec7efcad75666a38e06c76a455fd2ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312602420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c6e53214e3ae872b4342639c7ab87dcff287ccae70100970d4943b76794d03`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2026 20:16:49 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 10 Jun 2026 20:16:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Wed, 10 Jun 2026 20:16:58 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:58 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:58 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:58 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b86e375818761e002203fc33ba78131f1574e787131b4a5790b2bb0cf5dc97`  
		Last Modified: Wed, 10 Jun 2026 20:17:27 GMT  
		Size: 38.3 MB (38267827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25baf241a0b00864d74dda5de70ffaae2941fe618c2e0c3f27752b6f60d17361`  
		Last Modified: Wed, 10 Jun 2026 20:17:33 GMT  
		Size: 227.0 MB (227025020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:36fda0e5ff2bd507fdcb09e419be4090394970142d5ae33ec4e53e3c610538f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3665735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48222ce08e93f9b939a5cd059e3cbfe390c4f1f0204a81ca635d196927c91c0`

```dockerfile
```

-	Layers:
	-	`sha256:a6b0f0e5645fe606376ce08b21626965f08baf1902d94ca303cf70b1a06b9688`  
		Last Modified: Wed, 10 Jun 2026 20:17:24 GMT  
		Size: 3.7 MB (3650410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6940c489a219e4d58421b25f5e671103d157be6f1dd434d1a4e6e9284bff2b87`  
		Last Modified: Wed, 10 Jun 2026 20:17:22 GMT  
		Size: 15.3 KB (15325 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:59969eaa8c92da6c866326ad1bf0b380460e9884b9f47cd3d40993b51900a781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309554418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082fb34d0edd3f6ba6b24abc1e515d71ff5d1f43b43d8cdef64ae02c259d6513`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2026 20:16:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 10 Jun 2026 20:16:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Wed, 10 Jun 2026 20:16:44 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Jun 2026 20:16:44 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:44 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:16:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='d9b2b25f13a93424625f129bc9725ded401725e36ac819b9f4951f02bc8fc91c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='642cdb07549c099010edf29631c3ceea1b96000fcd1c15d23598eb99bcb16042'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 10 Jun 2026 20:16:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f896d53223649e4c3fc1414e4a74c9c179bf79042b61d3eb8a46f9c4feb4f`  
		Last Modified: Wed, 10 Jun 2026 20:17:07 GMT  
		Size: 38.7 MB (38665496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f811d70d73ca59fa19fc26d5d93b0b22f1e689c4d699067df1c637e70033c4f`  
		Last Modified: Wed, 10 Jun 2026 20:17:11 GMT  
		Size: 225.0 MB (224989832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:674d3867a24450fccd60f5095aae18e3706cc7afc77cc828b0ef267d601bdf22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d31925da093a1ab6ad28e5624dea20caba1f8a397fc10d537d1f1eb06a4296`

```dockerfile
```

-	Layers:
	-	`sha256:76a171e4aa1762ddac0ded0d585ccd0977304ac5de66a04f25708b0f23e07235`  
		Last Modified: Wed, 10 Jun 2026 20:17:05 GMT  
		Size: 3.6 MB (3648004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47ca762cb3e96ddc7bdbc59e1edf44a29019dc0fd4ae886ab56e64324aeb844`  
		Last Modified: Wed, 10 Jun 2026 20:17:05 GMT  
		Size: 15.4 KB (15445 bytes)  
		MIME: application/vnd.in-toto+json
