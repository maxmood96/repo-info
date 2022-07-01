## `openjdk:20-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:21953b60613d78040cd31d70a03d1c9dcbd36744461f14eff98bc0d7cb58cbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:627a9716b2f90a5f0eea4846a52fcc764167fc5528f89d85bd12a7c4d346ac9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230070674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f322b23ad3adc494af825360870a672b87f5945d3d4f34f5cb5d3ec40675c771`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:53:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Thu, 23 Jun 2022 04:53:52 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 04:53:52 GMT
ENV LANG=C.UTF-8
# Fri, 01 Jul 2022 01:28:38 GMT
ENV JAVA_VERSION=20-ea+4
# Fri, 01 Jul 2022 01:28:51 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/4/GPL/openjdk-20-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='74243a1b83dde07c3645cd0c7c3b00135fb9ca38c357e284560bf5be45a864d6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/4/GPL/openjdk-20-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='ce9dd88462c6fb6c6e8be53151164b95a738e03d28788f3fd64e0339dee96de1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Jul 2022 01:28:51 GMT
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
	-	`sha256:9bf5e050b30b9da0875abea4816c126988be55723d1c02d332f25d40e66f0f42`  
		Last Modified: Fri, 01 Jul 2022 01:39:00 GMT  
		Size: 197.1 MB (197109017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:be7cade25d8e33b922511b07060f882edc36178b31153a42b0cb23d316c2c83f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227174289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc6e039dfd1f57653b2f0a3e3022439ba6a169afd6bdfe075de83dfb8d7e5ad`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 15:14:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 15:14:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Thu, 23 Jun 2022 15:14:43 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jun 2022 15:14:44 GMT
ENV LANG=C.UTF-8
# Fri, 01 Jul 2022 01:41:46 GMT
ENV JAVA_VERSION=20-ea+4
# Fri, 01 Jul 2022 01:41:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/4/GPL/openjdk-20-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='74243a1b83dde07c3645cd0c7c3b00135fb9ca38c357e284560bf5be45a864d6'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/4/GPL/openjdk-20-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='ce9dd88462c6fb6c6e8be53151164b95a738e03d28788f3fd64e0339dee96de1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Jul 2022 01:42:00 GMT
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
	-	`sha256:61399336bc837d1bc51953cdad4ae9f930fea277ab5ebb87b0075f5bc6f474e1`  
		Last Modified: Fri, 01 Jul 2022 01:59:17 GMT  
		Size: 195.7 MB (195747308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
