## `openjdk:24-ea-18-bullseye`

```console
$ docker pull openjdk@sha256:e6c85d7b3640ecb41cc8e48ed4f7121dd49418dd2b740d788da7aba70d756e0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-18-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:ff4a33cc6848599a852cdb91fdaf399e057d455eeb68e7ee544e0880734f2d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351974531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd93c5ee95466c27efa8f539b46cf695e57e4948b77c510c7a4e2d4622efb52f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93334f4d2aa939a6faef8baa16f2d0db0b1869ae3e50893187d7a6cd179f8b7e`  
		Last Modified: Tue, 08 Oct 2024 00:01:25 GMT  
		Size: 14.1 MB (14071332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3f53f1aae4d8173cf7f86c04f5375aba2586f396d9c9ff5af2eee75917c724`  
		Last Modified: Tue, 08 Oct 2024 00:01:27 GMT  
		Size: 212.3 MB (212333840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-18-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:395462619a9a9cda31ce0d46f2190b4360ad70095046481af8b056edb432c56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8350962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe8425e6ae02596b8e9d4f69c84374ec4fbcb4589c521f4e486dbd1751b92de`

```dockerfile
```

-	Layers:
	-	`sha256:f01833e420bb63e630cdb6743369576bf57cef11e3c4242117b0ac988d226f05`  
		Last Modified: Tue, 08 Oct 2024 00:01:24 GMT  
		Size: 8.3 MB (8332495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fa43082af0e1e04f39d64965225c32a6b6106d894dbc39518d288d07eb602b`  
		Last Modified: Tue, 08 Oct 2024 00:01:24 GMT  
		Size: 18.5 KB (18467 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-18-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2fe2781ffc798b2511ac4f0b548e53347489eafa6a14887500ea16032cb81dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (350001907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f34a0ffb534d9ddb2e192c89847b79cd266d2ab22f65f59a4eb4f98ae261f8b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 				binutils 				fontconfig libfreetype6 				ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276d311d9f402489dfec5a936f53185ab42b5614ee505fdd12711722578e4d8e`  
		Last Modified: Tue, 08 Oct 2024 02:34:49 GMT  
		Size: 15.5 MB (15526229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ade73c91175613b2ac7405c3cbeedef97f97016f0c0dee2a742bf3cdfca8934`  
		Last Modified: Tue, 08 Oct 2024 02:34:53 GMT  
		Size: 210.2 MB (210157422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-18-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:3363f47e7ae5be8896c6b6c0f4e01a6db096eb7ac10c546dc3cb90f4d806998c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8451561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103a1f837d50a24d98565c8a4072a323922925ae76d31bf6ea616629a43a2053`

```dockerfile
```

-	Layers:
	-	`sha256:4264be23e8fe1ae17e6416bf3f1d41fec25c6207a5c3e58f2264039cb20835be`  
		Last Modified: Tue, 08 Oct 2024 02:34:49 GMT  
		Size: 8.4 MB (8432956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28435e8f7d1f36efdc16be4f613cc63d4785007c229433246b8cffe5078cb2ef`  
		Last Modified: Tue, 08 Oct 2024 02:34:48 GMT  
		Size: 18.6 KB (18605 bytes)  
		MIME: application/vnd.in-toto+json
