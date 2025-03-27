## `openjdk:25-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:ce32ccbb22aec1ccdeb6d931fa973332bc74a85b6ed1b4886cd887a63f0d7fec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:dacc771320760a9276edd69f574a4fbc0012bcc567d2408bb9a25b4f54e06a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243976075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f35b36c4683c7c904e932a90f0526139ad42d37d9dab7f61ca8aa8fbaeb232d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471f94150f5784592562a14d1950f8ab834eb36ef18f87981c149bd49e11ce43`  
		Last Modified: Thu, 27 Mar 2025 20:45:42 GMT  
		Size: 1.4 MB (1377199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f7ae9ba02636596272358153c5c97babef6bc24b4c2d1093cffd5c5edc9490`  
		Last Modified: Thu, 27 Mar 2025 20:45:47 GMT  
		Size: 212.3 MB (212345040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:75141c5ea307efc5dea8c58ef0d2fcda25468a8a164d69bdc0c0df12f8377dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2677d028408f9e996e4dbd25a910bab9359efcff8caf4363e2a33e5db2f2b2`

```dockerfile
```

-	Layers:
	-	`sha256:41d782453a0cbcbd1cecf851637fbb0c9e1611d7b571106f138d3ee3519fefc3`  
		Last Modified: Thu, 27 Mar 2025 20:45:42 GMT  
		Size: 2.8 MB (2827293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:639abda8b5559a3bb773659531612ffc4110bc486a01a51749846e7c78bb4352`  
		Last Modified: Thu, 27 Mar 2025 20:45:42 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cb37ecf1326c44b1c14f42ae2e12f60c8f15d53404a8f3021332e98d45a62395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240336984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f235b988a085555c593ea9edbc8e020f5ebc756994c0bf0f056c7508044270`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-25
# Thu, 27 Mar 2025 18:48:13 GMT
ENV PATH=/usr/local/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 18:48:13 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 18:48:13 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='0cf725c3714270c836ac114ec7ffeec45798e46613c2ae1a893b49ceaeced9b4'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/16/GPL/openjdk-25-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='e2ab5d0486dc4d490e62e81d09d3a7b0aade74d2bb743668864339e80f9b8f75'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 27 Mar 2025 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678ad60b709415e17943bc531e3f43337e0d0157061bede4b10b9f3d9786a76`  
		Last Modified: Fri, 21 Mar 2025 17:28:25 GMT  
		Size: 1.4 MB (1361285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c01436650cb00e54ce1891d9ebca003487fc284fcbbd18762edd03235d4fe61`  
		Last Modified: Thu, 27 Mar 2025 20:50:21 GMT  
		Size: 210.2 MB (210229776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:134fdd3632fec273dbe376ceb4e59bca067e75fa4f3dfa017b051a92be6926d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2844658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59f470d0bd8b9b7dedf3e8d14b780ec4c34ef62780d8d4a305bff28cd4583a1`

```dockerfile
```

-	Layers:
	-	`sha256:c18a7c95d0cc4c6713529493908ec88e1f08f6dffd39c1bfeda45725e46b6741`  
		Last Modified: Thu, 27 Mar 2025 20:50:17 GMT  
		Size: 2.8 MB (2826945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc452e1ceaff2af76387ed6c501e7f7aa3f0338a33675e031ddf8eb0c8940b5b`  
		Last Modified: Thu, 27 Mar 2025 20:50:16 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
