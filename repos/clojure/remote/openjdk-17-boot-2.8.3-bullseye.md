## `clojure:openjdk-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:dc23b644106f9de30c802bd68323f8da2de10bf41a41b1f16268f6a14f135dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0f2f7ed585b5515259efbcf465613c7c8a8a1b7baea4d39cc553479eb4a7a74d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.1 MB (387083541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55295a32aaee9de18479b639f1b1d42f0da968ee675aabeddfbfb9f7ef22c068`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:07 GMT
ADD file:e8d512b08fe2ddc6f2c85831c73e4c72b9c850fa428913d19da4bb1a34f84cf2 in / 
# Tue, 29 Mar 2022 00:22:08 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:29:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:30:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:07:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 23:09:39 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 29 Mar 2022 23:09:39 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:09:40 GMT
ENV JAVA_VERSION=17.0.2
# Tue, 29 Mar 2022 23:09:49 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:09:50 GMT
CMD ["jshell"]
# Tue, 29 Mar 2022 23:48:25 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 29 Mar 2022 23:48:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 29 Mar 2022 23:48:25 GMT
WORKDIR /tmp
# Tue, 29 Mar 2022 23:48:29 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Tue, 29 Mar 2022 23:48:29 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 29 Mar 2022 23:48:29 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 29 Mar 2022 23:48:50 GMT
RUN boot
# Tue, 29 Mar 2022 23:48:50 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 29 Mar 2022 23:48:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 29 Mar 2022 23:48:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dbba69284b2786013fe94fefe0c2e66a7d3cecbb20f6d691d71dac891ee37be5`  
		Last Modified: Tue, 29 Mar 2022 00:26:47 GMT  
		Size: 54.9 MB (54937710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9baf437a1badb6aad2dae5f2cd4a7b53a6c7ab6c14cba1ed1ecb42b4822b0e87`  
		Last Modified: Tue, 29 Mar 2022 17:38:08 GMT  
		Size: 5.2 MB (5155705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ade5c59e324bd7cf369c72ad781c23d37e8fb48c9bbb4abbecafafd9be4cc35`  
		Last Modified: Tue, 29 Mar 2022 17:38:08 GMT  
		Size: 10.9 MB (10874957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a994f6d4cdbb620339bd2e4ad47b229f14276b542060622ae447649294e5d`  
		Last Modified: Tue, 29 Mar 2022 17:38:33 GMT  
		Size: 54.6 MB (54576420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bf70d022dcc85ebcf204b1587cbb09fca454963d16c1afe48a80cc79c183e7`  
		Last Modified: Tue, 29 Mar 2022 23:19:25 GMT  
		Size: 14.1 MB (14071880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e935ee67cdc00ffcba7067195505ef3b9f503cb3e227f1a7e78154bc5fb40811`  
		Last Modified: Tue, 29 Mar 2022 23:24:23 GMT  
		Size: 187.6 MB (187628576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffe18dbecfb872a197c62809f19bd8e9685513a8a411a86e2e3ebf98242df73`  
		Last Modified: Wed, 30 Mar 2022 00:08:52 GMT  
		Size: 1.0 MB (1017424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b6e4746ad220911b2f0d1f810d834c1d6de93531c5bcb0c3778fdc1efe1fc5`  
		Last Modified: Wed, 30 Mar 2022 00:08:55 GMT  
		Size: 58.8 MB (58820465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd8319e897c7bb8575e31b69ae1a1322c9394177ec24e9efd9d83b108a8f376`  
		Last Modified: Wed, 30 Mar 2022 00:08:51 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6010943a1ce4aeca1773f03e2feb9ce9539d5e3a910c5480f0de34a94846abe7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385471909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c8cfef8c32a9004e84741892ed6b6d4b545cacc76f09f85919323dd28065a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:11:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:19:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 23:26:04 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Thu, 17 Mar 2022 23:26:05 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 23:26:06 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 23:26:07 GMT
ENV JAVA_VERSION=17.0.2
# Thu, 17 Mar 2022 23:26:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 17 Mar 2022 23:26:18 GMT
CMD ["jshell"]
# Sat, 19 Mar 2022 09:08:27 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 19 Mar 2022 09:08:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 19 Mar 2022 09:08:28 GMT
WORKDIR /tmp
# Sat, 19 Mar 2022 09:08:33 GMT
RUN apt-get update && apt-get install -y make && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot
# Sat, 19 Mar 2022 09:08:33 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 19 Mar 2022 09:08:34 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 19 Mar 2022 09:08:47 GMT
RUN boot
# Sat, 19 Mar 2022 09:08:48 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 19 Mar 2022 09:08:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 19 Mar 2022 09:08:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81267e40a2df9e572fe797e45dbc086008422eb2216df18b7a91f1cf13e22b`  
		Last Modified: Thu, 17 Mar 2022 22:21:21 GMT  
		Size: 54.7 MB (54671322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3aa309b6e3524c3f3c38e901096dcffe1aad16e70f0d64aae615a9d7baac20`  
		Last Modified: Thu, 17 Mar 2022 23:46:25 GMT  
		Size: 15.5 MB (15524647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca7da2abc413a6504dadbc635335478670f5d4568f25228522d60bb16dceebd`  
		Last Modified: Thu, 17 Mar 2022 23:52:10 GMT  
		Size: 186.5 MB (186472929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d87451bf59ebf57bd601df308c4abde1fd06f4db561a7c17e380a6c9361475`  
		Last Modified: Sat, 19 Mar 2022 09:33:13 GMT  
		Size: 777.3 KB (777318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaa8059250fa46f75bc619f3ac91d28703e1c40b161baa480fdd78952b5db8b`  
		Last Modified: Sat, 19 Mar 2022 09:33:20 GMT  
		Size: 58.8 MB (58815563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24931225fdbd4567970837f6718a696d757c4ceecd97bf201e979cab0584c1f8`  
		Last Modified: Sat, 19 Mar 2022 09:33:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
