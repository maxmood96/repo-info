## `openjdk:20-ea-19-jdk-slim-buster`

```console
$ docker pull openjdk@sha256:f22962d800ca8c84026fab30b98a0e7babf2bf50716a65f10e34feeaa17ad115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-19-jdk-slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:8785d565b421eccf5b5aedea41c92b776e0975dc111d9fe167de54408e48e31a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227848809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc73d8147fc1760b754d1a24b94a7551e117de45e2ea665bd491fb63fd47acce`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:01:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 05 Oct 2022 13:01:50 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 13:01:50 GMT
ENV LANG=C.UTF-8
# Fri, 14 Oct 2022 01:49:02 GMT
ENV JAVA_VERSION=20-ea+19
# Fri, 14 Oct 2022 01:49:17 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/19/GPL/openjdk-20-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='872bf878e925d040e586f05723275d769f00f5718745e0758e6345ab2ffa0b66'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/19/GPL/openjdk-20-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='3ea4c7aa0de5ed4d0e5e0d55d2ef9cfa261087e65af3fdf849ecb2186a414c0d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 14 Oct 2022 01:49:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e42b9ceb9670d3b07bff56104ed6b09d0fc403302f1722dbc879ad64349d2f1`  
		Last Modified: Wed, 05 Oct 2022 13:07:32 GMT  
		Size: 3.3 MB (3273408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a283706ff677a8541284b20f48b1b1f722e720664e0a26e632373740d2ec3d`  
		Last Modified: Fri, 14 Oct 2022 01:55:16 GMT  
		Size: 197.4 MB (197437358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-19-jdk-slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c00dd936e00587f7621b023c33ed8380a3c0303d89591a549d35b13cf2ffeac4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224821429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ad8720fc10c9329a69a397d3c7b58ae6715c164bd2d82383277298f9fed53d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:27:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:27:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-20
# Wed, 05 Oct 2022 04:27:48 GMT
ENV PATH=/usr/local/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:27:49 GMT
ENV LANG=C.UTF-8
# Fri, 14 Oct 2022 03:32:21 GMT
ENV JAVA_VERSION=20-ea+19
# Fri, 14 Oct 2022 03:32:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/19/GPL/openjdk-20-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='872bf878e925d040e586f05723275d769f00f5718745e0758e6345ab2ffa0b66'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/19/GPL/openjdk-20-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='3ea4c7aa0de5ed4d0e5e0d55d2ef9cfa261087e65af3fdf849ecb2186a414c0d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 14 Oct 2022 03:32:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a81927bc22acfe9508e423675967ad20111ed2c4daa880d6b1e9ac555cc7a7`  
		Last Modified: Wed, 05 Oct 2022 04:37:04 GMT  
		Size: 3.1 MB (3126082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d281267804a207eede128980aadf045b28c5f24c49ef2fcaa02218348f1eec`  
		Last Modified: Fri, 14 Oct 2022 03:41:52 GMT  
		Size: 195.8 MB (195783444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
