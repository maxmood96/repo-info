## `clojure:openjdk-19-boot-2.8.3`

```console
$ docker pull clojure@sha256:309dc5471495af0ec984bc1456da571f69518f7ae2f923580f74ce0bd6312868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-19-boot-2.8.3` - linux; amd64

```console
$ docker pull clojure@sha256:3ca86de352a44f8504150a7abae38c7edfc2eac89eacf6e27f60bdf1b18772fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285511725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056526a93e8df826b41cfd76ed39ab3ba0be9ee61710b0edf341e104053c632c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 14:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 14:21:07 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 14:21:07 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 14:21:07 GMT
ENV LANG=C.UTF-8
# Mon, 14 Mar 2022 20:14:51 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 20:15:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 20:15:05 GMT
CMD ["jshell"]
# Mon, 14 Mar 2022 20:44:59 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 14 Mar 2022 20:44:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 14 Mar 2022 20:44:59 GMT
WORKDIR /tmp
# Mon, 14 Mar 2022 20:45:03 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 14 Mar 2022 20:45:04 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Mar 2022 20:45:04 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 14 Mar 2022 20:45:41 GMT
RUN boot
# Mon, 14 Mar 2022 20:45:42 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 14 Mar 2022 20:45:42 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Mar 2022 20:45:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8366d5a4a5f71bf009ed651eb5566bf81bcd61ddaa4a2541fc65505bb076ca`  
		Last Modified: Tue, 01 Mar 2022 14:40:45 GMT  
		Size: 1.6 MB (1582090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742acb3c151b7dcc899c93aecfd3071182a72f9e4a2b948c348fc72b00819b51`  
		Last Modified: Mon, 14 Mar 2022 20:23:36 GMT  
		Size: 193.5 MB (193458806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ef21a681970e67ae1ba1b68f10c48756418bbc0a7a4fdd0e795d08d4729488`  
		Last Modified: Mon, 14 Mar 2022 20:51:39 GMT  
		Size: 283.1 KB (283075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b349fa816dbec81cdfcd33ebbce89ead38d556cfcc7a3a9a9b8a1fb33a4575f`  
		Last Modified: Mon, 14 Mar 2022 20:51:42 GMT  
		Size: 58.8 MB (58820953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febb6913a3dc73fcddf91e379e1373379c36d07387c6407c6787945bff80dc61`  
		Last Modified: Mon, 14 Mar 2022 20:51:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-19-boot-2.8.3` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c4ccbe652051766f4f87c343d7450fbaf122179f41866d48b4802329297e5c84
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282787206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2ea22f75aa14f9e77d45b0e302ee49740472a15fa56128220e73286a692ff9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-19
# Tue, 01 Mar 2022 13:48:14 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 13:48:15 GMT
ENV LANG=C.UTF-8
# Mon, 14 Mar 2022 19:05:56 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 19:06:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 19:06:15 GMT
CMD ["jshell"]
# Mon, 14 Mar 2022 19:57:44 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 14 Mar 2022 19:57:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 14 Mar 2022 19:57:46 GMT
WORKDIR /tmp
# Mon, 14 Mar 2022 19:57:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 14 Mar 2022 19:57:51 GMT
ENV PATH=/usr/local/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 14 Mar 2022 19:57:52 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 14 Mar 2022 19:58:26 GMT
RUN boot
# Mon, 14 Mar 2022 19:58:27 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 14 Mar 2022 19:58:27 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Mar 2022 19:58:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee4a8201309b4b9bb0e0e0efc8d45265ae39d932512f5edb149b65eaf107d9`  
		Last Modified: Tue, 01 Mar 2022 14:12:59 GMT  
		Size: 1.6 MB (1565936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b73f5fd6d754d54fb63d39608eab646b182489072fb9881fe0f42ed90d48d6`  
		Last Modified: Mon, 14 Mar 2022 19:20:43 GMT  
		Size: 192.3 MB (192280109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adb1fb51890bb6ba7e567f8ee18e68e33689486c67c9942e05689c2d3f66bef`  
		Last Modified: Mon, 14 Mar 2022 20:07:59 GMT  
		Size: 67.2 KB (67222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77770cd4c1beef2862a751adfec5f5c44e9336d51083f52374c1e92158336253`  
		Last Modified: Mon, 14 Mar 2022 20:08:06 GMT  
		Size: 58.8 MB (58816525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99efe79a223d5a113c0222fb39873dbab06b6b36bd2b55cfaae0b18409e92ca`  
		Last Modified: Mon, 14 Mar 2022 20:07:59 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
