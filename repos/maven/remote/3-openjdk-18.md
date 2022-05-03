## `maven:3-openjdk-18`

```console
$ docker pull maven@sha256:ab44a4fe1b5e5c943b0f37666bd22cc71468fff208112c328cc2b116ae01b833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18` - linux; amd64

```console
$ docker pull maven@sha256:e99ba7f49d284def4f0a14d9b932bda1632297587c2e4e015d6ab7e768643a10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 MB (433568425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a502452a80473a227ec26425526a4b0940c9a202328b8ba3f8b9c5a276aed1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 May 2022 20:51:06 GMT
ADD file:b2c3e9f338a70507ba6d9ec21f28c7023f4120a45f234ff9a28188119091c60b in / 
# Mon, 02 May 2022 20:51:06 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 21:07:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 02 May 2022 21:08:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 02 May 2022 21:08:25 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 May 2022 21:08:25 GMT
ENV LANG=C.UTF-8
# Mon, 02 May 2022 21:08:25 GMT
ENV JAVA_VERSION=18.0.1.1
# Mon, 02 May 2022 21:08:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 02 May 2022 21:08:35 GMT
CMD ["jshell"]
# Mon, 02 May 2022 21:42:47 GMT
RUN microdnf install findutils git
# Mon, 02 May 2022 21:42:48 GMT
ARG MAVEN_VERSION=3.8.5
# Mon, 02 May 2022 21:42:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 02 May 2022 21:42:48 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Mon, 02 May 2022 21:42:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Mon, 02 May 2022 21:42:50 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 02 May 2022 21:42:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 02 May 2022 21:42:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 02 May 2022 21:42:50 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 02 May 2022 21:42:50 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 02 May 2022 21:42:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 02 May 2022 21:42:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:121b730bab02bd12143950d97a621f2d2dcf4723433bbadc2777d594c871ee71`  
		Last Modified: Mon, 02 May 2022 20:51:57 GMT  
		Size: 42.1 MB (42114330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b275ba7e0da7889811d55da69069fd42118dd8875faded11d9d21a813afe7b`  
		Last Modified: Mon, 02 May 2022 21:13:42 GMT  
		Size: 13.5 MB (13531997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3986241e01958a3d1fc12bc5a6c6e97f3b8c1008c0735292898156d88bf62223`  
		Last Modified: Mon, 02 May 2022 21:15:03 GMT  
		Size: 188.7 MB (188723736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6395f01b5aafea45673c5a9d29e7d6da7a9555f88d7d548b26a1deee507346`  
		Last Modified: Mon, 02 May 2022 21:45:21 GMT  
		Size: 180.5 MB (180460761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e723a536e024190a7f1476fc4625b71149c8c704d88df784c7de3f9abdd249c`  
		Last Modified: Mon, 02 May 2022 21:45:07 GMT  
		Size: 8.7 MB (8736387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b5493965af2687522045493ce41599a9c4d9b19bb3f2a4e7df2534fc893eea`  
		Last Modified: Mon, 02 May 2022 21:45:06 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43137b14986fdd255e652d3a90595705219dbdeeb187bfae2ba1f26efd09875`  
		Last Modified: Mon, 02 May 2022 21:45:06 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c956ba522089e5b7bb5f60a438c609d153dafda9772db298eb233426e1e33b2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.8 MB (433797154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254f76e15347698062e4852017116588014c23949c7f0cf35fdf846f68abb25a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 May 2022 21:46:34 GMT
ADD file:e59d0ab85f777209561c628874489b9544223a23fed0755bedd408a55452b4af in / 
# Mon, 02 May 2022 21:46:35 GMT
CMD ["/bin/bash"]
# Mon, 02 May 2022 22:06:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 02 May 2022 22:07:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 02 May 2022 22:07:25 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 May 2022 22:07:26 GMT
ENV LANG=C.UTF-8
# Mon, 02 May 2022 22:07:27 GMT
ENV JAVA_VERSION=18.0.1.1
# Mon, 02 May 2022 22:07:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-x64_bin.tar.gz'; 			downloadSha256='4f81af7203fa4c8a12c9c53c94304aab69ea1551bc6119189c9883f4266a2b24'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1.1/65ae32619e2f40f3a9af3af1851d6e19/2/GPL/openjdk-18.0.1.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='e667166c47e90874af3641ad4a3952d3c835627e4301fa1f0d620d9b6e366519'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 02 May 2022 22:07:56 GMT
CMD ["jshell"]
# Mon, 02 May 2022 23:01:03 GMT
RUN microdnf install findutils git
# Mon, 02 May 2022 23:01:04 GMT
ARG MAVEN_VERSION=3.8.5
# Mon, 02 May 2022 23:01:04 GMT
ARG USER_HOME_DIR=/root
# Mon, 02 May 2022 23:01:05 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Mon, 02 May 2022 23:01:06 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Mon, 02 May 2022 23:01:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 02 May 2022 23:01:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 02 May 2022 23:01:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 02 May 2022 23:01:15 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 02 May 2022 23:01:16 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 02 May 2022 23:01:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 02 May 2022 23:01:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35f3f87cf615a8684aa1b866b03a7078bce1beea91489effc1e6c03c83124c`  
		Last Modified: Mon, 02 May 2022 21:47:34 GMT  
		Size: 42.0 MB (42016620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245e242efb2259690773e11adafa3652b3b5f5ac58742dfba66216c5527ec988`  
		Last Modified: Mon, 02 May 2022 22:17:46 GMT  
		Size: 14.3 MB (14292260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b465aca2bba621872c9adcf3e6a5a8ad81b145804735f70a52a0c71b179c4e`  
		Last Modified: Mon, 02 May 2022 22:19:23 GMT  
		Size: 187.6 MB (187644874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713674d5501d2b18223c26f79bed6144d5df53a89efc51f96a52c38e8986f773`  
		Last Modified: Mon, 02 May 2022 23:04:55 GMT  
		Size: 181.1 MB (181105852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9bab1144df635980e2cf4411f14e810e0924d1ec431770510617909c98efc1`  
		Last Modified: Mon, 02 May 2022 23:04:39 GMT  
		Size: 8.7 MB (8736336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95138afafa4e314c3c41eedc51aef47dea007627b18177a045dc834d22d6cf7b`  
		Last Modified: Mon, 02 May 2022 23:04:38 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba20a8ca1806c32b1b1d07af0a232e8da2d806358d86e3cae4813ba49051fda0`  
		Last Modified: Mon, 02 May 2022 23:04:38 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
