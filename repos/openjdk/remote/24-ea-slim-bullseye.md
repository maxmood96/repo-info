## `openjdk:24-ea-slim-bullseye`

```console
$ docker pull openjdk@sha256:5f68cf5d2e460d051b54c318e83ad58ecd85fb2c08415e05847be74f6e11a047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bullseye` - linux; amd64

```console
$ docker pull openjdk@sha256:429326c035220a21331a74e1bf95b2024297fde1b11f384013c9f573cf1a4589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244420666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa813eabc3ebb08148410748f3d12b10a6192d5e9cce5cfff3b3b10590e50818`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c737ec6c890b0aa1f41f0c1c791998e2a0f38e42ebba422868a59cce7c41046c`  
		Last Modified: Tue, 03 Dec 2024 16:32:05 GMT  
		Size: 1.4 MB (1377246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1849b390acfbb914f0667e4234737df901ffdd9a92eac0a0b700703e42101850`  
		Last Modified: Tue, 03 Dec 2024 16:32:08 GMT  
		Size: 212.8 MB (212790776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:7d9ca648273383e44ecf4fe2ea16f194222a6602e32f7d0e9d085122aaabf5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2843362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740757fd6e9a8b5bc0f0bc60f42cfa28f93430a4fb29cc8d958dc69f74b42d80`

```dockerfile
```

-	Layers:
	-	`sha256:a8511ce40cb05f22495d63df96645f6398e5b49cee8068efbc3c1c3b84e4a8cc`  
		Last Modified: Tue, 03 Dec 2024 16:32:05 GMT  
		Size: 2.8 MB (2825792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf42ed0ca2f91486d3f6cd1581b5bf719ef8d55a49fe97dc362e391b754518c`  
		Last Modified: Tue, 03 Dec 2024 16:32:05 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c183dd0773d284e345600ff56cc13eed45d77154f1551e5cda302f7971cc826b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241146048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7873f0e0981d550cd96f4ca3907b5a45ef0451a8099d6692c177c025b7794cb6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 22 Nov 2024 19:48:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2c4e35b68e199f2109b1f5e347b3633c30b226cd7107927f1d944c3e8d8337`  
		Last Modified: Tue, 03 Dec 2024 11:21:30 GMT  
		Size: 1.4 MB (1361244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8307f71c6506dda056cff6c87335b6d164b681987d65ae3959e49298fdc9b276`  
		Last Modified: Tue, 03 Dec 2024 11:21:34 GMT  
		Size: 211.0 MB (211039881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bullseye` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d2c8cb57a63c8b93e5c4ef8df0690618072711d01e80ad40ca6b3aa119672ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2843155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462232e6a46f59904a8023060904cc4fbb63cc38b204fe85eeb5ba8220cb31b1`

```dockerfile
```

-	Layers:
	-	`sha256:32130fa3ec61324cb992c874f24df6b69fa9b229b84fa5fbe0fc2c8f061126a7`  
		Last Modified: Tue, 03 Dec 2024 11:21:30 GMT  
		Size: 2.8 MB (2825442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d506eb97b47caed3384534ffe93e5cc8f08a308ea04f0ac177662ca44896b1b`  
		Last Modified: Tue, 03 Dec 2024 11:21:29 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json
