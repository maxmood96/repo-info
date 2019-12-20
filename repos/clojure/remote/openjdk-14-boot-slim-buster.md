## `clojure:openjdk-14-boot-slim-buster`

```console
$ docker pull clojure@sha256:90a21549ebf5bef67fc6a5a5a89d07d19af503cedc989b46e3545de785818e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:1239cbc69e1fcbfb3c55b7a31dd3b707f811c85f5f329f07360e64b693a43f5e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288729885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9c58c62c596769996adffe129cee3fa6742f16a1568237392df5db0b0f0b8f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 19:14:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 19:14:45 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2019 19:14:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Fri, 22 Nov 2019 19:14:45 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2019 19:14:46 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 19 Dec 2019 23:30:54 GMT
ENV JAVA_VERSION=14-ea+28
# Thu, 19 Dec 2019 23:30:54 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/28/GPL/openjdk-14-ea+28_linux-x64_bin.tar.gz
# Thu, 19 Dec 2019 23:30:55 GMT
ENV JAVA_SHA256=ce2e3acf3b20426545a2e835cad33b21351359c67bf30a7722aaa21d97ee5862
# Thu, 19 Dec 2019 23:31:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Thu, 19 Dec 2019 23:31:11 GMT
CMD ["jshell"]
# Fri, 20 Dec 2019 01:05:36 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 20 Dec 2019 01:05:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 20 Dec 2019 01:05:36 GMT
WORKDIR /tmp
# Fri, 20 Dec 2019 01:05:44 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && echo "f717ef381f2863a4cad47bf0dcc61e923b3d2afb *boot.sh" | sha1sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get remove -y --purge wget && apt-get autoremove -y
# Fri, 20 Dec 2019 01:05:44 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 20 Dec 2019 01:05:45 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 20 Dec 2019 01:07:10 GMT
RUN boot
# Fri, 20 Dec 2019 01:07:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dc2bdcfe193ce54affa45170354ca76667c40f8cf536b6282dd379e17e24a`  
		Last Modified: Fri, 22 Nov 2019 19:19:08 GMT  
		Size: 3.2 MB (3249119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646f7263fe2d59eb4bac3860d55c1438acbe162706df09f1f0f89198cdc35119`  
		Last Modified: Fri, 22 Nov 2019 19:19:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a73873182bc693254bdcba9b8cf687fd6889a831d332c3fa2fd8cffc4b05cb7`  
		Last Modified: Thu, 19 Dec 2019 23:36:20 GMT  
		Size: 199.3 MB (199287075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b011e2da1e3ed510865fd778a268117c625bfb14241b6b146b2b0018731330`  
		Last Modified: Fri, 20 Dec 2019 01:11:03 GMT  
		Size: 279.6 KB (279604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef26e81c963c29d83ee31345939a77ff2b77a228235fcd72897c41569f2c5ecc`  
		Last Modified: Fri, 20 Dec 2019 01:11:10 GMT  
		Size: 58.8 MB (58821223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
