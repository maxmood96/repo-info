<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.12`](#sapmachine11012)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:f00407b658328897ca948e23d54cc4b5136b91384f3aba6037a1e702527b4db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:90ba2995ab5055755f4eef77c6379f4cab3c7c5014fcda827a4753609babccc7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235080649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19d47a61517e52b78e6338fdf33a376d14404b81160dadae87aca7190f219a0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:53:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.12     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 01 Oct 2021 06:54:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f56e95321aa7072efcf5a75b0fa6046d0f73488d6b4358ca96edc90e63bf91`  
		Last Modified: Fri, 01 Oct 2021 06:55:15 GMT  
		Size: 8.3 MB (8319710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e5919b54d9f7573b123bcb3af9e47784095520b16df6c2419651a03ef5bfaf`  
		Last Modified: Fri, 01 Oct 2021 06:55:52 GMT  
		Size: 198.2 MB (198192025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.12`

```console
$ docker pull sapmachine@sha256:f00407b658328897ca948e23d54cc4b5136b91384f3aba6037a1e702527b4db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.12` - linux; amd64

```console
$ docker pull sapmachine@sha256:90ba2995ab5055755f4eef77c6379f4cab3c7c5014fcda827a4753609babccc7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235080649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19d47a61517e52b78e6338fdf33a376d14404b81160dadae87aca7190f219a0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:53:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.12     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 01 Oct 2021 06:54:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f56e95321aa7072efcf5a75b0fa6046d0f73488d6b4358ca96edc90e63bf91`  
		Last Modified: Fri, 01 Oct 2021 06:55:15 GMT  
		Size: 8.3 MB (8319710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e5919b54d9f7573b123bcb3af9e47784095520b16df6c2419651a03ef5bfaf`  
		Last Modified: Fri, 01 Oct 2021 06:55:52 GMT  
		Size: 198.2 MB (198192025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:33c531218bc86fed59d3e3a5415e1968bff8cc71dbcb62a87d7941c2be079708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:20eb8f012e39ed7fa2d61ff3de68ac22b35e1d0f991e1c0620b25a1b88b4a849
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234476096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3802c02996f1c451d3fd815a0a8103794e7055a9c337343b2061027f17784e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:53:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:14 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 01 Oct 2021 06:54:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f56e95321aa7072efcf5a75b0fa6046d0f73488d6b4358ca96edc90e63bf91`  
		Last Modified: Fri, 01 Oct 2021 06:55:15 GMT  
		Size: 8.3 MB (8319710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7722dbc68dce4b219b440d2813f499a2a7a407d21c9c6d78173943af1b17935e`  
		Last Modified: Fri, 01 Oct 2021 06:55:28 GMT  
		Size: 197.6 MB (197587472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:33c531218bc86fed59d3e3a5415e1968bff8cc71dbcb62a87d7941c2be079708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:20eb8f012e39ed7fa2d61ff3de68ac22b35e1d0f991e1c0620b25a1b88b4a849
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234476096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3802c02996f1c451d3fd815a0a8103794e7055a9c337343b2061027f17784e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:53:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:14 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 01 Oct 2021 06:54:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f56e95321aa7072efcf5a75b0fa6046d0f73488d6b4358ca96edc90e63bf91`  
		Last Modified: Fri, 01 Oct 2021 06:55:15 GMT  
		Size: 8.3 MB (8319710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7722dbc68dce4b219b440d2813f499a2a7a407d21c9c6d78173943af1b17935e`  
		Last Modified: Fri, 01 Oct 2021 06:55:28 GMT  
		Size: 197.6 MB (197587472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:f00407b658328897ca948e23d54cc4b5136b91384f3aba6037a1e702527b4db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:90ba2995ab5055755f4eef77c6379f4cab3c7c5014fcda827a4753609babccc7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235080649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19d47a61517e52b78e6338fdf33a376d14404b81160dadae87aca7190f219a0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 06:53:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.12     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 06:54:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 01 Oct 2021 06:54:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f56e95321aa7072efcf5a75b0fa6046d0f73488d6b4358ca96edc90e63bf91`  
		Last Modified: Fri, 01 Oct 2021 06:55:15 GMT  
		Size: 8.3 MB (8319710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e5919b54d9f7573b123bcb3af9e47784095520b16df6c2419651a03ef5bfaf`  
		Last Modified: Fri, 01 Oct 2021 06:55:52 GMT  
		Size: 198.2 MB (198192025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
