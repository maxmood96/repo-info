## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:227704a92c0310bbef1a63cf277fb8953fb26e2e435f90cc6fef75e1259f327f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:60138d00ef93b3ca893de49b1ccb687428794f0f25d1c6039413b89c7b40836b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160203899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45724479e285faf160d33e12e384cd50d34f7beb8b6e42a6df9d3281c4b89d0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Tue, 16 May 2023 11:35:55 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:51276179a664e5cd96a54d121baa8e69f0b9841c3686a9f410c3786a8b26c167`  
		Last Modified: Wed, 03 May 2023 20:58:50 GMT  
		Size: 119.5 MB (119484599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa7094380ff0c4ca7fb13d680257b75029e46cc0833d78e607c62e2798550f`  
		Last Modified: Tue, 16 May 2023 18:27:51 GMT  
		Size: 9.3 MB (9314412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07db40e0eeca931c6ce9e24e3356b7182f216add1babe0c92d7ca3b7cbd9265d`  
		Last Modified: Tue, 16 May 2023 18:27:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc596da48334085319b724a2047958869d7abbf41fcd15488f95a48c816d304c`  
		Last Modified: Tue, 16 May 2023 18:27:50 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c48501f9996fa3530c35fb6e75cfeaa26cf2b3a2dd41c55b75d0ca76482d09`  
		Last Modified: Tue, 16 May 2023 18:27:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:af185bacec7a326725368b266d75106592ab1538be89d15741e68f66c06ec604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142828875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231d545d9a5d8fb3d7c8c7919687a9d54344531fe36599e08b95eb41670d8324`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:15 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:37889826140d2b65e6080215fb4e4e3fa55d04297028b0dc659371758238edbe`  
		Last Modified: Tue, 23 May 2023 06:14:49 GMT  
		Size: 103.5 MB (103460333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af30e4328071e0f82746a800ab9858a7907dcff142b79c245f153e866bbd8b5`  
		Last Modified: Tue, 23 May 2023 06:14:43 GMT  
		Size: 9.3 MB (9314421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cc2cdb8a16a02a923d5b4ab4c2a6eb4d1c408e35fd67684b923e9fe1a548d1`  
		Last Modified: Tue, 23 May 2023 06:14:42 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d64a9af2402fbe54455ebd62f2f8a32788a7f20a4dc8e36464e3a6c04372a6`  
		Last Modified: Tue, 23 May 2023 06:14:42 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f73d0d9226c6faa3cdda1ce82a44ce8e539e25147d0e393d3a6b98d01ad99e`  
		Last Modified: Tue, 23 May 2023 06:14:42 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
