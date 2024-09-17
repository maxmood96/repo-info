## `sapmachine:21-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:218270aef492b264f35db95da8d38c1928964f5b4d85f817205ce29b71b53b5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:341411710593c55c3876002425721bd19c5f7eab5044df3fb89e05c3a7c80fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244749923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c0c9e64123557cf661059c85f964760527059a755623d24269a3facbc3dc90`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13160b1e2676a5eabc18a1a70b8ff4b82f967b62eaa0b4a6ef834a98ec3ce156`  
		Last Modified: Tue, 17 Sep 2024 01:01:13 GMT  
		Size: 215.2 MB (215214235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:32667124943062c0cb904e654025c63a0465cb3ecfceb8d1203b841f268ddf38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de94eb4dc98a5799c1c5fdf8661dd3c88a6596f74ac816369e7385ad9a1cd689`

```dockerfile
```

-	Layers:
	-	`sha256:32f33d1d316b0a17eeffb09f6521c864ba495d94788eea741f7e1c6a9d2533e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 2.5 MB (2475042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9081e1378ccddea460fe56bc200ed6851d7db1ec6828c46e96540f10121ef8b0`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 11.2 KB (11190 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d8ec4b9d5b21ddabb6974ca7202ae5e91da6a4bc24d2f6fe5a07f70a228488c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240620928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9459b5229de3a7201ca76d0a973c51dee1cd94cf06d46612aaf34fde2fe1b798`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b9d21db10ae9e91fca60ed99eb2babf6ddd8e4a2787aae58576ee3c54defc`  
		Last Modified: Tue, 17 Sep 2024 03:21:32 GMT  
		Size: 213.3 MB (213262599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5b4ddb78811b3f3b7de95458bd08b30c03c3039e48fe8774192b0bf1182ed5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f07e580d50fb72492a26a8164e13b0fc93d626228706f3e8f8e587b16870fc`

```dockerfile
```

-	Layers:
	-	`sha256:b7636c6da3682c6d8077110225637d871f4f8cea3fd31fc476009aa8e735c0b1`  
		Last Modified: Tue, 17 Sep 2024 03:21:27 GMT  
		Size: 2.5 MB (2474818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b184d31d323a9cf08acda7118afa1c99b883d96a12f906af6441782f8607825d`  
		Last Modified: Tue, 17 Sep 2024 03:21:27 GMT  
		Size: 11.6 KB (11588 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6a19bd35adc13afaef0550090f0e015618867009d9dc55182f464e576195dbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250990455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0495f2b780fdc14238a48af4bba4cfd3798b95bfc596afa3c1057e21d1b63d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254281285ede09901d5a74c4bf54fcd9d1f4e8579b68b9f00ac6221400f7f8ea`  
		Last Modified: Tue, 17 Sep 2024 02:37:23 GMT  
		Size: 216.5 MB (216542213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:45c49d73eaa1b800e4a3ff80549aa39a99af172cfc505ffc8080ca0a000551c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0ebda29dd8702efc6dca714ce38c9380f70845291e71a16099f34eccc5945d`

```dockerfile
```

-	Layers:
	-	`sha256:3f9ecdf69e686baf072bdea6c176f80f8c957ea22cdf0da4547de6c8a651d97c`  
		Last Modified: Tue, 17 Sep 2024 02:37:18 GMT  
		Size: 2.5 MB (2477120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036cfd9e05e4c4471d229bcfde2e4f12f676adfc92eb95af91cdb1d108cdf282`  
		Last Modified: Tue, 17 Sep 2024 02:37:17 GMT  
		Size: 11.3 KB (11277 bytes)  
		MIME: application/vnd.in-toto+json
