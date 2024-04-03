## `maven:3-amazoncorretto-11-debian-bookworm`

```console
$ docker pull maven@sha256:cf2ef25866b25a9cdd9e93e00b84edb4f4b6efc1095cdc5e55e5c1c473a559e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11-debian-bookworm` - linux; amd64

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

### `maven:3-amazoncorretto-11-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7f11ac6964a7ca4d6ee0f953090737ddd281106dcf67afb9e58db4d5624fd2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234812263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee87b91310164ef1873f4ffcbcae819f3aaee5d09989ceeae0ca352e7fabfb4c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
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
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbddcc1392cc36acff13f82c0edc50aa370446a45d60e6992bd5ddf4fcf2641`  
		Last Modified: Wed, 03 Apr 2024 00:32:05 GMT  
		Size: 196.2 MB (196174483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b8e806ac7b45091429085eaaf59b00a878d9a407cfb1ef28e86105fe32de4f`  
		Last Modified: Wed, 03 Apr 2024 00:31:55 GMT  
		Size: 9.5 MB (9479966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1fd1f586161998be48d26f5982ce4eed6b752412181e8e455223c0b60862e7`  
		Last Modified: Wed, 03 Apr 2024 00:31:54 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035e36024045094d9908df94a5365d4e7b719e0bb9348626e9c87fbb7662d6c9`  
		Last Modified: Wed, 03 Apr 2024 00:31:54 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ae467e704e31a0703c7d534f611b6499d6471e626d3e7038e0bfbd2304a007`  
		Last Modified: Wed, 03 Apr 2024 00:31:54 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
