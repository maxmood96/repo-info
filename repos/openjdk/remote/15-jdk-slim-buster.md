## `openjdk:15-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:79d2d88dff13e39f224708b967debc184be2a9fba38b33c83e6d156417297e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:96f2b7c21aabe9d320afb8f8fadb57c8a065aabc13a95b42dcea970c0e988ba4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229676129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f82d5b9397fc879e20ac5d0b492b9c10a3889ae4aec1e95ff7659b054b19977`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:22 GMT
ADD file:04caaf303199c81ff1a94e2e39d5096f9d02b73294b82758e5bc6e23aff94272 in / 
# Sat, 28 Dec 2019 04:21:23 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:50:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:50:14 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:50:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Sat, 28 Dec 2019 08:50:14 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:50:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 31 Jan 2020 17:23:04 GMT
ENV JAVA_VERSION=15-ea+8
# Fri, 31 Jan 2020 17:23:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/8/GPL/openjdk-15-ea+8_linux-x64_bin.tar.gz
# Fri, 31 Jan 2020 17:23:05 GMT
ENV JAVA_SHA256=ab41dd4e616e015ec94f26e4d2c8253f376f5f5d574db811f341abc6c55e333c
# Fri, 31 Jan 2020 17:23:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 31 Jan 2020 17:23:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8ec398bc03560e0fa56440e96da307cdf0b1ad153f459b52bca53ae7ddb8236d`  
		Last Modified: Sat, 28 Dec 2019 04:25:53 GMT  
		Size: 27.1 MB (27092274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e866b0959566a21a8fa7eb2f7f12da0d12aa3498d6c31bb25a6ede1fa632ac2`  
		Last Modified: Sat, 28 Dec 2019 08:58:53 GMT  
		Size: 3.2 MB (3249103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db296337eb0a20a0ffe194d9cff29d2b0f99f314f88faa43ca4d8ca337262a4`  
		Last Modified: Sat, 28 Dec 2019 08:58:52 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ba1655733cd3531e1a578e0f049a1c7a9f8f2fb0a6d72c6d7fc7a849136768`  
		Last Modified: Fri, 31 Jan 2020 17:28:20 GMT  
		Size: 199.3 MB (199334541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
