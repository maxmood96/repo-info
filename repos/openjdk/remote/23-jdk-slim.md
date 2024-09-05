## `openjdk:23-jdk-slim`

```console
$ docker pull openjdk@sha256:7e7ee1ee0e0e4819beb1a4b04b4035f34df405410691459e05c10a859661dc35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:96c9f6d7bc8556b787ca5103e08b8ba4441a07c2a4efe78d7bb782d728b25c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244594436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e419d13420ebe46cf290e7b098b4e784de3d7d4970d134b8c06c5690ccfa4e7b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249d8fef5e461e8a2b7d76faead69e1c0f57e7449173cb02c3d969f3491e1c85`  
		Last Modified: Wed, 04 Sep 2024 23:11:40 GMT  
		Size: 4.0 MB (4018064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21c214f0b6892c54095b7e38a18fa574cc9ecc0cfb9237d0c1450aeae42d855`  
		Last Modified: Wed, 04 Sep 2024 23:11:44 GMT  
		Size: 211.4 MB (211449888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:f1e2cd2e5cf8852d5a0cf732c88808bc9d2d748dbf116a86a2754b2c16f6c3a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0591d25597ac52a95dca871c654b81271d07f9244fd283be231780d1b6f07ef`

```dockerfile
```

-	Layers:
	-	`sha256:2defffa1c89d63952d34ee21860fe21ec37c355f8e050258a0e902e243775e15`  
		Last Modified: Wed, 04 Sep 2024 23:11:40 GMT  
		Size: 2.4 MB (2363986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944b88ecdbcc2d78fb2b768a84b1b0fbea629dc275efff53eb58ab9748179ee5`  
		Last Modified: Wed, 04 Sep 2024 23:11:40 GMT  
		Size: 18.0 KB (17990 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:271139527a2694aa3699b6bf970d3bffb46b6050e20ec90fea6d3623943e885e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242326673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec065b37cb22f18eb094efa28bbe89b1483c1aed719e9bd18b64c496bab1466`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ad1a7b135cfc20b14fe8f939339288000b4c174fe96fc371a457db5dda174`  
		Last Modified: Thu, 05 Sep 2024 12:58:44 GMT  
		Size: 3.8 MB (3833434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd56b330fc12241845600bc32ae51f1af7b35a3822eb82183e882ba00aff9045`  
		Last Modified: Thu, 05 Sep 2024 13:02:55 GMT  
		Size: 209.3 MB (209336694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:cc9f463e2a76c95e9483ce7caa3c730c4d69f1347ee010d292b8ae8e0a405603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d21f30102617bac0bc1b08ec52ef67e5edc3c833c60335a138293be07a04aa`

```dockerfile
```

-	Layers:
	-	`sha256:77d40b9c248ba6a05a548d96afc9fd509391c45fb8b964ceac9910b1efeba255`  
		Last Modified: Thu, 05 Sep 2024 13:02:49 GMT  
		Size: 2.4 MB (2364292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2cb284928842db3c28fa1ad61885977d04543b49ccb271d17ad41164a099ac7`  
		Last Modified: Thu, 05 Sep 2024 13:02:48 GMT  
		Size: 18.3 KB (18345 bytes)  
		MIME: application/vnd.in-toto+json
