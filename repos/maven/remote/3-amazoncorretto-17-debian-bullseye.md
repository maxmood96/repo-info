## `maven:3-amazoncorretto-17-debian-bullseye`

```console
$ docker pull maven@sha256:e11adb209b38984a1d01efc109297c38805e0999dbfe77a49aa1fdc904be090a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17-debian-bullseye` - linux; amd64

```console
$ docker pull maven@sha256:e727703582dfa8b0052b86a05769759e9aeae5cb38212aa5b76f48821a22ed41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235813555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef023d7e1f3dec3afb44d3fac9c7f88424b7a033bedb226a30619c9564ac1127`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Fri, 14 Apr 2023 15:35:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:de829c478e586daf2b8c44e0c2025a25230c6de603084c5956cbf4e8423316b3`  
		Last Modified: Sat, 15 Apr 2023 00:28:08 GMT  
		Size: 195.3 MB (195287788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b09f26866ecc3d5cf8282bf4e172cf94760150c0b0d55a596f4c011a98be00`  
		Last Modified: Sat, 15 Apr 2023 00:27:55 GMT  
		Size: 9.1 MB (9106161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226bab810d856fa86ae7631dfce9f1ab4e519e9a04fedde59a5e0a9de184b9f`  
		Last Modified: Sat, 15 Apr 2023 00:27:54 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4137d92d492910f2424dba750c27a58b0e63524c3b23c43094d88956e1e195`  
		Last Modified: Sat, 15 Apr 2023 00:27:54 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1179cd880cc68e584173fcfe5720b5ce0478701e3528932480db63bac74600b`  
		Last Modified: Sat, 15 Apr 2023 00:27:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17-debian-bullseye` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e8e2ed224b93eb1302e64fa4e40e0908443e3e78b2578c07d2a4947d9bfcccfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232929301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f4404ca8cf6a7556ed9c5188f4ee116fd997483511412bed31bbb4e22349a4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Fri, 14 Apr 2023 15:35:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b4619b3728acd60e7fab3131846904586da050eea28d54153ca9b8c35057741c`  
		Last Modified: Sat, 15 Apr 2023 00:46:25 GMT  
		Size: 193.8 MB (193757960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230330e78af329ee5a9097f10f7c8dc44b6ddf40c438dd8a31953fa02603fb0e`  
		Last Modified: Sat, 15 Apr 2023 00:46:14 GMT  
		Size: 9.1 MB (9106139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160a8408e46b835d0ee280909b2a3dc0b4d77dd7ff923faa76a3d9761ffd1f55`  
		Last Modified: Sat, 15 Apr 2023 00:46:13 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d082fe2cdb3056b379c6f7da112fdaa5f3d00c0e22123d8f05aa7b023d12a84e`  
		Last Modified: Sat, 15 Apr 2023 00:46:13 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1929802726968a2df07ef385af8608858cb283dd66598bd752a6eca22c040a0a`  
		Last Modified: Sat, 15 Apr 2023 00:46:13 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
