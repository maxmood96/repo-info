## `openjdk:27-ea-24-slim-trixie`

```console
$ docker pull openjdk@sha256:b036456d15d8d124abefa29102f945c72636aff9619f9564a0ac31bc816e7b70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-24-slim-trixie` - linux; amd64

```console
$ docker pull openjdk@sha256:e10f081006d1a738ec493ff33123c2803b15eccb9907c637d07a055218afcf9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259195623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33a0220bb0108a4e23c85a90d2214b86a35bb34356493ce3298520bb0355166`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 02 Jun 2026 07:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:11:42 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 02 Jun 2026 07:11:42 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:11:42 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:11:42 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:11:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e75964d88bf3b1f0b0bc561ec5c736378ebaeaa25bacd71dd4e1d411af526`  
		Last Modified: Tue, 02 Jun 2026 07:12:02 GMT  
		Size: 2.4 MB (2371321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e67f6d8fdeb1804da441f622c81b0362c8848845492f642476af0755692d3dd`  
		Last Modified: Tue, 02 Jun 2026 07:12:07 GMT  
		Size: 227.0 MB (227044376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:05f53ec1210db5bf6efa28b0d6bee9b5c771abe0bb427cba65fb5288972c6c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0fac2f95481511d2f4cd72f2de03168c04c8e0565573c7059c94bbfcd723c1d`

```dockerfile
```

-	Layers:
	-	`sha256:eec2715752583d5114dc4079dc25069b7a0c575e6a803442cda40e25974dbb08`  
		Last Modified: Tue, 02 Jun 2026 07:12:02 GMT  
		Size: 2.3 MB (2276384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c67a379e50fa31ae0d52ac19255b7e3d3cc7491d7601f72c5147fa0782befcd5`  
		Last Modified: Tue, 02 Jun 2026 07:12:02 GMT  
		Size: 18.1 KB (18109 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-24-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:14acd8dd07c321a086e9830ec44051acc6490e7e2198616752ce2f683ffd5a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257516795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597952756a4da0c4a096bfb24687bafff9e4582d5146908ba82d0f43051ecad7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 02 Jun 2026 07:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 07:11:41 GMT
ENV JAVA_HOME=/usr/local/openjdk-27
# Tue, 02 Jun 2026 07:11:41 GMT
ENV PATH=/usr/local/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 07:11:41 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 07:11:41 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:11:41 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='eb8d0fac160a096fc406b794465b245a8b40cb1b04bbb4c5824393cde263a8b5'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='832ef5a271052b9065f2b5b7a63ecdbbd0363edd74228736bab7227b45b21a66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 02 Jun 2026 07:11:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e58a1b07531510f81186a18ca8e89d42b3f0c2636308593501f23feb016a62`  
		Last Modified: Tue, 02 Jun 2026 07:12:02 GMT  
		Size: 2.3 MB (2314503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26e94252f00320bdfb62201cefed56076e238aa09e7766925efc2875ffec3a9`  
		Last Modified: Tue, 02 Jun 2026 07:12:06 GMT  
		Size: 225.1 MB (225060373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-24-slim-trixie` - unknown; unknown

```console
$ docker pull openjdk@sha256:dae3face8dfef20a664f3ab897fa1fc1c57da602eecfc7ff102cc970bf38b35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6664dcdb4a038d8aa2480e020d8740409dcd5f650b06a4149fa48e75aa46fc72`

```dockerfile
```

-	Layers:
	-	`sha256:2440bea547e6be13c43302d934814dc8fa2fe91baff6df0e9981192d1ffcf7fe`  
		Last Modified: Tue, 02 Jun 2026 07:12:02 GMT  
		Size: 2.3 MB (2276062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a0c81133ee061f7dbbcecca0b9ce25a6461cc2773566f42f643fa740adfe43`  
		Last Modified: Tue, 02 Jun 2026 07:12:01 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json
