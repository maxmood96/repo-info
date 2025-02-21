## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2d490a0cc7734940522056aa3af3660927c307f27aa269a91c557d21d6898b7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1b07353f70f1a66e288e4ffcc7cc7154c9a3a887480c50c4cd4b375414297a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242962172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aea2f550fa153a662af40c4eb4c6eb7a4d3d35be6f6b8f8b16616bdf22e7be5`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc052a312bd491e238099988ef12f4f6b5dd903c978be8729ca879bf4ef9e997`  
		Last Modified: Tue, 04 Feb 2025 04:49:23 GMT  
		Size: 213.4 MB (213426231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09f43f9b05a6b6c4711a7df584fd3385d4b7e061198f2641a52374bacf0e33b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694445c082348ff56300971e8b8223772c0f8f23455ee5daefa297dd8a738a54`

```dockerfile
```

-	Layers:
	-	`sha256:21f2848b9eb1153d80700161abff75e97647cb8b27362511900dbe52d4b87094`  
		Last Modified: Tue, 04 Feb 2025 04:49:20 GMT  
		Size: 2.3 MB (2250363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e63e3460ecb62554c166381e3c1c2e3240a5c2419049c71d71224e96fe11652`  
		Last Modified: Tue, 04 Feb 2025 04:49:20 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:380773965ef3ef73415482b336bb0631c3b38979ef47999400794fac31388a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (238983243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319d6500426b031dc026e271674dcd77d37c3a23ecd2fe4ff478d74a33657ad5`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:be4ad445f4bb4ed84bca632ff9ee80f92e691591080876b63bdd05d3595889d2`  
		Last Modified: Tue, 04 Feb 2025 15:31:00 GMT  
		Size: 211.6 MB (211625061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7cb696c6b59a8ae0a51cdfe66e1d897053e2a7a9eb65da2523b4a6c7cc3b60f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b716a653a3bce5eea029bf57b97f869b8ba3c73d6ae394a5e32f1a7063f2b5d`

```dockerfile
```

-	Layers:
	-	`sha256:ed89ff1c0cc024aae6b8f0bd97b89bde1e8dfd7714424ac048a786263d38e104`  
		Last Modified: Tue, 04 Feb 2025 15:30:55 GMT  
		Size: 2.3 MB (2250059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b485d28a4d8cea6de9bbe4e88e5bdbe7ab055060159764de4643db8239ff2cff`  
		Last Modified: Tue, 04 Feb 2025 15:30:55 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e6fa2f3d77ad2f15141caaa4dcc0f75a5efc26e31c76ad5d7723144647aec685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (249001925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f46f9e562c35511d9b16274cec6d800b82460e7670b6f924c425f4cde84202`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be735cd36cbe7c054332ebd99a8e55e7d1c3a9b6ff9d66e32e494e671f9acf6b`  
		Last Modified: Tue, 04 Feb 2025 14:43:47 GMT  
		Size: 214.6 MB (214553990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:528b5a4c10183a4f9b0e1a7043c96961fb3559fddd4277fc2eb22a6371f60233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1601789f319f06b20c3db0ba898ba407cb8cbd18505f6cd0e1af89e8ebe31876`

```dockerfile
```

-	Layers:
	-	`sha256:3ef84ef9732e8925c70f6d3d8f3d9aa988eb821e5ae2a31d80c8d9ec2a1ad210`  
		Last Modified: Tue, 04 Feb 2025 14:43:41 GMT  
		Size: 2.3 MB (2252340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5626c6a2023883765c33813f44cd36b7bcf1de270711a71798311a59edf0ba`  
		Last Modified: Tue, 04 Feb 2025 14:43:41 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
