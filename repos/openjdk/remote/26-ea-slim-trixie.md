## `openjdk:26-ea-slim-trixie`

```console
$ docker pull openjdk@sha256:830538288aa2ff295f13de1d03649e263243199ff1ce0eae999a6516ad25eadb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:03f3c3fd0d883cd2e27ccf3c3ee2bac59a85a5b6aaeea61a75e3419ef93c6ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255491583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01df12462e64848125279d11ce07d606203edb98c9a513e0c327114b61720a1d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 30 Aug 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Aug 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 Aug 2025 00:48:13 GMT
ENV JAVA_VERSION=26-ea+13
# Sat, 30 Aug 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bf1fc270d7d30fdafbb1df8cb75b7b9a0e40adba8b72e9655410df7d7475ecc0'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/13/GPL/openjdk-26-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='e0d0ccf09df66d71738ff9ba2a927e4169f52d99569f57a346797b83e2dea920'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 30 Aug 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba40873faacf0b0ac49f5fe7340ca09fad17c45810b179ac25395036c0fa28`  
		Last Modified: Tue, 02 Sep 2025 17:24:03 GMT  
		Size: 2.4 MB (2371096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f55e688a1a05b817cb13dc79c142831723ef3740ea1d19810777b580bc8e586`  
		Last Modified: Tue, 02 Sep 2025 18:07:33 GMT  
		Size: 223.3 MB (223347202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:d47be9711d2fcc6c0fdeb3b11b07675573105c8b473b0855d0d8b4c21fcfb63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19108c60b3f9619efd6c9053d5eb1359d836778a4a663a37fc984251b8f89479`

```dockerfile
```

-	Layers:
	-	`sha256:a3e0d29bc74a5313007408ae332b1314007a7043a6a31d8f95bc9dcea0116011`  
		Last Modified: Tue, 02 Sep 2025 18:24:17 GMT  
		Size: 2.3 MB (2281656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebccaccfea510538ad6f231942de673e26c84d66b72e418cba775c1bf0b1a523`  
		Last Modified: Tue, 02 Sep 2025 18:24:18 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9e092c8cbaa39258aeb75ad4034ac242bc80f4a487363daf2ced9d4d2e87131b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253589844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759fd514265d431173c58787b5217e866c24a04aa3a970c9706074b527a52ae8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Sat, 23 Aug 2025 00:48:14 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 00:48:14 GMT
ENV LANG=C.UTF-8
# Sat, 23 Aug 2025 00:48:14 GMT
ENV JAVA_VERSION=26-ea+12
# Sat, 23 Aug 2025 00:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='2d6177e017ca138d8990643910b989990751db9370cd78dfc51e5116411e7f6f'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/12/GPL/openjdk-26-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='b4e0c4bb252fe005ad3a46c54264e226c554fe95edcbdc9df81dbc268901c7cb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 23 Aug 2025 00:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8aafae0cffde53a4a97b3a67ecda78936d66918ef646e27519a1c2c6551a203`  
		Last Modified: Mon, 18 Aug 2025 22:23:58 GMT  
		Size: 2.3 MB (2314286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528fa522ef28b3a083e9b50110cc528e13636a74c15b89a50dea83336f4449a`  
		Last Modified: Tue, 26 Aug 2025 02:23:11 GMT  
		Size: 221.1 MB (221139514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:c6e38047cc2a452981d29905f27721897890f9602df7b7c0f5b8184b8598206b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f2fa7df9b4e9360edcc92a87c0f1f67fbce18c31e9d8cf0037edebafcab334`

```dockerfile
```

-	Layers:
	-	`sha256:e2daeac101db203786ac2b1a9872c0171affc04d6b7f1d84978dfb3e91db8f9b`  
		Last Modified: Tue, 26 Aug 2025 00:24:17 GMT  
		Size: 2.3 MB (2281390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:275ecf122980319ff4d9948aaf55165c1a9234adc3876b4d865e66af24a2ad22`  
		Last Modified: Tue, 26 Aug 2025 00:24:18 GMT  
		Size: 19.6 KB (19627 bytes)  
		MIME: application/vnd.in-toto+json
