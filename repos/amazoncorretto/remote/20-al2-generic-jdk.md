## `amazoncorretto:20-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:f27ac5d918485ac2155a01f1ac57acd4abd6f45c175adce258c90aff4f644859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3bd9bb8e218d811c04a3326ed025a7c3375f1dcbba8318baf4203f92f9ac043f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223408900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971c424ca0e36ad95ce868bbd62cfd325a3f19f09ec1d25dfdaf8e8702195419`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:22 GMT
COPY dir:591ada5c2fb65633b614a3ff732e6d83dcd91fe9ae925844fe9ba3323311bf74 in / 
# Tue, 29 Aug 2023 18:29:23 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 22:31:18 GMT
ARG version=20.0.2.10-1
# Fri, 08 Sep 2023 22:31:42 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 08 Sep 2023 22:31:43 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 22:31:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:8be3d01330d7e2e197495d440aa60d14ac366aad5e8d105d86e384876aefec18`  
		Last Modified: Fri, 25 Aug 2023 08:53:43 GMT  
		Size: 62.5 MB (62477278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be5205d9d6236e8e3cc95350c979247d9690ffa7bbcdcc32aa2b239a93d61a0`  
		Last Modified: Fri, 08 Sep 2023 22:43:00 GMT  
		Size: 160.9 MB (160931622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:97ef2df609be9747c08d32a73fe9d3e9cb9d793d18a575b7a40fc52cebc8c268
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223108556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8407822b932a5a8241b35cd799e361c5c130c0d44eac6e2a1c445f876a584dce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Sep 2023 21:49:00 GMT
ARG version=20.0.2.10-1
# Fri, 08 Sep 2023 21:49:19 GMT
# ARGS: version=20.0.2.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-20-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-20-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 08 Sep 2023 21:49:21 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 21:49:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-20-amazon-corretto
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfeec415054b3c0ca27e274cbaaee77fd04aeb29008107750f91b08432d9640`  
		Last Modified: Fri, 08 Sep 2023 21:59:33 GMT  
		Size: 159.0 MB (158978562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
