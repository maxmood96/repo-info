## `openjdk:26-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:20c3717f3c8cd5b6eb4f649e727158e791ff91ef630a21960b5f01381d148fdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:063b7fb8dc8753db3ec399bd664eb1897f4ba8867b5112f1d3a1bf896d050ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260031714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6bf89245a63ab97ff19c0910526ca2084016dbe926eb23e1873ea185d88a87`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:32:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 05:32:32 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:32:32 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:32:32 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 05:32:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 05:32:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65aff438d05829a5fc13cd7fbeb1d460bc1c1c827c743b3beb002b9241c2fa8`  
		Last Modified: Tue, 18 Nov 2025 05:33:03 GMT  
		Size: 2.4 MB (2370976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9987c99967aa6a490cec307a6bb9497872127dcdd29f5b992637cd71fe10737`  
		Last Modified: Tue, 18 Nov 2025 07:28:16 GMT  
		Size: 227.9 MB (227884254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:04ddaa1dc2fd6f32f60b18179476c308d29254576c3a1d4ea74079396237d706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3417e31196d542d4c89f4da2055f1a6a8a27d2ba91edc4347903228012ba59a`

```dockerfile
```

-	Layers:
	-	`sha256:653ebe33e13c0ad4c68e8318f7dc677247bc9735ada4a5bf5b1f3ef9367c843d`  
		Last Modified: Tue, 18 Nov 2025 07:25:11 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec2f1f2527671cf7a4a58ff4f984779fde66c84463a9d580da3950e7197a296e`  
		Last Modified: Tue, 18 Nov 2025 07:25:12 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f746e217a7793704b87e568bdd19c1958a23d88fb73014c6cf63cd18a652587c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258188040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0074b7582774f716e8f0f3a113bb5992b2c321716b338f852456d74429c6e82c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:07:31 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 04:07:31 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:07:31 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:07:31 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 04:07:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 04:07:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d0731205bce21bc25b848eeeb3c9912f6c9dfe778a457b2d7a819c4ad4b435`  
		Last Modified: Tue, 18 Nov 2025 04:08:03 GMT  
		Size: 2.3 MB (2314116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f87dd3cf99accc54367d82ae027e856c12bed2f9a69649d9efe0be1d88c81f`  
		Last Modified: Tue, 18 Nov 2025 06:12:19 GMT  
		Size: 225.7 MB (225735314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:dc79dda60da3bc17b0820d8b8950580ef4095364a115ebd9d536f0798b4ab7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a87a87511a1c38d5a8b62e96153866a8b5ac25c1003541b51e90bcda9dd787`

```dockerfile
```

-	Layers:
	-	`sha256:aa643476de3343def560663fbbde058a648acbcc595e0074ff61f7ce434def7d`  
		Last Modified: Tue, 18 Nov 2025 04:25:48 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df98485da027ad4e36b5fec2ec169ca40ffb21244ec67c22195c42d3fa2afaf`  
		Last Modified: Tue, 18 Nov 2025 04:25:49 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json
