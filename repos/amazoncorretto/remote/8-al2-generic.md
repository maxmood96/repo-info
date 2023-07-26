## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:3cdbfb35ad741f6430729aa8160422a32381598e7b56f1b6c48c81f735dc147d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:873581f1948ba337352b399d2efe797df5789be667c4013328aae8944bf00412
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138005572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466800abe3a2aab9133c373d04b503bd4d82ea9fbe64df36affbbc5c88ea3e98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:31 GMT
COPY dir:eb203b2e14f406c161ffae3b2fa7ec59db3f5a04437b6e040395c2bc34835c5f in / 
# Wed, 26 Jul 2023 19:20:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:12:48 GMT
ARG version=1.8.0_382.b05-1
# Wed, 26 Jul 2023 20:13:09 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:13:10 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:13:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a8d554425610d474f28e23ecfc3224dd78fca045a5c09515dbf51a8606c33d8f`  
		Last Modified: Tue, 25 Jul 2023 11:25:06 GMT  
		Size: 62.5 MB (62451920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2636316b868c613e3e0627c33426925c0ca079e846226d77acaea1b8cf2ba371`  
		Last Modified: Wed, 26 Jul 2023 20:24:44 GMT  
		Size: 75.6 MB (75553652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:60f67d3dbd3f6fbf81e1fd5c2c03b9e5f32ef5ff1efc8236b9c5f35fb6f04219
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123751156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ffa537c6de8f4fc32cac4c9e8345aeaa70adc349d05f69db0201ab2effb568`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:39:59 GMT
COPY dir:680654fa7b59b44a83c6e6e3392ca226b5dd93f22761e5f1147351db4c3466cc in / 
# Wed, 26 Jul 2023 19:40:00 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:17:32 GMT
ARG version=1.8.0_382.b05-1
# Wed, 26 Jul 2023 20:17:49 GMT
# ARGS: version=1.8.0_382.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:17:50 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:17:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:51a637e5b43ccbed5bec2958dc012693f30cc3c6b3a2760e6d675bedbae44e84`  
		Last Modified: Wed, 26 Jul 2023 19:40:35 GMT  
		Size: 64.1 MB (64129279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e978b8a8f022b0f5f01d1e6940d9246186e58075ae0443ee3a348a7bfd8b8c`  
		Last Modified: Wed, 26 Jul 2023 20:26:14 GMT  
		Size: 59.6 MB (59621877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
