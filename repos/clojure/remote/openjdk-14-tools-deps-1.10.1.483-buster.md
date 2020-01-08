## `clojure:openjdk-14-tools-deps-1.10.1.483-buster`

```console
$ docker pull clojure@sha256:5b2412aa68288458ee7557e9d1af8dbcda77faadfa8e35bb4930ff2b6560913b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-tools-deps-1.10.1.483-buster` - linux; amd64

```console
$ docker pull clojure@sha256:67867f0faf1f65d26194408e2dc8b2789b86e36d4afbfb20c873113a0003d42c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.9 MB (356853329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad97ca5cba2919145dea495a9509ed90acacad6078b658f3eaef2bd60243649f`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:08 GMT
ADD file:d6d0bdf8cb07a7a0dc32e9df50ac80ca1a524c3fa48136892ded195061f2194c in / 
# Sat, 28 Dec 2019 04:21:09 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:47:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:47:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				ca-certificates p11-kit 				binutils 		fontconfig libfreetype6 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:49:14 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 08:50:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Sat, 28 Dec 2019 08:50:51 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:50:52 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 07 Jan 2020 23:26:41 GMT
ENV JAVA_VERSION=14-ea+30
# Tue, 07 Jan 2020 23:26:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/30/GPL/openjdk-14-ea+30_linux-x64_bin.tar.gz
# Tue, 07 Jan 2020 23:26:41 GMT
ENV JAVA_SHA256=53a37319529ec0443d97e4fc138fc998fbfe7e32f3fc815c072d607fc31dd048
# Tue, 07 Jan 2020 23:26:53 GMT
RUN set -eux; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Tue, 07 Jan 2020 23:26:53 GMT
CMD ["jshell"]
# Tue, 07 Jan 2020 23:52:36 GMT
ENV CLOJURE_VERSION=1.10.1.483
# Tue, 07 Jan 2020 23:52:36 GMT
WORKDIR /tmp
# Tue, 07 Jan 2020 23:52:44 GMT
RUN wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 07 Jan 2020 23:52:44 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:8f0fdd3eaac017684c880d836abdaf02f9db7ac8ecca970356482e3d8e315650`  
		Last Modified: Sat, 28 Dec 2019 04:25:39 GMT  
		Size: 50.4 MB (50379720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d918eaefd9de8a1595f56900fdb8ab65a03d64b1da1078da7c0b0bf6f7552a14`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 7.8 MB (7811715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf3e3107f525b7dea5b3cdfd15f62666066202105a0aaddbab2a02aefad1f7`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 10.0 MB (9996202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27622921edb2aae9e0cb64f71a81b4a7cfef8f6a6c766514a018815834ba4e14`  
		Last Modified: Sat, 28 Dec 2019 05:02:00 GMT  
		Size: 51.8 MB (51790562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6522e32240cc901e3fc4dd0a386015b12118789e80eaaff2a864f0e096be6b00`  
		Last Modified: Sat, 28 Dec 2019 08:58:29 GMT  
		Size: 13.9 MB (13920215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57162a26a4826bf91a221b1aee8be41308e7a4fbf827b12b3dc52c9455cbce60`  
		Last Modified: Sat, 28 Dec 2019 08:59:29 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adae591d62fb1249c13fe67a7ad67ebc6b7915b5653ef51530ce5c0a97c6ce74`  
		Last Modified: Tue, 07 Jan 2020 23:32:06 GMT  
		Size: 199.1 MB (199058095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84ed8dcd6ab06394fb5362fcf4247f638a4e79444f262753a772133d6197fc8`  
		Last Modified: Tue, 07 Jan 2020 23:54:44 GMT  
		Size: 23.9 MB (23896609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
