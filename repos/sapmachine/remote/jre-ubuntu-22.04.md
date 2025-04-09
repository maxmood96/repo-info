## `sapmachine:jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:78a475bc157f256d7777f5d1517d45caa145d8c01d4388a225a37abd599bcb69
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
$ docker pull sapmachine@sha256:dfffb4a188ff3112ee02370f47de030dbaab04ae2081fe5453eb47223f789bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97193326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd26a3da7a2d384e960f6832eb18db1ea562a03f27bcf4f3317c3dcb2ae83bb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab36c2a3837ecc85a8bef65067487461d1d38463b4681c3c6d148de665936c8`  
		Last Modified: Wed, 09 Apr 2025 01:20:29 GMT  
		Size: 67.7 MB (67660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:26c693673efdd35f04e7c83e8402586d63bd5aeec94bb563082bbae5954d9d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892ea3435d53ef90c5d4d42e9104bc75c905cd9e4c413b0cb567d002f61f1d52`

```dockerfile
```

-	Layers:
	-	`sha256:625580056feba809cb63317c75a3737843048fc2619c04b0d68ff2fda2d9ada5`  
		Last Modified: Wed, 09 Apr 2025 01:20:28 GMT  
		Size: 2.4 MB (2415712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2753be1126697ab04ddfbe7657d4b985b3d5bb5a913e3e300106faee80ff6bc0`  
		Last Modified: Wed, 09 Apr 2025 01:20:28 GMT  
		Size: 8.8 KB (8776 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:65b1f6ce600c5aee75cb661c3c746145c5f0af031c02381ac826893523ccf9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94025601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af21db30fae4da56ade64f830f42425a3a2bc68b3e0694d5009c2599eab8b2d`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8493f821c8fdba445b33d07c091a4264a2684d16ec118ab034e9472d9baea288`  
		Last Modified: Wed, 19 Mar 2025 20:38:36 GMT  
		Size: 66.7 MB (66667419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c1c2c1302fde91765cfbc43e885575eec895559e2174b391074c70b0abbdd1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2611506095dcfa5d4696f9d746cbef1434a8457cae8bf938ebeed09499feb165`

```dockerfile
```

-	Layers:
	-	`sha256:0eca796af91d2217ff9836b0f40eb7e9a8c4a9231bb491bfa3b833beef9bdd9a`  
		Last Modified: Wed, 19 Mar 2025 20:38:33 GMT  
		Size: 2.4 MB (2415269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a88e18a325c3ce60bba7a724d772b85a0dd84955ae8e4bb6ed808dbfc9f234`  
		Last Modified: Wed, 19 Mar 2025 20:38:33 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:08f732fcf494558e79f035c91b73d4fc63c6140d9b5a2150dbc7695df284a8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103381330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856b253a69e9c658c7200013d5c7106bded8924f39d1d23c6b7bcfd29e6050db`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af2113ae789223d86990b529b0eb625348a6b02e1e8acaaba3e7f1b253bf1c0`  
		Last Modified: Wed, 09 Apr 2025 06:41:55 GMT  
		Size: 68.9 MB (68938634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a70e8e0752537fb1514564f490fc8563af01a763e3923c3ee27d07a8b70cbdf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a774dfe03ba38bd29b2c222cc1dc44e13114e0cac486804dfe565499c87fe99`

```dockerfile
```

-	Layers:
	-	`sha256:8b1cb24a9513b4467d14cac4236425b226617e7440e3bcc77100ee7e729247d6`  
		Last Modified: Wed, 09 Apr 2025 06:41:53 GMT  
		Size: 2.4 MB (2419063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c542c034eb50f6feca90fde86e0dc462baad32037499f0583fcc8164f4fb1d6`  
		Last Modified: Wed, 09 Apr 2025 06:41:52 GMT  
		Size: 8.8 KB (8820 bytes)  
		MIME: application/vnd.in-toto+json
