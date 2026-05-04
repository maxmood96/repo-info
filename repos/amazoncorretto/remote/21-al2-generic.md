## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:847bb1001ff27c3c380c35d6a7bb0b8c65280947fffb42a1c900983317cbe5f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:37975ca675bc3a4bbe361dff53f8ef0f52a612baadd317abf355d23ab2e3ad59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228555566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a5f5951648013bfb04913ee349256b7c9b4fa1ded88ab557d37801c4e46682`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:29 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:29 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:12:29 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34427ac8245f2bc54ae2269830d743a78c73c94138af0501660e55c8b91be1ff`  
		Last Modified: Mon, 04 May 2026 20:12:51 GMT  
		Size: 165.7 MB (165695557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e9ab569e51b47faccd0bf1dec7bc9badcbfd3eb02adcfe82c786e4088aca902a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208c7ecdf930cf843ca1d4f2c85988189c9b2798fcccf2f44c2d6334bf737001`

```dockerfile
```

-	Layers:
	-	`sha256:a34c827eb67e5d5f91fcba10d35d634f7088bee0cf3f85e8194cd3cb80e0db42`  
		Last Modified: Mon, 04 May 2026 20:12:47 GMT  
		Size: 5.5 MB (5536520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da6a25104cdac16da334e25a6a463bbbb71ac4c56daf46ebdab0f9bbd1e2354`  
		Last Modified: Mon, 04 May 2026 20:12:47 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:785d922ccfd411e1fb9cabd3e4269ef5f53ea917b1e62efdcf5b61b74a7b5d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228698368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa4844ce8153df42f8812c13b5d8ac7e927ebc1518176c8ba249401a3f2da45`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:07 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:07 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:12:07 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdfcdf3bd2c92c2567fd8412ee72fbd46db7b157b9d64a0f969635bd1431a4a`  
		Last Modified: Mon, 04 May 2026 20:12:31 GMT  
		Size: 163.9 MB (163902837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f1bf1563cdd6dfac8efbe171a618335c9ace74872a1a9773a7c4bc987bbdb54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f192a4824876b167d82b0bd527074fbda18aabddd7a01d29edc21d593b2f2d5`

```dockerfile
```

-	Layers:
	-	`sha256:781a575d4ae16835fd9ab2576f382445af47a186ac604f19ce9456f60569ed8b`  
		Last Modified: Mon, 04 May 2026 20:12:27 GMT  
		Size: 5.5 MB (5535209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0da76e9c87bbcd33aa2c5bbe6ebba1f5c486d64fcfdd15582a91374d700693`  
		Last Modified: Mon, 04 May 2026 20:12:27 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
