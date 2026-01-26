## `openjdk:26-ea-32-bookworm`

```console
$ docker pull openjdk@sha256:0b650835ec19c57aa403870312c15625877739ecea01fdc97ec61ff6586a1370
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-32-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:609fbd2ce10591ad6e757c466261cb9618638a14d901e45544bb0a70d4327b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.1 MB (380083225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e296cc22032ebf7ddccbf23ecfa52cedabd2aaad9f05513f9ff1c0283dfbec29`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:10:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:10:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 26 Jan 2026 22:10:12 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:10:12 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:10:12 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:10:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:10:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:05 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e358169f1669753d9ff281d5c20dc5c5270b8e48d846c5cf138c8bff4ab0ae4b`  
		Last Modified: Mon, 26 Jan 2026 22:10:38 GMT  
		Size: 17.7 MB (17728528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f391c1d3b6e3b0349e27045c80b785ce9bb06c23a21b4062362e67c230f21c18`  
		Last Modified: Mon, 26 Jan 2026 22:10:42 GMT  
		Size: 225.9 MB (225904349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-32-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7fbe6ecc706790edbc699eb86d85e8db83a9628799d0b8bb506f4572b2dc4712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a91641e8238a2df1a90aa53c7dbb4239b846d770b03f05e79184c6e17ea605`

```dockerfile
```

-	Layers:
	-	`sha256:8a55e67c6075646452c43f954af8ce58ab187860b20a465d04f2489e2bb74fe1`  
		Last Modified: Mon, 26 Jan 2026 22:10:38 GMT  
		Size: 8.8 MB (8805724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40904237866523ccecc65b7d3697699c4a4ddb174a39ccaa659ebd99d29f78e2`  
		Last Modified: Mon, 26 Jan 2026 22:10:37 GMT  
		Size: 18.1 KB (18057 bytes)  
		MIME: application/vnd.in-toto+json
