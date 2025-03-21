## `openjdk:25-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:1e0b19ba320359b1c1aa22ddfd88467971b9ffac5e9b3166139453532c1d8a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:bc9a1271fa995bf10dd6e42b6b87288130ce584368ef898f7fe8687b387cc2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244190686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437c91066a5593b003efc8441f361fccbbeb98aee7141c3ad817c772cca655dc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7ae504ec2b283bef65765fbde3d563317be73c4bd5ec86f74a17622268c07a`  
		Last Modified: Fri, 21 Mar 2025 17:12:57 GMT  
		Size: 4.0 MB (4018414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c96bd3ae4c5b93fa84da3d1e23d03e06a728d2dc3247e4505cb36c82290f9aa`  
		Last Modified: Fri, 21 Mar 2025 17:13:02 GMT  
		Size: 212.0 MB (211967407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:94e8132d263c24821eccc0fe99d803ba83f987182067492e5ef72bd8a359e0b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958ab388fa4206237ec0c0e455f6b71317ebaa0a64edbe3778e78723b78e51a2`

```dockerfile
```

-	Layers:
	-	`sha256:9426550ec925e15eac4d48be639c536c7086f177493d3ff8d1faff9790080315`  
		Last Modified: Fri, 21 Mar 2025 17:12:57 GMT  
		Size: 2.5 MB (2533916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3374f9bcf8c0c4bfa5b047cf0cc21c44e3e403412ea9414e1cd39410fc60b1e`  
		Last Modified: Fri, 21 Mar 2025 17:12:57 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e19994129f18570b25d5f793393c36b76689f906e2555dafb775f59063d4d694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241806469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5867fe34260c44beb45b8d0fafa84793425f0b6094e36314eebddbe4dd94d71`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 21 Mar 2025 00:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Mar 2025 00:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 00:48:13 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 00:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='7456a38bfdaa0d7a8a4aef20ff86803e727f250350b35aa263570c5df1dc46e5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/15/GPL/openjdk-25-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='30fab25ab72d34be3cb4ec7b0d372c0642d7dc7f824e3370b05501141245ba7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Mar 2025 00:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85002c03aaf9b2a8b6da54a3c02fb9e79017b35408eacd8f0e5615650794d7ca`  
		Last Modified: Fri, 21 Mar 2025 17:26:26 GMT  
		Size: 3.8 MB (3833732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b025bebeb59ab2411c9f0da448f16b11b07954bea4d8b99d7473dd44b9e637`  
		Last Modified: Fri, 21 Mar 2025 17:26:31 GMT  
		Size: 209.9 MB (209928700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:63c5dd67c5ec99e38337fc0c5d8eca30d36d52d0b53c77598e9b2dbf3e766255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9996f9963e8d6482ec45171ec00e5c454ff84f61519568587b9e97bf2949fc37`

```dockerfile
```

-	Layers:
	-	`sha256:9c0f304e59637c59528051e486675bb57a074624a7dcb27ef755e3a146cae241`  
		Last Modified: Fri, 21 Mar 2025 17:26:26 GMT  
		Size: 2.5 MB (2533646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18d6d7b5693f7d155f74e7d961cfd71961d9dd2f896de6d04ea1bf283eea668`  
		Last Modified: Fri, 21 Mar 2025 17:26:26 GMT  
		Size: 19.7 KB (19657 bytes)  
		MIME: application/vnd.in-toto+json
