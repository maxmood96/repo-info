## `openjdk:22-bullseye`

```console
$ docker pull openjdk@sha256:ac371349bd191b5d9315363cf38d45c445cef2d6b610927c945f964f42df5f17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:db8b74c85efe25b16e6e50cf45907436fc724050626760c982395d1a002a7188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342380979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc69d6d43f47eb59ba74e228d7bf9d84970bdb163a2b758c233e017c4f4e08f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Feb 2024 19:48:12 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
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
	-	`sha256:7340ebde2a6d06fb2531d24cd746b860f36988f2c16982f463df94dd504a302f`  
		Last Modified: Tue, 13 Feb 2024 02:58:14 GMT  
		Size: 14.1 MB (14071332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e9646c82aa25a5906bdb3ea56d10857a21c67f7b1ed10085621c8be481a136`  
		Last Modified: Tue, 13 Feb 2024 02:58:18 GMT  
		Size: 202.9 MB (202872816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:109921c87e28add903592815422e3cc0abf03ef95291adf1f2427a2704ea59e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7065512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce842bb6228a6281ed3eeefdf67134c5d380771f38ecd12772352ef5d013fd0e`

```dockerfile
```

-	Layers:
	-	`sha256:489fa9b3ab0df241cbcd33cc2218380d87238e288eb12ead8d199157c9b724b1`  
		Last Modified: Tue, 13 Feb 2024 02:58:13 GMT  
		Size: 7.0 MB (7047193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e230c3b4f46464cd2c103daf38e2ea3400838d0bbb7ace038eec0eaa5a7618cc`  
		Last Modified: Tue, 13 Feb 2024 02:58:13 GMT  
		Size: 18.3 KB (18319 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a5a843fa76a22463a6ab07ab00013726f5fed2174c9e5d5ae1bf4c4d8cfad9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340613723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e77947c8d98e717b2fc7a50d6f0ce093bbb49ec869e14c0adad48424e0fd8d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36799ce495b4202a2dd0034c9955834237665bad54a5154faf464f20da7eb84`  
		Last Modified: Wed, 31 Jan 2024 23:53:07 GMT  
		Size: 15.8 MB (15750615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da2c043d162bc242dc65d025ae4775153d19e07ae75f2d759ab1f51bdefb529`  
		Last Modified: Wed, 31 Jan 2024 23:53:22 GMT  
		Size: 54.7 MB (54699941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e361934ac48c39bb74079449b2f9bbddf18b39b92133150271ba85b2d8782bc`  
		Last Modified: Fri, 02 Feb 2024 14:13:35 GMT  
		Size: 15.5 MB (15527406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacea244292b543df9365d0e81df299154a74861caf0f62920f75d89ae109570`  
		Last Modified: Tue, 13 Feb 2024 00:34:40 GMT  
		Size: 200.9 MB (200927494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:6474f2b7a769406244418680bee6892feb6f840b2ade712bd8c580a9d652b4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7061864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de59271be9f49a07774dc755a4db1c11b24ad58895725f0c9238b310cf991398`

```dockerfile
```

-	Layers:
	-	`sha256:b6790918395c680dc5fc6fa2e9d5eba90e7df02681a4b943c3b510f072a4e48f`  
		Last Modified: Tue, 13 Feb 2024 00:34:36 GMT  
		Size: 7.0 MB (7044032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3445127824e2d6ff328e18ca996302c3f3cfa5314d4d9ed4f64754c5c4a0589`  
		Last Modified: Tue, 13 Feb 2024 00:34:35 GMT  
		Size: 17.8 KB (17832 bytes)  
		MIME: application/vnd.in-toto+json
