## `clojure:openjdk-17-boot-buster`

```console
$ docker pull clojure@sha256:f8a6c410d9c98b50c3644de3e1476366b0312187ff0e49dfa466ef2e1ead8a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-buster` - linux; amd64

```console
$ docker pull clojure@sha256:f050db7e45990788ee0a1617a107ff259c408428fbe5e6e1b575b2817324fe90
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379111246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e413a22544d64a4ecfc92529263710a6d3289716a6155abd245105db1110c24`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:55:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:55:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:56:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:47:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:47:27 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 12 May 2021 06:47:27 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:47:27 GMT
ENV LANG=C.UTF-8
# Fri, 21 May 2021 17:22:11 GMT
ENV JAVA_VERSION=17-ea+23
# Fri, 21 May 2021 17:22:31 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/23/GPL/openjdk-17-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b43ffb86cad128acb9955d2dec2b254ffd0e0c7b7d2a15d8b7ad93772e8f722b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/23/GPL/openjdk-17-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='b5979d864a5c527c98adc81b5430d669672a609a4c19cd8c8b03edb84de74949'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 21 May 2021 17:22:31 GMT
CMD ["jshell"]
# Fri, 21 May 2021 17:50:08 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 21 May 2021 17:50:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 21 May 2021 17:50:08 GMT
WORKDIR /tmp
# Fri, 21 May 2021 17:50:10 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Fri, 21 May 2021 17:50:10 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 21 May 2021 17:50:10 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 21 May 2021 17:50:33 GMT
RUN boot
# Fri, 21 May 2021 17:50:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d62473a22dec9ffef056b2017968a9dc484c8f836fb6d79f46980b309e9138`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 7.8 MB (7832938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8962bc0fad55b13afedfeb6ad5cb06fd065461cf3e1ae4e7aeae5eeb17b179df`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 10.0 MB (9997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d943ee54c1fa196b54ab9a6673174c66eea04cfa1a4ac5b0328b74f066a4d9`  
		Last Modified: Wed, 12 May 2021 02:05:07 GMT  
		Size: 51.8 MB (51841468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b53c8574903f2e47274cfe45903823235a9b4b846f7771f2a75a8e6a1462162`  
		Last Modified: Wed, 12 May 2021 06:57:35 GMT  
		Size: 13.9 MB (13921268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a982ff7b61c6113c8435ae950cdb851deb3ba8fbc1bf0e54acfd70eb3b90e5`  
		Last Modified: Fri, 21 May 2021 17:28:48 GMT  
		Size: 186.3 MB (186257729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd84f16101a35ea335fbabd8a65adc79ddd41251ebb073d4d39528dacff0bed9`  
		Last Modified: Fri, 21 May 2021 17:54:41 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbe341b670f262f50ba7e4ef8a2dfa34d4679447ebc699c18d68c77ae5af0a7`  
		Last Modified: Fri, 21 May 2021 17:54:46 GMT  
		Size: 58.8 MB (58820520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19d22e0831506d66ce2d92938015bec4308f5f22d4f517ead9ed72bb75db43f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.8 MB (374789794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97117eb2350936ac5f12ba48ec895c0ffb49ec73d81ce00b7beb5ed0889ec27`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:35:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:15:26 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 12 May 2021 06:15:27 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:15:29 GMT
ENV LANG=C.UTF-8
# Fri, 14 May 2021 19:51:22 GMT
ENV JAVA_VERSION=17-ea+22
# Fri, 14 May 2021 19:51:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/22/GPL/openjdk-17-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='68cbe678787e56de88967003071f05b47eb5cd3bbb1dd083f23bf4b8f23b25c9'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/22/GPL/openjdk-17-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='fef8858675921c49b693311954fd593ec8414e00609e96c1f6262ca8c9801a0c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 14 May 2021 19:51:44 GMT
CMD ["jshell"]
# Fri, 14 May 2021 21:37:40 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 14 May 2021 21:37:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 14 May 2021 21:37:42 GMT
WORKDIR /tmp
# Fri, 14 May 2021 21:37:45 GMT
RUN mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Fri, 14 May 2021 21:37:46 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 May 2021 21:37:48 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 14 May 2021 21:38:12 GMT
RUN boot
# Fri, 14 May 2021 21:38:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bbb3592d6685d1c683c8c20e60901274c636605800608685274c194d43d25`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 7.7 MB (7695057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d8c28b9129321858810cff4cd78385949579ed18d991f98c77f912c7a754f8`  
		Last Modified: Wed, 12 May 2021 01:48:24 GMT  
		Size: 10.0 MB (9984343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b3803033bfb8e0c8ab31f286ca427ccb8a47b7c63ca8e6d05d23ff7231733`  
		Last Modified: Wed, 12 May 2021 01:48:46 GMT  
		Size: 52.2 MB (52168431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569c7916ae87c8a06d01b70712e37e439334a5ebc14f56694a2c855ffd204a53`  
		Last Modified: Wed, 12 May 2021 06:26:16 GMT  
		Size: 14.7 MB (14673604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d571ea3453153a302a65fc8453abe083c81323aa5584782f5f88d5a0ab5c27ab`  
		Last Modified: Fri, 14 May 2021 19:58:00 GMT  
		Size: 182.2 MB (182215815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab701f99ab6a32a22a41ddfd5cb0aa64384248601fa64132c0ec1b54bdd742f`  
		Last Modified: Fri, 14 May 2021 21:41:50 GMT  
		Size: 6.9 KB (6922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da93a64309f455115a18c0f79557536e3e509cb21094c3878bf180b629f7c9c`  
		Last Modified: Fri, 14 May 2021 21:41:56 GMT  
		Size: 58.8 MB (58820271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
