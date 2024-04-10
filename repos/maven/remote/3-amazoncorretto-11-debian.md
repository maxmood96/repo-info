## `maven:3-amazoncorretto-11-debian`

```console
$ docker pull maven@sha256:eba73b8b4afdf2e05f1f2b0ded9a9cdcb599cbaf8f77e81edbab3c9daeabe556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11-debian` - linux; amd64

```console
$ docker pull maven@sha256:8212e5b9629ae4771b401741825479ccbaa62a3b5c68551fd43e46a7fa6995ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237913110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fd3f4e2e97a7f6aac2c4e3c2a4233f5e9293175fe8fc7a7de6eaefb82aa4ce`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Mon, 01 Apr 2024 09:00:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 01 Apr 2024 09:00:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 01 Apr 2024 09:00:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 01 Apr 2024 09:00:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 01 Apr 2024 09:00:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 01 Apr 2024 09:00:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacc571886a34bb1aa93ecdadb088a43703fd8e444ba97de7ae29cbd454d2361`  
		Last Modified: Wed, 03 Apr 2024 00:27:21 GMT  
		Size: 199.3 MB (199307609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19ecc6c84d5834c0fabd3fddf828ebbf223827bb5a52eb28797e4216d7134af`  
		Last Modified: Wed, 03 Apr 2024 00:27:08 GMT  
		Size: 9.5 MB (9479936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f8dbd0987c15a60707fced5095f03da2585368caeb292f6bb003e7a5ff60e4`  
		Last Modified: Wed, 03 Apr 2024 00:27:07 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be32346d04e37e7d25f5fc09d1b4cac955ff5f079cb3c3ca105d5d34899b98bf`  
		Last Modified: Wed, 03 Apr 2024 00:27:08 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70976003a091cc2baac4e161b21915ef518314b50f6a07736b7908f79beeecf5`  
		Last Modified: Wed, 03 Apr 2024 00:27:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:173cb6613d116db4a628e90f2df5122bfd0f448d46cae7df16a1a3f4793d9519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234817825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f62c325b91f7cce5a250578041d9d1664e0ac89493dc53f137c2d2b44e4a7b0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Mon, 01 Apr 2024 09:00:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 01 Apr 2024 09:00:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 01 Apr 2024 09:00:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 01 Apr 2024 09:00:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 01 Apr 2024 09:00:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 01 Apr 2024 09:00:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710dcc702e35e02af6a9daf1a6ea61b33bfbfaabed95770224e381133c65f2f6`  
		Last Modified: Wed, 10 Apr 2024 05:17:00 GMT  
		Size: 196.2 MB (196174325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c29b441e9a9348b2d6630ae7664520c1dce3d1379356d9b005c03ab2d9d4c0`  
		Last Modified: Wed, 10 Apr 2024 05:16:50 GMT  
		Size: 9.5 MB (9479963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17ec79ef0645891fb5234cfe68ce914bd9ccf359e7f69e210f43dff04a35a99`  
		Last Modified: Wed, 10 Apr 2024 05:16:49 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a237481dc0f9944b4cb2753c746c5895177c454d459e07604799a45bf1ba09`  
		Last Modified: Wed, 10 Apr 2024 05:16:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a05d89816d5d49bf725c4ddc8d40d438092196d4cc98deeed9af7491670c189`  
		Last Modified: Wed, 10 Apr 2024 05:16:49 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
