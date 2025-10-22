## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:11c58d0104bcd4acc3e100b4170ba99d68990211fbb868f17289c17c8a3a8851
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2ee4eb1c53d4beee2056bfd4268dd95b41e99c2da4009e793eb8f47fd9a1b50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78006143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a599e715fc2c129254a7824ace50bce7d25d44060acc753844f0b596a221b037`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 21 Oct 2025 21:30:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bd7fa4dc6ccbeecb97ee29892a3a21f75d104d5982e0db824a81dc43003d64`  
		Last Modified: Wed, 22 Oct 2025 02:45:26 GMT  
		Size: 48.5 MB (48469325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1e7f4e30d3c759bcce07a60956803dfaaa589634f1dca418f38758261398be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c419eb4a4433658b1944423016d6f0af6d905e1681fd2ffd43ed8d89160048a`

```dockerfile
```

-	Layers:
	-	`sha256:7000c292ef891dad2621faa88879c9f3f6fcf04d9b8e7f1c113ed6ee7ab653c6`  
		Last Modified: Wed, 22 Oct 2025 06:04:58 GMT  
		Size: 2.3 MB (2299106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6473828633095788beac4da66e65dc729fd4c280e9d9c1d3ad3f3cd6c566d361`  
		Last Modified: Wed, 22 Oct 2025 06:04:59 GMT  
		Size: 8.9 KB (8928 bytes)  
		MIME: application/vnd.in-toto+json
