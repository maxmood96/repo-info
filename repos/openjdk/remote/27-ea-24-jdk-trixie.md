## `openjdk:27-ea-24-jdk-trixie`

```console
$ docker pull openjdk@sha256:c966a2ba72fabca73e5ea80573fbc7b943fe8272a929471fa88a4db994155c68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-24-jdk-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:896d3788bd7dcee763df442075e3e47d361f03835cd64a5bbb42da992f246547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 MB (385782797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998da2379009c6e282b6ac14818256efa1f8d702c54bcb1acce7a1bfe8bff5d1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 07:11:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:12:03 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 02 Jun 2026 07:12:03 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:12:03 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:12:03 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:12:03 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:12:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee079e88698dba3c571f673ba87a650a65f0530f76657da9a6f6c34ae19bd2c`  
		Last Modified: Tue, 02 Jun 2026 07:12:28 GMT  
		Size: 16.1 MB (16065755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1223e5f183da5100fac6414cb0db9555ae05cfbd6b443eb9481f62eda86cca`  
		Last Modified: Tue, 02 Jun 2026 07:12:34 GMT  
		Size: 227.0 MB (226994772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:3a5ba68720c99bfb0295c8fe673be3da2bda816859015fcc09f0d1752a666d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8526700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62dabd3d8ae33de521e62e5c4f26e52eaaadf429df712abcb630f261c9359449`

```dockerfile
```

-	Layers:
	-	`sha256:357a3bf35c2fe7c0e236b33c1cb9ff2d5272be6a48a327d3d075f8373cf85708`  
		Last Modified: Tue, 02 Jun 2026 07:12:28 GMT  
		Size: 8.5 MB (8508787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc97e4aaaa86be83a3de2863edbc669c68d005db77de4feb9663fed64bd6f560`  
		Last Modified: Tue, 02 Jun 2026 07:12:27 GMT  
		Size: 17.9 KB (17913 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-24-jdk-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b487bf29e9b16b2d44337e58f163b70c2d0cfc1ca505d087d7ac27138854f420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.4 MB (383373192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8a6304c80142972fd6f7926c612bb8a7d8d4c11fe04d589a4de3e0691b403`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 02 Jun 2026 07:11:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:11:50 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 02 Jun 2026 07:11:50 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:11:50 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:11:50 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:11:50 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:11:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbcfc84c7d2292e91c64bb3c247bcebc27f60c00e21908a60452e00af6edc6d`  
		Last Modified: Tue, 02 Jun 2026 07:12:16 GMT  
		Size: 16.1 MB (16071421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568344aa88047a491a1e07e205ded09ec867282cfa99b0a8ecb8331b31c3301a`  
		Last Modified: Tue, 02 Jun 2026 07:12:19 GMT  
		Size: 225.0 MB (225011096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-jdk-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a3c6cdb19fab842fe6c9732489463a1677ac3511ad213f3b007d46edea4b414e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8720972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2988425a45dd46b2a5ea76b29e3cb8253606bb5062dbe72c39bf51bf641b1532`

```dockerfile
```

-	Layers:
	-	`sha256:7839b549a0588b0625be977b572b602583c1cdd97aa130d7c1f779afa3953048`  
		Last Modified: Tue, 02 Jun 2026 07:12:15 GMT  
		Size: 8.7 MB (8702940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b853024054fe8323dd041050aa25df92930a3dca8038353880982083ce670bbf`  
		Last Modified: Tue, 02 Jun 2026 07:12:15 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json
