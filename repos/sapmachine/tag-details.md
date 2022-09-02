<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.16.1`](#sapmachine110161)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.4.1`](#sapmachine17041)
-	[`sapmachine:18`](#sapmachine18)
-	[`sapmachine:18.0.2.1`](#sapmachine18021)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:fa6fb2ab5e87ba86278e347be43bc3a5a370f0939ad0641acbef969afe471047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:78e07cce1cbd29eb97bb5943b864e7951f0367147fba9cb3960af2249431db9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234784238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4e007cd7a66666837a38b2dd16bb92e7ec215faea8e944f630d8c2d28a582d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:18:39 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:18:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 02 Sep 2022 05:18:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c570590a938bf8b7518bc5060eafe4acaa5c72857686d92c6f4a4c37dc286d3`  
		Last Modified: Fri, 02 Sep 2022 05:20:27 GMT  
		Size: 198.3 MB (198291275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.16.1`

```console
$ docker pull sapmachine@sha256:fa6fb2ab5e87ba86278e347be43bc3a5a370f0939ad0641acbef969afe471047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.16.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:78e07cce1cbd29eb97bb5943b864e7951f0367147fba9cb3960af2249431db9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234784238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4e007cd7a66666837a38b2dd16bb92e7ec215faea8e944f630d8c2d28a582d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:18:39 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.16.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:18:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Fri, 02 Sep 2022 05:18:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c570590a938bf8b7518bc5060eafe4acaa5c72857686d92c6f4a4c37dc286d3`  
		Last Modified: Fri, 02 Sep 2022 05:20:27 GMT  
		Size: 198.3 MB (198291275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:7b9ed83057406647303593a69826f8bfd8347102c2c5c5479f00318016b891dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:12bd0a139a3170d99388a6e167abfb40432586a62a8ddb39bee859687d0ef2e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b491068ce00d2abf432adcd7d9fa906fea4cd8a3b6d37b114971389a1182c770`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:22 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 02 Sep 2022 05:19:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bfd7196d5bec726c806cc0c3a4ce44acfba55a52b7a148ef2c87fa58857af3`  
		Last Modified: Fri, 02 Sep 2022 05:20:52 GMT  
		Size: 197.8 MB (197764255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.4.1`

```console
$ docker pull sapmachine@sha256:7b9ed83057406647303593a69826f8bfd8347102c2c5c5479f00318016b891dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.4.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:12bd0a139a3170d99388a6e167abfb40432586a62a8ddb39bee859687d0ef2e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b491068ce00d2abf432adcd7d9fa906fea4cd8a3b6d37b114971389a1182c770`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:22 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 02 Sep 2022 05:19:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bfd7196d5bec726c806cc0c3a4ce44acfba55a52b7a148ef2c87fa58857af3`  
		Last Modified: Fri, 02 Sep 2022 05:20:52 GMT  
		Size: 197.8 MB (197764255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18`

```console
$ docker pull sapmachine@sha256:858751d7719710b39168b4e741c73988fada5b4ff8cd3e91832e4aca095a70f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18` - linux; amd64

```console
$ docker pull sapmachine@sha256:7dfbc14633587ffc07c729cba99bf071c70057a29c492c9e26cded85a37b70c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235300613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d9c5b2554c8ddae80962502888a87ec2c842cdbaac5009de66ab84f76c8d21`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Fri, 02 Sep 2022 05:19:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9981dfdf89b6d7c8500dc8653ed09e43f1fcf2e5d95ca71f5e9c63f36151af37`  
		Last Modified: Fri, 02 Sep 2022 05:21:19 GMT  
		Size: 198.8 MB (198807650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18.0.2.1`

```console
$ docker pull sapmachine@sha256:858751d7719710b39168b4e741c73988fada5b4ff8cd3e91832e4aca095a70f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18.0.2.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:7dfbc14633587ffc07c729cba99bf071c70057a29c492c9e26cded85a37b70c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235300613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d9c5b2554c8ddae80962502888a87ec2c842cdbaac5009de66ab84f76c8d21`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Fri, 02 Sep 2022 05:19:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9981dfdf89b6d7c8500dc8653ed09e43f1fcf2e5d95ca71f5e9c63f36151af37`  
		Last Modified: Fri, 02 Sep 2022 05:21:19 GMT  
		Size: 198.8 MB (198807650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:858751d7719710b39168b4e741c73988fada5b4ff8cd3e91832e4aca095a70f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:7dfbc14633587ffc07c729cba99bf071c70057a29c492c9e26cded85a37b70c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235300613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d9c5b2554c8ddae80962502888a87ec2c842cdbaac5009de66ab84f76c8d21`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:56 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18.0.2.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Fri, 02 Sep 2022 05:19:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9981dfdf89b6d7c8500dc8653ed09e43f1fcf2e5d95ca71f5e9c63f36151af37`  
		Last Modified: Fri, 02 Sep 2022 05:21:19 GMT  
		Size: 198.8 MB (198807650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:7b9ed83057406647303593a69826f8bfd8347102c2c5c5479f00318016b891dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:12bd0a139a3170d99388a6e167abfb40432586a62a8ddb39bee859687d0ef2e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b491068ce00d2abf432adcd7d9fa906fea4cd8a3b6d37b114971389a1182c770`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:22 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.4.1     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:19:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 02 Sep 2022 05:19:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bfd7196d5bec726c806cc0c3a4ce44acfba55a52b7a148ef2c87fa58857af3`  
		Last Modified: Fri, 02 Sep 2022 05:20:52 GMT  
		Size: 197.8 MB (197764255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
