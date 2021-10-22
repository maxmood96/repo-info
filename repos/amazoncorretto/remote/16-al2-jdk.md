## `amazoncorretto:16-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:1cf1fc0783898f6a3207fbf464bb6ea6b5b12020d36ab5d2cb84cfc6166f6de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2243e5330ae98263a9239b48f218e19cf24b3563e2d15e8d6d227db7d5cea53a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221968956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447a42634c07919e519500ccfdb6a78907e2a190338ef60cf89753e8bca6364a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 22:19:45 GMT
ADD file:7aef897e53c30ca977c42dd7692208abbd381b7d2e7e07a91d929f3f0ac4ea5c in / 
# Thu, 21 Oct 2021 22:19:46 GMT
CMD ["/bin/bash"]
# Thu, 21 Oct 2021 23:28:45 GMT
ARG version=16.0.2.7-1
# Thu, 21 Oct 2021 23:29:07 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 21 Oct 2021 23:29:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Oct 2021 23:29:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:5263c4cb36ce7acd05658a221ec502b376a281d7a6075ad09beb23ac02a7668c`  
		Last Modified: Wed, 20 Oct 2021 18:03:24 GMT  
		Size: 62.0 MB (61976108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e496c567e765041d6b768d9e10158d68d77fa5b1c482d9518f60fd914ab6549e`  
		Last Modified: Thu, 21 Oct 2021 23:32:38 GMT  
		Size: 160.0 MB (159992848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:813b68118d9f09760c6265ff00c6d3371e7cbab8d29513320be949a7deef1a5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223550871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51e62606d8beeb459f6d3d90e5f5e20ea44ef4d2341dd917901bf8e9cdcf74c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Oct 2021 21:39:54 GMT
ADD file:d9148106dadecc4050f37ebf22ea9e7e56102619349368d1ce40d36f5e2fadd1 in / 
# Thu, 21 Oct 2021 21:39:55 GMT
CMD ["/bin/bash"]
# Fri, 22 Oct 2021 02:02:39 GMT
ARG version=16.0.2.7-1
# Fri, 22 Oct 2021 02:02:56 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Oct 2021 02:02:56 GMT
ENV LANG=C.UTF-8
# Fri, 22 Oct 2021 02:02:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:e20b44047a77430ceb5678bf23278ca2841835a1b18a72adaace3d3a11c56031`  
		Last Modified: Thu, 21 Oct 2021 21:40:44 GMT  
		Size: 63.6 MB (63606878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72eedc8e4d5ac9433a3715396bb884a8599400ddd5a06babc301ca4c823104d`  
		Last Modified: Fri, 22 Oct 2021 02:05:32 GMT  
		Size: 159.9 MB (159943993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
