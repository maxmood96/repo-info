## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:9cfe41a64a5484b38d847e3a833e19b80448020b2fcabf13aa5908b432d99c29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5301563fd2271bfdfbf7842d46953d4d3ee26700b737201debc8ef09d95b99cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228474803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ce8096e04b928f9bd10856e63ce845b86057ae6e1c0de97f104b9680b8bddd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=21.0.4.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9853f22d8ff72bfc3a51ce0315e66e2b983c5c08c3199c216cd3e992714bf178`  
		Last Modified: Tue, 08 Oct 2024 00:00:04 GMT  
		Size: 165.8 MB (165796647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:39507b30aa28e87c2757262be90afc76ff8a204b0f0d57c40390d3a019e8a377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6115331e8c4dc27f74ec7388cbea250187edc23ec751bfd892aa3c45eb0101f`

```dockerfile
```

-	Layers:
	-	`sha256:ee054fbf3924c1030ecb00c3ffe653040fd1fa3b7c62bc63654cccc25fad0ffc`  
		Last Modified: Tue, 08 Oct 2024 00:00:01 GMT  
		Size: 5.5 MB (5527679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d91002ead44ec7b9f6117d7c727fc3e245fa7c236f7cee070536e73c42be8e`  
		Last Modified: Tue, 08 Oct 2024 00:00:01 GMT  
		Size: 11.2 KB (11218 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c68dd7ed7086454cb2798cbe037cd0c0dc23245f41d447e9b43f4ca90df369af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228419194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04033fd7c0c5927fe9f214b6b14c814017b0865b9761b9ca46aa7fc614fa94ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=21.0.4.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c496d594e3a59a8c1b22b93ffd11c8c3d617d1a78a24fdc4af4886a5b1e59514`  
		Last Modified: Tue, 08 Oct 2024 02:10:50 GMT  
		Size: 163.8 MB (163826535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b899c46ea79ca087412996f0a7326b484d74dc8f09aaac1a266fea78238a4e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fe755a2c0c970ca091574c8f1f63c6ce3433eba9ef6f8e55f77bf9b82c1a4b`

```dockerfile
```

-	Layers:
	-	`sha256:605fa9efbbceedf4a5bf0961481e0c3a91414d8b5185c0d1e28403eba05bad9b`  
		Last Modified: Tue, 08 Oct 2024 02:10:47 GMT  
		Size: 5.5 MB (5526366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ad4655c268c8dd7c21ccf00cf1b5dffa6d757f2ca5780344425b5de2fe1dccd`  
		Last Modified: Tue, 08 Oct 2024 02:10:46 GMT  
		Size: 11.4 KB (11371 bytes)  
		MIME: application/vnd.in-toto+json
