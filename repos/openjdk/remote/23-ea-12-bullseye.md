## `openjdk:23-ea-12-bullseye`

```console
$ docker pull openjdk@sha256:c27aa29ba99a514242380f2d0b60ce0f5ffddf05f2d4ef9bb8ccbe345e847547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-12-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:8ba457d77976ef5dcab3632cd9e253dda35b6c96215c61ef0d55bf14f0daa855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342737617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f58106e9d80c6463787093cef59fe8219b2331daad1473035f0eba052ba3ec`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Thu, 29 Feb 2024 19:48:15 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 19:48:15 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 19:48:15 GMT
ENV JAVA_VERSION=23-ea+12
# Thu, 29 Feb 2024 19:48:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='892346bd29f50e248ab5980903e5759f73d8ac2b6ee0cd918e3acdb132eb8776'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/12/GPL/openjdk-23-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='3e927b03ed3af88337e11918d05955c72b71c1664dc5791ba4a6590329004657'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 29 Feb 2024 19:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c7d862cba465d342dbf73dca7caf5e04c2ec7b374c918ec26f305e2ba3f78f`  
		Last Modified: Tue, 13 Feb 2024 01:32:03 GMT  
		Size: 54.6 MB (54588461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a969c1c5c543f8b1b0bfa6648f3371de38eebb626367838bf23854f0e198c5dc`  
		Last Modified: Thu, 29 Feb 2024 22:50:45 GMT  
		Size: 14.1 MB (14071415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c4d1fe43afc260f22b5318b27ad5f24e23fe30a90497add8685cdb64f4015c`  
		Last Modified: Thu, 29 Feb 2024 22:50:49 GMT  
		Size: 203.2 MB (203229371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-12-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:82d17244f5242d359e6814e08e259d69d2b08ca8591278478448f3497c4bd011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8175945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415c3597ab9f8a1d1a2fbd1417e652ae7a4869748134fe97f557d2be6b5dbd70`

```dockerfile
```

-	Layers:
	-	`sha256:790655507168d22d700617a4877d64842b61153389704ac0066fee2d87c368ec`  
		Last Modified: Thu, 29 Feb 2024 22:50:45 GMT  
		Size: 8.2 MB (8157039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f066270377ad0b847a1ba2988db6cc70e1c5bbcf357dc6fc01c83fe2eb6de34`  
		Last Modified: Thu, 29 Feb 2024 22:50:44 GMT  
		Size: 18.9 KB (18906 bytes)  
		MIME: application/vnd.in-toto+json
