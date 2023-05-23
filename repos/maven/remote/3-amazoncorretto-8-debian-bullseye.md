## `maven:3-amazoncorretto-8-debian-bullseye`

```console
$ docker pull maven@sha256:f9a0906dbe47fd7951fd8bd52d0b90773291c7d0dcecb24059ee0f713151b38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8-debian-bullseye` - linux; amd64

```console
$ docker pull maven@sha256:1c8b043d2b72c1c4073539fc3ff940b8204abb518dc37b6e2b6742a2de3b0846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160203873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c87270c8a73881ad4684eb5aaf008e0990ef4bcf7d9597ea837c2aa3ab51b6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:20:14 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0389bbb596e8a9c3cbab77b0693ebc22c82163db6eacb6c8c316fda3bac2bd08`  
		Last Modified: Tue, 23 May 2023 08:59:51 GMT  
		Size: 119.5 MB (119484499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c18ba6304b5e4f6527066db15df0da4cedf2f7a421ac27992bb1c6b4da0ad8b`  
		Last Modified: Tue, 23 May 2023 08:59:43 GMT  
		Size: 9.3 MB (9314413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677183068fdc50cd56fd29223733590f2dde7907f17171607e6ad9b7e14c2b95`  
		Last Modified: Tue, 23 May 2023 08:59:43 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129365e295a75255bed017b6d7e9871db7d6367e469aa7d1428317250dbbdd69`  
		Last Modified: Tue, 23 May 2023 08:59:43 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c1d9874e85072ceca0e2a722545c02a995b1435768ec57312e01aea1e3d2d`  
		Last Modified: Tue, 23 May 2023 08:59:43 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8-debian-bullseye` - linux; arm64 variant v8

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
