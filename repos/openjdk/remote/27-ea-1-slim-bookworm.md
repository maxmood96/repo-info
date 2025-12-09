## `openjdk:27-ea-1-slim-bookworm`

```console
$ docker pull openjdk@sha256:dea37426b28bea93f43b671d4c64518b61bf82e1db2cebb536a9e01879bf6b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-1-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b73a64cd4bc047bdb00ab76a0ecf174085bc8bc988fce0dfdbca9a2ddfa8c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260310716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d41143177eb9a530d8c9259e3254b550be8a55d1a99aac7bce3a73e58a8234`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:17:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:17:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 08 Dec 2025 23:17:53 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:17:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:17:53 GMT
ENV JAVA_VERSION=27-ea+1
# Mon, 08 Dec 2025 23:17:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 08 Dec 2025 23:17:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33666a827d9d781719c587423b46875cb81fd3f088805158eb1cf4098498cec`  
		Last Modified: Mon, 08 Dec 2025 23:18:25 GMT  
		Size: 4.0 MB (4027319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63070a2ddd39884baae82a12670b37048ef86f48a37d89ce6cb5bc084e24681`  
		Last Modified: Mon, 08 Dec 2025 23:20:57 GMT  
		Size: 228.1 MB (228054979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-1-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c1b8dda28a1309d7c046228dcd9c44ae006bddf5392b161f2e6edcb7b1bfa2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bbbc781b536e42f539c6e14831118bbf6b8b1894c6a25adb3eb6f5d795c984`

```dockerfile
```

-	Layers:
	-	`sha256:83cbc6f25d801b633390f9431734ed1e0c1515d1a9e04671b530a2607253af4f`  
		Last Modified: Tue, 09 Dec 2025 04:25:18 GMT  
		Size: 2.6 MB (2649777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced409d8d0973dbc891ff401ccf66cf8f17e97bb956e0932ba014eea1b26b276`  
		Last Modified: Tue, 09 Dec 2025 04:25:19 GMT  
		Size: 16.9 KB (16857 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5097a2f11c5b231814217758d76fab41b5ec7963c265f3f9483b78852d6c3fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257913327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b8f1fb267ef11590c680c14c8940bb754ba16930f2817217b780cb21e2d3e9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:21:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 08 Dec 2025 23:21:34 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:21:34 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:21:34 GMT
ENV JAVA_VERSION=27-ea+1
# Mon, 08 Dec 2025 23:21:34 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='1aa364bd43fc19955536763cfbf4ed9019a9766283b6b00c7813301c229ac2ff'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/1/GPL/openjdk-27-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='48552e3ba3f4c8a08d0078fe9af2c25a1145a36e3cccdc56f61aa90786cade22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 08 Dec 2025 23:21:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba1c300c4562826585c1863d16680f0f2d64506114a43a9282cfb8b25263394`  
		Last Modified: Mon, 08 Dec 2025 23:22:06 GMT  
		Size: 3.9 MB (3851422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1eb3f9437cfd201044ee0c1d58d28b832806806033df38930738e32bd3f2a9`  
		Last Modified: Mon, 08 Dec 2025 23:22:18 GMT  
		Size: 226.0 MB (225959676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-1-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:96f77fb1ed37ef25fc71c3205de435ef9353cf0cb5c05ace861e468a51105ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b242d0a27b44555a08896670c9832e4caa6ec85dcadfc21168227012033146`

```dockerfile
```

-	Layers:
	-	`sha256:5ef90f6ac21eb35000c47d4c970f46bbdb2dda9d94f12cad521d85fb81296418`  
		Last Modified: Tue, 09 Dec 2025 04:25:22 GMT  
		Size: 2.6 MB (2649411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f974690ca3750cb327340124d6c756a5603052fa4973a311b1638cdd89e1f0`  
		Last Modified: Tue, 09 Dec 2025 04:25:23 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
