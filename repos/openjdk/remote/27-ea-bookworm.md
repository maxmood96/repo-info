## `openjdk:27-ea-bookworm`

```console
$ docker pull openjdk@sha256:d11de9eca8ed4202ad5d0c65b0f302a256080b2503f1620372f3c33b02427565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:85ea3598f2b90f7e57a6b61abc804993bd657a1e0f54376344df281e7c23e2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382798837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db077aa3dac9b903d3b6331a385eb698738ec56eb0c7ae5b80dbc152be6fe5ec`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 20:18:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 20:18:46 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Fri, 15 May 2026 20:18:46 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:18:46 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2026 20:18:46 GMT
ENV JAVA_VERSION=27-ea+22
# Fri, 15 May 2026 20:18:46 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 May 2026 20:18:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82d1edf1c71699dbca2ceefa28844e97ce43252c369111de61c11a463cc89e`  
		Last Modified: Fri, 15 May 2026 20:19:12 GMT  
		Size: 16.9 MB (16946730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a5d622be574764b7c431bae421e26e65ec60fb525b61da07b422d3d095dac9`  
		Last Modified: Fri, 15 May 2026 20:19:19 GMT  
		Size: 228.9 MB (228924215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:c19d9738546130883a6ac476f408ec06c097f1d92601158ed02aad284160b57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8685556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489865e2d55ec7722f809639412bea403fc849397cf1e8d5e80160f9e060591b`

```dockerfile
```

-	Layers:
	-	`sha256:29f69bb0e24e73e3b37523c19fb6aeabf29d61dc759d4c225d8ac2e435c9dbc4`  
		Last Modified: Fri, 15 May 2026 20:19:12 GMT  
		Size: 8.7 MB (8667617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20922cd3f69499c88defae0dbc409216e0a3ef1201543ba5d006e60f0369e473`  
		Last Modified: Fri, 15 May 2026 20:19:10 GMT  
		Size: 17.9 KB (17939 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0ab11f04ee2c53233ed6fbea018552108b7eb0ae6d370384c44c88bf6ce802fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381085413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa46dd055768a3309b7690b55f3c14c1cdf88047e3529f708232c4445fff57f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:17:52 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Wed, 20 May 2026 01:17:52 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:17:52 GMT
ENV JAVA_VERSION=27-ea+22
# Wed, 20 May 2026 01:17:52 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-x64_bin.tar.gz'; 			downloadSha256='47b58a37806dcaf954eb174f682514b06f17b8205d154ad84c2f68666c302570'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/22/GPL/openjdk-27-ea+22_linux-aarch64_bin.tar.gz'; 			downloadSha256='87c706c502d3fa5d8a8ff7bf543c7903207fb8d5a11ed637fe05ed33b8179702'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 20 May 2026 01:17:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457e43f59500aa65f31ea874492c4565d113ef70b9dfa92c6aae5915c1881d4`  
		Last Modified: Wed, 20 May 2026 01:18:19 GMT  
		Size: 17.7 MB (17730275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fdcf021661fcf81812d6814f038d013996e01b17d3dccd13b3107abf9ededa`  
		Last Modified: Wed, 20 May 2026 01:18:23 GMT  
		Size: 226.9 MB (226874657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:83bbae90e616f7fe063dc55484565bbe2fc9b179e4e928018435c1f7b8bf8d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8822542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b27c4d7f37e2fe458efca8883d31c00e5325eef72ee2fc851f06d582f6485a`

```dockerfile
```

-	Layers:
	-	`sha256:46417b5f2abcb8f7746e15c26601f2f7427f57024c0181f83363d8cd9151d1dd`  
		Last Modified: Wed, 20 May 2026 01:18:19 GMT  
		Size: 8.8 MB (8804484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e44ede7c7f8176aef4e69bdf791b97ec361cbd070b7b878b82a72e264e041af3`  
		Last Modified: Wed, 20 May 2026 01:18:18 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
