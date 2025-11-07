## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:e78655f68688b69195ab5e0c528ba607a3e55e2fc9e356bb009dca5f6737a0d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:326fb001683a2f17a199922632ab29691eb4938ced875ea3782b4ac024caccc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228420084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76e23fb7f8c354d41053b0654cce82a76bb4a0e3ba8e58fec6457070defc297`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:15:05 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:15:05 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:15:05 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:15:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b6e807c1a7c53af4ccdd4780bf792c6494ade14902f1c503d47c104f25cfd`  
		Last Modified: Thu, 06 Nov 2025 23:11:15 GMT  
		Size: 165.5 MB (165485950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f5fa944b0d535910675e22f7142e7fd893b7e54cebbbe81effe28337498ffcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e27a00848493372f6e9ace7ef260e2ba7bbd399a33fd1e8c7c0fae546e19da`

```dockerfile
```

-	Layers:
	-	`sha256:e3327acc7928608f534a712c706c33aa296b457563ed9523b6aabcb0d781e76d`  
		Last Modified: Fri, 07 Nov 2025 00:16:11 GMT  
		Size: 5.5 MB (5535595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4695e054f57759839c374900618b5cdaccdeb5ec91bc6c496991cbf8d68a470`  
		Last Modified: Fri, 07 Nov 2025 00:16:12 GMT  
		Size: 11.2 KB (11206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f41484855da42398042087c4c5bb1483798fadb2a6e55b31998f6649feb11a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228376255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a5f1067b1b7c6e31d34394c1820c0361a6cd91d3c1d62b9b153b520be47ac9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:08 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:14:08 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:14:08 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50fcdfedf41173aea97496be730854d377fdf96be58c639f421a2d1bff774e7`  
		Last Modified: Thu, 06 Nov 2025 23:13:01 GMT  
		Size: 163.6 MB (163582959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:141273cf4e25b08c699a2bf8498662833dc313836851e2a5c662abb57acdfaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d323ba67fde5dcd440921f157ff4b7ab8315e4f622286f8f93c218f8f31132`

```dockerfile
```

-	Layers:
	-	`sha256:2ebe05deb5e92c47571f264ce09f40bdec5efc50858523f66f8656f429f593ff`  
		Last Modified: Fri, 07 Nov 2025 00:16:14 GMT  
		Size: 5.5 MB (5534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8e4340f015321023066b07d2ecf5827b3193c5dd686b44cba99ff282d9611a`  
		Last Modified: Fri, 07 Nov 2025 00:16:15 GMT  
		Size: 11.4 KB (11358 bytes)  
		MIME: application/vnd.in-toto+json
