## `openjdk:23-ea-11-jdk-slim-bookworm`

```console
$ docker pull openjdk@sha256:0cd4918422ceb32dc0f19700f8a4a2c3b89b270c51db6217c89cb78544b5518c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-11-jdk-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:db301ac83f97fd5dbfd8befdc0a10a19113d480c15fc17d5085c1cfe175d82e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236408208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a3ba29ec1ccc279ee04aaa7f9ccb9b4c2aedac54293f3ddfc37115935fa10c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=C.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da61041b6fe080a3cdea0dd96b5cacb9b1507c4687f5b7cc68299176edf8a893`  
		Last Modified: Fri, 23 Feb 2024 18:51:11 GMT  
		Size: 4.0 MB (4014974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba31301c73a068d180f2eb1bbe72a60a03b6852363a7772bec0e6d3a04f750f3`  
		Last Modified: Fri, 23 Feb 2024 18:51:18 GMT  
		Size: 203.3 MB (203269143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-11-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:34540fa08e9c2bf8f73eb1e6aabda0b0df45af94535be4836efbfbee50ad2dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012d553ee9a39ee144d936e54f5400d781cdb9f8e16305c8c4aa46e9e373452e`

```dockerfile
```

-	Layers:
	-	`sha256:ed2e7642eebc391315f4ac0fcc02cc649ea07cb4ac441588b6d845459695b0b4`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 2.3 MB (2347502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40cd245e07bd18b1677547999b8af6c4e77c029ad548ac7c53ab4777c2e601ff`  
		Last Modified: Fri, 23 Feb 2024 18:51:10 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-11-jdk-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:da6d90163a7c7fef31f37d560af66c52621fcc155c33ba2aa69f0f9c4cfda6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234147393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8250a506ce5e220ac5df0e4b982ab011691fdca2f0e7438818137a4848e2a7a2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=C.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1e9c7916a6ccf7810e822d985a2f9d022599aef32a11c6676f3590484cf2cd`  
		Last Modified: Wed, 14 Feb 2024 01:16:16 GMT  
		Size: 3.8 MB (3820100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bec951b32b71bb74bb6d5daf7c25bea3b2faf79c6f8ba8aa64542060e6f6e82`  
		Last Modified: Fri, 23 Feb 2024 19:04:40 GMT  
		Size: 201.2 MB (201170930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-11-jdk-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:2ddde755efee0e0cb485a4d66a9ddecce2378fd2c2b7b77132a0eeb36c02d805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6205a7581e630058ba44f52f3ee0e8bed43c9a610e06f71919fe4a5e3cc566b0`

```dockerfile
```

-	Layers:
	-	`sha256:b9ae6957a105f0127abcb295033ad2d06f20a40b146e2953ab7c26de446e0880`  
		Last Modified: Fri, 23 Feb 2024 19:04:37 GMT  
		Size: 2.3 MB (2346772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68201122642d6074c5ab8ab11cb4d2505a74907aa260581eaab135a04f9b26b2`  
		Last Modified: Fri, 23 Feb 2024 19:04:36 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
