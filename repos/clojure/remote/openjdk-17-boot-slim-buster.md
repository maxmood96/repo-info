## `clojure:openjdk-17-boot-slim-buster`

```console
$ docker pull clojure@sha256:88630552e6b99a1ac1bf57f5699507882e686e775385a355db04e6cc4876c0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-slim-buster` - linux; amd64

```console
$ docker pull clojure@sha256:1e248ff73b9afe3ab344bb37bfcf3280e31e16dae23565a1659553accb9c991a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (276040793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258f8349622e382e02229eaccdcf97873a4a5e47058b34cdaf54125df8be951c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 06:48:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:48:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 12 May 2021 06:48:04 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:48:04 GMT
ENV LANG=C.UTF-8
# Fri, 21 May 2021 17:22:36 GMT
ENV JAVA_VERSION=17-ea+23
# Fri, 21 May 2021 17:22:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/23/GPL/openjdk-17-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b43ffb86cad128acb9955d2dec2b254ffd0e0c7b7d2a15d8b7ad93772e8f722b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/23/GPL/openjdk-17-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='b5979d864a5c527c98adc81b5430d669672a609a4c19cd8c8b03edb84de74949'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 21 May 2021 17:22:52 GMT
CMD ["jshell"]
# Fri, 21 May 2021 17:48:57 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 21 May 2021 17:48:57 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 21 May 2021 17:48:58 GMT
WORKDIR /tmp
# Fri, 21 May 2021 17:49:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 21 May 2021 17:49:08 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 21 May 2021 17:49:08 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 21 May 2021 17:49:55 GMT
RUN boot
# Fri, 21 May 2021 17:49:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2b89b6081832b112f9483322d4710c661f12135e79279dc3fb1672883ada8d`  
		Last Modified: Wed, 12 May 2021 06:58:18 GMT  
		Size: 3.3 MB (3268772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2849376b3065ab1da39c2d84c06bb6fde30a4928e1707314fb808607c89684e`  
		Last Modified: Fri, 21 May 2021 17:29:24 GMT  
		Size: 186.5 MB (186525609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3baad5634890bac152170c92a30627edaea3d43738e63fcefb53d72da03cc5`  
		Last Modified: Fri, 21 May 2021 17:54:21 GMT  
		Size: 279.7 KB (279695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00efba59f49542c13a5b18d3202b13a4fc2581749b48e0d68ef54abbf1504059`  
		Last Modified: Fri, 21 May 2021 17:54:25 GMT  
		Size: 58.8 MB (58820802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-slim-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfaee6db48b263847fa69ea0331467638bb7b8b88db5cbc8be08aa85bc59608d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270610756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583b5e0099eb972a78d5ddad57bed3c48402672ad9e57860ec4d697285ccfdb5`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 May 2021 00:52:19 GMT
ADD file:91ba1791cab3ad29a1469d1e78f21f4c0b5d3d30598683b7104980604c318854 in / 
# Wed, 12 May 2021 00:52:34 GMT
CMD ["bash"]
# Wed, 12 May 2021 06:16:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:16:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 12 May 2021 06:16:12 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:16:13 GMT
ENV LANG=C.UTF-8
# Fri, 14 May 2021 19:51:53 GMT
ENV JAVA_VERSION=17-ea+22
# Fri, 14 May 2021 19:52:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/22/GPL/openjdk-17-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='68cbe678787e56de88967003071f05b47eb5cd3bbb1dd083f23bf4b8f23b25c9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/22/GPL/openjdk-17-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='fef8858675921c49b693311954fd593ec8414e00609e96c1f6262ca8c9801a0c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 14 May 2021 19:52:20 GMT
CMD ["jshell"]
# Fri, 14 May 2021 21:36:32 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 14 May 2021 21:36:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 14 May 2021 21:36:34 GMT
WORKDIR /tmp
# Fri, 14 May 2021 21:36:46 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 14 May 2021 21:36:48 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 May 2021 21:36:50 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 14 May 2021 21:37:31 GMT
RUN boot
# Fri, 14 May 2021 21:37:32 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:fcad0c936ea5c12e1c8c4edb81a97c0cde04ee71e7067ee3b246474cf1854d7a`  
		Last Modified: Wed, 12 May 2021 01:02:02 GMT  
		Size: 25.9 MB (25911250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49feb8163b50086a917c966dbaff372d7e4189ec1a1a504bb2b3b5258a09d616`  
		Last Modified: Wed, 12 May 2021 06:26:49 GMT  
		Size: 3.1 MB (3118874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe480aa8da764b16e11468cb1c4541008c289e3894681863dc8983d3d49d794b`  
		Last Modified: Fri, 14 May 2021 19:58:39 GMT  
		Size: 182.5 MB (182480277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf04f8474a03b427b5579cb448627871293937ba1ffa3c163c1de0881bbccf6`  
		Last Modified: Fri, 14 May 2021 21:41:35 GMT  
		Size: 279.6 KB (279601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd15b551fe7ddefc24f3d9a3db9fd7eba1e01c058bd169a344b29e2f16e414a`  
		Last Modified: Fri, 14 May 2021 21:41:40 GMT  
		Size: 58.8 MB (58820754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
