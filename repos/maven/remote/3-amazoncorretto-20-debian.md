## `maven:3-amazoncorretto-20-debian`

```console
$ docker pull maven@sha256:ad8b5b49534d4b31fa72aabaeaaa30cedd63b98d54c46918f368cd2ddaf951b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-20-debian` - linux; amd64

```console
$ docker pull maven@sha256:71c0ebab3db642a5cd7ed47c479f0f1e4b9873bf732faedf9f59d1941a8b971e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246040022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0398af8fe0a661f6c8f7aced139b5f39aa1862921bccc4114b9040c76f34967`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:20:14 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-20-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 May 2023 01:20:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 23 May 2023 01:20:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 23 May 2023 01:20:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 23 May 2023 01:20:14 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 23 May 2023 01:20:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 23 May 2023 01:20:14 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 23 May 2023 01:20:14 GMT
ARG USER_HOME_DIR=/root
# Tue, 23 May 2023 01:20:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 23 May 2023 01:20:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 23 May 2023 01:20:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee49848a72a5c48d5171ec9fa49c842dd3dd83f9bcd6026b32f58b95d19a5583`  
		Last Modified: Tue, 23 May 2023 08:59:25 GMT  
		Size: 205.3 MB (205320643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fa8d574b229a7f31203d5d0c372eaf42b2ffe02033b4c5598b4f0060140bb7`  
		Last Modified: Tue, 23 May 2023 08:59:11 GMT  
		Size: 9.3 MB (9314413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6740c98beb4970875cdee9d531bd962ce08b816947a551783fe5e9dfd479f6`  
		Last Modified: Tue, 23 May 2023 08:59:10 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8373693ab719a71e93a1aa52b700395b263e8450cfd1fefa6c77178f9d2cb63b`  
		Last Modified: Tue, 23 May 2023 08:59:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301cdb4388eef5b6a15a3b6f3095a97d5d9b700f1421e021c0202189875ff249`  
		Last Modified: Tue, 23 May 2023 08:59:10 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-20-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2bcfddaec5d3951c19cca23a3fb1c5a3ed2979ff1a7798d2f7315397da7a3956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242660109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4f7828767ec00d07c1abeae61f75e9588121ad360c92cfee5a8639f5f4da53`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 16 May 2023 11:35:55 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-20-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c4b6153784a4582b3f6613f704f33726bc2aff918b9812e45ba5874a5af887`  
		Last Modified: Tue, 23 May 2023 06:14:24 GMT  
		Size: 203.3 MB (203291571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fb02475688c19ffdac579decf8e2261f37ce06380c79be04832371a9856af9`  
		Last Modified: Tue, 23 May 2023 06:14:14 GMT  
		Size: 9.3 MB (9314414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1403aa508f91b4b48902603d2ca13d0d6cf09271266d6478aaa67795a8668e`  
		Last Modified: Tue, 23 May 2023 06:14:13 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4be5ae518a36b3fd697a7487b3b7773ede1d7d2d75aea7e6e5bf3c5edda67c`  
		Last Modified: Tue, 23 May 2023 06:14:13 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ffe361e50d0c5ff386b8fa5475d336e728ae2c4d10f300d17c9806a4ae9f3`  
		Last Modified: Tue, 23 May 2023 06:14:13 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
