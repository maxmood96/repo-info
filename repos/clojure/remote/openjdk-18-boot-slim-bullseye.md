## `clojure:openjdk-18-boot-slim-bullseye`

```console
$ docker pull clojure@sha256:2254fd76446590b5ebc0f20800bd9b4e9c76230f4479a3458611388fb4431b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-18-boot-slim-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:77110b879e617b6426b7c1aab8ecaa91b085f48a15320a26f44840e9d52c2f0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281072491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fdae61f05b1d5e54dc45a0520841b81936a3cf541ced4562ba6e52666362b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:20:29 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 09:20:29 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 09:20:29 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:20:29 GMT
ENV JAVA_VERSION=18-ea+31
# Wed, 26 Jan 2022 09:20:45 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='d57d6a205ea5a0b891490b6d9e45315f719ba92123775c4e0e3e76464504f7fa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='668f2637087591644db894f1f03c5782bb491fd4452b0c736ab7f6e70f1eb036'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 09:20:46 GMT
CMD ["jshell"]
# Thu, 27 Jan 2022 17:16:33 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 27 Jan 2022 17:16:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 27 Jan 2022 17:16:33 GMT
WORKDIR /tmp
# Thu, 27 Jan 2022 17:16:39 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 27 Jan 2022 17:16:39 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 27 Jan 2022 17:16:40 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 27 Jan 2022 17:17:02 GMT
RUN boot
# Thu, 27 Jan 2022 17:17:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 27 Jan 2022 17:17:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 27 Jan 2022 17:17:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc79ff7de66b9ef44dc6cd4f500aa92bd1f0b09ccd13eb0ee6441084fbb719cf`  
		Last Modified: Wed, 26 Jan 2022 09:41:32 GMT  
		Size: 1.6 MB (1582049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0571c1f5243da2c44429c8d89cd05e68129ed5da11c1589b9206f2d50ae1da3a`  
		Last Modified: Wed, 26 Jan 2022 09:45:04 GMT  
		Size: 189.0 MB (189020006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a899704cd4c2b8e1f3cb5c7187143afc7768bf3050f9f97bacc55fb4558c07`  
		Last Modified: Thu, 27 Jan 2022 17:37:34 GMT  
		Size: 283.1 KB (283058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cad8b524e617585bedb52ac2f47ac3209135b6e86889fb642f7c37e6f2dc603`  
		Last Modified: Thu, 27 Jan 2022 17:37:37 GMT  
		Size: 58.8 MB (58820713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a8ea7e6f0c5d7b04b711f4e5e1269f010bd1462715e2145475c5ebecf88c7c`  
		Last Modified: Thu, 27 Jan 2022 17:37:33 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-18-boot-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:64c932298f7d581457f4ee8984c4243d6b6874f9cf578cd22960e04ce7276a14
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278252645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c221d1442fb1ee82535cb6b94bb51790eeb5c896147c53e107da778293ea277d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 05:49:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 05:52:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 26 Jan 2022 05:52:14 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 05:52:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 05:52:16 GMT
ENV JAVA_VERSION=18-ea+31
# Wed, 26 Jan 2022 05:52:33 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='d57d6a205ea5a0b891490b6d9e45315f719ba92123775c4e0e3e76464504f7fa'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/31/GPL/openjdk-18-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='668f2637087591644db894f1f03c5782bb491fd4452b0c736ab7f6e70f1eb036'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 26 Jan 2022 05:52:34 GMT
CMD ["jshell"]
# Wed, 26 Jan 2022 21:34:26 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Jan 2022 21:34:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Jan 2022 21:34:28 GMT
WORKDIR /tmp
# Wed, 26 Jan 2022 21:34:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Jan 2022 21:34:33 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Jan 2022 21:34:34 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Jan 2022 21:34:48 GMT
RUN boot
# Wed, 26 Jan 2022 21:34:50 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 26 Jan 2022 21:34:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Jan 2022 21:34:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abf67e3e34eccefabf68f15c7d753f1a4c8e241beb1818f97e276186d54124e`  
		Last Modified: Wed, 26 Jan 2022 06:13:02 GMT  
		Size: 1.6 MB (1565889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0757b80b26e34db1a6e8f5a5ef43dbce47146ede4299b964b5214317b119d258`  
		Last Modified: Wed, 26 Jan 2022 06:16:49 GMT  
		Size: 187.7 MB (187746739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efc83730244434ef10a15c39c759798b13c4e279359419c0621e9618a58b0c2`  
		Last Modified: Wed, 26 Jan 2022 21:56:37 GMT  
		Size: 67.2 KB (67220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0fe6c1ff4a0b7e6d0401b423cbc19603eb01171368ad43f71a9a0b36b238d6`  
		Last Modified: Wed, 26 Jan 2022 21:56:42 GMT  
		Size: 58.8 MB (58815620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265139b6f3307a7f7d9c215626328918fe5668983f99554a623efbae39485de9`  
		Last Modified: Wed, 26 Jan 2022 21:56:36 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
