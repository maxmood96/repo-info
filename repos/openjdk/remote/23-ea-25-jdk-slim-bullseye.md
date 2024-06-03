## `openjdk:23-ea-25-jdk-slim-bullseye`

```console
$ docker pull openjdk@sha256:4254559aeca088e81d304e8b16f17962b57ac8e8336133afdc37dc947115e1e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-25-jdk-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:df7bd1a6fb1bdce64fd87db7cfe7d70988782873c304cc1cf5d82f7551295778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244148876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a085c8788f71ba913427c78e663191e590acda2c282968a8a60c84ce9c777d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_HOME=/usr/local/openjdk-23
# Fri, 31 May 2024 00:48:11 GMT
ENV PATH=/usr/local/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 May 2024 00:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 31 May 2024 00:48:11 GMT
ENV JAVA_VERSION=23-ea+25
# Fri, 31 May 2024 00:48:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='155a1386301d0ac6cd1ce5769b31f550bb400d652f4211454b9988bf25fa173d'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b00cd1591ad9727c48c07e598f57cdec15fa40b605ae712b67f35f221534d1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 31 May 2024 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dac714cf0afd3a25006ac6f8f3a03108d0e11c0a8e745c31af4856e21f24be`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 1.4 MB (1377991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f823d0ac97a4e32260e14236031ededb51a551bdc0a62092f4425e814ad257`  
		Last Modified: Mon, 03 Jun 2024 19:01:07 GMT  
		Size: 211.3 MB (211336954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-25-jdk-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:a1db6e3cb43a0788a7832019150b9aaf08e45756744fc8936cef21c10f1815bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2655803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991cff7a96be85c4666069d46314e16af2bf85e36e38c9c043c002861be16a3f`

```dockerfile
```

-	Layers:
	-	`sha256:2e5fc1e2f2e854e6f9633a86ce85b4eb70fae6f132ffbd25061c6ed516cf1e4b`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 2.6 MB (2638494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2177943815c22ba0e78c78032e39b9a7bab5582b2b9a3114240c4fe13579ead3`  
		Last Modified: Mon, 03 Jun 2024 19:01:03 GMT  
		Size: 17.3 KB (17309 bytes)  
		MIME: application/vnd.in-toto+json
