## `openjdk:24-ea-22-jdk-slim`

```console
$ docker pull openjdk@sha256:20f7a233bd7032cd05af7eca1b0810b69e9f37782aef97fca381f52e78af422e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-22-jdk-slim` - linux; amd64

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

### `openjdk:24-ea-22-jdk-slim` - unknown; unknown

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
