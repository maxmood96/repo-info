## `openjdk:26-ea-27-slim-trixie`

```console
$ docker pull openjdk@sha256:37cfe0e23743ae18a69b7fe407d9993c6e7a411116a6cdf80ef294b02d907095
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-27-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:ba28a13d8dc2e3d87055f16646940d579c18a94ad8824e605e974add2dce7f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260132372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33079a2d30434d6507afeb9224a37aa8022c0445780adc38e1574b529240fcca`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:16:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:17:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 08 Dec 2025 23:17:15 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:17:15 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:17:15 GMT
ENV JAVA_VERSION=26-ea+27
# Mon, 08 Dec 2025 23:17:15 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 08 Dec 2025 23:17:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd22d0f0a2547dcdb64927b5bf856dd1ab657561b6c054e747c129b26ba411b`  
		Last Modified: Mon, 08 Dec 2025 23:36:22 GMT  
		Size: 2.4 MB (2370987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a2903f37b5b348dcbd9c3de3a80b8fd949e6f3b3d28bf1973b634d48e35cab`  
		Last Modified: Mon, 08 Dec 2025 23:18:50 GMT  
		Size: 228.0 MB (227984889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-27-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a23f2b890ef8efc3230b4968e5e338f6703a03521c0ca9ca4cbedcee6921fccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620b2c36a60785845e773919a89adfab8a41b43e8d7f4e9bb0a2871f56b3dcb2`

```dockerfile
```

-	Layers:
	-	`sha256:508af008e289a7a28d7e791bbf4b38b53b938e49772a95d0c9ad9643f858777d`  
		Last Modified: Tue, 09 Dec 2025 04:23:55 GMT  
		Size: 2.3 MB (2278789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe588ab39acf8c7fa5da593def85d35d82fd6f4369ec19d1bbc301d909a8cc18`  
		Last Modified: Tue, 09 Dec 2025 04:23:56 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-27-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f0b4c82132579c9ef22809a50b530620afbe716c386aba447b5eef59d08c9c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258356876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383e8a7bcbb0d2f7420b891981a8cf00d4049ae0940cb12ebc8a9943eed9d881`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:20:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:20:53 GMT
ENV JAVA_HOME=/usr/local/openjdk-26
# Mon, 08 Dec 2025 23:20:53 GMT
ENV PATH=/usr/local/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:20:53 GMT
ENV LANG=C.UTF-8
# Mon, 08 Dec 2025 23:20:53 GMT
ENV JAVA_VERSION=26-ea+27
# Mon, 08 Dec 2025 23:20:53 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='c219dd04012af56a87523d69c6dd07a66adce846ff11981335a361ae9e0b4472'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='8b59cc8266e8d1eadc2919567b907da7098542b2c0d602eb73484728a0e7b2f7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 08 Dec 2025 23:20:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57f00236c13f5fe07cea215af894c2bc99658c9bb25786ab674e9a2f9526f2e`  
		Last Modified: Mon, 08 Dec 2025 23:21:28 GMT  
		Size: 2.3 MB (2314115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5c26e6884e5069cb356211c2972974caa9e92c3798d5ad528ea754b8f01067`  
		Last Modified: Mon, 08 Dec 2025 23:21:43 GMT  
		Size: 225.9 MB (225904133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-27-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:a567e5c14fbe4345522856b1066a5af3ce79539bb80d969b5e65c6e6dfa92154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2165ed2bc75ece83d6776d3a4b5b81b33944907817a441ec7ba1abd3822816ad`

```dockerfile
```

-	Layers:
	-	`sha256:7c72c040efb12b62be67f3166a54b2e527d40e60ba01a641bcdda39092919058`  
		Last Modified: Tue, 09 Dec 2025 04:23:59 GMT  
		Size: 2.3 MB (2278475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59b85675d01797b668a8eb8cba0ecd0759e69e56c6c9909414e0c5a39b22485`  
		Last Modified: Tue, 09 Dec 2025 04:24:00 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
