## `openjdk:27-ea-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:c22371735fc5cee16c9bd0c6314c52a05c8ad545b39525e8d78042e3268d1a96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:a0f87c076aa3c47b7c42190b270b55455daf9f5164e8e4298de811c75971550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260848026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0da3a62bf44031ac8ec2d236f01fe9e01cab049637ec8f7eb35eddb7693910`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Sat, 07 Mar 2026 00:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:42:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 07 Mar 2026 00:42:14 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:42:14 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:42:14 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:42:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:42:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee1dc1936964443c3b29688e973f23683cde7d8cc7e4590a44fe2cc8bb18a36`  
		Last Modified: Sat, 07 Mar 2026 00:42:32 GMT  
		Size: 4.0 MB (4029194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7709dc036e144dcc18ab36b72288a64fce451cdb67b7b4f5ef75cbc7371b079e`  
		Last Modified: Sat, 07 Mar 2026 00:42:37 GMT  
		Size: 228.6 MB (228582553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:7479672065db7ed5b306caade883ee7d7835fc58e5b02e6fed3f176e84f1e8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7953d675c1423c0df857413dfd5627e091ea47331028ba1519b1c5d6ed0f4ba7`

```dockerfile
```

-	Layers:
	-	`sha256:d02dc2936499caba6866857be3821b4cff4b466417b7fca939413881c9d67d80`  
		Last Modified: Sat, 07 Mar 2026 00:42:32 GMT  
		Size: 2.6 MB (2649807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5257cfd2e176062bb118c8148abcc8c8ef9607bba2a10fca4be78b5f4078cb8`  
		Last Modified: Sat, 07 Mar 2026 00:42:32 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9a3c43bbbf50c818aae15fa70c421ff5d4711e5c0533b9de29884f1aedcda55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258504996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e2bc37bd6e1983b64568452a7ca9e468b096f647a9b2e12ad382d01ae116b3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Sat, 07 Mar 2026 00:43:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 07 Mar 2026 00:43:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Sat, 07 Mar 2026 00:43:24 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Mar 2026 00:43:24 GMT
ENV LANG=C.UTF-8
# Sat, 07 Mar 2026 00:43:24 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:43:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='952af4c17b753724c0f1e7ac4cd90f73568c2121ac60a1ae05ff804481e2ae48'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='09bc1159ce7ffe4b495d58e30271250015d0d9902e670027e1491bc9f1cf1b52'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 07 Mar 2026 00:43:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c162ceb13096a84a3b7fa1d33301121b8c2c9f69467dd227624ca8e4510798`  
		Last Modified: Sat, 07 Mar 2026 00:43:44 GMT  
		Size: 3.9 MB (3852006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8077631a2f06e46945ef20b2064cb8c74035e48405d8adc291c6a36521b5a4`  
		Last Modified: Sat, 07 Mar 2026 00:43:49 GMT  
		Size: 226.5 MB (226536909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:29b36458af292541d964f5ca0589fcd639d5e0d10f9e6fd95e00e2d274e7208e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed6014c6eb22b7fa4bc4b433846a56ff394ebb1ab3392f66331bce36db7ef16`

```dockerfile
```

-	Layers:
	-	`sha256:a6cb5ce8711b99eb25a596389f3b39310885766bf9e9b4b00ba3bff20891ec20`  
		Last Modified: Sat, 07 Mar 2026 00:43:44 GMT  
		Size: 2.6 MB (2649441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7742aab189895a4c9375d7b8a48049e6635205b80c222395bfd660d6c02bd02`  
		Last Modified: Sat, 07 Mar 2026 00:43:44 GMT  
		Size: 17.0 KB (16989 bytes)  
		MIME: application/vnd.in-toto+json
