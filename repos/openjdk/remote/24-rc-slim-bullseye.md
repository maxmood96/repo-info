## `openjdk:24-rc-slim-bullseye`

```console
$ docker pull openjdk@sha256:98c9ca34657d79118680916187169590a32a7656085de3f31b24688fd6e9fc0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-rc-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:bf0710d0b8488e728f441a112d63a4edbbf15ab2988d8d1bcc32edeba17078f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244629988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9be0e359e51dd87c6d6078ae5f680b196bc95c0a3aa18b69acb104ea4bd2b8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10f7d2ef5f71c6e99dd1e69de9d4829da102c8581cdf8f33b3ffa54e237171b`  
		Last Modified: Tue, 11 Feb 2025 00:28:10 GMT  
		Size: 1.4 MB (1377245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967a717a7737f1eafcb578fef6d17ce6c41a2d75a7600439cd4bf7e005920fc2`  
		Last Modified: Tue, 11 Feb 2025 00:28:15 GMT  
		Size: 213.0 MB (213000155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f38e229c55e54960662ab2e5d33f2803c6fd25a265953e0bd2e9269dbcb9923f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae05a80d8511451847858509a5b24863f225fcccf5127a648a38785629ba2ed5`

```dockerfile
```

-	Layers:
	-	`sha256:041b9d9be114008753027593bc506494333c5a9a7ca1fd5fd2c7ec79f5bbf943`  
		Last Modified: Tue, 11 Feb 2025 00:28:10 GMT  
		Size: 2.8 MB (2830998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49bf4a29ece85fe9a8bda07d8216545c6868da9abbf411b86f7b56c7ae42c27f`  
		Last Modified: Tue, 11 Feb 2025 00:28:10 GMT  
		Size: 17.0 KB (16966 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-rc-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:eb2c71a4b45fbb15c8c766ab284eae5273f8e4d05f02cb06853afd89699f105c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241057016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97739f9a00db8cbba80055aa79105475b5aef127730e3f9358add89a44a4b259`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0b8342410f5de7992f24293c7ba6dfbca7729223103def73b5319fa46cc62b`  
		Last Modified: Wed, 05 Feb 2025 03:02:01 GMT  
		Size: 1.4 MB (1361282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f02d23026571b8a3f835f617fe490644b9e1acc7ee6f004953fbd699f59288`  
		Last Modified: Tue, 11 Feb 2025 00:42:32 GMT  
		Size: 211.0 MB (210950924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:c94a4d9f6b308120408844af52af927e31e0334acd8bfcc1928f06b59030e903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d062f6757d02b4174ee25ebbd38bc2afffe6020332f701c7dc33a72479400575`

```dockerfile
```

-	Layers:
	-	`sha256:345dd753c1afe4e0b845b377f3b3b3180f052810e30c6239354ae0829065cfcf`  
		Last Modified: Tue, 11 Feb 2025 00:42:28 GMT  
		Size: 2.8 MB (2830626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc1baa487a8de83f09167af66e6f26dca0190af186d4e2286ac8c2b302ad3cf`  
		Last Modified: Tue, 11 Feb 2025 00:42:27 GMT  
		Size: 17.1 KB (17085 bytes)  
		MIME: application/vnd.in-toto+json
