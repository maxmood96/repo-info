## `amazoncorretto:20-al2-generic`

```console
$ docker pull amazoncorretto@sha256:796b6cf8e4244a422261b6d59e0cfb80e5ba55a25e8484d69f4f962710b9e855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:62a06b483db4c7a7d4d1fc37843fc12d6681d2af147b1cdd88ac957e1e7870ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223250837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b766ed728338578bd5539a307af2450f7d3465dce3aac7fdf0a0a56d811fbd7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 22:20:15 GMT
COPY dir:129c77392b447afbaa234a34f434bed5ec790278efd165e1d59d4425216de49b in / 
# Tue, 20 Jun 2023 22:20:16 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 22:57:14 GMT
ARG version=20.0.1.9-1
# Tue, 20 Jun 2023 22:57:37 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Jun 2023 22:57:38 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jun 2023 22:57:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:0086aac11276884f299f6c13a98f93369cc50f7c0518989c2d4a29dd999feb70`  
		Last Modified: Fri, 16 Jun 2023 00:07:41 GMT  
		Size: 62.5 MB (62487611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a67431843d9e5854a588042bb3ab1dea757eb095a929ea60bef489fc4f13e9`  
		Last Modified: Tue, 20 Jun 2023 23:03:25 GMT  
		Size: 160.8 MB (160763226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4258f4c708b37467fd50e8ee25b5fe768dc1a044d21c3c12e170942a0a6f88f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222924774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a864573b9bec636589396b4db45719e68b61f0cb57005e673229780e7375aa3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 22:40:04 GMT
COPY dir:ff562af1eb403156d540f974a5832a6973c9f08f4a181bdb7b2f5a2faf708d9c in / 
# Tue, 20 Jun 2023 22:40:05 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 23:26:12 GMT
ARG version=20.0.1.9-1
# Tue, 20 Jun 2023 23:26:33 GMT
# ARGS: version=20.0.1.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Jun 2023 23:26:35 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jun 2023 23:26:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:322949bc3f462f25edd57d234e2687af2a359a973c83b2d139df37b10dda65be`  
		Last Modified: Fri, 16 Jun 2023 18:06:42 GMT  
		Size: 64.1 MB (64129772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ce14cd66ceb90d76b657ab4ad5fb1fd02f1c4c50a40c9cb0adc1f8e0f57ba4`  
		Last Modified: Tue, 20 Jun 2023 23:31:26 GMT  
		Size: 158.8 MB (158795002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
