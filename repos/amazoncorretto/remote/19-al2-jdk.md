## `amazoncorretto:19-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:fdab704eaeb551a302b014bfd3711d09abff5295aa854991525dbb42d49c1ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:19-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:81d0df4412140416b27211c999e1f3c4565ae89a5cd92889475d20af422ba507
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221694415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e149b4ee28ea337c3323eec2e133b89d51e7946dfad701c71aa44e26364e46b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Oct 2022 00:19:49 GMT
ADD file:33ce740675602f8911c110c617b08d74ebe9c26c82226b4815019d8c2d0a2263 in / 
# Fri, 21 Oct 2022 00:19:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 01:10:48 GMT
ARG version=19.0.1.10-1
# Fri, 21 Oct 2022 01:11:13 GMT
# ARGS: version=19.0.1.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 21 Oct 2022 01:11:13 GMT
ENV LANG=C.UTF-8
# Fri, 21 Oct 2022 01:11:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:e3cfe889ce0a44ace07ec174bd2a7e9022e493956fba0069812a53f81a6040e2`  
		Last Modified: Wed, 19 Oct 2022 18:11:43 GMT  
		Size: 62.3 MB (62306642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf6c501567b9864d5477f3bb4e798e53137c8a50576fa5bba6ccbb83c2d6faa`  
		Last Modified: Fri, 21 Oct 2022 01:16:26 GMT  
		Size: 159.4 MB (159387773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:19-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:435df6e8205525ded484754d3e0609ba40989e1920dca0fdd07e159b8a08645d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221743888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8894b4b289ee1430cb49516e15cfa87d7672564230f49bde73c0b213247eca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Oct 2022 15:27:06 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Wed, 26 Oct 2022 15:27:06 GMT
CMD ["/bin/bash"]
# Wed, 26 Oct 2022 18:56:09 GMT
ARG version=19.0.1.10-1
# Wed, 26 Oct 2022 18:56:32 GMT
# ARGS: version=19.0.1.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Oct 2022 18:56:34 GMT
ENV LANG=C.UTF-8
# Wed, 26 Oct 2022 18:56:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e48d5af71f1011c2a195007b5e77fe27cdf006eac9b0fe3b573d468ce6e7e0`  
		Last Modified: Wed, 26 Oct 2022 18:58:31 GMT  
		Size: 157.8 MB (157824019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
