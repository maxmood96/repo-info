## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:3a2ed04334a85a6b790b557c27c67bcf50c8a6e5407ea795592ed31c519840e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd90e8193c05bdcaa92f0c9a817934e5911d77c3d7e6b3b7e7bb952106e2fdbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228279825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a43ec967e933f59ff7e91f5d255381f7e56a26c3acecaeb2e87af3cb7482816`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 07:59:14 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Sat, 16 Mar 2024 07:59:14 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:41:24 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 13:41:49 GMT
# ARGS: version=21.0.2.14-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 13:41:49 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:41:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e49efdabe18d080499bb81cf60869f43212994c7325a67b45c2f62d148e29e`  
		Last Modified: Sat, 16 Mar 2024 13:51:04 GMT  
		Size: 165.6 MB (165629272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8968dcf7cc35a595d6ae1a6521c96a1f075fa89f73c62aedc339efccffbb8d42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228270382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e245367ffad4aaf55a1d0b81137d828043c367e4d6244d6613a6c650c70114e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 00:06:05 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Sat, 16 Mar 2024 00:06:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:46:32 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 03:46:51 GMT
# ARGS: version=21.0.2.14-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 03:46:53 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:46:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201946717303295f4c7e20fd112327a99499a834cb08fec92e62353b3f0a7a6e`  
		Last Modified: Sat, 16 Mar 2024 04:00:49 GMT  
		Size: 163.7 MB (163694008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
