## `openjdk:24-ea-17-bookworm`

```console
$ docker pull openjdk@sha256:527ae09fc0a98e0f3d9bef5f38b0a64f6ee3a3bc266b9667caf4d84f830edc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-17-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:01f4c195957e80e45a365850a62b6a3fbf49a0ea90f1fe777764adbfe93a70a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367197120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d356dda04f587244ba57be3c67d86f9e04bea5144082892610bebde70b01d8eb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 27 Sep 2024 06:48:27 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 06:48:27 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_VERSION=24-ea+17
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='983faf25eff38b5b396afabd191a91b239a1d803a0dadd01863861ecf731f034'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9eb980b4f1fde9c2387e0fab6b91b6f68cb109e3ddd43eda0013d9ee345f2dc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f0752e2f6d985e3b2e91465fc1226a60c1e5931ea75481d4a967f1d012d283`  
		Last Modified: Sat, 28 Sep 2024 01:01:23 GMT  
		Size: 16.9 MB (16943004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e90a01fb0eb8567f5a02f83f45a2d8786520df956828199a1db867f0107e98`  
		Last Modified: Sat, 28 Sep 2024 01:01:27 GMT  
		Size: 212.3 MB (212253693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-17-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:64b267f54d820769c2b0326e546df5020f7acaa94e637cbf9c654fd28245e524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8421979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ba2bac77b39e71e3ceee2d20569b1efcd74e6fcb8f5f23add5703290fcc30d`

```dockerfile
```

-	Layers:
	-	`sha256:6b555cdf982d3417d0fa6e54173ae7918f0b2376444f3bf0749ddb0086595885`  
		Last Modified: Sat, 28 Sep 2024 01:01:22 GMT  
		Size: 8.4 MB (8403516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c50b2fd67278f9569df464748ab0057d20de2f3ff7a5dfde1b9e78c59583e0e`  
		Last Modified: Sat, 28 Sep 2024 01:01:22 GMT  
		Size: 18.5 KB (18463 bytes)  
		MIME: application/vnd.in-toto+json
