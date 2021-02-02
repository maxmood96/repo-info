## `sonarqube:lts`

```console
$ docker pull sonarqube@sha256:a8766457c5325ba7aae23b4e5e0f5cfbcccbc5fa1e4fdcf4f623e38ef8d3c642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:lts` - linux; amd64

```console
$ docker pull sonarqube@sha256:f4102ab1a7b0104985c8b4cf5de11b4d1329e435ca11e935661ae6adf87655c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290438570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314e5390544d7d0915ad7905cf3dd52a7804335d043d5f877a2486191f2d578f`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Mon, 01 Feb 2021 19:54:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:54:48 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:54:48 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:54:49 GMT
ENV JAVA_VERSION=11.0.10
# Mon, 01 Feb 2021 19:56:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 01 Feb 2021 23:03:20 GMT
RUN apt-get update     && apt-get install -y curl gnupg2 unzip     && rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 23:03:20 GMT
ENV SONAR_VERSION=7.9.5 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Mon, 01 Feb 2021 23:03:20 GMT
EXPOSE 9000
# Mon, 01 Feb 2021 23:03:21 GMT
RUN groupadd -r sonarqube && useradd -r -g sonarqube sonarqube
# Mon, 01 Feb 2021 23:03:22 GMT
RUN for server in $(shuf -e ha.pool.sks-keyservers.net                             hkp://p80.pool.sks-keyservers.net:80                             keyserver.ubuntu.com                             hkp://keyserver.ubuntu.com:80                             pgp.mit.edu) ; do         gpg --batch --keyserver "$server" --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE && break || : ;     done
# Mon, 01 Feb 2021 23:03:37 GMT
RUN set -x     && cd /opt     && curl -o sonarqube.zip -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip -q sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && chown -R sonarqube:sonarqube sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Mon, 01 Feb 2021 23:03:37 GMT
VOLUME [/opt/sonarqube/data]
# Mon, 01 Feb 2021 23:03:37 GMT
WORKDIR /opt/sonarqube
# Mon, 01 Feb 2021 23:03:38 GMT
COPY file:d7c6edf99ad4508dcb273783aad5da8017e549d505d617619117cc576bbc8850 in /opt/sonarqube/bin/ 
# Mon, 01 Feb 2021 23:03:38 GMT
USER sonarqube
# Mon, 01 Feb 2021 23:03:38 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0601982f39d5609688d3d24a2f70ac6655e1628df369aa95dcda6ad9aab845f0`  
		Last Modified: Mon, 01 Feb 2021 20:09:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0940164d1964ff9d11b1aea461a6fa253e1300e97f204bec73f228f11d3acf`  
		Last Modified: Mon, 01 Feb 2021 20:10:22 GMT  
		Size: 47.0 MB (47036369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c32e5627cb50c50e9cd614e9d2f1ca6bd88b64a49cd9efd5204941d7f671381`  
		Last Modified: Mon, 01 Feb 2021 23:04:07 GMT  
		Size: 6.0 MB (5985182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fd430249945365197f05a4d2459ce20aa5eb0378157f2570842565b9266d75`  
		Last Modified: Mon, 01 Feb 2021 23:04:06 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc3657fc6859ad520b35ca77728f7f699971c36102c334a01974e044353e5d4`  
		Last Modified: Mon, 01 Feb 2021 23:04:06 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4bbbb60bdef6194cd946aedea751f5818bd31508efbcdd8a2e1fc7e63ec272`  
		Last Modified: Mon, 01 Feb 2021 23:04:22 GMT  
		Size: 207.1 MB (207055839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfe310549358fe86c58348f476fe3cf3c04c13b34c2fe5bb4ca743f10fd9ca5`  
		Last Modified: Mon, 01 Feb 2021 23:04:06 GMT  
		Size: 819.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
