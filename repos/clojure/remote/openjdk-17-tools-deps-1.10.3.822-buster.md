## `clojure:openjdk-17-tools-deps-1.10.3.822-buster`

```console
$ docker pull clojure@sha256:a321ff50d53d02ad6ab0bee5af95bbb737771f949aeb0d81e3468b877c22ab2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:openjdk-17-tools-deps-1.10.3.822-buster` - linux; amd64

```console
$ docker pull clojure@sha256:68b9601b46bd0395712882dd9a57533bb22e58823cf1ae2ba52df36ba75e0ae9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.2 MB (347191353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8e80bd5583b11856915d88f3e10ca69f12f658cf9f60daed56a8cd3abc8e28`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:44:08 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 12:44:08 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 12:44:08 GMT
ENV LANG=C.UTF-8
# Tue, 11 May 2021 00:15:15 GMT
ENV JAVA_VERSION=17-ea+21
# Tue, 11 May 2021 00:15:29 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2a923efe7bd6c682d5550551a16dadfe8057b0106e0b4b4aad2aa56b8bed4c19'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb389fe6915c9e70e639db6ab630342a5ccc275f5a06aaded43321eeea9ba6ee'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 May 2021 00:15:29 GMT
CMD ["jshell"]
# Tue, 11 May 2021 01:30:37 GMT
ENV CLOJURE_VERSION=1.10.3.822
# Tue, 11 May 2021 01:30:37 GMT
WORKDIR /tmp
# Tue, 11 May 2021 01:30:49 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ebc820fe0e74de4bd77e6d5bd7db4a262ec1902efdf4d0553309485afcd75abf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 11 May 2021 01:30:50 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37aabde37b87d272286df45e6a3145b0884b72e07e657bf1a2a1e74a92c6172`  
		Last Modified: Sat, 10 Apr 2021 02:02:22 GMT  
		Size: 51.8 MB (51841093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4aa53f9ffbf7bd8ebaa551102ae5146025c9f5063b12dda7d8d42de26e2ebcd`  
		Last Modified: Sat, 10 Apr 2021 12:53:45 GMT  
		Size: 13.9 MB (13921315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56bce962879e8d757aea295ab5aa75012833715a3a90151718d9f05241beef96`  
		Last Modified: Tue, 11 May 2021 00:22:30 GMT  
		Size: 186.1 MB (186137929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c05e2231f289a053ce97040bd44bf350321f0e1b34cb34fedaf491406f2ea0`  
		Last Modified: Tue, 11 May 2021 01:34:50 GMT  
		Size: 27.0 MB (27027918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:openjdk-17-tools-deps-1.10.3.822-buster` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8669ace888608b0343de516012c4efc6dcfb93dbde25f84536acbf864b60a4d9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342576179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e349b8df11610bc29d9582a9e70d96a004f4d01bbba7e28b046a7ce6b12c3ab3`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:01:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Sat, 10 Apr 2021 23:01:17 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 23:01:18 GMT
ENV LANG=C.UTF-8
# Tue, 11 May 2021 01:45:14 GMT
ENV JAVA_VERSION=17-ea+21
# Tue, 11 May 2021 01:46:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2a923efe7bd6c682d5550551a16dadfe8057b0106e0b4b4aad2aa56b8bed4c19'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb389fe6915c9e70e639db6ab630342a5ccc275f5a06aaded43321eeea9ba6ee'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 May 2021 01:46:04 GMT
CMD ["jshell"]
# Tue, 11 May 2021 02:42:47 GMT
ENV CLOJURE_VERSION=1.10.3.822
# Tue, 11 May 2021 02:42:48 GMT
WORKDIR /tmp
# Tue, 11 May 2021 02:43:11 GMT
RUN apt-get update && apt-get install -y make rlwrap && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ebc820fe0e74de4bd77e6d5bd7db4a262ec1902efdf4d0553309485afcd75abf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)"
# Tue, 11 May 2021 02:43:12 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7f1cf823a7fca9771e278355d8924fac8d9cef1f8e3ecbc87332c4859d1d4f`  
		Last Modified: Sat, 10 Apr 2021 02:01:23 GMT  
		Size: 52.2 MB (52167974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c00066088349286faa32311c9ea25724917bd388d9a9fdf3b8b0235bfcd5cac`  
		Last Modified: Sat, 10 Apr 2021 23:07:43 GMT  
		Size: 14.7 MB (14673668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72290feeb72347156cd002b30a35d66994ff4539d5272eed7b871383f104c9`  
		Last Modified: Tue, 11 May 2021 01:52:28 GMT  
		Size: 182.2 MB (182216939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de158be1f4d34413bd8464ee825a1f0370921b158e6259bb19618175193067cc`  
		Last Modified: Tue, 11 May 2021 02:46:00 GMT  
		Size: 26.6 MB (26612309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
