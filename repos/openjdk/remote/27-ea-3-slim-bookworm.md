## `openjdk:27-ea-3-slim-bookworm`

```console
$ docker pull openjdk@sha256:8f690df57a08b2f343e2ffd4260367a1017c2e71cdb4e058ab1c4ccf4d6727a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-3-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:3541f82b7e0d3999e8b1c689b877361981b0b9920c0ed0a021f2b30783cb35c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260359323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c02260d641434daea636ed20e80b1dbf22ec5f5307bac11d21bea4e2eded42`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Wed, 24 Dec 2025 05:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:20:36 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 24 Dec 2025 05:20:36 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:20:36 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:20:36 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:20:36 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:20:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dd6f91f4bda9ac47e6b986809e70ccbee5838db29568be69fea87bf15af3e5`  
		Last Modified: Wed, 24 Dec 2025 05:21:07 GMT  
		Size: 4.0 MB (4027345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4abf3310141c0d7f4a423cd52d73470f77b264daafb6622319041e0913ef1f`  
		Last Modified: Wed, 24 Dec 2025 05:23:04 GMT  
		Size: 228.1 MB (228103560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c931e7ac728c86f8276a7acc92767251b75f1d3eccc544ed8ea576b514ef7841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d00cfa78687401f62986c1ee56545fa466f5d9d55e03c181ad510298071d639`

```dockerfile
```

-	Layers:
	-	`sha256:beef74eaf106adb67773da0c2e75a8bd24941e53a7ea2639a7914bde64b67ac2`  
		Last Modified: Wed, 24 Dec 2025 07:26:54 GMT  
		Size: 2.6 MB (2649781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f8614611f08553b1de939ab29c4370bed83981be671b7bae4bb24b5e74e7e9`  
		Last Modified: Wed, 24 Dec 2025 07:26:55 GMT  
		Size: 16.9 KB (16858 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1bed178f000630e9a8f4526d409c3b34e49bfe3111f6615636b97435967ead00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257971557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e00793e0448b3293d3cbbe6c42fc2af419c6778642a7a7273bec9d40825a47a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Wed, 24 Dec 2025 05:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:22:24 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 24 Dec 2025 05:22:24 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:22:24 GMT
ENV LANG=C.UTF-8
# Wed, 24 Dec 2025 05:22:24 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:22:24 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='aaaea47c6d93cbeb444a08dfa58105ee17a15ab5c6d07b98c71952d8c12ead80'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='b90b89ea9b49abf85ab7ae4323ddb7ef028ab69054d08d43e72b1f6e0b8860f6'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 24 Dec 2025 05:22:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a654ffa1c04fc44906d5dd3ab51bdd933d02425bbae802f5c73c2147f949fd8`  
		Last Modified: Wed, 24 Dec 2025 05:22:55 GMT  
		Size: 3.9 MB (3851440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7d6402d80db2305e764faf55d3086e74f69ad7f273d0a248489711a7eb8e4b`  
		Last Modified: Wed, 24 Dec 2025 05:23:03 GMT  
		Size: 226.0 MB (226017888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-3-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:10012ae396766ba58825f8c49d4223a32b481d35557f04915eaf95937c27d4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2666392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d664ae5081f2e38acd93f665b42225272a5da772b68211ea5ad06f79b4fcc3`

```dockerfile
```

-	Layers:
	-	`sha256:8b0ee23421ce51a70fe08b85787cf6a235fe919d28b244c6a8e4def459e89247`  
		Last Modified: Wed, 24 Dec 2025 07:26:59 GMT  
		Size: 2.6 MB (2649415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7725d5def9fe14355667817e8a6b743e31f6b42c84612606012692e1e6776a`  
		Last Modified: Wed, 24 Dec 2025 07:26:59 GMT  
		Size: 17.0 KB (16977 bytes)  
		MIME: application/vnd.in-toto+json
