## `openjdk:25-ea-13-slim-bullseye`

```console
$ docker pull openjdk@sha256:ce5256ef566cf80c845c274e152162cd6a01c0ed57f0da91fa784f13858a8cff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:25-ea-13-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:5dd9c5027d8c50236bd4471ae57fce06623d5a4c684e00753d572c6349916438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243444949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddd91b349a4c785f6c3f664ac8c1d8caf4612875ddc3c0431f6f2c3ec6f0850`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Sat, 08 Mar 2025 01:48:16 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 01:48:16 GMT
ENV LANG=C.UTF-8
# Sat, 08 Mar 2025 01:48:16 GMT
ENV JAVA_VERSION=25-ea+13
# Sat, 08 Mar 2025 01:48:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='456a1dced4795cf35e28459b6289a9eb1d6921f83c79cf460c5c694cb52e11ba'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/13/GPL/openjdk-25-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='518a0d1c64c68f4563c167e052f135827c1b218933dd68a481a7973694fc64b2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 08 Mar 2025 01:48:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b6e21690c9a6c12e03a74784f5cb785604c71d895702e0fbeb19c269b042ee`  
		Last Modified: Mon, 10 Mar 2025 21:05:59 GMT  
		Size: 1.4 MB (1377235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f905d73c56ac336aeeda19fb55bc97a7f80f4d0a96d162155cb9074855722`  
		Last Modified: Mon, 10 Mar 2025 21:06:03 GMT  
		Size: 211.8 MB (211813784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-13-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:82277f67074fc59d95001b9e7e841e36d4a265ee612b970fae29d00719eb950b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d9e1081a1dfca5eae90c88a9f40666e62033d62ac88e9d7998f9784bc9a120`

```dockerfile
```

-	Layers:
	-	`sha256:f093b03ddae33e80cf898685029f92b91cb5283161fc84fb86971460685ea732`  
		Last Modified: Mon, 10 Mar 2025 21:05:59 GMT  
		Size: 2.8 MB (2827293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33571506ed3fa47818f093f0a4c902f97a4e5436f08fc79f104a0c5a5147bef4`  
		Last Modified: Mon, 10 Mar 2025 21:05:59 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json
