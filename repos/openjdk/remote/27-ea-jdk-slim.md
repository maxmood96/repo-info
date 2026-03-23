## `openjdk:27-ea-jdk-slim`

```console
$ docker pull openjdk@sha256:26cce067f87a6ecbcc41cb458679507bcb15d2466ca284dfce402b374c6879ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:a6babee1c34e5bfa3b1d5e0c1432cbd794d9e1ae7f52a8381844438f612ffd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260786100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569f391cb6d1e3487135edc29060320aa666b76a52d9e04ecfaf91043542e03d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 17:58:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 23 Mar 2026 17:58:47 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:47 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:47 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:47 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70486b187ff43edd554bfd16993ebfb2e28f38281cfc9b970d9c4b3411393b2`  
		Last Modified: Mon, 23 Mar 2026 17:59:06 GMT  
		Size: 2.4 MB (2371155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e5f1f73fc04108a64909b90b094626fcdfaf75603385015f92651f930b183`  
		Last Modified: Mon, 23 Mar 2026 17:59:10 GMT  
		Size: 228.6 MB (228639445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:34fe9c5441cedae3204bc45a0adf89f25a2013af274c1778921104def085d8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2297004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829dce859b9b75a838ef8cbe1935808711837919c2b2898d3912d4fb94e3f2df`

```dockerfile
```

-	Layers:
	-	`sha256:e1790e32f3b3ddd21c87291f21d007a3da0802b9a74a8b5e3b6db0d0245ebd96`  
		Last Modified: Mon, 23 Mar 2026 17:59:06 GMT  
		Size: 2.3 MB (2278895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71bf89f18de05c492fbe97d2d02806deafb7cdb84212a108f578c579d0982f34`  
		Last Modified: Mon, 23 Mar 2026 17:59:06 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:686334a1d756fed0be9bbceedf111ceb4717dd7ec071d938707c5fa91979b1c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259062004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81ff2ac18ef7a77cadb464a57db69c587dd52c5d6b186e31b18e5350b6b411c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 23 Mar 2026 17:58:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Mar 2026 17:58:32 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Mon, 23 Mar 2026 17:58:32 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 17:58:32 GMT
ENV LANG=C.UTF-8
# Mon, 23 Mar 2026 17:58:32 GMT
ENV JAVA_VERSION=27-ea+14
# Mon, 23 Mar 2026 17:58:32 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='64b478b9973d8d04e1680cdfaf11a8e93f8a17f962af3ddb1c61b76a62c0d699'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/14/GPL/openjdk-27-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='c99686ed0406f05a113b6467b6a57699864922c476481609a703c6dd91534f45'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 23 Mar 2026 17:58:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28245ad63ff4dee642fb305947ed95b449981bc7c2800d3fb5217b22e174d19d`  
		Last Modified: Mon, 23 Mar 2026 17:58:52 GMT  
		Size: 2.3 MB (2314445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6514b33568e2c6701a021d1b417ff1fb1afe430dcc5a66c21d07443841021ca9`  
		Last Modified: Mon, 23 Mar 2026 17:58:58 GMT  
		Size: 226.6 MB (226609143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:a9232f229330b1d4319700b5c2b4fd4475959cdb905f1cdd625a95665b69d9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911202aff25d0507f750d59a6e40acbf7d849649a42f28681f215a2ba5ca433a`

```dockerfile
```

-	Layers:
	-	`sha256:a62dbe219808946e1d92f07de9076898811e1d036920b09144812b06d6a80124`  
		Last Modified: Mon, 23 Mar 2026 17:58:52 GMT  
		Size: 2.3 MB (2278581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca67eeee4ee9178d9af51f0a32f107e54d9eda68844cd7417be39691b867a095`  
		Last Modified: Mon, 23 Mar 2026 17:58:52 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
