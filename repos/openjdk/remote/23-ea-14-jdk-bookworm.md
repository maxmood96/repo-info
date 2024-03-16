## `openjdk:23-ea-14-jdk-bookworm`

```console
$ docker pull openjdk@sha256:a185d066b29d244698d758b486ec8ac2cd929d295b24eac43ae9cd74f7cb7693
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-14-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:8c3f158ebdae72a41b77e32348fe7354132d8d2cd27ec2348b2b92b3fc10a2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.6 MB (357560622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a22829a417843017c4112c14bcee12b73a8950c11ab6406942ec61e0defd625`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Mar 2024 00:48:42 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 00:48:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f899db30843f8330d5a40d1acb26bb00e93a9f21bff253f31c20562fa264767`  
		Last Modified: Tue, 12 Mar 2024 06:02:43 GMT  
		Size: 64.1 MB (64140360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c364b454ff3f0b215b1f6efadf6d0f44f1cb5accfe9400aef358dff96aa011`  
		Last Modified: Fri, 15 Mar 2024 23:56:01 GMT  
		Size: 16.9 MB (16945720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1944d9e657de4c7fe193aa4c2130b353cb6beaba675e175ae5f2bc3ea8455f9`  
		Last Modified: Fri, 15 Mar 2024 23:56:04 GMT  
		Size: 202.9 MB (202875612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-14-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:188d044c17f442a090e271bb2eab6ea8b077041fa95802f534a220372d59ab13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe95b5fce8a99c9234118b3700a8561beb54157d176c4f087d23052a2d6f464`

```dockerfile
```

-	Layers:
	-	`sha256:975ed3167ca6bcba69d0321e9c051b6040595e57fec573525e945e512b778f0e`  
		Last Modified: Fri, 15 Mar 2024 23:56:01 GMT  
		Size: 8.2 MB (8229203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4950a5fe3156bb404b5b4ae705d68f03eda6c230caba9cbc518bdfbb1e8f1935`  
		Last Modified: Fri, 15 Mar 2024 23:56:01 GMT  
		Size: 18.9 KB (18907 bytes)  
		MIME: application/vnd.in-toto+json
