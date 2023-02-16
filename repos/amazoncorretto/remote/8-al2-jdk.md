## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:8819fccb4347e559d1e2c82a48f8940059b871d6fd1b0775a3844c67de366eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a413f6ddb79223492772a157a1ef134c955681eb12a6b78ca2220647ffd37a18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137951258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96a3ed3b5155939458b795f42ec783364a7a4c6f125fbd700705aec902c9828`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 21:20:09 GMT
ADD file:29cd40b7c56d98385ece53bcbadfefd25bc70ccf0326777986ef6a5720bdfe83 in / 
# Thu, 16 Feb 2023 21:20:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:38:58 GMT
ARG version=1.8.0_362.b08-1
# Thu, 16 Feb 2023 21:39:19 GMT
# ARGS: version=1.8.0_362.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 16 Feb 2023 21:39:19 GMT
ENV LANG=C.UTF-8
# Thu, 16 Feb 2023 21:39:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:d78505e615251c4f4af6eaa9507b67917d263d23551dcc5a1eed3c012d32a54d`  
		Last Modified: Wed, 15 Feb 2023 00:09:42 GMT  
		Size: 62.4 MB (62386320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f241d723942436595a2e7f4af6ad658e8b35a0509301fffb0f60de1e1d84c78`  
		Last Modified: Thu, 16 Feb 2023 21:43:37 GMT  
		Size: 75.6 MB (75564938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e4523d4406813e19385b46ba08823793d19862b7353ab3579b98de5fbed93a67
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123610754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779d6f7ee6b684e61009fbb75afe43ae373de9020f84a53ad3aeab225e9854e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Feb 2023 20:39:31 GMT
ADD file:17574026c2754afa903450c59a6d8f7d0905209b174cbe9c13252a61d5a6f916 in / 
# Thu, 16 Feb 2023 20:39:31 GMT
CMD ["/bin/bash"]
# Thu, 16 Feb 2023 21:05:26 GMT
ARG version=1.8.0_362.b08-1
# Thu, 16 Feb 2023 21:05:42 GMT
# ARGS: version=1.8.0_362.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 16 Feb 2023 21:05:43 GMT
ENV LANG=C.UTF-8
# Thu, 16 Feb 2023 21:05:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:71343c2791199c6e2c19c308cff6493497a02f57e225c11405e1934dc7428b3c`  
		Last Modified: Wed, 15 Feb 2023 03:16:17 GMT  
		Size: 64.0 MB (64003805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b9a0290cddf3ca6685e4cb9dc1139d87ec575d77a85f10794f976ef6927cab`  
		Last Modified: Thu, 16 Feb 2023 21:07:56 GMT  
		Size: 59.6 MB (59606949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
