## `clojure:openjdk-17-tools-deps-buster`

```console
$ docker pull clojure@sha256:b7a0b92374f2f48d100771a13d0a90c3c1f2cd08b1e76b20ffdf0da4e3f0be68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-tools-deps-buster` - linux; amd64

```console
$ docker pull clojure@sha256:69880c007621bd5311d4f7b0b85f01638eeabb0a88a5e187a3625cb1c2e9d89e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347312096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0b6a17ec5fca040c3ea2aa8bdb4b797dc8f9d45b5bb76522b1ff763ba7126d`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Fri, 21 May 2021 17:51:04 GMT
ENV CLOJURE_VERSION=1.10.3.839
# Fri, 21 May 2021 17:51:04 GMT
WORKDIR /tmp
# Fri, 21 May 2021 17:51:18 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba754dcf1d88cd1e8fe8337637fe249b91dff4f63115b4b9550947539869c804 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Fri, 21 May 2021 17:51:18 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:134e24a7c928133dce9ed0f2aeba221a0abd84a7f572a3f175dbf69c1372beb8`  
		Last Modified: Fri, 21 May 2021 17:55:20 GMT  
		Size: 27.0 MB (27028294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-tools-deps-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:583aba5d82fa1f425012cc3c7c04020ff830d72fd24364366792934ce74ea26a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342575291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15900fa0b3cdb3102b5f3b38f03cbae524f41b94d7b892959e0ae99dd7446e83`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Mon, 17 May 2021 23:36:44 GMT
ENV CLOJURE_VERSION=1.10.3.839
# Mon, 17 May 2021 23:36:45 GMT
WORKDIR /tmp
# Mon, 17 May 2021 23:37:13 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba754dcf1d88cd1e8fe8337637fe249b91dff4f63115b4b9550947539869c804 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Mon, 17 May 2021 23:37:14 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:1497a38b3490fbad787ca19fd7957c34e538676d637407e5aebcb9a208353b69`  
		Last Modified: Mon, 17 May 2021 23:40:25 GMT  
		Size: 26.6 MB (26612690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
