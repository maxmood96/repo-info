## `sapmachine:lts-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:1a736fc28e206ccb962954c9245875261c226d1affb1f1da8ca3e924057d31d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:be82054fee018a21447caa06c0f4d7b4aa986ae1de7568f12fb387a246949ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251186208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319ce464587662766aabc067d4f7bb9c893db6bf714e3df1e4c0c9ae150c07fb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7261e992e549107f003743f60a1ec623fc178881e63f5e0d7dd4716cbbb2117d`  
		Last Modified: Wed, 15 Apr 2026 20:58:41 GMT  
		Size: 221.5 MB (221453230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d7c20fe63c9fa448de00eae620e1f90137cb1266fe82811c7299bf9d7baad4f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2613669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caadfdfc92b5260adafd89e45fb21b79d1fc289d10d1ed9c682f8c8dfae06f4`

```dockerfile
```

-	Layers:
	-	`sha256:6da8335c776f62bccccf444da808cde569c24f0e2425be4752b27bb074d16e54`  
		Last Modified: Wed, 15 Apr 2026 20:58:36 GMT  
		Size: 2.6 MB (2598827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8bc5845f731297eb6a0975259ff01a86fc33999f054ca0c5b8cd64d2e7b61b`  
		Last Modified: Wed, 15 Apr 2026 20:58:36 GMT  
		Size: 14.8 KB (14842 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c84675fb223a8012ee1c91f6297c447258e9111463acc6e030a43af08aabffed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248142292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3d14caf979b30753f2eca85c0820343740a1db1d6566c6b9027c517ab0872d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:07:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:07:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:07:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8551e8c16388e78ab94c5d6f978fa6399edbcb20e0e40b0012046dd6e9617d`  
		Last Modified: Wed, 15 Apr 2026 21:07:57 GMT  
		Size: 219.3 MB (219266507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e62a85fb2912e05c96671017b565d6ee46f729d8d06daa739fa836bc8d75e292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6244d08fa1aa72abe05058dbfd03188bd2f01a4e8b81b2e89b1043372ca6697a`

```dockerfile
```

-	Layers:
	-	`sha256:8106ee95e68a6d16b6e20061212f0e120ff74f3db162497aea631d4e321bce2c`  
		Last Modified: Wed, 15 Apr 2026 21:07:50 GMT  
		Size: 2.6 MB (2599520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb6c19c06038872aaeac6bdf8a14da3524f94d1c046a328c252ee3135d164bf`  
		Last Modified: Wed, 15 Apr 2026 21:07:50 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1095bc492b5edbb897421e0dd7469393cfee96b4b9346c1c4122249829531b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256665007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f7645ab8c1196291eae52d9b53ac2987deff50cb4c1f9e44e1ab50860adeb7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:02:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:02:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 09:02:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af1eb519a9c0294d2c0ffba67fd5006cf829710f4a208f1d662a7e0118dfaf9`  
		Last Modified: Tue, 07 Apr 2026 09:03:35 GMT  
		Size: 222.4 MB (222351673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c0102d4d9ec3ed1586dc82b8e0db4882a9ede5e221ad5e9e1145dc1d781ed7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2610851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94adf693b63798ecf63141e633136ec6f31deeaf3bdc96ba2c8ca2992921411d`

```dockerfile
```

-	Layers:
	-	`sha256:49edb7e283e35097fac399c6e443afb31e083a9c5b744fe10ad13c85d5a363e6`  
		Last Modified: Tue, 07 Apr 2026 09:03:30 GMT  
		Size: 2.6 MB (2595851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042beccf89ba4ddc07b4d87181969a853c17a53caf55a659d6ae1162b9f373e8`  
		Last Modified: Tue, 07 Apr 2026 09:03:29 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json
