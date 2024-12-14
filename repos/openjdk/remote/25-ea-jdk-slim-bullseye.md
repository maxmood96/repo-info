## `openjdk:25-ea-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:77ee2d921a2223e7e01e3fab9c28408f6129ddd6646ca4132d28afd1e23da648
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-ea-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:0ad8b9bfbb03d829e485721cd1c19a85fa09c17aa5c8c209943125ac1c82f579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244654370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb344da9fe8a39bf4de748c952f1d8793a96f09d82df77cfa48d2facc53ff41`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3529ad9f819082a40fe07efd378c9a2cdb7be262cc6d7075581e2f793245fc`  
		Last Modified: Sat, 14 Dec 2024 00:29:57 GMT  
		Size: 1.4 MB (1377266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c895573d0136bc1a80fc12a3b606aa25db7f4500a37525aadebf77ef13b92`  
		Last Modified: Sat, 14 Dec 2024 00:30:01 GMT  
		Size: 213.0 MB (213024460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:5dd06f7327f4d822a976c67cadaca056129f4689867ca5787d10f6e091d86fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178a3aaaa46234c74877c50271aa5874ebd1ea8e982d5d9ddf16a245fc5f7e94`

```dockerfile
```

-	Layers:
	-	`sha256:fef85343802787f77f57ee06bacb3fdec9afbdf4a775a8638fd20f3f4e4af945`  
		Last Modified: Sat, 14 Dec 2024 00:29:58 GMT  
		Size: 2.8 MB (2830871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1083a0d7f2ed1a8016db1fd707d7989297d273d0b0b961e39460047d7a97035`  
		Last Modified: Sat, 14 Dec 2024 00:29:57 GMT  
		Size: 17.6 KB (17557 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-ea-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1b371b5d293380f2d4535b5643ec63edad622581a645e1aa7b7c50269e83b47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241085003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437b9bd7c647c3aa6d8828bf505cbb07442a456d882e9b34485402d1ef90eec4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Fri, 13 Dec 2024 19:52:09 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 19:52:09 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 19:52:09 GMT
ENV JAVA_VERSION=25-ea+2
# Fri, 13 Dec 2024 19:52:09 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='00d23f37267bee9e859091c506e986262ad9b7fc9f7818d3e9d602191252626a'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/2/GPL/openjdk-25-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='c3b55a9e0597d7942cadec32e1e920bdc4022d893bb4501ef8b54eb6a9ff2bd7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 13 Dec 2024 19:52:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7ad6e84f249b4b319e4c8cf12e7929732105f68e6f8a67945acfd605733bd`  
		Last Modified: Tue, 10 Dec 2024 01:31:31 GMT  
		Size: 1.4 MB (1361283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc665277319cc5ce1f6066905c008f920df6ad33535744f82c748503329ba61b`  
		Last Modified: Sat, 14 Dec 2024 00:34:12 GMT  
		Size: 211.0 MB (210978797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-ea-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:f57cbff66fbf6a578b0639ecbb251a477225e6c124645f1081abfdc7b233f29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2848221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07b4fa0128bdbbfe5c6eb3eaa99a06fc65a1581ce86f9ffbc504321a14a2c77`

```dockerfile
```

-	Layers:
	-	`sha256:5bc23f8d162f8f7118f4a6658517502b790493c123b9650e68317dfd67db94a4`  
		Last Modified: Sat, 14 Dec 2024 00:34:07 GMT  
		Size: 2.8 MB (2830521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4868bb4aba6f1004dbe847f0449b23568086be079ee88514accc6170f90fa203`  
		Last Modified: Sat, 14 Dec 2024 00:34:06 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
