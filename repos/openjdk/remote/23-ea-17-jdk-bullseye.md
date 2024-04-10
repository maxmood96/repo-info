## `openjdk:23-ea-17-jdk-bullseye`

```console
$ docker pull openjdk@sha256:f8ca902eb51f4060b8be18ff86251666fa48f2bb0eec53cbb0410d1d3a39fffd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-17-jdk-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:786fc49d325768140152a6e0f49f1ab392654606289ef1efe8fabe28106cbbf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350471815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930c1b5255f7be11ed994f884e1c337072f7ec4d9198e4e9b897bb444a6dd674`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 04 Apr 2024 18:48:10 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1398841c7f8f6076829395a84b36cc7c9ab671abe4d8eb797e2041fd904f5b66`  
		Last Modified: Wed, 10 Apr 2024 06:54:03 GMT  
		Size: 14.1 MB (14071345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d792a7373242092915990590a641ae0a75a27c85d7eccfc645c7287164ee7671`  
		Last Modified: Wed, 10 Apr 2024 06:54:07 GMT  
		Size: 211.0 MB (210957945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-17-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:1e4e90fd8d42bf5fef483a48de27cbac6e82778283c1f5a1c8b96e957398d23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e4ea7a12f1ad09b1fb164e37663678aa8a66630b3e709599d7daf981fb07ac`

```dockerfile
```

-	Layers:
	-	`sha256:915f18e51d66548ee07fa751f51f973a39d815d1d56d534dccd13c09a5c1b141`  
		Last Modified: Wed, 10 Apr 2024 06:54:03 GMT  
		Size: 8.2 MB (8157041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28dd375160836fd075697df0fe642c0ec31595f060d93957d2a0dbff98176c8`  
		Last Modified: Wed, 10 Apr 2024 06:54:03 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-17-jdk-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fc0bdd0b90bebb9093434098330c9a8319756df9c0507d6ba5d4e9c1e7a40b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348534836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996551fd35bb18a35c2a748783350901deece873809192deef186d257a724914`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 04 Apr 2024 18:48:10 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Thu, 04 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+17
# Thu, 04 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='e7d451c3caeb76083337f090da37588acb90bb60417bff99ef160a3a8b730bfd'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ede1afd67be11e1e99e13b78f8b3159c14107cc919920d0e1e30636f67b92b0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 04 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30b8c5389ca3462453192b2d7fc54b23f09cb28a8493cd3552017946cf27e51`  
		Last Modified: Sat, 16 Mar 2024 15:55:17 GMT  
		Size: 15.5 MB (15526011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e5fb8bf73ac875ac14d11208fa9a450f85181bbadd030b2b3a34412200a109`  
		Last Modified: Fri, 05 Apr 2024 17:59:45 GMT  
		Size: 208.8 MB (208843222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-17-jdk-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:73999915365465127900290a3ebc4012402a69d06020f8029963832a23e1256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8276151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3038e8c32f0d86cff3d533e34f142cafde5aca56219303403875c81a4a481d70`

```dockerfile
```

-	Layers:
	-	`sha256:68500329a6c82f384e392652730962f56c88e4b4ede3af571a3a9c63f5d00860`  
		Last Modified: Fri, 05 Apr 2024 17:59:41 GMT  
		Size: 8.3 MB (8257727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd4807143a3c5beb3c461a65ecc6b278704630434bee0cac273390e978d71144`  
		Last Modified: Fri, 05 Apr 2024 17:59:40 GMT  
		Size: 18.4 KB (18424 bytes)  
		MIME: application/vnd.in-toto+json
