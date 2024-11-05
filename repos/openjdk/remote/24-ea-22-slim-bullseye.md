## `openjdk:24-ea-22-slim-bullseye`

```console
$ docker pull openjdk@sha256:009dfb9b46868ea39006a0a5d003f1e29df36e7e185ceba90f1ebaedd8cd7376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-22-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:5791c61e5cf2425a3fc139a2574dd743e76ccf6bed74901c079250739ce3a6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245207448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db9509506ed50f98e3b34171223f32d7db91290815db51228aeb41bc31c2ee1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab2d6107ae178cd835732d2a8f9dccfec6e3bbabb47994f2f92a8ee6fd39337`  
		Last Modified: Mon, 04 Nov 2024 23:07:35 GMT  
		Size: 1.6 MB (1581809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9994396a8affbf678b2d0ccbf7e442b5a338b8ca0caead7ecc4e506069a6b413`  
		Last Modified: Mon, 04 Nov 2024 23:07:40 GMT  
		Size: 212.2 MB (212196839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-22-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:ba843341eb01e4f285657d0b2ce1beac00d22abf5ea28856b52bde054dd0690a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef4f86b9aacbc4af86a9d01728e1845d99b293bfa82cf4fcf839a7d362d7ebe`

```dockerfile
```

-	Layers:
	-	`sha256:11c4cdcf7460e16c944603bd80680d91e088ef47c6637791f4cc3a8b3531791f`  
		Last Modified: Mon, 04 Nov 2024 23:07:36 GMT  
		Size: 2.8 MB (2812354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35732c311e4961ca8b32b85a8e04b1522ca607b07490319f359c82c552b92d1`  
		Last Modified: Mon, 04 Nov 2024 23:07:35 GMT  
		Size: 17.4 KB (17392 bytes)  
		MIME: application/vnd.in-toto+json
