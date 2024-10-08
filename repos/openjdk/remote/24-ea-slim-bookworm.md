## `openjdk:24-ea-slim-bookworm`

```console
$ docker pull openjdk@sha256:026d6ad7d5c1fd756982c885406a36b6aa810ec87e0a562451e2786c2d1d7899
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-slim-bookworm` - linux; amd64

```console
$ docker pull openjdk@sha256:af234c7ae54146fc8c657e7e892280904214aa04a0e01d3d45ec31e88c15afd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245534147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c7bd744e58fe5e1291e09ffec037ab32a727e4d389407ff3a7957aee90bc99`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6dd72039b26a27c434a20753645d7504c754fdc2b1cc838614fe4c28fdf180`  
		Last Modified: Tue, 08 Oct 2024 00:01:27 GMT  
		Size: 4.0 MB (4018080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e34bfcc2968b157927a101afc203492a42380434edcb149ec0d1a01a5848a71`  
		Last Modified: Tue, 08 Oct 2024 00:01:31 GMT  
		Size: 212.4 MB (212389791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:8f79ae5c759f8ebcf57aed00b8bc3a59b9b666577e81fdc463c3b0e4dea69730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2523107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c52e7e348faab0d2016676b658f281243cb36d9c57736733be40bb96632378`

```dockerfile
```

-	Layers:
	-	`sha256:8d7db466ece64d7007ba0ea3d1b9e7fa122c5cebf44ebf9915af811a5e076049`  
		Last Modified: Tue, 08 Oct 2024 00:01:27 GMT  
		Size: 2.5 MB (2503891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1faff244195129fce4210cdf5c7ae0ff9c25b552acb0742d5a82b725a62f267f`  
		Last Modified: Tue, 08 Oct 2024 00:01:26 GMT  
		Size: 19.2 KB (19216 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b24d758dd888f883850c7b5f07873967b11f9257a8a1bc15a1ba3c5f7e416ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243198743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e16d55324c72c4715d7e22fc040995d6802184a4096ca5174ae0de8523c2116`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-24
# Fri, 04 Oct 2024 18:48:13 GMT
ENV PATH=/usr/local/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Oct 2024 18:48:13 GMT
ENV LANG=C.UTF-8
# Fri, 04 Oct 2024 18:48:13 GMT
ENV JAVA_VERSION=24-ea+18
# Fri, 04 Oct 2024 18:48:13 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='04f26aabbc1c5cf21303b08acbd073e87b08bc8522a9f23db6995356cff4c9c1'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/18/GPL/openjdk-24-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='8cf1e6199534b6b9c57616ec38aac5ff15846eed5e82573ecf27535848d9e810'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 04 Oct 2024 18:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8e98c18bb100b8376335c659a5d79503ec285937398e497db00019025b3d0f`  
		Last Modified: Tue, 08 Oct 2024 02:33:35 GMT  
		Size: 3.8 MB (3833439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63efb28a69bc16d1a44688fc4f61eb902aeba112885e6a537835ff7df40750`  
		Last Modified: Tue, 08 Oct 2024 02:33:40 GMT  
		Size: 210.2 MB (210208935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-slim-bookworm` - unknown; unknown

```console
$ docker pull openjdk@sha256:0bf5a4e4d76679471d1366b387cba04bb5dcabc2288c2806b9706485986963f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2522439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951be2b2ab910fabf83ab36ae4dac5b828c8bedb92872b8f4f203f8d9673705f`

```dockerfile
```

-	Layers:
	-	`sha256:8279898feab9d49fc8fbf3382c371ee163a9a5877da3360d05fe95a6bdb56de0`  
		Last Modified: Tue, 08 Oct 2024 02:33:35 GMT  
		Size: 2.5 MB (2502996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9672eb2dcba5ccec51ad46e1dd5f4d23f10407f14e640482a56062810c32162`  
		Last Modified: Tue, 08 Oct 2024 02:33:35 GMT  
		Size: 19.4 KB (19443 bytes)  
		MIME: application/vnd.in-toto+json
