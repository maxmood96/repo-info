## `openjdk:27-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:3cc7a4ff6b3342ceaa05e92aa8f19a37977faa98d04c72a481328300fff17437
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:fcdfe6ccdadee57747a8841d30ff1db718ed7877a3401dd9b17e33589421aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260866341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7b7d3e26b6f1116b1b396bd83178d626216e30fdf1e1aa6d963b33a1bba9c1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Tue, 28 Apr 2026 23:34:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:34:40 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 28 Apr 2026 23:34:40 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:34:40 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:34:40 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:34:40 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:34:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177b6523d856feca06d1a464ec40b1e47731e59786ebef17173d40575c95e005`  
		Last Modified: Tue, 28 Apr 2026 23:34:58 GMT  
		Size: 4.0 MB (4030611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91478cc67de84a47735dd83757bf47aa961b33c2cc9f84c94ad382e16a319bdd`  
		Last Modified: Tue, 28 Apr 2026 23:35:03 GMT  
		Size: 228.6 MB (228599478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:ce003a76d9b971e6b2a18a0892b4a063d2f153618f4efd3ec30f286fe706a07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2eec24b533486b2ca1ef92a2f031c4deac3c27a212a7c8bdca4d2f15b1968a`

```dockerfile
```

-	Layers:
	-	`sha256:7ceff7a9ea2902982b8a9e657aa1de97694bc60b1b1309c376e779dfd0d5bd69`  
		Last Modified: Tue, 28 Apr 2026 23:34:58 GMT  
		Size: 2.6 MB (2648537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ce11ff022eb933e7ff0f22284c6a8f300383b545deceba1d21e5b5e557b30b`  
		Last Modified: Tue, 28 Apr 2026 23:34:58 GMT  
		Size: 16.9 KB (16870 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ff3ef754e539957c2e219d2a480c6773c5e3d087939a67fc5628721897f8958e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 MB (258514268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ecbb456184872539261fd5afae91fa3dcf12708151b1326a1cd842ae80f860`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Tue, 28 Apr 2026 23:35:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:35:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 28 Apr 2026 23:35:43 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:35:43 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:35:43 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:35:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:35:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9ed2580edaa5b831643778686d22e1cf582aba8deb954147b3343838aeef77`  
		Last Modified: Tue, 28 Apr 2026 23:36:04 GMT  
		Size: 3.9 MB (3852308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e9ab0f041fec5e8ce0734b3618327b094a6851f940097516afa8957bc97492`  
		Last Modified: Tue, 28 Apr 2026 23:36:09 GMT  
		Size: 226.5 MB (226545846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:78974d203f0c5d91867500f5eede7991fa5b0ebc10b79162f01df591e840ab7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa2a280c75a3e909620f85d0d4c53b3fe544a8bb03b3170945388afd0371d82`

```dockerfile
```

-	Layers:
	-	`sha256:c42c6b42b0caee5a94a5e5060ec19f93b78e9104719617bd5c8a2af472b5d644`  
		Last Modified: Tue, 28 Apr 2026 23:36:04 GMT  
		Size: 2.6 MB (2648171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ebbedf63a55455d2963d139cbe8f9819d90f66eff257c2dc2acd18062ebf307`  
		Last Modified: Tue, 28 Apr 2026 23:36:04 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json
