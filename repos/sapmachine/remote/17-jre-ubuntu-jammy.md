## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:5ce450b4dc8f094698195c08741050874e6fd2c0cc60458bf42c2c973fbaa5aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:6991699efa39ae068dcd7a0ecea897c7fb43c8513b996b92178ee35f6a0ddaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83409375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb5e7e04b1b562fa489d95ba1bb50d4ded451a6f2c919a93fc862cf93e657bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4079be8a32a4110ca7575b63aacb6f56df4ecf6f1e80641ae72d9b49609f3ec1`  
		Last Modified: Wed, 17 Sep 2025 17:41:59 GMT  
		Size: 53.9 MB (53872440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:45daafdb0d177df2e75af3896fd247a32b18fe332f9fcc6569cc8f9cdeddde81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eebf7972ff713342ec67e750ca870c18ff1f42068951480d4175440cc9ba683`

```dockerfile
```

-	Layers:
	-	`sha256:b3e0643d30a1657af730d01989908586f3228e8ee18a1921475d886dbe27e1a5`  
		Last Modified: Wed, 17 Sep 2025 21:06:37 GMT  
		Size: 2.5 MB (2543639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938916c06444605bda870212ad9bdd95a25d6ebcd34e00dcc9406748bb12a555`  
		Last Modified: Wed, 17 Sep 2025 21:06:38 GMT  
		Size: 8.8 KB (8817 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c6b4380eecda2f958d2fa70cbce7557629aa81845d2a4f968a60da25b961f105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80630847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733f83b51980131c886f002ffe2d5e23449ffc016c0f1dc7ab9c0ff8b4415dae`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351f9fc820cbb0c2c2aba51a05b9c5f8482fd3a0c6556839a75fc9da45d18099`  
		Last Modified: Thu, 02 Oct 2025 01:35:31 GMT  
		Size: 53.2 MB (53247740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0298a59faab37d0027ea1670c793293910d0a93190dad149ef3ea99f2f211a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c489547eac3049c78cd26c3e6ee42425715fdf84ef91c961b77e2ab193df9169`

```dockerfile
```

-	Layers:
	-	`sha256:490fda53e21898e2f3d21c1885f59a8f41050b6e4bbd55c9919a3bcf905d2889`  
		Last Modified: Thu, 02 Oct 2025 03:05:42 GMT  
		Size: 2.5 MB (2543321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904b77c4060b2f38bac82ea228f89730f0d9d47e2de71ab037f8bc4956b4caa3`  
		Last Modified: Thu, 02 Oct 2025 03:05:43 GMT  
		Size: 8.9 KB (8920 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6700ebc45a9cff80b4a4df6af7ac9f8a064d4d9b7ab0ccd606e47184c65ac2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89391562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:618a6a65aaf629d339e546fc309140b6f551d1d6bf3764a908a414c91db98f97`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4259d8033f30bc4b649845e2525112964031b105224cc1ebab96c79633621343`  
		Last Modified: Thu, 02 Oct 2025 04:53:16 GMT  
		Size: 54.9 MB (54944773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d298b32060629a4b9c4656a063f2ca15e3e2388ea5349296293ac7517f8cda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2550615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4498495c8cc5767502832b98078aac26a227cc0ccd36f54ea8073845a4199b7`

```dockerfile
```

-	Layers:
	-	`sha256:f9c06c66cafa218abc6c78d9b02d6679ad5d760df2e1c00b07eb318e7fdf629c`  
		Last Modified: Thu, 02 Oct 2025 06:05:51 GMT  
		Size: 2.5 MB (2541754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c54b8e66ee3db410b9cdc9e5fb787344d35f879440410fdddcc2b072055c8b1`  
		Last Modified: Thu, 02 Oct 2025 06:05:51 GMT  
		Size: 8.9 KB (8861 bytes)  
		MIME: application/vnd.in-toto+json
