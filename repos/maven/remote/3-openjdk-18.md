## `maven:3-openjdk-18`

```console
$ docker pull maven@sha256:b2be87adfeee407cd970f5936993b3f96804f6f4025474d5856bb15908c2849a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18` - linux; amd64

```console
$ docker pull maven@sha256:5dddfbf5a9f21440bf0899fdf9ca1ff3de7b3c50ee99854da95fb8277b9b3250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.4 MB (431352266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5fd1cafe3df114bf1f2dd9b921a7ebf9649a4139fcaa5cd677be688a96d8aa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:47 GMT
ADD file:eaa532cad071c531a759e73fd0fd381f440f180ab45b05a74314f10b0374df67 in / 
# Tue, 29 Mar 2022 18:35:47 GMT
CMD ["/bin/bash"]
# Tue, 29 Mar 2022 23:06:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 29 Mar 2022 23:08:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Tue, 29 Mar 2022 23:08:11 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:08:11 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 23:08:11 GMT
ENV JAVA_VERSION=18
# Tue, 29 Mar 2022 23:08:20 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 23:08:21 GMT
CMD ["jshell"]
# Tue, 05 Apr 2022 16:55:46 GMT
RUN microdnf install findutils git
# Tue, 05 Apr 2022 16:55:47 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 05 Apr 2022 16:55:47 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Apr 2022 16:55:47 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 05 Apr 2022 16:55:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 05 Apr 2022 16:55:55 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 05 Apr 2022 16:55:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Apr 2022 16:55:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Apr 2022 16:55:56 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 05 Apr 2022 16:55:56 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 05 Apr 2022 16:55:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Apr 2022 16:55:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4430e06691f65e516df7d62db0ee5393acea9ade644cc6bc620efef0956dd17`  
		Last Modified: Tue, 29 Mar 2022 18:36:53 GMT  
		Size: 42.1 MB (42113609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce5342b806de618f4fa582eca53ecee5a73ef976daa060d249227e1927d814`  
		Last Modified: Tue, 29 Mar 2022 23:18:03 GMT  
		Size: 13.5 MB (13524329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d5f9b71bbca8d232871fefa888f7259b6eefc4c87fed1b4aae7bf2fc27c761`  
		Last Modified: Tue, 29 Mar 2022 23:21:05 GMT  
		Size: 188.7 MB (188669555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c0dae1b5e2d048f823b436a8d932531f70838f0775373045961aed5eab59c2`  
		Last Modified: Tue, 05 Apr 2022 17:02:33 GMT  
		Size: 178.3 MB (178307167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c4bdb0b32e2e07895a96d409d8b66bb7c957c11b4df66c3a5176985263d147`  
		Last Modified: Tue, 05 Apr 2022 17:02:20 GMT  
		Size: 8.7 MB (8736384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98acf0b605a20ec0f6b11de4079c2dd17c46d0f36115e86af475bed791711c90`  
		Last Modified: Tue, 05 Apr 2022 17:02:19 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69126203652134e6f28af0d7e001bcd8ba16692aa6082c4baf21ca8752153b78`  
		Last Modified: Tue, 05 Apr 2022 17:02:19 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:498a6f414cf051ad03e2b668d6366f28b397c42bcd9249b5567e585b08e7f6e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.3 MB (430308092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed77bfba6c512bdd320bb5d585de449006bf24d8f5ccce490a25579d6c090227`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 08:57:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 30 Mar 2022 09:00:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 30 Mar 2022 09:00:20 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 09:00:21 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 09:00:22 GMT
ENV JAVA_VERSION=18
# Wed, 30 Mar 2022 09:00:34 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Mar 2022 09:00:35 GMT
CMD ["jshell"]
# Tue, 05 Apr 2022 18:35:21 GMT
RUN microdnf install findutils git
# Tue, 05 Apr 2022 18:35:22 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 05 Apr 2022 18:35:22 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Apr 2022 18:35:23 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 05 Apr 2022 18:35:24 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 05 Apr 2022 18:35:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 05 Apr 2022 18:35:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Apr 2022 18:35:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Apr 2022 18:35:35 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 05 Apr 2022 18:35:36 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 05 Apr 2022 18:35:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Apr 2022 18:35:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200eb5167ed838a74239544d81e10c3d37a59ea571f23c1d6ed6e0c207cf997`  
		Last Modified: Wed, 30 Mar 2022 09:18:31 GMT  
		Size: 14.3 MB (14293802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ecd50b98f450445002af6b8c949d1550c76990e5f8c17179d640ea9d72fd65`  
		Last Modified: Wed, 30 Mar 2022 09:22:01 GMT  
		Size: 187.6 MB (187592644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd06e236df76ec9879fd8742e7201b987fcc25a304539f9f949c26e4e4a52435`  
		Last Modified: Tue, 05 Apr 2022 18:46:42 GMT  
		Size: 177.7 MB (177665003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53796a44c5a28315ee002d5c43c7dff7c1e9482ec632725e9403f83bb16b138a`  
		Last Modified: Tue, 05 Apr 2022 18:46:26 GMT  
		Size: 8.7 MB (8736332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95867063ac7858e7c0ee48773aec319c24b94289307825deca27f8d1e060a6ef`  
		Last Modified: Tue, 05 Apr 2022 18:46:25 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd402d71d83b69d28e563121da890f4da9330f17c6df7a7c498f44af4d3e5c41`  
		Last Modified: Tue, 05 Apr 2022 18:46:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
