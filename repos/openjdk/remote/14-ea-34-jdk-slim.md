## `openjdk:14-ea-34-jdk-slim`

```console
$ docker pull openjdk@sha256:f382dfb6ad143574db14c6b1ba71757f9332e511212296a4edf037d5068582e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:14-ea-34-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:472abd007e134408a58c40d6252fccd015658f24c01638c1c302be4e9672e227
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229778059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e947a91979630008fb9f60cf452633df2e3afbf58abe257da67761ade71317`
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
# Sat, 28 Dec 2019 08:52:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Sat, 28 Dec 2019 08:52:35 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 08:52:36 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 31 Jan 2020 17:24:27 GMT
ENV JAVA_VERSION=14-ea+34
# Fri, 31 Jan 2020 17:24:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/34/GPL/openjdk-14-ea+34_linux-x64_bin.tar.gz
# Fri, 31 Jan 2020 17:24:27 GMT
ENV JAVA_SHA256=51d9dd2161a912ab7bd2bf2e08043cdd175ce22b28608442e0d06bc777286158
# Fri, 31 Jan 2020 17:24:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Fri, 31 Jan 2020 17:24:42 GMT
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
	-	`sha256:7ab72a68614df7d0d9d800dc8bc5b3378c9d144c38bdf0865dbdb5d13bce631a`  
		Last Modified: Sat, 28 Dec 2019 08:59:58 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bba24643d078b67a922c0528301d0104c10c3443775f10f772915867eb0f4a0`  
		Last Modified: Fri, 31 Jan 2020 17:30:17 GMT  
		Size: 199.4 MB (199436471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
