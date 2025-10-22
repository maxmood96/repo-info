## `sapmachine:21-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e985dbc0570a9b1047e8ffbd92ffc839848a3341e67460853c9df58486a61379
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fa6c06a1d753398995efcee1a5c7d45a889b51069da5116291f0f5933744c597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244514679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80132a3723d5dc971cea8fa2cd57e9461443cdf22389dab53de1f6bd441b4861`
-	Default Command: `["jshell"]`

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
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9081b02e079adbc4efd186a6d2beac9a646033f6c42b7dfbf1989edcf7fff1cb`  
		Last Modified: Wed, 22 Oct 2025 11:47:49 GMT  
		Size: 215.0 MB (214977861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ccaeac555326e30fb69053828e626f54f69c0d8505d5c53633d4c2aaf4473cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9ecf490f52dc4aa8075d296ff082f91d875fecc8fb233f2296e31b96c1a5dc`

```dockerfile
```

-	Layers:
	-	`sha256:f3f45c4714b0e9fc27d662ede44986fa5ae58cc8432d4e0d12c2e916ec60abcf`  
		Last Modified: Wed, 22 Oct 2025 06:10:19 GMT  
		Size: 2.6 MB (2629722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d04e880d65b675e0c089292d42227768a5189d43352cb55083a72d43b1ead6d7`  
		Last Modified: Wed, 22 Oct 2025 06:10:20 GMT  
		Size: 10.1 KB (10124 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:49d623744a156f91fed3fd5c1b3908ed4f9ca6e28ce6b8ab9e01872a2b84d745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240559469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a7d9cc39f8b9ae4f9ce9e34769fe3300a9ab882a30786bf0ddf242281cbc58`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628e94d875ae521863af54e009151a42da824c4acb63799cdf56b132716b3dae`  
		Last Modified: Wed, 22 Oct 2025 00:06:14 GMT  
		Size: 213.2 MB (213176362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5d608a440b95f2ca05906c1342c5cc33b1dac3ff088b61777fefeffafb1c8064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f6b5d503859c46ed75ae92934576355d92c48d62a16326e29e93a3449fc803`

```dockerfile
```

-	Layers:
	-	`sha256:58acc557a15a7d707b98e423e263415591610251a78f37832a2127f799f1e63a`  
		Last Modified: Wed, 22 Oct 2025 03:07:35 GMT  
		Size: 2.6 MB (2629452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff5ada04c86ee3aa85ca5ba5ec21f5c3c20d8af75a132aef8ee18e975b51aac`  
		Last Modified: Wed, 22 Oct 2025 03:07:35 GMT  
		Size: 10.3 KB (10276 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a50f4a8ebde5abe22b83c82a7e4d55f402f7083e72b9072766ab9d75de874a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250211712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2a5b293302f379179a96ee848fe167d37fa798964e8048435cc7efb28895fb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14745a7d4747ef126db444e469a49fe309b2b8decd3a5b90400d246ad39aea60`  
		Last Modified: Thu, 02 Oct 2025 04:35:09 GMT  
		Size: 215.8 MB (215764923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d47a33b9b774bcd23f0a50d9dfb4a2ed8f6072ff4893a4196d439509798c89ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b251ae477ab9b26104470262b917a7b5c710ad29a839beca4ae5db5ce7c571f`

```dockerfile
```

-	Layers:
	-	`sha256:d1efed793eb3901ed3ac85ec05b1a7f92194191e698a40fbba835bb3a70a2457`  
		Last Modified: Thu, 02 Oct 2025 06:07:59 GMT  
		Size: 2.6 MB (2625915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e126d096b53b724e842870359ac054b69b68c6901dea06b9eaf6c2d7d8ddb5a`  
		Last Modified: Thu, 02 Oct 2025 06:08:00 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
