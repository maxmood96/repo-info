## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:61001fb7305b444af86110dbc4383f03b54a86b4a3be8262e9414e48e2bb2d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:b80647b5c765bfbd90e60fa49c8cee8d7c54bd0fdac68d3cc6209ae6dcb82e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160023029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ed821f39d07ed10b6ad9f7e1c7e12f742aace7425fdc4735b4c16dcb409734`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Fri, 14 Apr 2023 15:35:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Apr 2023 15:35:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
ARG MAVEN_VERSION=3.9.1
# Fri, 14 Apr 2023 15:35:23 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Apr 2023 15:35:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Apr 2023 15:35:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Apr 2023 15:35:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103cac1fd33a918c30fdfaec3839d173741cbe2b77427f1d493bcebabb56b959`  
		Last Modified: Sat, 15 Apr 2023 00:29:38 GMT  
		Size: 119.5 MB (119497257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa86c4c2ca85684a80ea1b22c9d4f009f637d325202835c1d64c74ea2b4112ea`  
		Last Modified: Sat, 15 Apr 2023 00:29:31 GMT  
		Size: 9.1 MB (9106161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925936e670c055cbf8812e2dd4e400f10a8c6bd210f3c76c217a62a9ac6b9ed6`  
		Last Modified: Sat, 15 Apr 2023 00:29:29 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7c1c0aca589aa874c174590c558c536f00b067bc9bc658a9969c5f6405211f`  
		Last Modified: Sat, 15 Apr 2023 00:29:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b094d8aa453b19f16a9f576fe930f7a59163b00202b0f705b4d1f8c76bc0def`  
		Last Modified: Sat, 15 Apr 2023 00:29:29 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8bd0aa957da87ca1fd89f22c6c23b036a16c031f5f49fba923fe6877e7901e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142647966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545c7f736f4022a8f0a2c90fdb80c7d282f0ccf94f97e8d5081468f47cf6e4d7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Fri, 14 Apr 2023 15:35:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Apr 2023 15:35:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Apr 2023 15:35:23 GMT
ARG MAVEN_VERSION=3.9.1
# Fri, 14 Apr 2023 15:35:23 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Apr 2023 15:35:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Apr 2023 15:35:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Apr 2023 15:35:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd711f6b262eca8ad01f43107afc3c7e93d77baad15343bbac47c8d873d098`  
		Last Modified: Sat, 15 Apr 2023 00:47:49 GMT  
		Size: 103.5 MB (103476619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcde348af67f6fd121d3278f4352b0f6eb1a2e239a49049ec5a902acfa50352`  
		Last Modified: Sat, 15 Apr 2023 00:47:43 GMT  
		Size: 9.1 MB (9106143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a181246ed71bf9d4c8043a3a5dac800698963483f8dda328506a6c1f801d94a5`  
		Last Modified: Sat, 15 Apr 2023 00:47:42 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f668a767ee1e908fad7fb52edc6f601045c6684d42a4abf09f6b63e0a72a177`  
		Last Modified: Sat, 15 Apr 2023 00:47:42 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb22a39706cec1c62f61876ef140f832453e93c9b0f1460a57d32ac31ab006d`  
		Last Modified: Sat, 15 Apr 2023 00:47:42 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
