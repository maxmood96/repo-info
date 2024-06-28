## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:6df2ba8db69944efc312e2e11d55a374e30fcc539aeeac5134d0d64a90febae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2effe982f2176fd368992017ad1ce537b6902c332d12f4c7007d27e9d9a8d025
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214791522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5d2bbcf3e2e37233e6de19d958e7c4182e53bc8daa002832750e8c1c2a5573`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:55 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Fri, 28 Jun 2024 00:19:56 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 01:10:12 GMT
ARG version=17.0.11.9-1
# Fri, 28 Jun 2024 01:10:37 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 28 Jun 2024 01:10:38 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:10:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e034acdf66e3297a49cf63d7d0b9ab75bbc1b44c38ab12befb2dd66d3c21de5`  
		Last Modified: Fri, 28 Jun 2024 01:23:30 GMT  
		Size: 152.1 MB (152144884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2d0e34d0a79bdedb0be9c2f1a842173928cad31c504fb1634ecdbc02671ff45b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215358958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb001fe2a6a29f1856815d49353f7f0a323e8873a1b27549a4a8eaf32b90845`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:40:02 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Fri, 28 Jun 2024 00:40:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 01:18:18 GMT
ARG version=17.0.11.9-1
# Fri, 28 Jun 2024 01:18:37 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 28 Jun 2024 01:18:38 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:18:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a5400ea07504e79bc0fc093c0447820e98babd760b87a6024f8b58349c8a68`  
		Last Modified: Fri, 28 Jun 2024 01:28:50 GMT  
		Size: 150.8 MB (150790193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
