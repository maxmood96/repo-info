## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:928dae49555fe75eccbfced18f2727e055387941c82a6f14abfcaf6281c436bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6edcb0831b29456a8410d5d62fe07ca128551a2d73750184f1a76939df3a5496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215358041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493d3bdf200db74cd2d1d21b0d0df60bbf50ffc1462ca65602295f9aa5731621`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed5eb262f0b7dfe71c1c0fc62fc5d0f8b4f6b25e17d18c45cdecf03ed463633`  
		Last Modified: Wed, 22 Oct 2025 00:50:00 GMT  
		Size: 152.4 MB (152417421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:95e73dca31fdf1eb1542a3be020bb7cd239ac8e23dfcc542b7d3ed3f91adcdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33722d01b314156c4f615d1b55e85e13308cfd15646581706763e660343e74f4`

```dockerfile
```

-	Layers:
	-	`sha256:db0df84ff542090b8ea89a376fda449207040c85038a001ce2eec4468dc90ef1`  
		Last Modified: Wed, 22 Oct 2025 00:49:20 GMT  
		Size: 5.5 MB (5535704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1c727eab642e7843ff826a61787b92f89bd99e1e9a9e423e0504bcc530a59dc`  
		Last Modified: Wed, 22 Oct 2025 00:49:21 GMT  
		Size: 11.3 KB (11256 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:319c3f15a6edbfe6f4148e5cff705dcd715dfc6c4f74dfb305e8bbe9ad0a6648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215781147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9425f62eeea52115a3047f821c8a04c100f920fd35d23f051afa0f2152d6c0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd285a6ccc0f7574660524adabe694c5ee580549dd27eb3a1add6f7d397deb5`  
		Last Modified: Tue, 21 Oct 2025 22:13:33 GMT  
		Size: 151.0 MB (150987939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0924547345b1f3402d256acec3d0163d103893b38eb9d4200ac5000476516b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fe764f4d98066558f43aafba0ff37106338249c2f6ee32d6f04c14c834465c`

```dockerfile
```

-	Layers:
	-	`sha256:a38b9e8f2766c321d59b543cc4f9c12fcf0935bd01c612947649c318f5c8dd40`  
		Last Modified: Tue, 21 Oct 2025 23:17:28 GMT  
		Size: 5.5 MB (5534393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7c541768bca302705bb143d23a9c71f0a48e5aa9c09b7217353a0852533b3b`  
		Last Modified: Tue, 21 Oct 2025 23:17:29 GMT  
		Size: 11.4 KB (11408 bytes)  
		MIME: application/vnd.in-toto+json
