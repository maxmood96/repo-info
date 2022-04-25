## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:46b7db1329d85ccb22a4f385bfb0d4be9fb7528c59404c6b59dc25bd48ca58a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:b84b3a2400d5cc6f679cf3a21395b4cda37e9cc84898fd9bc53b03d3bdbb0008
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275105835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a589dd115e129bbbe64a19b7cc33e56b8c0b938e5992a7887ba6350176054240`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 03:56:59 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 25 Apr 2022 18:44:05 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.15     && rm -rf /var/lib/apt/lists/*
# Mon, 25 Apr 2022 18:44:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 25 Apr 2022 18:44:06 GMT
CMD ["jshell"]
# Mon, 25 Apr 2022 19:59:33 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Mon, 25 Apr 2022 19:59:33 GMT
ARG MAVEN_VERSION=3.8.5
# Mon, 25 Apr 2022 19:59:33 GMT
ARG USER_HOME_DIR=/root
# Mon, 25 Apr 2022 19:59:33 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Mon, 25 Apr 2022 19:59:33 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Mon, 25 Apr 2022 19:59:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 25 Apr 2022 19:59:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 25 Apr 2022 19:59:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 25 Apr 2022 19:59:41 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 25 Apr 2022 19:59:41 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 25 Apr 2022 19:59:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 25 Apr 2022 19:59:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3497eded1e3eecf8f2698c510b36e1d91b42337d37bd2dc6e64189ae252b6`  
		Last Modified: Fri, 22 Apr 2022 03:58:43 GMT  
		Size: 7.9 MB (7925521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f1a728fd0479aa514d7c373b2e5c987341cbdb6afa8d7ed9a1cc0de35a0920`  
		Last Modified: Mon, 25 Apr 2022 18:46:01 GMT  
		Size: 197.8 MB (197843718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1565687d05b8d84f38f8714951fd1e4eaac066b1a1b64a7dc6eb2b3913a994`  
		Last Modified: Mon, 25 Apr 2022 20:03:16 GMT  
		Size: 32.0 MB (32033012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1105bac7d8ca2917e9d89fc2b535ac30cd8b5788b0b11b782da9942600ee5f8`  
		Last Modified: Mon, 25 Apr 2022 20:03:11 GMT  
		Size: 8.7 MB (8736375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7178feddc2b1d17d420f4505a512fa21dd2c5ce952641fc1b2494ee6fa1461e`  
		Last Modified: Mon, 25 Apr 2022 20:03:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8678413f7c17a0cba731aad89141d6841069e8012398ec1ecf2250e5307ed52`  
		Last Modified: Mon, 25 Apr 2022 20:03:10 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
