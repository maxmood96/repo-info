## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:2a6aaf77eab6a5b86164b4b8831288b8a67e6dfc38c9647c359eaf258046ded6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:3d33b202699e49c0cfb7ae20af52d1e58541e20ba18d5d7d250a5c0baa0f7304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83798719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8da140402abf95d6b3337785cea8c2ae0fab3d8e8fba902d922a06c8521d662`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d50ecfd29d9bcab126ec78bc6a1f931ccf4fa4170cd0e45c9d9c43ff67f47ea`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 54.1 MB (54093566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17ec148cf3ac7a11505548e64ffdac8f12d1bed6ead215825dffa299e70c91c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314b8ad168c5edb2d5687667d74bdb3b5b011faa8f164d6d0b322b03dbf3325b`

```dockerfile
```

-	Layers:
	-	`sha256:efb9d74785485eeef994daad68eea9ca45e5afa4512aa0b022594fa66f1ef6a2`  
		Last Modified: Fri, 19 Jul 2024 18:00:09 GMT  
		Size: 2.4 MB (2360201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30d41d5b86f49c2deca47b971191ba6a0a9cbce545ed97f9de16f0defc795463`  
		Last Modified: Fri, 19 Jul 2024 18:00:09 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:058970662fd2d032a2a7fc14337e1de671938b8461ddb47ed8e010b779bdbebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82274285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92645ed25cd90a228bd08a283abf2ad0172cfbb84353863a1f7b6fa3ca972043`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2f63489dcbf04349ec35420cdb0d8d91e830f91b7839e50ef4f6d47f420e47`  
		Last Modified: Wed, 26 Jun 2024 00:16:54 GMT  
		Size: 53.4 MB (53431242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3aea6f7fe92a6a2f4a896ae1d9e049dfe5e7e5779e6ad913fb8297ee6ae284ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2342808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77efb268804d10bc65954390fcc8b28c0470cfe46c857962885c24b3b8e4ecad`

```dockerfile
```

-	Layers:
	-	`sha256:c522b040fbe73340bc2b7836cb5bf6cd50fc1937c58938cf2cadf99dc1e4751f`  
		Last Modified: Wed, 26 Jun 2024 00:16:53 GMT  
		Size: 2.3 MB (2333248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d417df7bbe44c895f3456c300e22298b4836aacbc071898c7ed08b0b50cfaeca`  
		Last Modified: Wed, 26 Jun 2024 00:16:53 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:41d1e1a8716d40644acfa781933437d4f70a5825476c30f6816853b5e60b86f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90162537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2f0fe7346b350cc2ff0297787f3821da5c9403af7e1e1fdc17e11d425293e6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470fbbb1284d5185c9005ee14d1a9431d1765b0e016892d3eca6140fda041a87`  
		Last Modified: Wed, 26 Jun 2024 00:50:26 GMT  
		Size: 55.7 MB (55656508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:593eb1d4e6a64b0bfc728d906bb0a0a62057dada0098a67f8a91ad8e627ffd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2345991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b6df64eb245d98dba46d437762834388353ec6a04b28b02f9fde0fedfcd5e0`

```dockerfile
```

-	Layers:
	-	`sha256:3a578e974158783ebcef28b41d26f56b6de53e3536d0db79be7e77d36821d1ae`  
		Last Modified: Wed, 26 Jun 2024 00:50:24 GMT  
		Size: 2.3 MB (2336706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb930a228e6dceeca87bfa544230f04b44cea717db07019c0382b7930bec4fb3`  
		Last Modified: Wed, 26 Jun 2024 00:50:23 GMT  
		Size: 9.3 KB (9285 bytes)  
		MIME: application/vnd.in-toto+json
