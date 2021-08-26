## `maven:3-openjdk-17-slim`

```console
$ docker pull maven@sha256:f5592aa44439b99cb05f6ba51c54cc74baf760a83aa7df603f5a641422accacf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-17-slim` - linux; amd64

```console
$ docker pull maven@sha256:a05e7c5264656a202341d7668e1deb779504ed925ae4c19c4031894d968e8b96
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232325723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2885d657958b441bf13a814d16ab647a206b5da7b24310f561d50c0ec9dcf1b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 17 Aug 2021 01:23:40 GMT
ADD file:5e8343ab9a73edc27c2889634896e792ab289b85c206de0fc31183fdc0a32ac7 in / 
# Tue, 17 Aug 2021 01:23:41 GMT
CMD ["bash"]
# Thu, 26 Aug 2021 00:33:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 26 Aug 2021 00:34:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Thu, 26 Aug 2021 00:34:06 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Aug 2021 00:34:07 GMT
ENV LANG=C.UTF-8
# Thu, 26 Aug 2021 00:34:07 GMT
ENV JAVA_VERSION=17
# Thu, 26 Aug 2021 00:34:20 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 26 Aug 2021 00:34:21 GMT
CMD ["jshell"]
# Thu, 26 Aug 2021 02:02:05 GMT
ARG MAVEN_VERSION=3.8.2
# Thu, 26 Aug 2021 02:02:06 GMT
ARG USER_HOME_DIR=/root
# Thu, 26 Aug 2021 02:02:06 GMT
ARG SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222
# Thu, 26 Aug 2021 02:02:06 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries
# Thu, 26 Aug 2021 02:02:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl procps   && rm -rf /var/lib/apt/lists/*
# Thu, 26 Aug 2021 02:02:19 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 26 Aug 2021 02:02:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 26 Aug 2021 02:02:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 26 Aug 2021 02:02:20 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 26 Aug 2021 02:02:20 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 26 Aug 2021 02:02:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 26 Aug 2021 02:02:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:99046ad9247f8a1cbd1048d9099d026191ad9cda63c08aadeb704b7000a51717`  
		Last Modified: Tue, 17 Aug 2021 01:29:35 GMT  
		Size: 31.4 MB (31361314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97c10298fea9915576e7ff72c6eca3d7c589aaafd6bc6481a5814c4271d2251`  
		Last Modified: Thu, 26 Aug 2021 00:43:26 GMT  
		Size: 1.6 MB (1581998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7507e4a32853e80f68402f289794596a4641eacaab7f5b9af27ff132c9378`  
		Last Modified: Thu, 26 Aug 2021 00:44:59 GMT  
		Size: 187.5 MB (187520143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a12650f0d665b4ee92de3ff146a7d4f2043fef18a50b7665d1f441a4cd90eb`  
		Last Modified: Thu, 26 Aug 2021 02:06:48 GMT  
		Size: 2.5 MB (2455603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a693c4b937fb4421bc19dc5d2fb6ace75fa1e4e0df4744ee433ede26d30114`  
		Last Modified: Thu, 26 Aug 2021 02:06:49 GMT  
		Size: 9.4 MB (9405449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d922fe80abba2ffe44a17d6781ace55e36ccb3b3adc495410f5fb1a136e6bf6`  
		Last Modified: Thu, 26 Aug 2021 02:06:48 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cc6ea5842ec5123a261e5a76c306f3665242e345d3d658ce3df93cf3d38b16`  
		Last Modified: Thu, 26 Aug 2021 02:06:48 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-17-slim` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:59835e4322ec13d4f4e5645a3d144d00b6a117e60640b2113b4dcece2acd2f8e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229833566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1622390bad66f1d61bb04c818b278b738deab583b5fac160150d894b17d2d85`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:04 GMT
ADD file:0a42d4a201f0ac7889187c3212fbdfc2747f31f36e690d59c22eec50fe542614 in / 
# Tue, 17 Aug 2021 01:46:05 GMT
CMD ["bash"]
# Thu, 26 Aug 2021 00:33:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 26 Aug 2021 00:34:55 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Thu, 26 Aug 2021 00:34:55 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Aug 2021 00:34:55 GMT
ENV LANG=C.UTF-8
# Thu, 26 Aug 2021 00:34:56 GMT
ENV JAVA_VERSION=17
# Thu, 26 Aug 2021 00:35:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-x64_bin.tar.gz'; 			downloadSha256='aef49cc7aa606de2044302e757fa94c8e144818e93487081c4fd319ca858134b'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17/0d483333a00540d886896bac774ff48b/35/GPL/openjdk-17_linux-aarch64_bin.tar.gz'; 			downloadSha256='b8108a6b6c2579bd585281937cf09d401a5a971c59b9624e18abcf596b9caa22'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 26 Aug 2021 00:35:08 GMT
CMD ["jshell"]
# Thu, 26 Aug 2021 01:18:22 GMT
ARG MAVEN_VERSION=3.8.2
# Thu, 26 Aug 2021 01:18:22 GMT
ARG USER_HOME_DIR=/root
# Thu, 26 Aug 2021 01:18:23 GMT
ARG SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222
# Thu, 26 Aug 2021 01:18:23 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries
# Thu, 26 Aug 2021 01:18:27 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN apt-get update &&     apt-get install -y       curl procps   && rm -rf /var/lib/apt/lists/*
# Thu, 26 Aug 2021 01:18:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 26 Aug 2021 01:18:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 26 Aug 2021 01:18:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 26 Aug 2021 01:18:36 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 26 Aug 2021 01:18:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 26 Aug 2021 01:18:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 26 Aug 2021 01:18:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3716b9f3c2f9e7592f5b47c2e6e13e64132071620c7551e0aa3c5c248e106139`  
		Last Modified: Tue, 17 Aug 2021 01:53:29 GMT  
		Size: 30.0 MB (30048801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8aacccebb7931a5eafbf1992d4ce71f633f062d73ac3b147a0f85c5fc090f`  
		Last Modified: Thu, 26 Aug 2021 00:50:06 GMT  
		Size: 1.6 MB (1566164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc666e5346540b944de9115328a38da9d3392c0cec2c1a6a79b9bba43a58e10a`  
		Last Modified: Thu, 26 Aug 2021 00:52:14 GMT  
		Size: 186.3 MB (186333301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91325153ac67f806c73fae3fd417cd928e05f73de7b9a666710e8bc969ead46`  
		Last Modified: Thu, 26 Aug 2021 01:24:42 GMT  
		Size: 2.5 MB (2478644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516a291f87757f099c9b2a39a27c0234c291b7ca958a95270706bdacb5e80331`  
		Last Modified: Thu, 26 Aug 2021 01:24:42 GMT  
		Size: 9.4 MB (9405441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4edbbca7c6811064b845aa1e507c270303cad95b39b688055791c391fa4937e`  
		Last Modified: Thu, 26 Aug 2021 01:24:42 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9563009fc537510e821109c891427cc8f062e3f0ed9320dedcfdb940228645f`  
		Last Modified: Thu, 26 Aug 2021 01:24:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
