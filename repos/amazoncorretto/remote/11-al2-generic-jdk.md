## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:b35cc4ce22e19da98991fca8e0049c8cbe47a83e93899a287846075211b3f3e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:66746cf40b67b92650c5d809f8660ff06b32c25144c5ddb002a891f143ed53b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211073691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3f13e849987212231ed744a35141299ffa898cb24c655b06c87e709851a7e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:24:12 GMT
ARG version=11.0.30.7-1
# Wed, 15 Apr 2026 21:24:12 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:24:12 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:24:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f889f80a08d9942d941775fa5fbd5062ab478854872f8451cf918fafd8783a`  
		Last Modified: Wed, 15 Apr 2026 21:24:32 GMT  
		Size: 148.1 MB (148118425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ea4ebc727085c647d825513ef56138c5153eebdc0836f09c7f72e66cffbb64b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e6e0a29cea912eba1e74b07ce7a53a604c71413ab7e14c460fb2232b399bd4`

```dockerfile
```

-	Layers:
	-	`sha256:fa9727399e84cf72420c7af8a9f35e31d7db1b3537a5d1b7f3ae5c0a7f455ece`  
		Last Modified: Wed, 15 Apr 2026 21:24:28 GMT  
		Size: 5.5 MB (5543106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f61a3a3bd7d238a632e5ffca69fda12e0dc484f6762fefb506b955aa63b7225`  
		Last Modified: Wed, 15 Apr 2026 21:24:28 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:53807f39f1fabe93cbfe2c09458af349485e8f5fb714beea018acd2bfc56dd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210022070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bb6185c0998e845a4535f21082992d5bee7d834cbbc3edb33761799861bf1e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:14 GMT
ARG version=11.0.30.7-1
# Wed, 15 Apr 2026 21:38:14 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 15 Apr 2026 21:38:14 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc41dd512eba15547765998d4e676ad13bd0561b820ba3e5ed260f3d81ec292`  
		Last Modified: Wed, 15 Apr 2026 21:38:34 GMT  
		Size: 145.2 MB (145219095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e9cb5cc0501961c42e459e2c42eabd68a8cd2cf0f80690dda6c163530a5e286f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33e1dcc3174b38ffcb4238dfb9814bc342e3f54e86f9829463ce35668dff35c`

```dockerfile
```

-	Layers:
	-	`sha256:aecd210da6083c9bfd6ea67c0c4bd7c7403fe570f7d8d24c1dc960c32a160c02`  
		Last Modified: Wed, 15 Apr 2026 21:38:31 GMT  
		Size: 5.5 MB (5542600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf348e5e08f132e50ef70de7b9e14e9f01b969240997c83407c456043a8d6bb6`  
		Last Modified: Wed, 15 Apr 2026 21:38:31 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
