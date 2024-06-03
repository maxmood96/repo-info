## `openjdk:23-ea-25-bookworm`

```console
$ docker pull openjdk@sha256:7c6c90349faf18d77b90ad9069a99f7d7d9c7f4beeb6bc641ed0cc58e1615f7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-25-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:700cc7e239f7196b0185fbae048a0146491c45f894c74199733022ea947c9741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366014892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d04e1f4caccad1a99711f3bdfe83dbf63220602ae958e8ee53b25dd0a6aa1e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 31 May 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+25
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='155a1386301d0ac6cd1ce5769b31f550bb400d652f4211454b9988bf25fa173d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b00cd1591ad9727c48c07e598f57cdec15fa40b605ae712b67f35f221534d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33424f4dacca3f83b128e905560e732d9e1d8a177506041232fe05b4c5e2cc8`  
		Last Modified: Mon, 03 Jun 2024 19:01:05 GMT  
		Size: 16.9 MB (16949391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfff797443deabc2fc9d6db0e00fe2a115b0812158d21ee70ead07a9e7bbba`  
		Last Modified: Mon, 03 Jun 2024 19:01:08 GMT  
		Size: 211.3 MB (211296640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-25-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:1280e484879377d04c9ef0e2da8e570b57e32b2377ec11532b8b9f767a27ebf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8240240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852f39a58f616e94467c11ca1e1ca2e4496265cefe3151686a3bbae7f15c439a`

```dockerfile
```

-	Layers:
	-	`sha256:f1669e40584a297e112169a9233fdfefd40f5427058531cf43c688fd5a3558b5`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 8.2 MB (8221827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90dd94d668633ca211ebf7940b2b66fef5cdf28acd6212e4f59b351004280e72`  
		Last Modified: Mon, 03 Jun 2024 19:01:04 GMT  
		Size: 18.4 KB (18413 bytes)  
		MIME: application/vnd.in-toto+json
