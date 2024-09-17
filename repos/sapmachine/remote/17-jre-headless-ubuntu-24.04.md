## `sapmachine:17-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:1fdff8e67e56f6788474469e0a7489b1875b03131fc19431836c684982b86985
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7bcc285d074e08a4aef900caf13465d890698292900e54e98c1472b16177fcfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85061317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dabce3b56281e86aff12d6bb68fa38215d0dc858dedfaf58ae621ce4af21251`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f823d3a8f08f3323a7fb687b07b2cc63f191b84f39e608a520528f07968251c1`  
		Last Modified: Tue, 17 Sep 2024 01:00:35 GMT  
		Size: 55.3 MB (55311489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0e5bbf24846cabf3c4fdbce130194267cda63d3e7a6b2f77e26e9c5fce3b103a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552861c2fb3cc60a65ba743f023f4b2d6d3c3a4c5a54165d8440a7ed76db5959`

```dockerfile
```

-	Layers:
	-	`sha256:fde8a14b3cce623c7494bd2a3cb8b909ff3e6c005e0e8fd69bab7f7e62596677`  
		Last Modified: Tue, 17 Sep 2024 01:00:35 GMT  
		Size: 3.1 KB (3149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc058665bd2e919e71002cccaf8fc5f19b9981e0f62a9acc80940fb95a40e44d`  
		Last Modified: Tue, 17 Sep 2024 01:00:35 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:70b013a89a9741f61b8b9c065918ae15588113d45fc7b2bea3277f86e7137b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83386866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6684deeaac7d54972cdd321f17897e9107cec0968b995d4a108708ef91641134`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ce84562284bda3190c18599d0969add7f1ed5129cdfe855fc2802122e91809`  
		Last Modified: Tue, 17 Sep 2024 03:29:30 GMT  
		Size: 54.5 MB (54501267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17db8e0ebda80446779c0d403d7fd46a4d83c841b231de68fc5ac5979459af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c999ec849aeff38ddea47487e3d6e0d5a98ad7f93e88b6ac4befddb4aaaccf`

```dockerfile
```

-	Layers:
	-	`sha256:dfa25ea4a8688e0569e5c07e079c17dae1e7714f61d8502bc0c8525fc8c1ec64`  
		Last Modified: Tue, 17 Sep 2024 03:29:29 GMT  
		Size: 2.1 MB (2127146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbc299a848df8f0d9daa5162c9dcc7b0fb6954ecadf2094737f49fe8369dacb`  
		Last Modified: Tue, 17 Sep 2024 03:29:28 GMT  
		Size: 9.7 KB (9689 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:32a861911deb1e27700dd013e81ce7e09439e720e4df31f446431710725eec00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91344229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036a8d04e46e3bf6360b6593cc1fa0a83baa5adc40c4bff850d206a3e9fcf1e0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e956f2192fcc34fef5dc90ea286ba23a50fd1be3fedad023d86ffb287f56fcf7`  
		Last Modified: Tue, 17 Sep 2024 02:49:12 GMT  
		Size: 57.0 MB (56951884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ac15295ed41102a025daec8afdbe050aa9216292501dcb6f2d4e6dac1f3b3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5524f0b859a13055df5844ea8ae8e04a21c04c0336b889715c68183b4faff5`

```dockerfile
```

-	Layers:
	-	`sha256:61fcfddf215d96a8aa6719d3fdabf39978ebbeebcbac11bcd446d55c63bed2a7`  
		Last Modified: Tue, 17 Sep 2024 02:49:10 GMT  
		Size: 2.1 MB (2130550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a50969acd7fc49ed475b982d604aa7bf1203e6c68c49a7c380ec2505de67ad`  
		Last Modified: Tue, 17 Sep 2024 02:49:09 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json
