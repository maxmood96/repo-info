## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:c26e10ed8cf8300aacc0952a4869ed64e14d47d2cfdb24235b891233e4c5385c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0a2035339ee5429f848a74f82520736c0c803307b5194355812777f2300c8fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228433417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27006688aa29893ce2da0d8e2ae12897d3d4c52c545e19f1cdb249a1f79adf44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:10:39 GMT
ARG version=21.0.9.11-1
# Thu, 11 Dec 2025 22:10:39 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:10:39 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:10:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c73201c30a88e880e6229084d36045851b72833fd9c44da833c4c57bbc506b`  
		Last Modified: Thu, 11 Dec 2025 22:18:42 GMT  
		Size: 165.5 MB (165492442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4656c201dc5d748d2bb715b050981d4db40e4b523523b3b168235bad3438e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbea0a0e21a5e274e798cd502fce909486fc10e465f6ea7f54aec27aa2e93c2`

```dockerfile
```

-	Layers:
	-	`sha256:29adc7ecd897e53d53d302530d5b66e72f298a6acf9ed17086b7a27e7906f707`  
		Last Modified: Thu, 11 Dec 2025 22:49:48 GMT  
		Size: 5.5 MB (5535599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c9dc7c1d6ee735b5f9db339642180cc2fbabbb94262b5486ccde501c62f96b5`  
		Last Modified: Thu, 11 Dec 2025 22:49:49 GMT  
		Size: 11.2 KB (11206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:87a7e89284c02e911a5c040d27f822aa6603aac546c76001875bd46c85ef1e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228376863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e5f91e91af9602aff6048470b10db724ce6fade993e805cb7153a70688bf96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:29 GMT
ARG version=21.0.9.11-1
# Thu, 11 Dec 2025 22:12:29 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 11 Dec 2025 22:12:29 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c2c5078281eb8091217039abf543aea6f691ff8ab258416d86e6107eac5395`  
		Last Modified: Thu, 11 Dec 2025 22:13:24 GMT  
		Size: 163.6 MB (163581108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d22ed18d2a779bc7b193dfbf161465340ff0920bd0fd85366c7b0edc5ad61b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109a85ba453ec498d961436b702757fdfe9deddbe28d70fb1a0a6d10ccbc23fb`

```dockerfile
```

-	Layers:
	-	`sha256:e77a3715b90e1fc32a9f2b0a22328ffa9e95e8a275deacb45423db6bf0ebf684`  
		Last Modified: Thu, 11 Dec 2025 22:49:54 GMT  
		Size: 5.5 MB (5534288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8682df2f710d962697a18c02c4c0874e376fae550eb77ebca2a0ac88c17bfde`  
		Last Modified: Thu, 11 Dec 2025 22:49:55 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json
