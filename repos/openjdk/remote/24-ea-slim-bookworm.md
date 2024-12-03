## `openjdk:24-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:d94c810a40d41a831e25a9d6cec0143351bcf9e8b8b24a2207f475ce1f1fbb6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:9ea460a7005d5dd5dce48b3a89e86e9a3fe12d2ecfd65bf9ec5eb4fbca8d0c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245142154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc35bb47906dd1afe6b89abb1c3cbea0ac8c136cdacc06670bb4a7fadaa670d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 22 Nov 2024 19:48:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 22 Nov 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_VERSION=24-ea+25
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='06d2571c8af4948ac1eaad2b912ab59f320f01744bc4152f3476a65512bb3901'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='022d2edea028f26d0aa8cc933429f305abac8f8a74451095a55b1354f0db7966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86244bea353ad5035b29752094d0686c6dc1c3b9701af2596a93ce5d3a301da`  
		Last Modified: Tue, 03 Dec 2024 02:33:06 GMT  
		Size: 3.8 MB (3824662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fa8f185a59ba8350451a495c7d0267be0f150a76baac4b5d12ce2299d4cc96`  
		Last Modified: Tue, 03 Dec 2024 02:33:09 GMT  
		Size: 213.1 MB (213085912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2accdd54d0ca9d9a1299d62bbcc34b92fc947c5c2419551b27f810875dcde60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fa00c28e3e7c7d57f7128a696ec3523a888278a60c13394dfa3f2153927f33`

```dockerfile
```

-	Layers:
	-	`sha256:8bc531cf57db511475e5f77415c2efecc8ada3faf5637bc9763e5f8180c59fcc`  
		Last Modified: Tue, 03 Dec 2024 02:33:06 GMT  
		Size: 2.5 MB (2531683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7732d5c31d530af21483d9b74311d1e9343a8de356a684f0b074e572fc71dd86`  
		Last Modified: Tue, 03 Dec 2024 02:33:06 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:16fec4086dcbc04e77fef2b5385c70671f52cadfc4d68a4023fb842ab8303453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244029150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebbeb5be6880463af28e90e824575e5d67d34cf588f63e82efda885cc9639b1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 22 Nov 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_VERSION=24-ea+25
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='06d2571c8af4948ac1eaad2b912ab59f320f01744bc4152f3476a65512bb3901'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='022d2edea028f26d0aa8cc933429f305abac8f8a74451095a55b1354f0db7966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4673eba2ce884b45695c35e47e79fd06460ec1a9ccf94078b7ffec6a8236bb1`  
		Last Modified: Mon, 25 Nov 2024 23:28:31 GMT  
		Size: 3.8 MB (3833740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150ff6a9aa4c7dcf6042fc79b0caedc97a0cfdf80e7568a217795b4c5bbdfb5a`  
		Last Modified: Mon, 25 Nov 2024 23:28:36 GMT  
		Size: 211.0 MB (211038054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:e0a9ccd605fd1fef5a49ac1c9a3985f678e527c33e9d8fa5b36bbb2d81c8f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea23b8ace7eddffb7b1903091cbe6552e45df0501a7b6439623c9040712526c1`

```dockerfile
```

-	Layers:
	-	`sha256:3118181c8c4cbf7da8ba3ce13d61fbc55dde89afd7efcf310eb0d3c1f77a1197`  
		Last Modified: Mon, 25 Nov 2024 23:28:31 GMT  
		Size: 2.5 MB (2532659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4484b8c7479c5376840dd808245f432001dafc92276a29e1388d7d3ba1e669f`  
		Last Modified: Mon, 25 Nov 2024 23:28:31 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
