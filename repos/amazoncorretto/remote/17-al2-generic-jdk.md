## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:7bb172db13c913818adf869991dafb636f86668e71c6d921c9f1184638e5e603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f9fd23a2fb9c78de9722bfd95e35dc7098f78493bc2a7cf33f160c3651994f57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214455645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751302ba469679688ea5ac04d02c44a589aa98927961dc2f9650e586267a2bce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 22:20:15 GMT
COPY dir:129c77392b447afbaa234a34f434bed5ec790278efd165e1d59d4425216de49b in / 
# Tue, 20 Jun 2023 22:20:16 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 22:55:38 GMT
ARG version=17.0.7.7-1
# Tue, 20 Jun 2023 22:56:03 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Jun 2023 22:56:04 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jun 2023 22:56:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0086aac11276884f299f6c13a98f93369cc50f7c0518989c2d4a29dd999feb70`  
		Last Modified: Fri, 16 Jun 2023 00:07:41 GMT  
		Size: 62.5 MB (62487611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63560138ab92e35f069c08d4c0c90d11daf6f7600a77676c4ae84382c0ca5e6`  
		Last Modified: Tue, 20 Jun 2023 23:01:52 GMT  
		Size: 152.0 MB (151968034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:49e11026931381516e9c73cc4b5b827538d79c7c60bdd7eea56621ee6bcad8dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214614954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98045e2cd1b6c996108bb495f87addb71b71fb201cfbd96ee6f83f7f7820f670`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 22:40:04 GMT
COPY dir:ff562af1eb403156d540f974a5832a6973c9f08f4a181bdb7b2f5a2faf708d9c in / 
# Tue, 20 Jun 2023 22:40:05 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 23:24:47 GMT
ARG version=17.0.7.7-1
# Tue, 20 Jun 2023 23:25:05 GMT
# ARGS: version=17.0.7.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Jun 2023 23:25:07 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jun 2023 23:25:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:322949bc3f462f25edd57d234e2687af2a359a973c83b2d139df37b10dda65be`  
		Last Modified: Fri, 16 Jun 2023 18:06:42 GMT  
		Size: 64.1 MB (64129772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa245e3dd0fe029babd214df2ded379eaca3979400936b10453d93b7721ab5f`  
		Last Modified: Tue, 20 Jun 2023 23:30:04 GMT  
		Size: 150.5 MB (150485182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
