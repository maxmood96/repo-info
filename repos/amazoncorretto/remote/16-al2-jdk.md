## `amazoncorretto:16-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:4cd70fd46abfe11986e9810deac8a85d7614e8c91f70d9922f84deb096233d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:16-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:69884e8bc35a198faabc5262618b9fc5c03ac85801fe1261d032e5e9555cec66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221944577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afa07247b4363f02d16639253c650aac54a145fa4cca1abfaf03522fe98692e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Mon, 26 Jul 2021 18:19:40 GMT
ARG version=16.0.2.7-1
# Mon, 26 Jul 2021 18:20:02 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Jul 2021 18:20:03 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:20:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aed8a232bf7a40fe973a4cd182928ebe6b7e9c09023452fcf7803138da37056`  
		Last Modified: Mon, 26 Jul 2021 18:21:41 GMT  
		Size: 160.0 MB (159978571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:16-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d81b411e5a1d7d53ae526b7c6b3750f9b033ff799a640db9e5d5aabdac819aed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223510361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21a773d1f1432117d9f554a7f2a5ec59987d64426e5a151da5c4012e86546f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Mon, 26 Jul 2021 17:39:46 GMT
ARG version=16.0.2.7-1
# Mon, 26 Jul 2021 17:40:14 GMT
# ARGS: version=16.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-16-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-16-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Jul 2021 17:40:14 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 17:40:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-16-amazon-corretto
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d6c00fa286044c267ce902d9051a1210ba685bdeb2e004a2325ab4b854a22e`  
		Last Modified: Mon, 26 Jul 2021 17:41:26 GMT  
		Size: 159.9 MB (159942469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
