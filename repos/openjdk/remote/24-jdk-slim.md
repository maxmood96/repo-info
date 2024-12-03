## `openjdk:24-jdk-slim`

```console
$ docker pull openjdk@sha256:248d48d40be1692a50452bcaa8c73bc9cc73075814ff76f5f9685732a28c579c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:031351b444969e9d0b1efaee355a2b773948040e2cd1b6fcae0a221aabf5d1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.9 MB (244851148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff27569d9ea0a613529de5272fba1ed3245d5cf9bc279b4732dbc1a521c3b189`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 02 Dec 2024 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Mon, 02 Dec 2024 19:48:14 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 19:48:14 GMT
ENV LANG=C.UTF-8
# Mon, 02 Dec 2024 19:48:14 GMT
ENV JAVA_VERSION=24-ea+26
# Mon, 02 Dec 2024 19:48:14 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='5a912c97361c098aaee25aa395745f77456ec2af1541c1aaa707b20f20e50fb8'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/26/GPL/openjdk-24-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='fd075f47c3ef0e3e6270244864a33309becf3f2fbdff615d20a86ea15779caf1'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 02 Dec 2024 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594afb9d2e11627f09296be77b11882b66536a3345422d8a44bb1cc94572cfa3`  
		Last Modified: Tue, 03 Dec 2024 16:32:09 GMT  
		Size: 3.8 MB (3824650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50771ab82e62d5be4a2becdba70eaafcf5c34790afa6fdd12a1b24143f456dc4`  
		Last Modified: Tue, 03 Dec 2024 16:32:12 GMT  
		Size: 212.8 MB (212794918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:a868dbae60d8e16e0b7518f6a0b9475d9ff9496732b81beaaa90d5cf5419bee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481cf080d6a0178468a6b3c73ff0e5901683b41ddda00185ea54f33a67b44356`

```dockerfile
```

-	Layers:
	-	`sha256:1cb2646c7e90250589a805526af61452ee1ee9624ce24aba4e42ef664fcb99f3`  
		Last Modified: Tue, 03 Dec 2024 16:32:09 GMT  
		Size: 2.5 MB (2531683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f422ec37e2b8fdafe37967657279c96cf9a144c275b6fba2258a10096584f3`  
		Last Modified: Tue, 03 Dec 2024 16:32:08 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8ee7163d0b0924d6318a4fe9720a15cdc1f7b74cd5259748a3e2d2cb91787529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242736302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68d5509e24320d0e6543c4df08e1d5b436c2c5c23a745a01715674c7ccca661`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 22 Nov 2024 19:48:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 22 Nov 2024 19:48:12 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 19:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2024 19:48:12 GMT
ENV JAVA_VERSION=24-ea+25
# Fri, 22 Nov 2024 19:48:12 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='06d2571c8af4948ac1eaad2b912ab59f320f01744bc4152f3476a65512bb3901'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/25/GPL/openjdk-24-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='022d2edea028f26d0aa8cc933429f305abac8f8a74451095a55b1354f0db7966'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 22 Nov 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9dc90d5f2585dac7f75845211c0f07675ec89993d78940b46c23a56130d6e8`  
		Last Modified: Tue, 03 Dec 2024 06:39:18 GMT  
		Size: 3.6 MB (3639426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d20716b1de4621691156cfc150843c560101ce2d66dae1d9f97903dba500b6`  
		Last Modified: Tue, 03 Dec 2024 06:39:22 GMT  
		Size: 211.0 MB (211038066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-jdk-slim` - unknown; unknown

```console
$ docker pull openjdk@sha256:86fa58321be58c2015f696ab3cf05bd606b72a2aadf4cdce6f64d58146b3f926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ce61e7f1a9cfe098bcfc59947b100376caec0ffac66e6020c3b0e52865d84f`

```dockerfile
```

-	Layers:
	-	`sha256:b5f0e9517132ef8f475279721e6b993310462351567b24fcaafdd70f4b1c0b7e`  
		Last Modified: Tue, 03 Dec 2024 06:39:18 GMT  
		Size: 2.5 MB (2531411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde236da8d5105ae89163a6606c667472f8bc9f08541d4068f0e7584c6205cfe`  
		Last Modified: Tue, 03 Dec 2024 06:39:17 GMT  
		Size: 19.7 KB (19656 bytes)  
		MIME: application/vnd.in-toto+json
