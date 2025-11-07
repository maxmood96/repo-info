## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:1fde0b897adae564d57db14bd9d0aa7bc7372f2154fef8abe989cac3a16768f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eac32d36bb024d5e61cc35faca6f335167085ec1bed650671a29c00ddebc6eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (210978887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e6f74c625bf46ff85ec08f852dc2d38b95868344b73389587b310866032f8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:11:43 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 22:11:43 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:11:43 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:11:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d698af529dfc04b48b4625b22e044bbbbde679eaff562a9eac50396c1bb0c1b7`  
		Last Modified: Thu, 06 Nov 2025 23:13:03 GMT  
		Size: 148.0 MB (148044753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:006bf294e482df50fb8c44672496844f296ab0b857ce619e6da22c53f9be0e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e11b832ae4448967a889cdc77c9d31d0fd84c424e0551628798c898860b1ef`

```dockerfile
```

-	Layers:
	-	`sha256:62ede8f6618e32dcb13c1db80d669e40c9e30b783ac44690d1075b78158c1a29`  
		Last Modified: Fri, 07 Nov 2025 00:16:41 GMT  
		Size: 5.5 MB (5543005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4354c4302c01d77e43c8a7e3dd33b53055f25fdfaddb76ad35835c85c50ea7e`  
		Last Modified: Fri, 07 Nov 2025 00:16:42 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e7259369b015844de3876884a0ad97996aa606675051dbb3cc86e89a0ae468d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209937803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e637623d44cd58aea21f48eeda908c826952001bd3467238e8b3f05ffccdc3fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:09 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 22:13:09 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:13:09 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b3dbbf9942d831705af842b5b4d8637f885aef547dbffbb26a5f48f413b10f`  
		Last Modified: Thu, 06 Nov 2025 23:11:18 GMT  
		Size: 145.1 MB (145144507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ed984101a4926d0e8a9bcaf59d7f46d4c5d780604044110328d688f9db81c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb1cf8c3e217c0550c088dac0eb13e88a35bf5b421b529a039d60c15f108e8d`

```dockerfile
```

-	Layers:
	-	`sha256:fe08a4de26a9cfd8bfd90b01e4f17dfc2b947c4856fd1768d3104bb8f72d7e25`  
		Last Modified: Fri, 07 Nov 2025 00:16:39 GMT  
		Size: 5.5 MB (5542499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bac8588ab6ce106e32455c47afb3bc9120c94d5d8b7356ae500c04d408f5f4b`  
		Last Modified: Fri, 07 Nov 2025 00:16:40 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
