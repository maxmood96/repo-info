## `openjdk:26-rc-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:71bfc310101a58948162a9e0b9922387a2982dac0847439009be57fe807f06bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-rc-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:c9e6689598144382b4b915cf59e1a24cb4ec690528dc2bc5dc9365e7417e3bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260371899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2687f60f1736b0067656baac1c8c47170152b50220ce526e5573fcd474ea528f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:28:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 24 Feb 2026 19:28:14 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:28:14 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:28:14 GMT
ENV JAVA_VERSION=26
# Tue, 24 Feb 2026 19:28:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 19:28:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca15a7365b14f58bd0f9673afd501544fd7d0a12ceb70cd31c97afb7ec1736`  
		Last Modified: Tue, 24 Feb 2026 19:28:33 GMT  
		Size: 4.0 MB (4029170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4719df9103edf749ba48c33c9d5b7a1782cb401d57e2282a0f9c5373e4599d90`  
		Last Modified: Tue, 24 Feb 2026 19:28:38 GMT  
		Size: 228.1 MB (228106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5de113927a4e76521374d9346753ea640747b07f463b0d1df51d1e3b0498dbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a406e47abb381b513ccff48db36e42d88273d4890ca0099ddc324d73d0263115`

```dockerfile
```

-	Layers:
	-	`sha256:441d707d5f9685b63d6f43dd07a0811b5f64b841fd51f3cebb9c4d60e5d8f2fc`  
		Last Modified: Tue, 24 Feb 2026 19:28:33 GMT  
		Size: 2.6 MB (2649744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a9c5709e8cdb1040b2393e2238c0e9b56cc4f004bf00ad28cf7a6ae4b7d6da`  
		Last Modified: Tue, 24 Feb 2026 19:28:33 GMT  
		Size: 16.3 KB (16267 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-rc-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:db6b0f7d53d54d72a8dc95b63011193690c6375d2e99d4e264088dc6d8eedbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257997882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c10f985568116f749fcd3f148374277e5c851b02a577e225fa1651fcd1690d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:32:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:32:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 24 Feb 2026 19:32:55 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:32:55 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:32:55 GMT
ENV JAVA_VERSION=26
# Tue, 24 Feb 2026 19:32:55 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-x64_bin.tar.gz'; 			downloadSha256='83c78367f8c81257beef72aca4bbbf8e6dac8ca2b3a4546a85879a09e6e4e128'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_linux-aarch64_bin.tar.gz'; 			downloadSha256='403ccf451e88d0be9e1dec129fcb9318de9752121e0eb92dfa9a8cf06f249007'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 24 Feb 2026 19:32:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ad08cfb1ffecb3ef899aa6e891b03d06d4db8383ebe8be57acbf48a50662dc`  
		Last Modified: Tue, 24 Feb 2026 19:33:16 GMT  
		Size: 3.9 MB (3851974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b2d9b9ad33a3c710be2e50e168945fa4009b1726f711e077c27ef9a28aac1a`  
		Last Modified: Tue, 24 Feb 2026 19:33:20 GMT  
		Size: 226.0 MB (226029827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-rc-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e749ae338c1cba6ecd1d75e8a52b82f12b9df1969b6a4677ddf18698d441231b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadfd98c2d8c8b88a611db6d302e6e52901be6f186bb5d7a354330039eb4aeae`

```dockerfile
```

-	Layers:
	-	`sha256:5cac3d93010ef4d3f51de3d122046109f7b265a7403dc1be4ea5925dc229eeaf`  
		Last Modified: Tue, 24 Feb 2026 19:33:16 GMT  
		Size: 2.6 MB (2649354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9661392ae3268b6addeb1a77da867415d4be25a01a7a37a67fb9bd4247dcbdba`  
		Last Modified: Tue, 24 Feb 2026 19:33:16 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json
