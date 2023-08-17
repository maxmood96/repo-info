## `openjdk:22-ea-11-jdk-bookworm`

```console
$ docker pull openjdk@sha256:13f8558a399468662e0a64c1b2b9533687af5c4c831634b0a39aaf407a31fc70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:22-ea-11-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:11c085aba4d964cc70a6a0f3698cf0d09abd82f9af26314e03470ebd31b45b98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358150605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bead1a924ee14689d39af2a4a2dc033e36e7d5fbf02ac7b91ba988923af74048`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:49 GMT
ADD file:ca43018e3d97d44b49e60fe002bb20834a74cc1163d7e95ad50d549f072de158 in / 
# Tue, 15 Aug 2023 23:39:49 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:21:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:11:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 16 Aug 2023 04:11:27 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 04:11:27 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 21:47:04 GMT
ENV JAVA_VERSION=22-ea+11
# Thu, 17 Aug 2023 21:47:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/11/GPL/openjdk-22-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='dce8ce5e81ef514ed2faafa3099af148988d8ef1faf5bdd4f7775eff0c3d6179'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/11/GPL/openjdk-22-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='12210754c3958bf625bcd480cc2381c1059dff46c417dcbe71f0baff189f7df0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 17 Aug 2023 21:47:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a014e5e7d08c37cf1703b97e701ccdc850e4a18d0ee679f03aa875dcd520aa85`  
		Last Modified: Tue, 15 Aug 2023 23:42:59 GMT  
		Size: 49.6 MB (49591310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715cea74ecbb15cb82efef1e77dd60c31d90b01d1286d6f39b4562afaebe75f3`  
		Last Modified: Wed, 16 Aug 2023 01:38:30 GMT  
		Size: 23.6 MB (23570046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003f1109a21287fa17dc866e87e8c6685113960cbb0379fee8f42b83de63c647`  
		Last Modified: Wed, 16 Aug 2023 01:38:47 GMT  
		Size: 64.0 MB (63988473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e1d2ce07002848455170902f2b6ea91a492e5b318bc6ae2fb7691c51b7e9ed`  
		Last Modified: Wed, 16 Aug 2023 04:16:10 GMT  
		Size: 17.7 MB (17729096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0901664667df4cac6480c0f32e366f434193016cedd6434e7d4fdfb5d13f7435`  
		Last Modified: Thu, 17 Aug 2023 21:50:23 GMT  
		Size: 203.3 MB (203271680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
