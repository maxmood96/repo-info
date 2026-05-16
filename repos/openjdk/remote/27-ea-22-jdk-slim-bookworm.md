## `openjdk:27-ea-22-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:7a427b405022651a7236e65d57b99eb26333a3f85fc21c5746d862641060b00c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-22-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:efea2e165a38d09de62fceb75cc4af6daa9d5b468bdf78a765e56ee7fa97a74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261239349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1873526b5e58ef20ecef20cb7bdad35906f097b12e9c92360e1e24517552654`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 20:18:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 15 May 2026 20:18:44 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:44 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:44 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:44 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50813eeddaefc53775295350ba9322af56b932df0bf4ffc34dc49e27f73b649e`  
		Last Modified: Fri, 15 May 2026 20:19:05 GMT  
		Size: 4.0 MB (4030732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d698ab0ef5038dbb16439f77d86f66956038a0391bbdcfeb38c4f7f0a154869`  
		Last Modified: Fri, 15 May 2026 20:19:09 GMT  
		Size: 229.0 MB (228972335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-22-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c06bf4157af39bb781b35811e2fec30a912d33920096abe060f51bc25815aa52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d52b2cbab9120d50c3c24a545b705c4b4307357f353044f94ed4daa4f151e10`

```dockerfile
```

-	Layers:
	-	`sha256:723b7e9ca528f47c97864bb1671da290f24cf00759ab844d75376c7c53ae9e6f`  
		Last Modified: Fri, 15 May 2026 20:19:04 GMT  
		Size: 2.6 MB (2648537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0eef9724203aa87d0e4c6404a4a2c469574209b92fbe9fe79dfa481d40735ce`  
		Last Modified: Fri, 15 May 2026 20:19:04 GMT  
		Size: 16.9 KB (16871 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-22-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7a6dea1b755044359a927f5b02d6ce01c46c3817555d25af746002eaabdc334a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258893461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e267319551a9f193f432074e0bf3d01d9130c561058b94445c8eaafb061474fb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 15 May 2026 20:18:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 20:18:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 15 May 2026 20:18:27 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:27 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:27 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:27 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b8ed3963913f8ee24a7b5f0e288c8a6f3c08b8aadc0308436cb998b0dc431`  
		Last Modified: Fri, 15 May 2026 20:18:47 GMT  
		Size: 3.9 MB (3852312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd33c390156060b55dc3b7b9fa383e908a317ce3edfa6fb7620f21fa2172f7b`  
		Last Modified: Fri, 15 May 2026 20:18:52 GMT  
		Size: 226.9 MB (226924984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-22-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ab99e9ca8dccc3b75e15083d99e5650e422bc5293cade9b3412a90491cc5f362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103a8349f625caba341832a43fbae1c2e3fd7a1297c0e615fc01681feda1c32e`

```dockerfile
```

-	Layers:
	-	`sha256:032b51c7612f8a8b63d1187bc9c1c0df66340ac891c2f5f8129440d6209dc5c7`  
		Last Modified: Fri, 15 May 2026 20:18:47 GMT  
		Size: 2.6 MB (2648171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa90d66f8f74116a2e03d1451878a60518ab6a7086deaaf62b112f4a144df62`  
		Last Modified: Fri, 15 May 2026 20:18:47 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
