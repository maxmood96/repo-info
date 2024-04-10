## `maven:3-amazoncorretto-21-debian-bookworm`

```console
$ docker pull maven@sha256:c9f79ca12945c7a94f412ff817664d3c2f6f0cad2b712d5a8f65c74e2cd5d880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-21-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:36d764f2b7a9c7beb6994ee055019df04f2988c439971a448743e12d0ce78d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.2 MB (252174293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427249d44a36f4cec0f64a105b93dbe7a497d8c098b8862ca2d3a169f35e03a3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Mon, 01 Apr 2024 09:00:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:07e3dd1746c59ae40b3b7df6c9d26a9011a47bbd1979a31b6bcd460121063f2c`  
		Last Modified: Wed, 03 Apr 2024 00:28:59 GMT  
		Size: 213.6 MB (213568768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f143bf0aba76a13f589e65777020746a9cb35563acd800071904d73c79c9e9e9`  
		Last Modified: Wed, 03 Apr 2024 00:28:44 GMT  
		Size: 9.5 MB (9479961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aec35a2b2078dde00d211c469465791d3fb3cb8bf1a62b219695fe6310e3174`  
		Last Modified: Wed, 03 Apr 2024 00:28:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30996a056c9f4caadc7b263ce8f6c61d91ac82d0c9c1935ac63ec6e534a76e1c`  
		Last Modified: Wed, 03 Apr 2024 00:28:43 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80fa9538cc76e6a8a3c76d108b0bcd2623948f92e7b7f3a01b94306e87a12e6b`  
		Last Modified: Wed, 03 Apr 2024 00:28:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-21-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:424d8d40fa4c6f0407e49b5112514366d497e58642509bb2ad4a3b8ccecd75a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249976383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8508ff4e45a6a464e53707550ab2af7422bdb58d065348423b9733d572c8ea86`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Mon, 01 Apr 2024 09:00:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:5a0f41527a877b0976ef695d3f5dfb3306f99189f471382318e9db30f156a260`  
		Last Modified: Wed, 10 Apr 2024 05:18:00 GMT  
		Size: 211.3 MB (211332905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde5ad958cde1906e3f0d95c8e3e249869f5b6c707856f9e50e9db1de4b075c3`  
		Last Modified: Wed, 10 Apr 2024 05:17:49 GMT  
		Size: 9.5 MB (9479944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4d51229686dc2480151a5b9ad3a21b4fc1bd8f5aa12d7ec0babfa942d27359`  
		Last Modified: Wed, 10 Apr 2024 05:17:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e97d67de29398dde064ee278e19250c18b3cb1b1c635941617f50eac527dd1`  
		Last Modified: Wed, 10 Apr 2024 05:17:48 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4d03628ef376fdffb8973a6409fec02a552130b0fadd4fa9d22e5e0f1fe021`  
		Last Modified: Wed, 10 Apr 2024 05:17:48 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
