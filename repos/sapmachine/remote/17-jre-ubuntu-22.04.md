## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c7468ea90e959e7b18247958803bb8ecd1d0d825a2c94a624fe0522b052e707c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:9ce4929485497dfac8a5dcf8695f082e04d6689fd7f162e50689c698c6290021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83275897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff8389f171e3a7924a3dbc021393f19774ff75e553f3c8c486fee76fa001056`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199762461944434101bc00c7e60317256820d48c8f6cae662c7b557c1333ff75`  
		Last Modified: Wed, 16 Oct 2024 18:59:45 GMT  
		Size: 53.7 MB (53740209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5e2da01aae076b7d9037d71abe4bc00dc844054278b6e658beae55039642a38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c8568a89a6e2c9f2bba3a4dbe1a90265bac0be9d9e246f4c139c9a7c90e122`

```dockerfile
```

-	Layers:
	-	`sha256:d3e46514146e03557b6ae1ef637e4e41a9873f76541ea0680f7868f6cd7c52ad`  
		Last Modified: Wed, 16 Oct 2024 18:59:44 GMT  
		Size: 2.4 MB (2393521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8c526a26cb0f6e132f4e0229f00cd19e8a80b83e08510f8e820c86d1e285e4`  
		Last Modified: Wed, 16 Oct 2024 18:59:44 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:baff999c9964a0a05b4af569a4051793752cd0098cc01e20304e2229473d5447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80477687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807480194a665b5c05b35b303256505cacf1569dd932a09f37d7c2be979af17a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e0c7cd7a922466d6802afb26b83b54c56c73f1ca226d3989f87fc52ad95630`  
		Last Modified: Wed, 16 Oct 2024 19:35:23 GMT  
		Size: 53.1 MB (53119358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:af611f7fdec48e5fba42fd98b9bfd62049e53559e1168ba560c1786df3b750cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd829ac1b8ab3d9c6cd8ce9ab4bcd7caa976b45c4cfa00a4da606230cd0067c`

```dockerfile
```

-	Layers:
	-	`sha256:47befa864ef7e8352309301e918eb94cfd4dac7ae784bac5ff0dfb58cca17f72`  
		Last Modified: Wed, 16 Oct 2024 19:35:21 GMT  
		Size: 2.4 MB (2393201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:169978e1b1887503fa3c6df2862c5c36739581b2d074fdd2e0f9e8ab12381cdc`  
		Last Modified: Wed, 16 Oct 2024 19:35:21 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a899752995b76e6b53b8c7a97719cc2480e6abbca4288d6eab72fc43e37a2c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89643341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480248f78e54dd1fb4ac734f8ac173ad356cb3b0ba281e5c89ad371be8dce837`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e46a9fb33d862e9b1db64cb7c7a0b6fa265738bbed3238683dba7b562f555df`  
		Last Modified: Tue, 17 Sep 2024 02:54:40 GMT  
		Size: 55.2 MB (55195099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dec425303a02701ed11c8fa1fb2c5efc321574acee3f160d7d52019fdbc57990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918ef1e64da6961a48192494848cd2bab0246d6e5a99b682b910088027417332`

```dockerfile
```

-	Layers:
	-	`sha256:e132c9d9a405252c82d66de3841307181963e8dd13fee9ec5f8b62904de61f07`  
		Last Modified: Tue, 17 Sep 2024 02:54:38 GMT  
		Size: 2.4 MB (2390841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bee4c2efb9be065f384f50f9160f31e91eaaa257abca926c655432cfd3d115e`  
		Last Modified: Tue, 17 Sep 2024 02:54:38 GMT  
		Size: 8.6 KB (8605 bytes)  
		MIME: application/vnd.in-toto+json
