## `sapmachine:lts-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:978493d1b44ca0e8f43cf776beec6e0cdc670b37f935a1df75ab4229e03ee0f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:be51c24590e78c34465d7a1beea9e5b802b338ecd6bbf291dcc4929aac9635ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89270981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be976605836910c8e85f29794e301ce50a75df8789a131836c685959de7d45f0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8510b6b6bc5b448b940b22d4853ed9d1f845c73f9a4c1fee313451ad48f686e`  
		Last Modified: Tue, 03 Jun 2025 04:17:34 GMT  
		Size: 59.7 MB (59737978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:870cf380fca9f1c9daada2c5d1426621881b7ae6d2a3692752bae33e99f69ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2445186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faab99a7a481773148db9f35d24caaf12aee37a6a4f819514fab2571bc202af`

```dockerfile
```

-	Layers:
	-	`sha256:cc8fab341436abf14c3c18e5a3f3fedd74b12d636ff7aa0cfd5ed6a13d94c647`  
		Last Modified: Tue, 03 Jun 2025 04:17:33 GMT  
		Size: 2.4 MB (2435706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b702a272a359ab4be2c68cc87cb2a35f7102c3325caa4ea4ed975a152c1b879`  
		Last Modified: Tue, 03 Jun 2025 04:17:33 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:44a387161852466b8bac0aecb39d2d3a0153ce4322daeab58e15a80599023c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86222424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282f628a2be4a7320d75e4839a87674dbf9082fbe4e800781c2109d61cce2f1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Fri, 30 May 2025 23:34:51 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934576aecd4287bcd976be469757084901f2423aa57a4aad9ef84a92409adfa6`  
		Last Modified: Tue, 03 Jun 2025 06:07:16 GMT  
		Size: 58.9 MB (58866843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e13467b104d2c2fffdfdecee2579af32abd97f790cc095089a3dfc639b600e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2445020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c183e22a32aed5f07106ffd20b1c8fab900424514e76580ef95a50883264c71c`

```dockerfile
```

-	Layers:
	-	`sha256:48b66ef7be246b9520d01d95f9352431ab6bd78343c4c4fc963c3ef4d351b482`  
		Last Modified: Tue, 03 Jun 2025 06:07:15 GMT  
		Size: 2.4 MB (2435412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:560d1256b490d06edb461a11cfe73cc769ddacf017226478881a98118a32ff5b`  
		Last Modified: Tue, 03 Jun 2025 06:07:14 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5b2571049323d7a3c43a3747be26b9fcf659709a25bbb369560138e41ffa6b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95752340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01eac4f3c9d4047ed69954642d17e2d15f9c20d5389bdb5a83d394899e399c61`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Fri, 30 May 2025 23:35:04 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190f05a6d0716bc72f153c49559304db8fecc249c18e5472132d3ea267112e6`  
		Last Modified: Tue, 03 Jun 2025 06:11:29 GMT  
		Size: 61.3 MB (61311983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:426ea39c77fbce0bdb3ba531552c16ca8ba876b7923b3a0178d45c3560bef286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2449385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9626b0650c6e87db1cecba42cdd83bd8be5f2dc1162272483f953cc91b1b4d2`

```dockerfile
```

-	Layers:
	-	`sha256:ed85cebe4a9e6e7d463694b2d05561a85e773d0b2b4ecff0d4c58e49c0e201fa`  
		Last Modified: Tue, 03 Jun 2025 06:11:27 GMT  
		Size: 2.4 MB (2439849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66ad49ce32935573df9bb0ec5fea2e39ec701d1476361c6342bdeed0413cfd6`  
		Last Modified: Tue, 03 Jun 2025 06:11:27 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
