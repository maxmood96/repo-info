## `amazoncorretto:16-al2-full`

```console
$ docker pull amazoncorretto@sha256:d9afcdd511e89d9fb14faf06e2d67a0a95eb21a30f0b04e177320d7a21eb379c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5762d905428e54a32a01969c3af4d336adf5411eff02ff5cf827894da7cd0a5f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221933296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39a0f01b50cd6527c3a6024c82706823a355719a84eccbef7677ad66b00c163`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 01 Oct 2021 21:20:20 GMT
ADD file:21dc1ad70daefae1cf0e1b3e78fab06decda5cb9bc958d8a178adb3eddd1fb32 in / 
# Fri, 01 Oct 2021 21:20:20 GMT
CMD ["/bin/bash"]
# Fri, 01 Oct 2021 21:40:04 GMT
ARG version=16.0.2.7-1
# Fri, 01 Oct 2021 21:40:26 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 01 Oct 2021 21:40:26 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 21:40:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:0728ce74490afacced1ac863ee989913071f97c52ab996e46cdd6b5369a2d63a`  
		Last Modified: Fri, 01 Oct 2021 10:54:14 GMT  
		Size: 62.0 MB (61952638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fbbed6cc4f9ba9c3dab92347907958ecd7856fd692f22d21740c22c87c4565`  
		Last Modified: Fri, 01 Oct 2021 21:42:53 GMT  
		Size: 160.0 MB (159980658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:db77b276efd4461e5bee0e08b60718f4817075a2d0fc94a9da1b0f8a5971bfab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223518326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256638cb0cde5daf5726d8762a9a92c2766b8325478445dc69cd3b9c1f854882`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 01 Oct 2021 21:39:54 GMT
ADD file:1d2ae2bfc4c1f83dc53f48b42503812d345622ab95d8fc84536216ef3d53d807 in / 
# Fri, 01 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 01 Oct 2021 21:58:24 GMT
ARG version=16.0.2.7-1
# Fri, 01 Oct 2021 21:58:43 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 01 Oct 2021 21:58:44 GMT
ENV LANG=C.UTF-8
# Fri, 01 Oct 2021 21:58:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:5aa4871be3ec1bcadf7a5257231adc7740edac9a612749884f03ab14b4b2d4ec`  
		Last Modified: Fri, 01 Oct 2021 16:32:04 GMT  
		Size: 63.6 MB (63581978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2add0483dc55a7ae5cb842410cc8ef3d74b2d82d0b240cee4a5fe038c83a34`  
		Last Modified: Fri, 01 Oct 2021 22:01:35 GMT  
		Size: 159.9 MB (159936348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
