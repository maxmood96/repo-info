## `openjdk:25-slim-bookworm`

```console
$ docker pull openjdk@sha256:fba49efefe0286d1d52eeb90786315922b40227ae31072a60add3a1e00e262d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:4de2ff2f39c50dc84c8e4de107ba07a7e06cbb2eaa1523d4fba937301a8aa605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255012671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb19bd90665b1dcad8ef76fa8eb1cfeebd174098d6931dcff4cb46072b6417a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3b45af26c2a7719ad18c3a80fd0cd22dd05d2e543c5243fe747637a6d721f1`  
		Last Modified: Tue, 03 Jun 2025 13:39:03 GMT  
		Size: 4.0 MB (4019965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebde3ec1f95bf63caad789a5fcd96c882fcd4db841fdd4b6a9f7ce4b4cea3bd2`  
		Last Modified: Tue, 03 Jun 2025 13:39:13 GMT  
		Size: 222.8 MB (222767376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:f01d0581594e2f1a37ddfb8339647d431d593071e3584884a973e48c2aff0cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c6e0e5e2ddfa324cbed0756af479acd79ae01a2f789550511e3c15e138adf3`

```dockerfile
```

-	Layers:
	-	`sha256:b390710e33f23bb4a2f0021b2b778e67346e5ac4c95a76fb968e13677f67f268`  
		Last Modified: Wed, 04 Jun 2025 07:55:22 GMT  
		Size: 2.6 MB (2553977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16beb783d79b60bc8e4cc42f67b42c96b404fb243271fe52834cec1f2f78e0ff`  
		Last Modified: Wed, 04 Jun 2025 07:55:20 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7106a4815fff079a4c11b72e06dc37d528f7188ed7514c67191864c55023fca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252457400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c70224c19511489ed04fbd027e025561478c46795a2ec774e1b340dbd7614b1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 30 May 2025 06:48:10 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 06:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 06:48:10 GMT
ENV JAVA_VERSION=25-ea+25
# Fri, 30 May 2025 06:48:10 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='bc7d25b610ced7056d3985b35440337c5dd07818d8929a0dc247b7b3669712d8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/25/GPL/openjdk-25-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='3c4453d1cb4eafc8899b51154215251d72b551482710d30ae725e70012b311fc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 30 May 2025 06:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8146c9804947f80186d66b9250eee5d43b401e06d60a6f4b0867bfcea74b84e`  
		Last Modified: Tue, 03 Jun 2025 16:25:08 GMT  
		Size: 3.8 MB (3835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b088d0829c9fbe41da18b65e9384eaa0c2be62f9eb406ca21f37842139a63f11`  
		Last Modified: Tue, 03 Jun 2025 16:25:39 GMT  
		Size: 220.6 MB (220556855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:4b5cb5c1996fe6d5b8589c2d199415079d6d4d6ef818e239a13796dcc51ddae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2573364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144e89876356d0695ca6a87e045c06d507aa2a65d73e43387094a741ea390ea1`

```dockerfile
```

-	Layers:
	-	`sha256:59ccb26bf82ebfbc691406119cc6344d700e6cc53942230def88b38ed6147bf3`  
		Last Modified: Wed, 04 Jun 2025 07:55:22 GMT  
		Size: 2.6 MB (2553707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99302ff40709e6fa673c498716f59f7664c4a1b7d4d24a04d97241c9bb57c23c`  
		Last Modified: Wed, 04 Jun 2025 07:55:21 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
