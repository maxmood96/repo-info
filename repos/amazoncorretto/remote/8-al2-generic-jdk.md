## `amazoncorretto:8-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:79f08a081e1b3726cc17e56618c7842750d284cce0fe2766b76adb521fd936b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4da18bbaf8c92c2eab7948d0931bc2d66b2e8e4c6ebb7450b68833d456d96648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138978037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff59331534259cd230c9a1d4def99c4c023030d08ef78c9ce478cb2c79a4b444`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:09:00 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:09:00 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:09:00 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:09:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e39b529a4a5652bd7d45eb86176943dec43fa669d17329c3db61c37ea5cdb3`  
		Last Modified: Thu, 06 Nov 2025 22:09:30 GMT  
		Size: 76.0 MB (76043903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:96a399e7b995be72727a60e1c5094128e209ac95db8de6e0078ffecb829283f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5302dd47dfd95af5f13146b98157d373bbd7c8c563e2472aae3a15e6327b5a55`

```dockerfile
```

-	Layers:
	-	`sha256:cda4bd5415b4f5089ca549667a2ec0a5d8a9d130332b56639b00fe36474b6f3c`  
		Last Modified: Fri, 07 Nov 2025 00:21:10 GMT  
		Size: 5.4 MB (5377354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd472a2bb990e539802ae52c483c744ba091227f6e1524768f34ba45c82edf7c`  
		Last Modified: Fri, 07 Nov 2025 00:21:11 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7e1547d93350ece118f6fa05cd1ed3960d0d6f9c1a85ad37a3490ab4a03c613b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124912224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadc08999ef3cb3a895070b2fccbefe5b7e64dba90ff65756980ea3e730bbafc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:10:35 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:10:35 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:10:35 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:10:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d294085a6bcd7866789fb9fde633a724ff73c7136fda7e739a5fd3350db72557`  
		Last Modified: Thu, 06 Nov 2025 22:11:06 GMT  
		Size: 60.1 MB (60118928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b00965653e21f9bbcf6b7b8995e8c275de0a5c12392a35a408272599323eaac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842dd73bc84d82b3d5e4683dfd2187c1cbceb154fc47a1072957136e271561d7`

```dockerfile
```

-	Layers:
	-	`sha256:390c1218bfc875a0a8aea33a9a1ddd449660813db7ab83543bdc3104fe79a26a`  
		Last Modified: Fri, 07 Nov 2025 00:21:06 GMT  
		Size: 5.4 MB (5355853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b63c941bab69a1348884f4770109ef296db3eaba67c6e13b7e820732ac8409`  
		Last Modified: Fri, 07 Nov 2025 00:21:07 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
