## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:759f912b96b3aab92dd071cdc9582fe71e527016020716f98ddd2dfd6d42b4fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6151c9f30e1700a0fa05caff02a10fdad1b8424688783e05490a6a0a229aa545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227978163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ba3958fb3e37b2c0839a0e5aa7ceb6a90593762c309c8224958d1c8481379c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:fcc68e74b985a5b6eee4c73b52bbf6b5465b7b43a029c51e8950289a9262b97b`  
		Last Modified: Fri, 19 Sep 2025 15:29:12 GMT  
		Size: 62.9 MB (62933841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e750caf8f1aace6b2a40b4d03ac34238ad41147f9852aea71ac3fd0f305ecc01`  
		Last Modified: Thu, 25 Sep 2025 03:16:04 GMT  
		Size: 165.0 MB (165044322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:474d5bf9af5b194a427b4806db18806a324990ebbece06d82e95e7a5f4fedba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5543612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd357dd5983def74d54bd1fad32052dd67f2178525fccd36d9ef81ea98759ef5`

```dockerfile
```

-	Layers:
	-	`sha256:0db920910de4384739f6ffb51f170c6839e1be85ba479565845b2811594c9823`  
		Last Modified: Thu, 25 Sep 2025 03:49:59 GMT  
		Size: 5.5 MB (5532364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cfe0e910d9620c66370fba09df725c7ff860288b5bc38494efbef9b524a1a3b`  
		Last Modified: Thu, 25 Sep 2025 03:50:00 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a55cef0dad73c072a55a1c8e984bd2c304a898b5674965cb18455d2936536e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227905412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f096ec2cb6f91f46fe586ad30504966037bd2375a9e078c36e25f8f180b2cda`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9c868e5c107db6ab89ab40ef0c51c4a502a10ecc34ea2109f2dd64bd446a85`  
		Last Modified: Wed, 24 Sep 2025 22:12:58 GMT  
		Size: 163.1 MB (163112265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42926b65d00de118c9103b152e56598ea2ad45c94d7fb005bbeded5a956613b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2603142d833c249c8dd85b967c03fc9612e7ebc1af536d519eb91e6c95b2d492`

```dockerfile
```

-	Layers:
	-	`sha256:10580d4130393fb990fe88fe3cac9028aab3d1b08829360ad50dbdf96d88c4d9`  
		Last Modified: Thu, 25 Sep 2025 02:15:44 GMT  
		Size: 5.5 MB (5531053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a04f431fb2ecf603ffb96998ac7dabeef146ecc302dfd1c6a361671698a264e`  
		Last Modified: Thu, 25 Sep 2025 02:15:45 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
