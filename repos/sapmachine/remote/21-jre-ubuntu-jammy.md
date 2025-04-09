## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:127daf8b29b3c850866b733eced9e3565d562d75105abf8a5e0e38252165fbcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2b30aeb9da3ac320f531c26f780d23974e120abee0806fa4152f8dd00c5a3f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89257106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4c685989864a7b94f2bb9f75ffb57b0ab29b6fd45157140d27af9c0ed8b4dc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee534d44c1594fd2887ee42502ead08fb9f58d7c5132c297ff0564a2a9b6dd1`  
		Last Modified: Wed, 09 Apr 2025 01:21:05 GMT  
		Size: 59.7 MB (59724741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6ac01e8a5c24e16a34e90d3a837b12ca9c67f5966dba9d09bff675688729682a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55137f24627a20590f88d76850d53008212546ec4495f6f92591cd395ead770b`

```dockerfile
```

-	Layers:
	-	`sha256:c3e5489f0851e37fbe549177ef922b9c87e40d2f615c389da1ccfee906755ea8`  
		Last Modified: Wed, 09 Apr 2025 01:21:04 GMT  
		Size: 2.4 MB (2409372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15a96e7be661538415daa3c4b8d5f1b38102209929a9217c021a6cb449f0fba9`  
		Last Modified: Wed, 09 Apr 2025 01:21:04 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:badbb8e0ad36163ee9ed816c05a4f7f4cb44fe962522ed3e065ff714c62a1ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86216778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1754fbc0a83083ebee56a0a53e95af50d5ee83ddaa398e47e3266f15119ff3c1`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9565fa9574d0298e9a8c270e9bde79fd81b1c2df371ee2a213c0e9b99e7ed9df`  
		Last Modified: Tue, 04 Feb 2025 15:31:53 GMT  
		Size: 58.9 MB (58858596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1359120e217710fd59c2f5c587ad528fbba4f9c7778a4d46131e548d43c62275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b14a66acbd382a841b12cfa1498725f94478bf4b27e9369da3e5fd95f24a3e`

```dockerfile
```

-	Layers:
	-	`sha256:9da2e0fee41f4f4deeda8b6623a6977f3ca2eb65a093ba8d4789db74a5b55254`  
		Last Modified: Tue, 04 Feb 2025 15:31:50 GMT  
		Size: 2.4 MB (2408956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc8fa75d1f2f5091d7f7ca87051b10d820a5e578b4d48c72b8a56d16aceb80a`  
		Last Modified: Tue, 04 Feb 2025 15:31:50 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5654beb223f23aca91cb30a22c54d722bac729c467d1965b026f688b3066dda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95738464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d04c5b2a0284261b82027d9e4a67f7e83cb209d2348749d02c4d9db2483f2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f343a7efc884c1e057ede44d8c7285f78618778056bd912c181e24ea7be35a1e`  
		Last Modified: Wed, 09 Apr 2025 07:01:02 GMT  
		Size: 61.3 MB (61295768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d4c7add7bfa702b72638fdc7472b4b301b8225e081d8c511de0a13a0250093b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5ed644ac61c661e847be76e4ce48e19114a45767a4bd574fc1d24da39fefd1`

```dockerfile
```

-	Layers:
	-	`sha256:55ecbda50499f0f2cc93bcd2dc43b4faeb8cd21e65281b4f1c4db4a0b5425f10`  
		Last Modified: Wed, 09 Apr 2025 07:01:00 GMT  
		Size: 2.4 MB (2413365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b50bdee5f986b01a44a562d8820d8563faa0c2ac81a00242723abb6fb45dcd2f`  
		Last Modified: Wed, 09 Apr 2025 07:00:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
