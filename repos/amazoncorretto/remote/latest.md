## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:11fafa4a4148a23a0497ef61baed59a91f5dce812719af3903e55f4e09bad72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4034dbb585394a137c0d62c48aba0fc09c6b35e4e3f77901e09f19d0a9592b47
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137766199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33aa6dcd64873ad321c6ce752aff9043ecd807b6e7566f86db2b125b366a5ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Feb 2022 23:40:28 GMT
ADD file:871c80292a1347a65a30c9d2cd343d927528a61b8d89fd82f268d5f8ad4d2944 in / 
# Fri, 04 Feb 2022 23:40:29 GMT
CMD ["/bin/bash"]
# Sat, 05 Feb 2022 06:31:46 GMT
ARG version=1.8.0_322.b06-2
# Sat, 05 Feb 2022 06:32:08 GMT
# ARGS: version=1.8.0_322.b06-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 05 Feb 2022 06:32:08 GMT
ENV LANG=C.UTF-8
# Sat, 05 Feb 2022 06:32:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f964900200fc1f8473ac70d9da14cde8bae251ffb4a8f4792e2bf9baf6aaac70`  
		Last Modified: Thu, 27 Jan 2022 23:12:55 GMT  
		Size: 62.2 MB (62237845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c511bfbb086d471fd10312fbd7190d4f5902a7df9c2f19280978c05740db52`  
		Last Modified: Sat, 05 Feb 2022 06:35:18 GMT  
		Size: 75.5 MB (75528354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a7b1c5aba8057c924f437fac0d2b002ca7e0476c999234530f1b58a87daa8bf2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123421479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8738f4ccea9e50ed697afaafc5add490eceedb20f07d0b5c9a7fbb7068a7c429`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 04 Feb 2022 21:33:28 GMT
ADD file:38bb92c68a8a2ac1145ea8d422911f6f0d9c62cccc02b3bdeda096047efecef5 in / 
# Fri, 04 Feb 2022 21:33:29 GMT
CMD ["/bin/bash"]
# Sat, 05 Feb 2022 00:10:58 GMT
ARG version=1.8.0_322.b06-2
# Sat, 05 Feb 2022 00:11:09 GMT
# ARGS: version=1.8.0_322.b06-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 05 Feb 2022 00:11:09 GMT
ENV LANG=C.UTF-8
# Sat, 05 Feb 2022 00:11:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:591d91c97b5df29e14efc53ca38020094df8fa114d32d412bb8f02344aad2411`  
		Last Modified: Fri, 28 Jan 2022 02:04:32 GMT  
		Size: 63.9 MB (63857619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7db63499db48a06e4b13ea1dca78abe8aa53b85e767338723238309e80eb28`  
		Last Modified: Sat, 05 Feb 2022 00:12:46 GMT  
		Size: 59.6 MB (59563860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
