## `openjdk:23-ea-14-slim-bookworm`

```console
$ docker pull openjdk@sha256:44818c5d50ea9e1b478ee365137b4e9bf4f0f739bcc51f68cc5aad4b1448cf30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-14-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:416d233a35bac62bfec0a1210793c1c0c0e087d4684e8daad7edac2bd2263e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236064590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e59b9ada4c1997df92701de611a9b1df1c8718895f192facdb309303c33c98`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Mar 2024 00:48:42 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 00:48:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73517539e2e020e29f798e00616aa4dd52436b07c3e9f9371185841d190feb30`  
		Last Modified: Fri, 15 Mar 2024 23:55:52 GMT  
		Size: 4.0 MB (4014993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef1616643f626f1cc4ecee28feb0285fb146e121ed596bb7709bb5c80933423`  
		Last Modified: Fri, 15 Mar 2024 23:55:55 GMT  
		Size: 202.9 MB (202925416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-14-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:a9d316c203d5184be03cef6803cef41ff05a9f660cbd6f241955317892db7f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03203a8da17958dc8547394f03c1a5fb39b44968f21344b0093e195fe4f1a34a`

```dockerfile
```

-	Layers:
	-	`sha256:9bb0f58e98795e0e2277c982cdf59a7af4b6c81ae86653459baf74868a894dcd`  
		Last Modified: Fri, 15 Mar 2024 23:55:52 GMT  
		Size: 2.3 MB (2347504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e64859442d4b7073a346aac6b6fe6ce8c583437b645fb779f3e21c4bc358c3`  
		Last Modified: Fri, 15 Mar 2024 23:55:51 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-14-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bb4fcdcb0a3da4325389475d2084f7514e9b804c44d708f4cb35a3782a4f3617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233770341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3b0fd47974166a99da6070511f00e76d2d06ba6ba83fa8872fd87e384188c2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 15 Mar 2024 00:48:42 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 00:48:42 GMT
ENV LANG=C.UTF-8
# Fri, 15 Mar 2024 00:48:42 GMT
ENV JAVA_VERSION=23-ea+14
# Fri, 15 Mar 2024 00:48:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='9305399006d6c477d1c84cc48d42d44839199f603c1802298225c13160f1d9d2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/14/GPL/openjdk-23-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='7eb97e59d151dbd147eb589d4de888a522e5f5ec8688a65465ecc8ddee5a0f84'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Mar 2024 00:48:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63bd5c67700cc24a2dc61525fa979c1c1bf6d9931d1c89140c1658dc404a1d`  
		Last Modified: Sat, 16 Mar 2024 15:54:12 GMT  
		Size: 3.8 MB (3820092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704a1a11839259a7ecad6697a081e84ee689693ede0b1750618e5c6f51375660`  
		Last Modified: Sat, 16 Mar 2024 15:54:16 GMT  
		Size: 200.8 MB (200793815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-14-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:5c5a0ce9f9b5d8640955e4065689a9573fb2dd4297e8a4b012b7885bd0ba0adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e04573ef13558a70a3991d92a7933394bd2cc608751afc5067774f3c4ca018c`

```dockerfile
```

-	Layers:
	-	`sha256:180052ff15ec94565d5462afb8de2d69814cc649341d58910db411432c539604`  
		Last Modified: Sat, 16 Mar 2024 15:54:12 GMT  
		Size: 2.3 MB (2346772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c668a86571f3c8beb51f43b1eb5b11ed27365c3212eddbc57c2c6dfe7422e0`  
		Last Modified: Sat, 16 Mar 2024 15:54:12 GMT  
		Size: 19.4 KB (19370 bytes)  
		MIME: application/vnd.in-toto+json
