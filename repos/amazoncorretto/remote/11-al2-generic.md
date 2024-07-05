## `amazoncorretto:11-al2-generic`

```console
$ docker pull amazoncorretto@sha256:8038321c58c0053b337a10e55e04b35c99ae1b1163ed523520be20f0ecd535d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a3b37fa8f39a07aeb6b00ad3819f452709ea3356f9c950b74b8d18559482c872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210752005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6516c64515839ebdf25b10c98849982dfe135213443436f322bab23bc390b18`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773bb01e826ce1f8c25d9da3686ec45a2167a1ae106e9f7ffed80ba96ecee9c9`  
		Last Modified: Fri, 05 Jul 2024 19:56:28 GMT  
		Size: 148.1 MB (148105367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be676378f05de02ab63b71e218754679de73a121e3e3a87401601cd747b6492c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5524023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3a1494b5f438c662d5ebf5b85e1b501366249c7367cc31469443521a189791`

```dockerfile
```

-	Layers:
	-	`sha256:27d356d55d6b6a17a1f9c050322c8809d2c91825ae076e214db807ee44e8d164`  
		Last Modified: Fri, 05 Jul 2024 19:56:26 GMT  
		Size: 5.5 MB (5513007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b8d0ae0c8367514576870592e67df55e3af0b3273feeff294eb049e9c4ba88`  
		Last Modified: Fri, 05 Jul 2024 19:56:26 GMT  
		Size: 11.0 KB (11016 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bf3efb1da878a2b483f2e44d83c26832dca6d99254685409ef5a10b54890ff43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209794397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adddce4f83e9e85f7c6b40efa6292310993be424a74eb53b7e38dbc9b9ad25e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3e7292128fc0b4b3aa0b80f12745c354576e9e6d548648d39ecd340991e0b1`  
		Last Modified: Fri, 05 Jul 2024 20:03:32 GMT  
		Size: 145.2 MB (145225632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d08ac3231977e03b4e017d34adb8abe7eac250f2fea0cc72a877c6f0dac5b8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5523866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b2c122be0cd56769ab48c77af0dc1c331f394d009e3c3f758e7a9d880347f`

```dockerfile
```

-	Layers:
	-	`sha256:aa9df0fae028b054c796b62cb4d03a59ea15e606c56782a9fa12e4883d383cbb`  
		Last Modified: Fri, 05 Jul 2024 20:03:29 GMT  
		Size: 5.5 MB (5512500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9a937b8ed97ff939d49eb64e057143cac778284939196bef7e512e4ee827c5`  
		Last Modified: Fri, 05 Jul 2024 20:03:28 GMT  
		Size: 11.4 KB (11366 bytes)  
		MIME: application/vnd.in-toto+json
