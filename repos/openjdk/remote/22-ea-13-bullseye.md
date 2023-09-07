## `openjdk:22-ea-13-bullseye`

```console
$ docker pull openjdk@sha256:f7f8ccb2540e0b79a0704e361dc6832864de58e5d96d8cf5b98901ddbe0be2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-13-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:4cdee1d3a3b5edd6fef20c135d46c04e5de50bcbc1c86003ed7111551f3a3180
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344465402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d0a8e74adf01221702e816d571107add2842bd9881c838683313920f415cd7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:57:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:58:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:02:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:02:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 07 Sep 2023 05:02:08 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 05:02:08 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 05:02:08 GMT
ENV JAVA_VERSION=22-ea+13
# Thu, 07 Sep 2023 05:02:19 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='fb110a662f4aaa988d446d09ec4ad4683cc96ee24d9f4ebf5c96177b441fa1f2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='d8c826ad7c22505872c310eb7651a071dc380ee14401b65b08861ec4ffc6b95d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Sep 2023 05:02:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d190df514e96e82a9048dff1406b65e853dbdfbfc0d8474b85ef6bf37bfea62a`  
		Last Modified: Thu, 07 Sep 2023 03:05:52 GMT  
		Size: 15.8 MB (15760386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b939be1a16917d966978485a9a71e7b85c49562a3c586f5e4a1f29a4e37eea`  
		Last Modified: Thu, 07 Sep 2023 03:06:08 GMT  
		Size: 54.6 MB (54584978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60457fb06988b48992c8e41a334622830b901c56d04aab1e9e05986fd19c9eb`  
		Last Modified: Thu, 07 Sep 2023 05:06:07 GMT  
		Size: 14.1 MB (14072043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab5299676e54d761094eb5c76c7533f9b78de5758c074169309768811b2c93e`  
		Last Modified: Thu, 07 Sep 2023 05:06:23 GMT  
		Size: 205.0 MB (204991750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-13-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:bf8617dc9823cea78b25866e3dc6f00d7b8caa9a5d0089ff196deb2123062f1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.0 MB (342980892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b812c72a468e3d971e815fb12a6ea382c510aeab4502d6efcd9e532688e8244`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:52:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:52:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:20:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:20:34 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Thu, 07 Sep 2023 11:20:34 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 11:20:34 GMT
ENV LANG=C.UTF-8
# Thu, 07 Sep 2023 11:20:34 GMT
ENV JAVA_VERSION=22-ea+13
# Thu, 07 Sep 2023 11:20:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='fb110a662f4aaa988d446d09ec4ad4683cc96ee24d9f4ebf5c96177b441fa1f2'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/13/GPL/openjdk-22-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='d8c826ad7c22505872c310eb7651a071dc380ee14401b65b08861ec4ffc6b95d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Sep 2023 11:20:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b3f92a99188e47f7b0b8d38aff11fd0ad90510e0d26506aec007d24fe539b6`  
		Last Modified: Thu, 07 Sep 2023 07:00:19 GMT  
		Size: 15.7 MB (15746623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbd1eb48e6c614e3e3767ae9ba92cd3104dc0df1c1cf83b5211c232c4962473`  
		Last Modified: Thu, 07 Sep 2023 07:00:33 GMT  
		Size: 54.7 MB (54676071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c181f7392b1aaab37734498c7f3d28d320b34ff61008cb4f0391de98601b2233`  
		Last Modified: Thu, 07 Sep 2023 11:23:37 GMT  
		Size: 15.5 MB (15528980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4168dbcdcb3f214d9ec6890a1df1d4fcf4b58ff8fb4838e619a570a3b9e5b9c2`  
		Last Modified: Thu, 07 Sep 2023 11:23:47 GMT  
		Size: 203.3 MB (203324502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
