## `openjdk:26-ea-20-slim-bookworm`

```console
$ docker pull openjdk@sha256:27c3ab190ad2c62e6436900ab89f91e27a2af89219baa1d7ff75f66f391a0111
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-20-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:53b378506855a55e9417271d89cb35629568e6d73b44de4f519142cae7eb2c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258086876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c832f3f2ebf871258bea731d732e4cf45440c928c9143f2bd2f01ca7c90fe74d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28e0250992889741a9a7ef27b2775b966f31cbd4a102862869773f5d296eb4`  
		Last Modified: Tue, 21 Oct 2025 20:20:50 GMT  
		Size: 4.0 MB (4027365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcebf62e4b63d468004df0e9e6f69a1fcd1ffee0bfc12a1fcbcfbd0623c74e7a`  
		Last Modified: Tue, 21 Oct 2025 21:41:49 GMT  
		Size: 225.8 MB (225831190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-20-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:36406d0631bf128fb5a52e32b97781665c82781bb028b6d33c5083364fc9a230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137770318015fb99847bd537fbb096677a5068765845162dff51fdeb5e92cccf`

```dockerfile
```

-	Layers:
	-	`sha256:88adf9f8722f8e314ec590f6a6e063c89b35ec7a78627566b7a92d01b822a267`  
		Last Modified: Tue, 21 Oct 2025 21:24:19 GMT  
		Size: 2.7 MB (2651699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a16519c92f288c5af13180ac0593a9c4a18b7e44b827d89c8d2381c23f12bd1`  
		Last Modified: Tue, 21 Oct 2025 21:24:20 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-20-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:566d0475f0ec561e5f19f8baec3b8ef5c5ea0dc077af59cefdbbdc68e3b14a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255644479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1a9e5005d12c0db9ffbe66539876ff677455bdc732383bb035074125c049e5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 20 Oct 2025 18:48:18 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 18:48:18 GMT
ENV LANG=C.UTF-8
# Mon, 20 Oct 2025 18:48:18 GMT
ENV JAVA_VERSION=26-ea+20
# Mon, 20 Oct 2025 18:48:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='5a59bcbbbee3ef3870abde737d101b8688ff06144c853ff29ef6ac8247c96a87'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/20/GPL/openjdk-26-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='bf2a13c36da561391ccbda5d5d8dcce3963d35f2d5b0819a1fa725999f090aa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 20 Oct 2025 18:48:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3202bada07c5ab0b983ca48b49561caae658903ddcbb2bc122aba9c04cad5a3b`  
		Last Modified: Tue, 21 Oct 2025 18:14:18 GMT  
		Size: 3.9 MB (3851337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a7b3172e1e24bb35a8e87bc6999886549214ba3328b1b76764156842239a6a`  
		Last Modified: Tue, 21 Oct 2025 21:43:07 GMT  
		Size: 223.7 MB (223690952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-20-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:fbafea1f563ae4c5ff055e982df588b019bcb6eece06658403d01111b51cfae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875d7e3fbdc5f23a88a0615f7d8c979fb084386af171da560646aa03365ac96f`

```dockerfile
```

-	Layers:
	-	`sha256:8164fe3d03c2ecc34b766abea850721176e43794ad86700fd164e90087d38b04`  
		Last Modified: Tue, 21 Oct 2025 21:24:24 GMT  
		Size: 2.7 MB (2651357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ae1b9bda3e493db0cb3a1ddc7dcdbc91bbf5d99344af24821544c283e0fc223`  
		Last Modified: Tue, 21 Oct 2025 21:24:24 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
