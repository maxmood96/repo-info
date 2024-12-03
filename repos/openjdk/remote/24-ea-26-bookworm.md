## `openjdk:24-ea-26-bookworm`

```console
$ docker pull openjdk@sha256:76692cd005539cc3b9d333f03f68465fad80fa208279c0c3019952d97efa2e31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-26-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:b42f20be85ce67e2359e71bd82015e3749003205b8a4aca478ce726ba8982f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366441597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0af13c24238919abf7a1bb7f1a03b84b76569cef5d641aa8bb71c688822eb6e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Mon, 02 Dec 2024 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 19:48:14 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 19:48:14 GMT
ENV JAVA_VERSION=24-ea+26
# Mon, 02 Dec 2024 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='5a912c97361c098aaee25aa395745f77456ec2af1541c1aaa707b20f20e50fb8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='fd075f47c3ef0e3e6270244864a33309becf3f2fbdff615d20a86ea15779caf1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33684568071a1993b712f3975843137ebc53066f7cd8fceaaf39308018b637dc`  
		Last Modified: Tue, 03 Dec 2024 16:32:14 GMT  
		Size: 16.9 MB (16943024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616f2e0a36192eb8e808cdecb5685038e8c45c0b81c545c3dd5330525bb8b403`  
		Last Modified: Tue, 03 Dec 2024 16:32:17 GMT  
		Size: 212.7 MB (212743979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-26-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:b87a619752e795d6ad694d06c5e398cf5caa05409c9e556131222705ea36480f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8461340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711d5055d94294b092c76caa6a4e9c15037b9710ad049bf1cfc57bf249a2605e`

```dockerfile
```

-	Layers:
	-	`sha256:77270010db3db6e8ae988fadbb772801399ad8f820fdccb157548a1340426aa3`  
		Last Modified: Tue, 03 Dec 2024 16:32:14 GMT  
		Size: 8.4 MB (8442722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876a00af8b1226bd57f62499367296fcabb10632a50f65cd106982cef2e3282b`  
		Last Modified: Tue, 03 Dec 2024 16:32:13 GMT  
		Size: 18.6 KB (18618 bytes)  
		MIME: application/vnd.in-toto+json
