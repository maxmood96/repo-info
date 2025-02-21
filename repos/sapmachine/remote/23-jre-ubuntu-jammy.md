## `sapmachine:23-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:28d679f85eccc8947d6f6566614d65abb2f0294df297c792bef5688c330bf85c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:96b0a56f85afe24ce8373ebd54e6d1bb3b8966f38eca231e779e990d87015fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89315454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9695f56b5ec5398576017c1b05e7c847d2d48b314a11baa42df9c27f1acdf4`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ab39496461e25f8eb18a7afce85cdc47b946365c3e3148c2a2af4da79e2404`  
		Last Modified: Tue, 04 Feb 2025 04:48:34 GMT  
		Size: 59.8 MB (59779513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09686074e0ccb519c7df46e04ba2585f7ab8acd4d46308225237edc51d9c741a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6935dc7a2cb75fed6fd1df62036721de9cd0eace881c6d71fcda7228505a97`

```dockerfile
```

-	Layers:
	-	`sha256:4672bd0d48d28c79407f67abe365f2241bfe6d4f80720df4655a4a96bd4d06e6`  
		Last Modified: Tue, 04 Feb 2025 04:48:33 GMT  
		Size: 2.4 MB (2410512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52f60a7d9d76b3b43fd701104b7e76220cfc35607ca66b240c4cb93e5e7313e1`  
		Last Modified: Tue, 04 Feb 2025 04:48:33 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1db14e0a309eb1ffc161ca50ac7546697e69eac6546585bc44ecb42a5fe5462c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86153607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6818f13b39551d2d312c4f9f4d4135f770e986a0226f66803f48f03b09c5a7`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159b943c6cdc47aeb379012da0768d28059a6e8f30fc696d5fd5aa805f11c772`  
		Last Modified: Tue, 04 Feb 2025 15:23:58 GMT  
		Size: 58.8 MB (58795425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:917a184551dcc9758bcaff778a7e1e38e402f4c16068541af19a764a3f66d058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c34ed9f64131e619be3a85fa2f60989c3a9cab673aaa1d1e25fdf1e432a7e04`

```dockerfile
```

-	Layers:
	-	`sha256:c47ffab6ee10fe91e8864e51e8eeee24bf1495cdd699540773eee7617a8d43b9`  
		Last Modified: Tue, 04 Feb 2025 15:23:57 GMT  
		Size: 2.4 MB (2409588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eec0822f95e9da48cc25b66ea344df6ba80adca44e4db4d46b0cfa20f226c4d`  
		Last Modified: Tue, 04 Feb 2025 15:23:56 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:05786663b3f50ecdd652e856ed658b34eb485ae5149de146d925ba39e43db3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95671801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8eb1128d8da5599b32226f863f85e049f31798b1158313b319fd9c53441f31`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f7d20ff355150d3957194d4f34f752a75c820645262b27effbacd9275883a`  
		Last Modified: Tue, 04 Feb 2025 14:31:06 GMT  
		Size: 61.2 MB (61223866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c9ef7dcf4ce105a435aea4764743f087947ea817aae7e0cff7ea7bd1acea9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd58e9bb507104981929dd5e4858041bd9c4e71a248753058d90160405e3b712`

```dockerfile
```

-	Layers:
	-	`sha256:499152b08c7a316040ee0478549121509f8546c454bf83bd24b06d09205bdd7f`  
		Last Modified: Tue, 04 Feb 2025 14:31:05 GMT  
		Size: 2.4 MB (2413875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89542e36682fade5bca550cc326e30d72a493dcff336e215697b99a28e9b19ff`  
		Last Modified: Tue, 04 Feb 2025 14:31:04 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
