## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:39fdd3df2e3bb6d439b52bbd8bd2a0b7a48fcc342e327d2b56c56a7bd9b4da6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e510b06bc0f66bf890f222912d126625cacb7e2b3150c6cc2491bd71c79dd2a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210238963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec845192da97b742ea5dbe2fde4ea51d0bbbe00fad269200750f4b1dfafbbd46`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:31 GMT
COPY dir:eb203b2e14f406c161ffae3b2fa7ec59db3f5a04437b6e040395c2bc34835c5f in / 
# Wed, 26 Jul 2023 19:20:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:15:50 GMT
ARG version=11.0.20.8-1
# Wed, 26 Jul 2023 20:16:14 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:16:15 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:16:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a8d554425610d474f28e23ecfc3224dd78fca045a5c09515dbf51a8606c33d8f`  
		Last Modified: Tue, 25 Jul 2023 11:25:06 GMT  
		Size: 62.5 MB (62451920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e9a45c51abe09a7f25455b6e5379965f9937355361f9760bfad7aa1ff4ba6`  
		Last Modified: Wed, 26 Jul 2023 20:26:58 GMT  
		Size: 147.8 MB (147787043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:777a6ace5a3c1e457dbc730b432de7f7854a0165183edd0573bbc3da727ed746
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.1 MB (209059222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43adbbfd1806eacce5347b10eaddf875ca6d06e3910560e32998c46a7c794cf2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:39:59 GMT
COPY dir:680654fa7b59b44a83c6e6e3392ca226b5dd93f22761e5f1147351db4c3466cc in / 
# Wed, 26 Jul 2023 19:40:00 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:19:03 GMT
ARG version=11.0.20.8-1
# Wed, 26 Jul 2023 20:19:23 GMT
# ARGS: version=11.0.20.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 26 Jul 2023 20:19:25 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:19:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:51a637e5b43ccbed5bec2958dc012693f30cc3c6b3a2760e6d675bedbae44e84`  
		Last Modified: Wed, 26 Jul 2023 19:40:35 GMT  
		Size: 64.1 MB (64129279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17b5eebd6c82ddcb88fa2d048cb3b49d0a6d35f016831171e8f5ef11022d8c`  
		Last Modified: Wed, 26 Jul 2023 20:27:49 GMT  
		Size: 144.9 MB (144929943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
