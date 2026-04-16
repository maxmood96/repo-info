## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:87a4410a43458bc6a31158c30bc7f270cbfb505795f3d8be400931197b9e8834
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:28cd7ca013933ff957bb3af89e11b0eba7069b0e32afa880573670df0d791e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139093532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd1ad1441f3dbb1c65b61825fc0c2575e9b7808becbf9e5d451ba20e936a427`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:23:31 GMT
ARG version=1.8.0_482.b08-1
# Wed, 15 Apr 2026 21:23:31 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:23:31 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:23:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcd204687eefedb33c241ec5266d9946073183cbac96ddfea7fde194955efd8`  
		Last Modified: Wed, 15 Apr 2026 21:23:48 GMT  
		Size: 76.1 MB (76138266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5678cc42e5e7d18dcf9dadb39dd854d1795d5c6d3c3e4659cb490eb227267752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4899e687ed498df7ee282792bb799d58fbc9c2d13232626cbd28bc2f889467bd`

```dockerfile
```

-	Layers:
	-	`sha256:6b75b2a5a03014e912599f56ebaef6d7b37aff46c282269338eb96745dff33c2`  
		Last Modified: Wed, 15 Apr 2026 21:23:45 GMT  
		Size: 5.4 MB (5377455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0e72dfa7131de16a3f8834c58e2d710aa3c01b7e5857b0dd29bec5c01b1204`  
		Last Modified: Wed, 15 Apr 2026 21:23:45 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c9612ddf9638c7544d4087dec5dc572b899468425ce13f30543d647c50dc32cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124732545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7346d1f6ae59c6e26d8c43721bca3b0a4f35b4af601e7bdffdbc88bf2d8740`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:37:52 GMT
ARG version=1.8.0_482.b08-1
# Wed, 15 Apr 2026 21:37:52 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:37:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:37:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64e0762b89b01c2723358ff571ebad5cc6c2cb0a038287e362b26432dea9e9e`  
		Last Modified: Wed, 15 Apr 2026 21:38:07 GMT  
		Size: 59.9 MB (59929570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48b1689eb5d4486b949528f6fa9cfb7db8a89efc6787eeb5f355e07566a71bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572a851142ee09fbf218d1e22cf96b7c552934864281927d91ca62012086426e`

```dockerfile
```

-	Layers:
	-	`sha256:9dbbabfbe94ee38ab1bdaad32b5a7316513ef31209cc486934dd3d713352f630`  
		Last Modified: Wed, 15 Apr 2026 21:38:05 GMT  
		Size: 5.4 MB (5355954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb06c4d6d30833b294e66a14269e1f017bf0ea45ea13623da653b9b2544084aa`  
		Last Modified: Wed, 15 Apr 2026 21:38:05 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
