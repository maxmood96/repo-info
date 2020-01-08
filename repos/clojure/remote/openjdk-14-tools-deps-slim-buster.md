## `clojure:openjdk-14-tools-deps-slim-buster`

```console
$ docker pull clojure@sha256:15e64e007e9c5e70fcedcf8fcfa1af86d259f99d098010d3eb4b5be9063712ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-tools-deps-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:0e175e8918140ee2fb8f81dd51b670fdb4182c221fdbd94efcfd715ec6d988f4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276287836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326bfc84131437108a0e101da9b13255a935a1ba1b4a8a516a7aad0987a1d77e`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Tue, 07 Jan 2020 23:26:58 GMT
ENV JAVA_VERSION=14-ea+30
# Tue, 07 Jan 2020 23:26:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/30/GPL/openjdk-14-ea+30_linux-x64_bin.tar.gz
# Tue, 07 Jan 2020 23:26:58 GMT
ENV JAVA_SHA256=53a37319529ec0443d97e4fc138fc998fbfe7e32f3fc815c072d607fc31dd048
# Tue, 07 Jan 2020 23:27:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		javac --version; 	java --version
# Tue, 07 Jan 2020 23:27:15 GMT
CMD ["jshell"]
# Tue, 07 Jan 2020 23:52:12 GMT
ENV CLOJURE_VERSION=1.10.1.483
# Tue, 07 Jan 2020 23:52:12 GMT
WORKDIR /tmp
# Tue, 07 Jan 2020 23:52:31 GMT
RUN apt-get update && apt-get install -y curl rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get remove -y --purge curl wget
# Tue, 07 Jan 2020 23:52:32 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:ee7e3ab0a7d7524594fa5c523f020cd031d6c224fa1e846d3badd0b679e2082d`  
		Last Modified: Tue, 07 Jan 2020 23:32:46 GMT  
		Size: 199.3 MB (199327839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1543d1f6faa721a335cc38c1b52b07cde7b00e8018a5762300109cad989496ad`  
		Last Modified: Tue, 07 Jan 2020 23:54:37 GMT  
		Size: 46.6 MB (46618409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
