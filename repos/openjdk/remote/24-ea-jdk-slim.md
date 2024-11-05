## `openjdk:24-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:a93533beb8ca7f847475a72ca29ab61ecc58214100c91f6db560e157c45515ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:4e35263c190f6e2ad8bf06ec24ce3e7b12bff8b88b8473da9a4cc9ac26f1b98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245351862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ab753e35bfded5e09f84b7edf6f241e1f82c6280fc5878244fc63ad118a10e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:29 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 17 Oct 2024 00:20:30 GMT
CMD ["bash"]
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 01 Nov 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Nov 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 01 Nov 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+22
# Fri, 01 Nov 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='623a217a8f87e35d4ff793f172e2c66ac4abdd9ff21835d7ad8b1f0e1ad83fe4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/22/GPL/openjdk-24-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='9a0070483615cc2db61a47afaec955cc7be38ec88f75856307bee73c9f601cbd'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 01 Nov 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d39a904317cf592902437b6e7109490236673d3d9347e2c7eba6e6971ddb76`  
		Last Modified: Mon, 04 Nov 2024 23:07:32 GMT  
		Size: 4.0 MB (4018006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab91b8f89e62de8d531f35e76fd8de5339f98fe4039cf7f5d5062b4805a8fd09`  
		Last Modified: Mon, 04 Nov 2024 23:07:37 GMT  
		Size: 212.2 MB (212207567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:22296ebcb8b765d41a01bcc755699372caef635dc1a54cdda16030ee37fb8524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6a040f1fcd7de7468fb8630845c03addbb404650c5b17431a03cc3573b4e08`

```dockerfile
```

-	Layers:
	-	`sha256:0cab440a9add95ca9c06eb0b93b62bf26bbd5f1a48da894ef26cc4afb0b2978c`  
		Last Modified: Mon, 04 Nov 2024 23:07:32 GMT  
		Size: 2.5 MB (2516068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c3c3982caf839d9dd7ac26dabd7cfa1ab00db791a46539865140cd012913c8`  
		Last Modified: Mon, 04 Nov 2024 23:07:31 GMT  
		Size: 19.2 KB (19246 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2ea5b373cbf4237f8afe96b984bd0d773b39c3690a47cee6f0df99a72d1ffe50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8dac50646d28a80eb3fec399f3fd8e2eafddea3ef8faeee3626a0267abe18c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 25 Oct 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Oct 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Oct 2024 00:48:11 GMT
ENV JAVA_VERSION=24-ea+21
# Fri, 25 Oct 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='c67029681a2f1c745c3a73366080881b2d349b4ffb9ce6a4e1e4b2c423555c5c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/21/GPL/openjdk-24-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='3850e8de3f5cc9a22fabc0963a04d6205a9f242cf2cfc0d67a4399a54deb725e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 25 Oct 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328d4e5e755a8c20be53048231731c59a31aa047ce2ed09fdda179c9357245ba`  
		Last Modified: Fri, 25 Oct 2024 23:02:12 GMT  
		Size: 3.8 MB (3833431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82734ca9dac622059fbda06c4929b34f8faa137b0ea692223848587d03ad0f5`  
		Last Modified: Fri, 25 Oct 2024 23:02:17 GMT  
		Size: 210.5 MB (210480185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:d88e9bec4c8a45e18fe3cdcf7c86ae121e64aeb57a0c9cedd9b975395f15b700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2534646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977aac7e7b5c40c970aa3b3bde4728a5fe7a12b15da22e9de7fdaa575504f7d6`

```dockerfile
```

-	Layers:
	-	`sha256:c54c82fc48e87e3426ce1f82f414c206fd3a13391673af26c822e9ba8eea0710`  
		Last Modified: Fri, 25 Oct 2024 23:02:12 GMT  
		Size: 2.5 MB (2515173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b5905502e3933a15d913162a847dcfadd6fc0940af2c454adcf06df4a30d29f`  
		Last Modified: Fri, 25 Oct 2024 23:02:12 GMT  
		Size: 19.5 KB (19473 bytes)  
		MIME: application/vnd.in-toto+json
