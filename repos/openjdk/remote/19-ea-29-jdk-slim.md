## `openjdk:19-ea-29-jdk-slim`

```console
$ docker pull openjdk@sha256:9ea32329239d1d59a8402972f6938ec2257ddc43eb2db83c048c2afa62f131d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-29-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:992328ef3248b0e70162027833d890c2034d90d874cd234010c9b047f92092a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229491287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03391dadeb5ef8696b93e127f7e0eacfb79de174e29f23cf4a80e733debe522`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:55:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 23 Jun 2022 04:55:18 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 04:55:18 GMT
ENV LANG=C.UTF-8
# Fri, 01 Jul 2022 01:30:10 GMT
ENV JAVA_VERSION=19-ea+29
# Fri, 01 Jul 2022 01:30:22 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/29/GPL/openjdk-19-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='04ada1133ef2771a80998706ff9168ca511e4f4e7c42b1ba4c9cdbd570d6cc31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/29/GPL/openjdk-19-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='d2d5d6b1b6f1116f93a6f934f2fb03d8a4d257f0c72ad95c61a1aa2011ceb833'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Jul 2022 01:30:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4dc029a36926590a5070a9a58443942497e3b2d48cff116b8b15004d386a40`  
		Last Modified: Thu, 23 Jun 2022 05:07:14 GMT  
		Size: 1.6 MB (1582249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e370d224741a2fc87e22f9bd05cb037e0567831aa2344e6dc20795614959a38d`  
		Last Modified: Fri, 01 Jul 2022 01:43:20 GMT  
		Size: 196.5 MB (196529630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-29-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:658b7d32f06f5f80351aa4ed20c1c4c0b52405a6b8a7f35b2b479101871fae24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226582810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838720257dda0e12fe2393a0ba376773a68eab5769248dd73f74191604ac1207`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 15:14:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:16:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Thu, 23 Jun 2022 15:16:52 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:16:53 GMT
ENV LANG=C.UTF-8
# Fri, 01 Jul 2022 01:44:03 GMT
ENV JAVA_VERSION=19-ea+29
# Fri, 01 Jul 2022 01:44:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/29/GPL/openjdk-19-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='04ada1133ef2771a80998706ff9168ca511e4f4e7c42b1ba4c9cdbd570d6cc31'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/29/GPL/openjdk-19-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='d2d5d6b1b6f1116f93a6f934f2fb03d8a4d257f0c72ad95c61a1aa2011ceb833'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Jul 2022 01:44:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145b1362d29199a34271f94fac2115a6940998ae50f16fd5de481ae77825beed`  
		Last Modified: Thu, 23 Jun 2022 15:36:55 GMT  
		Size: 1.4 MB (1361261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73735b6cb27fa3683327a0765cf677c98cc03a78dfb926a161c9de34e6aa91fd`  
		Last Modified: Fri, 01 Jul 2022 02:04:08 GMT  
		Size: 195.2 MB (195155829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
