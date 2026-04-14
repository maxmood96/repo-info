## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:44994bfa666cafa22fda482f1c2d014c15b96b550f7071874e5348f190c57007
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:016639770f69e450d5f8a3e132f204356ece03aacc98202d3269265b89001018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139078970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdf3ada39374e069dd66bfc4542c88e5f95b8b1e86d14f3af879a3650e23549`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:57 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:47:05 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 22:47:05 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 13 Apr 2026 22:47:05 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:47:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a794e049eea4656f53218f0a128a5ac86b2b1d0ecba2ae7bcacfb35ebf5a1a`  
		Last Modified: Mon, 13 Apr 2026 22:47:20 GMT  
		Size: 76.1 MB (76123704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:83b54976b1efe3d9203573711f7adb4a0975416e0a4e73bbd594093525cb304d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c85529f80131babac1f3c18115b3fc942fb14b782950272dc1dce2e21c6d5`

```dockerfile
```

-	Layers:
	-	`sha256:95df114c3cd8c8bd9e626e88f3b76649a996007be279a8187fbd0d27036de9da`  
		Last Modified: Mon, 13 Apr 2026 22:47:18 GMT  
		Size: 5.4 MB (5377455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12ab4f20396be7c06708f71dac59c1ac1951cd09cff19e2ce5b18e6ca297b9ed`  
		Last Modified: Mon, 13 Apr 2026 22:47:18 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:416777fe197ba117f22ae169a3be46b64c27d515f0c71a52f244f363e568b113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124726028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f04ae680b9932b780db428f982a2068a0642eef21bd738db542b59953e3afc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:22:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:22:09 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:10:05 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 23:10:05 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 13 Apr 2026 23:10:05 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:10:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4147bf2fb905861a3018f299d8138ed0cae5ebe1b7d027943acb9616ee34ebb2`  
		Last Modified: Mon, 13 Apr 2026 23:10:20 GMT  
		Size: 59.9 MB (59923053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b5b8ddf1a9ef2a3f1c764124f6b0efdd88fdba9210c983614b46aaadf7d5cddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7279ca18b2ad2d5537b5deedd8151d354c4f73c9de1cbfccde3741206681ee8e`

```dockerfile
```

-	Layers:
	-	`sha256:a1db4b2500f9ae1f1f8e50b2ed26eaa0a737006a26d975c275372d132016a6a9`  
		Last Modified: Mon, 13 Apr 2026 23:10:19 GMT  
		Size: 5.4 MB (5355954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4b0802ed643c41255252c39844f7d3dfce259d2984faad8f0ab164a6a8b5c4`  
		Last Modified: Mon, 13 Apr 2026 23:10:18 GMT  
		Size: 11.7 KB (11690 bytes)  
		MIME: application/vnd.in-toto+json
