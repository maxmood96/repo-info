## `sapmachine:21-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:cf52cf8c99c84e22b579a55e95f65508ccf7b984408619359cc98c571b0cc049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:b2f0c5b44c2a682ea10066a9e554d501cc3663bff4c732a35d396f645342ae02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88045970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176433e9305293bc3044fa4213fd2e5a568837a424e63ca851206a7bd3337658`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c175626c642016aab0c4cb288c2a8a375fcaca83bd7fd91e76139b4b40c0ea`  
		Last Modified: Tue, 03 Jun 2025 13:56:52 GMT  
		Size: 58.5 MB (58512967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:36b755e08e4b266517fa0d9fbe26c212932d5255e5eb338af451520924061a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740cc45db4277abd1038e5265f96a8115183ba502e69868f971304319ab2188f`

```dockerfile
```

-	Layers:
	-	`sha256:e00f5d0feb29ccca1829767705ab5557e8c4106bd223284876d17583663548ec`  
		Last Modified: Tue, 17 Jun 2025 09:54:10 GMT  
		Size: 2.2 MB (2190010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:971b6e2f97c2bfecb10e205d02b4b7608d497ccd58a2ac1083fb61a6e526ff58`  
		Last Modified: Tue, 17 Jun 2025 09:54:12 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fa99ae9f876f63f0acb11b70d31f96208e5173e152c32e2937a33eb5248b36e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85011789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d09a2a1d95564b7b74955986754f43ecd02925b7ec8f3adbc2ce6a5db3d10f`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08346ab44796d01445fef33aa694c19d8ac1e4a3e2fc3b8a8d210fa5ca94ce5c`  
		Last Modified: Sat, 07 Jun 2025 16:11:53 GMT  
		Size: 57.7 MB (57656208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:958385b0a44e2b0fdd3e5917c38eb757531e8da2df897c14000b4d0f96d31bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f1bb6f04d377eeba9c7d3ebbef76f4a76a7815a73065415ee09aaa71fa8fa0`

```dockerfile
```

-	Layers:
	-	`sha256:30825a98748b63802b6d34ab2edd1a8614c1a25813153b9877ba234f97803075`  
		Last Modified: Tue, 24 Jun 2025 17:44:57 GMT  
		Size: 2.2 MB (2189706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b25c177483246c780cf424c08afb7ddaf1611f4dc0ba886854b2a3a7790c6e`  
		Last Modified: Tue, 24 Jun 2025 17:44:56 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fa1ed437d461ae6eb6e0516fcaf1a9cc44c3aa5f879bce815b747ed7126a8d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94351128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19cd66354d6f5675b58662fbdabb9c005316e99d67748bebcf75e9e653b7bd7`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c0a3e300aed07962f9dbc8205a10642791f500d53bd4df9ab68c7cf699662`  
		Last Modified: Tue, 24 Jun 2025 17:46:01 GMT  
		Size: 59.9 MB (59910771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5df1a25ae73196b6a445da98530e72e880dad30ff30b39e84225707fa91d1092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0e89d7657485267548a24c9cebce167733db3e6e692e691f7f16c4ec978410`

```dockerfile
```

-	Layers:
	-	`sha256:f5b009fe39633c810e62e9f30a46b576ca77b26b5b02f3682aa14d74af0ed2ca`  
		Last Modified: Tue, 24 Jun 2025 17:46:31 GMT  
		Size: 2.2 MB (2194063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b136a98ae8778c29af48868644739fceb639e806f42adadc3b9abd59828edaf7`  
		Last Modified: Tue, 24 Jun 2025 17:46:20 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
