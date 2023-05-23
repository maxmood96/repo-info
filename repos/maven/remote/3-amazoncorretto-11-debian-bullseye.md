## `maven:3-amazoncorretto-11-debian-bullseye`

```console
$ docker pull maven@sha256:9aabefae888e685cae32622bc751c7f7253dc844bcc171183017841329caa4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11-debian-bullseye` - linux; amd64

```console
$ docker pull maven@sha256:89ab857e21491ccf031f0fb948f410ee8e36ce43b890074633f4af6ea7402829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237432626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193a6fb30acc34e0b2c50ff345dc67a3ad746e99cc3e2be56550bc8ee9d56308`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Tue, 16 May 2023 11:35:55 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5cf382ce17d19ae1496d9f3a50f322adacd3666ad8bfca2235e6b9409e50f8`  
		Last Modified: Wed, 03 May 2023 20:56:47 GMT  
		Size: 196.7 MB (196713321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c08791865d6174d584128c77024fa1d3a92777259f76589e7edfdc823eb2b5`  
		Last Modified: Tue, 16 May 2023 18:26:25 GMT  
		Size: 9.3 MB (9314411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e9eb150d44d40c387f0d366120c490c3786c9aa7e3599d36d92b3385dea6dc`  
		Last Modified: Tue, 16 May 2023 18:26:24 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3c7da688cd258327e1b67373f1cb96fa790eb4b7a9e35903c2b5280f794f74`  
		Last Modified: Tue, 16 May 2023 18:26:24 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c58e0e66ca1e22e21aa9555c44f1834726fa59c18499d7dae6be70ae262232`  
		Last Modified: Tue, 16 May 2023 18:26:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11-debian-bullseye` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:446732645a2a16194eedcda472fd03e64fc167253c35b1f943166790e3b48317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233168659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd310824b0e436721f156e3296e6d8cbde6e37ca36439371861efc2c0fa57ff5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:15 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 May 2023 00:43:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 23 May 2023 00:43:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 23 May 2023 00:43:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 23 May 2023 00:43:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 23 May 2023 00:43:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 23 May 2023 00:43:15 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 23 May 2023 00:43:15 GMT
ARG USER_HOME_DIR=/root
# Tue, 23 May 2023 00:43:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 23 May 2023 00:43:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 23 May 2023 00:43:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88311993c787cdb280e30f6adf90608ee757b9136058b7fb08eb9fb7ef033373`  
		Last Modified: Tue, 23 May 2023 06:13:23 GMT  
		Size: 193.8 MB (193800121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287af1dc210b06041194fab256283b15abf54ed1db5e296fb3f6ccbbc538edd4`  
		Last Modified: Tue, 23 May 2023 06:13:13 GMT  
		Size: 9.3 MB (9314414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae210119d767e3c73b449ead88a073878386438ae0cffac585d9bcb0d3bd51c`  
		Last Modified: Tue, 23 May 2023 06:13:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07c424eb1ed585a03dfb74bac20088876681f4bb55cad238d0626adb37b5c15`  
		Last Modified: Tue, 23 May 2023 06:13:12 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d16f07fd62051f92977876643f5a9e65a155d1bd830006212f6a7f06cbb9966`  
		Last Modified: Tue, 23 May 2023 06:13:12 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
