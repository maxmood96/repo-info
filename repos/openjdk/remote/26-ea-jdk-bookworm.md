## `openjdk:26-ea-jdk-bookworm`

```console
$ docker pull openjdk@sha256:35ea804195bf1eab432bf0cfea788f9dca674b385935c65b50b05acdb0450c57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:d8323bd0ab1a5c12e93a46fcc6b9817d25e5a6a3cbd9505b8d57d13eea9d18e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381677798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f014dc936f49f9a26fa657a2d709f6f0fe52df1b909159fc6cecc01dc22b049`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:27:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:27:18 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 10:27:18 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 10:27:18 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 10:27:18 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 10:27:18 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 10:27:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e11476ed9a0c9afbd08c703aec5d55eb5d8dc40e57d80e10dc0c162edbf322`  
		Last Modified: Tue, 18 Nov 2025 10:27:59 GMT  
		Size: 16.9 MB (16943579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f322cc2ad0a60868dada2c1e6862ce05e5eb26dbfeaae256b93cccbf84b0d9`  
		Last Modified: Tue, 18 Nov 2025 13:55:42 GMT  
		Size: 227.8 MB (227827848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:261a65e8bd3ee4ee3743e30a4905d389a05752a025b9aeaff7fa8e471b2aeb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8686138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a9e0cbdf152425f487ec4b5a818b00f335d5c214bffc635755679303b63929`

```dockerfile
```

-	Layers:
	-	`sha256:b2d7347cc9fff5a5452c63b98fc86450804b63e20baa7f7f4f13a505ab3a49e5`  
		Last Modified: Tue, 18 Nov 2025 13:23:20 GMT  
		Size: 8.7 MB (8668200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feda030490670d68d9422a75b3d1c0fb5469bec1371504ca35342ff8325adcdb`  
		Last Modified: Tue, 18 Nov 2025 13:23:21 GMT  
		Size: 17.9 KB (17938 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c02d1eb927eb914c83846525992859c928329b31ba72020ae836affae9ac614c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379740437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441d838b5bb01b2344a842e91d096a70e1cc3dcaa96fb19010f61445be28dbc5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:43:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:43:16 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Tue, 18 Nov 2025 06:43:16 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:43:16 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:43:16 GMT
ENV JAVA_VERSION=26-ea+24
# Tue, 18 Nov 2025 06:43:16 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='4ba2cf8ca6a66fbea892ba55048f82d8cd4fabe95d9364ac28a79b282c6207f8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/24/GPL/openjdk-26-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='d6f947b5c9fa605b41f4890ef6e09f2c0c321215681497f2174efa10adfab326'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 18 Nov 2025 06:43:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339b20fa22c26d49c5f0ce316a2782156283418f067d324a0329b50cae4152f2`  
		Last Modified: Tue, 18 Nov 2025 06:43:55 GMT  
		Size: 17.7 MB (17727678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d0f214a7029205e610cd301d7c861c43c588ee888b44197de17fecf8017176`  
		Last Modified: Tue, 18 Nov 2025 07:35:43 GMT  
		Size: 225.7 MB (225683887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:876af603204ae6f574e90a4c7fad7fafa42efd1c03b96288f29752502bdc313b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8823103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfea8981d57eb0113ee2884ea9b80cfd87f17b29779f405de3c44c53fcf0cd30`

```dockerfile
```

-	Layers:
	-	`sha256:9f3fcf11880f437a93707994824db8a169a0dbda1334bb5320e306d0cf5d0bb6`  
		Last Modified: Tue, 18 Nov 2025 07:25:02 GMT  
		Size: 8.8 MB (8805045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7606aa329fb4bdf674a94d0bb21c58add45e1c6d93106c23bb322011746c9e26`  
		Last Modified: Tue, 18 Nov 2025 07:25:03 GMT  
		Size: 18.1 KB (18058 bytes)  
		MIME: application/vnd.in-toto+json
