## `sapmachine:21-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:47cab6fa7b8f484c92dc93854134b8217ba6bcd65f7e906e2005855fc934fd57
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
$ docker pull sapmachine@sha256:6523a40678f5f6b75617d228ebd294e2edd6c8513d36211a48158e57dddfb590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244468449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf8f0bd667074b79796bfe85af433a16aad2b7f73b7ddbed4aa6f7413cf00ab`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3915ff5494fc50134ad6ef219f4ac08ac6654f733763d21c9dc5a1a454572e1`  
		Last Modified: Tue, 02 Sep 2025 21:44:23 GMT  
		Size: 214.9 MB (214931514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a846e813ab19d2c69d2affeb9b433d200255e885323096682977eb5e620c1105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdda9f6799092e21980d9c10edfb40411082fece0404f05081db8aaef1fdf2e`

```dockerfile
```

-	Layers:
	-	`sha256:97191018b6e3ccd21f9bda92f7c44401bfe78f3b995f2d3c2b9d00ca416aab18`  
		Last Modified: Tue, 02 Sep 2025 03:07:32 GMT  
		Size: 2.6 MB (2631042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7190cf3b85b404b5f1e1afdbc6440c82736b2c17bb089ecf0ae9496da5c78a3`  
		Last Modified: Tue, 02 Sep 2025 03:07:33 GMT  
		Size: 11.4 KB (11444 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9124691898e55e36ce577c5ff426fd6102eb70f6f4c862dcaa6a3f3a36a8c5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240490269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4617b73d988abd727bc567ceeb9e4d656c382d47653261d90d1b9becd05190`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32b46b0410114532e5a867f7373b5b6b65cba169ae2a0f66e76e805752ae825`  
		Last Modified: Thu, 02 Oct 2025 01:35:00 GMT  
		Size: 213.1 MB (213107162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec57a637001fd8b4831505f082914130a6b3fb83d59bf996e9300709ffd934ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9341d3350c4781ebeea518385972fb2b710f4d3bd2442d51cbd7494a0b6df6f5`

```dockerfile
```

-	Layers:
	-	`sha256:a86f3891b8bacbe0e5a498bdb7de13a5955d5e1d789f1ed9a5342f9ba2fb38c4`  
		Last Modified: Thu, 02 Oct 2025 03:07:53 GMT  
		Size: 2.6 MB (2629452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2d9b88ef7dde65a5622ecd1895b43b605c9deb8aff0bd93dc6e841bd7125a3`  
		Last Modified: Thu, 02 Oct 2025 03:07:54 GMT  
		Size: 10.3 KB (10277 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-jammy` - linux; ppc64le

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

### `sapmachine:21-jdk-ubuntu-jammy` - unknown; unknown

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
