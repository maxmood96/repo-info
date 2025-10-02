## `sapmachine:jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:0bd9d5341e2aeb86dacb26b16b2f7e0549d91e943f2bbf7234389551dfc9c964
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:f636eb7707d789eb55c72b6eca3b96afcd1655e5fbe062a0177004ca2895a799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98125195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6785f96500c6be0cbc7829f49573998cb9185aed4e29ec58fbaa3d5389a2e6a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e996b40ee13684ad75f69edafdeeffc9d40ed17fcfff7b2ee15a6779476b2b6`  
		Last Modified: Thu, 02 Oct 2025 05:19:10 GMT  
		Size: 68.6 MB (68588377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f5e9d8def4ca7bdd9c236f87de5cbe8d78af546a27ee05bdbb9141869871f94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dca8e38ec6d53785ddcd7f4247c47dc171d6e134254a7452192d22d33f6c82`

```dockerfile
```

-	Layers:
	-	`sha256:bb3686bf7285e7defd3ec173ea38e791ba1f7ad81604c44aa405bcf98026fabd`  
		Last Modified: Thu, 02 Oct 2025 09:13:13 GMT  
		Size: 2.6 MB (2552571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e51de7d971409b23e5f9dccda1678d76477cb40c2650966ed85530e7dd404ffd`  
		Last Modified: Thu, 02 Oct 2025 09:13:14 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2a3c422894dc44dda2c4d874e75e6a38547e88eff76eaa1d7aabe9914696273c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94904768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1049d647b0a6d4253571988437079489894c2ecb5db461db5f2bd6a7da33a6e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c356412f0c5c46c1965a5fbf35f18c7cd464915a1b719dd8c5194c0ffab9d62`  
		Last Modified: Thu, 02 Oct 2025 01:34:00 GMT  
		Size: 67.5 MB (67521661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:092f42a874a28931e66cc96239aa54226be126a0902871a50d5f91eff608539e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51d686c5a47e50b3a3bd5eb2d22f65e2e343be792d1efd0a14c22354cea3d54`

```dockerfile
```

-	Layers:
	-	`sha256:823cd76d30e75c52e9b6778208d05b9f7aa322632b49d331db3e2ec8702dab6f`  
		Last Modified: Thu, 02 Oct 2025 03:11:22 GMT  
		Size: 2.6 MB (2552274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3c9076173d40fd430bc5e84368e6fe98ca42e8a3921b751cd8c16934567dde`  
		Last Modified: Thu, 02 Oct 2025 03:11:23 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d92dc1f0ab14c864cad2ee07ebb325f05c4dc2eb89a350d95d70df219fa776f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103870567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d25149ab4c97d6046ef677a6070be35df8835bd9f309200b02120b37ce99b1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350a0f8fe2228e0044300258ad9eb05679192e4c68f047a012c7ac697d33007d`  
		Last Modified: Thu, 02 Oct 2025 04:24:03 GMT  
		Size: 69.4 MB (69423778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0a4bf334cf5f67187eb0ac25a55152849d308c8f49bdcf71e99df2237320d8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaec115530cfdc5a5fa4fe843711efa76130a75919171e539977c7fd19129832`

```dockerfile
```

-	Layers:
	-	`sha256:3551a8b8e4eb729d51408178157cee22959e884a0eb7e28929d09ce7ab363271`  
		Last Modified: Thu, 02 Oct 2025 06:11:36 GMT  
		Size: 2.6 MB (2550068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edbe0e3efdddef399b800090a741b6ae51502b4adaf6f58e1691518d928c07a5`  
		Last Modified: Thu, 02 Oct 2025 06:11:37 GMT  
		Size: 9.5 KB (9496 bytes)  
		MIME: application/vnd.in-toto+json
