## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:1eeddfebad12cf17f02c2137fde4c8ba984a1ca3cf4c4375e59759cde3c8f9c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:953658250582004c1c7e4e81fc6fe447c37fdcbcde878ebef80e01730585f47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210990100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ba50a3eb428440adb964d73c07d936d03625c85e1aabe9872460af2e64452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=11.0.26.4-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279e4a4cbef7e00688d7451b377129431dee56917079ed641c490558f3d924c3`  
		Last Modified: Thu, 27 Mar 2025 23:58:33 GMT  
		Size: 148.2 MB (148237211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:66a042f9b890b3eb2110725a7efa8b0586856bc649aba26db7863677e9b06230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d08c2ab5638c5be8f741db5f0a8a820c3012cbaec24995e24c8d381a90ec36`

```dockerfile
```

-	Layers:
	-	`sha256:1148041c043efb8bef151a40ac38e7588501e70e58483b0235e7cd35a9b2a907`  
		Last Modified: Thu, 27 Mar 2025 23:58:30 GMT  
		Size: 5.5 MB (5524415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9372cfdcde35a3385b3ad6f422c7d44f18835f31ad37ba41b6fa51d0c6eb6921`  
		Last Modified: Thu, 27 Mar 2025 23:58:30 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1202613e7bca9203d69ba33fa2482cef27ed0e7fcf4991143c738473e9e401ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209859027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3476bd4126420941396d7e6aca180ddd163d4cc016694d3b652788c029d3d90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=11.0.26.4-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7e5adfcb78d2aa013a85846125ae796bd1e3982b60f36fdb457a186c83dddb`  
		Last Modified: Fri, 28 Mar 2025 00:07:57 GMT  
		Size: 145.3 MB (145293205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:30296aebb4dd75e0dee94f337f6e394bb8d3a344df3699edbdc004d82a076123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90e8800d2d5f884c9b4814f5f2837a126206dbd56b7100c462ecd986fa4a7dd`

```dockerfile
```

-	Layers:
	-	`sha256:df13db0b91b8a994bfe7e17e94f30fc8d506b084d1f6bbb1fab8f8cbc50f4f90`  
		Last Modified: Fri, 28 Mar 2025 00:07:53 GMT  
		Size: 5.5 MB (5523909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fc53d7645bcc2e119d87dde1928428b9548cf55de17058ca38bb950bcd838d`  
		Last Modified: Fri, 28 Mar 2025 00:07:52 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
