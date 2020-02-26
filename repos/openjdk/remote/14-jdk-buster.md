## `openjdk:14-jdk-buster`

```console
$ docker pull openjdk@sha256:a2d79a7228e1e636108fd93fbf9d943c4713cf9d96cc513fe743de2964c9aeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:14-jdk-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:24e86d1b42c1505cb31126fe5911f056a5e0ecb70a845d31932371c13087d1be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.1 MB (333072572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aa8eace556c1ca08cda13177911b5ce2a766e36ba37aa75e8e69ac7dd4c5a4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 26 Feb 2020 00:37:07 GMT
ADD file:e05e45c33042db4ec7f71a5952d65ee8cb3786dcd76fa7a990f48a2def1344e2 in / 
# Wed, 26 Feb 2020 00:37:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:06:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:06:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:14:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:14:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:15:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Wed, 26 Feb 2020 20:15:54 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 20:15:55 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 26 Feb 2020 20:15:55 GMT
ENV JAVA_VERSION=14
# Wed, 26 Feb 2020 20:15:55 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk14/076bab302c7b4508975440c56f6cc26a/36/GPL/openjdk-14_linux-x64_bin.tar.gz
# Wed, 26 Feb 2020 20:15:56 GMT
ENV JAVA_SHA256=c7006154dfb8b66328c6475447a396feb0042608ee07a96956547f574a911c09
# Wed, 26 Feb 2020 20:17:15 GMT
RUN set -eux; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Wed, 26 Feb 2020 20:17:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:50e431f790939a2f924af65084cc9d39c3d3fb9ad2d57d183b7eadf86ea46992`  
		Last Modified: Wed, 26 Feb 2020 00:44:04 GMT  
		Size: 50.4 MB (50381971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c6d374ea51e3dd671f71b28d025a7794ebea181b00838987d0b4d8a51372f`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 7.8 MB (7812140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85513200d847a64a6e8f2cb714e2169f559b24b7736c586ff7b9aaedf71f410`  
		Last Modified: Wed, 26 Feb 2020 01:20:25 GMT  
		Size: 10.0 MB (9996282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55769680e8277a4ff083d05f0993d1483b3d26b93a8814cf3c6f04fe5975ffa0`  
		Last Modified: Wed, 26 Feb 2020 01:20:44 GMT  
		Size: 51.8 MB (51790538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a6ff6826f6ff050dac5197a43ec030d0203c4d15e003fd9b61e48635802002`  
		Last Modified: Wed, 26 Feb 2020 20:23:28 GMT  
		Size: 13.9 MB (13920236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08afebabfaaacea79cea7774a871e9163fa7105b5698ca8fcf7ef4595fed4651`  
		Last Modified: Wed, 26 Feb 2020 20:24:29 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21f39cec49b358f2c2973ef587a1cd94f9e3973687ee3aeda5c2df6fe12db4f`  
		Last Modified: Wed, 26 Feb 2020 20:24:49 GMT  
		Size: 199.2 MB (199171195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
