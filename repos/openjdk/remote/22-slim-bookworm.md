## `openjdk:22-slim-bookworm`

```console
$ docker pull openjdk@sha256:86fe336fa9807de6a02086ebae79f80ee1f61b21e4cf45967ccee9aeca8433e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:07fc2c3f4fbf62e1af2407584a870c2bee94e41e2cb3b33269d970e7265d1070
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238332335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b86d68057de2417f119542d22874f4b282f1cfc2350d96c6271ddf6c0e558da`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:46 GMT
ADD file:997f5a9b32407d96efac41a1cfafb318f77de077c8b5cd7065b6ec9796b4bf5e in / 
# Wed, 16 Aug 2023 00:59:47 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 15:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 15:16:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 16 Aug 2023 15:16:24 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 15:16:24 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 22:30:43 GMT
ENV JAVA_VERSION=22-ea+11
# Thu, 17 Aug 2023 22:31:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/11/GPL/openjdk-22-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='dce8ce5e81ef514ed2faafa3099af148988d8ef1faf5bdd4f7775eff0c3d6179'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/11/GPL/openjdk-22-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='12210754c3958bf625bcd480cc2381c1059dff46c417dcbe71f0baff189f7df0'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 17 Aug 2023 22:31:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:52d2b7f179e32b4cbd579ee3c4958027988f9a8274850ab0c7c24661e3adaac5`  
		Last Modified: Wed, 16 Aug 2023 01:04:30 GMT  
		Size: 29.1 MB (29124563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3598e3a6e3d078dcd510fa6b7615003c697e699b901ad502f44cd87ec886a707`  
		Last Modified: Wed, 16 Aug 2023 15:20:04 GMT  
		Size: 4.0 MB (4008027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62554109f116d637ebf69a61654a0d10855680e371257df106e1f8c83c807e4a`  
		Last Modified: Thu, 17 Aug 2023 22:35:23 GMT  
		Size: 205.2 MB (205199745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:590b34f28df08b5e07bd61aab56219253819c98ba8fa330c175a4a5cffbb37f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236538607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57400c97a38c04bdcc725eb0cb4b3092be51d91d4c208823dceccb2784536ba`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:57 GMT
ADD file:bc58956fa3d1aff2efb0264655d039fedfff28dc4ff19a65a235e82754ee1cfa in / 
# Tue, 15 Aug 2023 23:39:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 04:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:12:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Wed, 16 Aug 2023 04:12:03 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 04:12:04 GMT
ENV LANG=C.UTF-8
# Tue, 29 Aug 2023 00:11:39 GMT
ENV JAVA_VERSION=22-ea+12
# Tue, 29 Aug 2023 00:11:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/12/GPL/openjdk-22-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='e46c5ea4f8d5c55ba96ac2116faf9e31aae6f47c5317733d7dcdfdb8689ccddf'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/12/GPL/openjdk-22-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='92ab4cea6b4351893b5ce66ce559b3b98b138e7eb96c3acaba52b98747904443'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Aug 2023 00:11:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ee097f9a36616fddb52e45aba72142c4bc6f2e594f0a746e406acfde4f02f51`  
		Last Modified: Tue, 15 Aug 2023 23:43:21 GMT  
		Size: 29.2 MB (29157256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172099a50b305c337853db6cc8f37db4ddab2574750ef0c0ba2cb7a530828888`  
		Last Modified: Wed, 16 Aug 2023 04:16:37 GMT  
		Size: 3.8 MB (3817636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851898bda91ada16653a365d8d26b1c290ce11c0c0a1d99b461bf8615c6910f`  
		Last Modified: Tue, 29 Aug 2023 00:15:13 GMT  
		Size: 203.6 MB (203563715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
