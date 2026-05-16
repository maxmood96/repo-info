## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:175d386ddef0c189e2ff7689b48b814bd054431443f2ada7c06e5cc5524abe3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:23a3a4e6fa93406c6d675f957266ccded23db492765c8fef5e22ba9de14ad2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88351458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c093386c3b3daae5e6342ec52b0e23a4e9ba8542bed13ba50cb56a7c333699`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:20:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde05792978aad45d68faf832b222d1d71b2b96a98b56b837452f05e2f039655`  
		Last Modified: Fri, 15 May 2026 21:21:02 GMT  
		Size: 58.6 MB (58614774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:28561941f361ebc0a65ba22698c60ad7d86dbad48e56696124eb43505a3bd5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771076e6b17c9fb38138f9a29ef7d9db3de03250bf856e4c62425d73e48f4aa7`

```dockerfile
```

-	Layers:
	-	`sha256:71a95fb728b0443a4e0fefa3d9948c3284a080fb2ab3058b7ecf605258c00c49`  
		Last Modified: Fri, 15 May 2026 21:21:00 GMT  
		Size: 2.6 MB (2551805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6737230b0e662097f9c302f014b4c130d8b47b4be713961dcab764f98bac557`  
		Last Modified: Fri, 15 May 2026 21:21:00 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:56d7b78c31b163b827db0084de2791ce02c00b2d8abff797a95f81d920d963be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85200295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac9979d99405913ec7106ff7a1e92da5d84e484cdec40d28806d6ecc8b96fd0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:21:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96907a8cb2069b20940df9b43bd56f83a23c51d63e4d31f6653c850a7d1d2e53`  
		Last Modified: Fri, 15 May 2026 21:21:28 GMT  
		Size: 57.6 MB (57593672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5791e839b33767233e3426a9f8efd246d7aaa4295708dddfacd6ba87ce2d3710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c0524f2f3900fb1234e1414b568bd1655837e92d17badfec83d94647d8e88d`

```dockerfile
```

-	Layers:
	-	`sha256:54132b0e4f835d696ad8930ecdc690206e8e66c8b5555b87f9c2d85aacbe0713`  
		Last Modified: Fri, 15 May 2026 21:21:26 GMT  
		Size: 2.6 MB (2551508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea2d29bd6407065974606940dd8e218c5d64f6b7bdb0842bc42e49bff830c14`  
		Last Modified: Fri, 15 May 2026 21:21:26 GMT  
		Size: 9.5 KB (9549 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9ddfe4bdea75ffc9586bb0c23f2c4eef742c49c6fd32f943dd191da318ed9c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94342684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36263a5159c78d324ba87c07f6384aed45a120bd384cbbba6b2a127e13cc3374`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:34:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0509fd7c94a1f9d38c2be5418125c2d2730da6ff54401914577a599ace98af2a`  
		Last Modified: Fri, 15 May 2026 21:35:07 GMT  
		Size: 59.7 MB (59695964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c555d1a6abf3c6bafe4a556fff621a33530beb677e0100da60bb13b0778cd172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2560195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ce7b36bc6f2d98439fbf7f7355928c7f3fc00aa93fb289931ee31134412895`

```dockerfile
```

-	Layers:
	-	`sha256:ec3a14b71e1b6a6296398d4c92a78ed06f76e9afbfd3de96df60cfefb70c2a48`  
		Last Modified: Fri, 15 May 2026 21:35:05 GMT  
		Size: 2.6 MB (2550719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5d214ca3b1ac8b50a477a05d3792477d1523540b9068f6f52008c71e1a0507`  
		Last Modified: Fri, 15 May 2026 21:35:05 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
