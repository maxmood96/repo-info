## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:3eaad6113d6ce59149f4a19ad80c62781e9acb9677ac4322054d1d666eb27fee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2db81c70a395ef20dadbca987547b0fc1f4517f60d4bdedd849ac9f1a7f37acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138373660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24313de4301455da7ada5ec33ccb52e535fe28243aa8985ad0b4361688570419`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=1.8.0_442.b06-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180cf8d95519d92c308d6ab5c5828c0dfc7691ca1b60e774022a3586bea65253`  
		Last Modified: Thu, 27 Mar 2025 23:58:27 GMT  
		Size: 75.6 MB (75620771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7b85a6fdc4b5f203fe18c72b5827e39b84f95e546381173531e6b01450228345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead67d5658776502f3df7f27b6afde344ebaa8129db53c81aacd347ca54a3967`

```dockerfile
```

-	Layers:
	-	`sha256:301124835d87857b8dbf2df09507a83ad62b9caef1af30a13dcb91767f861999`  
		Last Modified: Thu, 27 Mar 2025 23:58:26 GMT  
		Size: 5.4 MB (5359568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2a5e2ffe3bc66651e57bfcf83f22a3d5e286c6bccb6e930ba8d9bcd8b7cf58`  
		Last Modified: Thu, 27 Mar 2025 23:58:25 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:343e7ae3d7d9e4051ac5944a62979820f713eafbf2b5aa172f6bc08eb3c25f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124242483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76be1b7cc79351e2ea5ec3ddec7837329d309976d19c316397309384254df38f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=1.8.0_442.b06-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf9305f37d32bfd5dd85b61aed0d4844d41add69f72ed13643b20e09a4a3110`  
		Last Modified: Fri, 28 Mar 2025 00:04:46 GMT  
		Size: 59.7 MB (59676661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c2bd81bf421071cbafbe43941082f7a64b687db540202c82b68b9d7cb9febd4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdf3bc36296b5407db5b5bec280aa1bf8ac232338b68ee1200f242132fc6f62`

```dockerfile
```

-	Layers:
	-	`sha256:82680337463233027ecfa8b9ae047dec857d90d605d160d55817af76f126da3f`  
		Last Modified: Fri, 28 Mar 2025 00:04:45 GMT  
		Size: 5.3 MB (5338067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c87f340803debf063ea13f6978a6b714cdce858e177272832c2bdd27d9d535`  
		Last Modified: Fri, 28 Mar 2025 00:04:44 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
