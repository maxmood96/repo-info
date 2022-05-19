## `openjdk:slim-buster`

```console
$ docker pull openjdk@sha256:7483362ef37a19245638038ab3e902f10a69d29390359364d1763b998869fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:slim-buster` - linux; amd64

```console
$ docker pull openjdk@sha256:1201f5d5750aac6efa9e97c50bbedb6490a617b408b7ade93358d6388e261bcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218316605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97928de0b87ebaeb9dd5b6e5f18c2be3b6cd5d52f8e0ce08b480a66db9a6a59`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:51:43 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 20 Apr 2022 10:51:43 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:51:43 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:51:43 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 20 Apr 2022 10:51:59 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Apr 2022 10:51:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b97724dec0639ffbe1d30e60defc8ff8fc2e27a3844e7c6173e64cb73e25b88`  
		Last Modified: Wed, 20 Apr 2022 11:02:57 GMT  
		Size: 3.3 MB (3273257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a8e5c4d31807097cbd665b38de64e8a7d442e0e99b9cca01b3800bb803a164`  
		Last Modified: Wed, 20 Apr 2022 11:08:24 GMT  
		Size: 187.9 MB (187902684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:slim-buster` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1a50f5d6ecea6091ce4846219426d205feff69f403a01fe48d6654df9a4e2f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216850556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaddceb6caa9a954d0ca63d3705aa66d813cab8455d7a9a84a50cd4eb53924e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 May 2022 00:47:26 GMT
ADD file:2536146c773d09db1a8fbbff00933acc459d8929feb3cff5b93ca4c23b577845 in / 
# Wed, 11 May 2022 00:47:26 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:16:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:18:56 GMT
ENV JAVA_HOME=/usr/local/openjdk-18
# Wed, 11 May 2022 14:18:57 GMT
ENV PATH=/usr/local/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 14:18:58 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 14:18:59 GMT
ENV JAVA_VERSION=18.0.1.1
# Wed, 11 May 2022 14:19:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 11 May 2022 14:19:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:383d573fdcf2c6da56fdb61e120549d7bc200471208ca4c7c6605c57a0a87ef6`  
		Last Modified: Wed, 11 May 2022 00:54:36 GMT  
		Size: 25.9 MB (25909014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ef35bf9af0d08f4a170567ffeb4f2374230da90c85eec67344eb6c8994306b`  
		Last Modified: Wed, 11 May 2022 14:35:37 GMT  
		Size: 3.1 MB (3125755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ce35c1992f41932ae70d4b0d575b4edac95fdb839a523d5baecc9c64c70452`  
		Last Modified: Wed, 11 May 2022 14:39:47 GMT  
		Size: 187.8 MB (187815787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
